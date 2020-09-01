import java.util.*;

public class Matrix_Manip {
	public static void main(String args[]) {
		Scanner scnr = new Scanner (System.in);

		boolean isRunning = true;

		//Continuous printing of the main menu until user chooses to "quit"
		while (isRunning) {
			System.out.println("Matrix Calculator");
			System.out.println("0: Transpose a matrix");
			System.out.println("1: Add two matrices");
			System.out.println("2: Multiply two matrices");
			System.out.println("3: Quit");

			int userInput = scnr.nextInt();

			int[][] matrix1, matrix2;
			switch(userInput) {
				case 0:
					print_label(1);
					matrix1 = fill_matrix(scnr);
					transpose(matrix1);
					break;
				case 1:
					print_label(1);
					matrix1 = fill_matrix(scnr);
					print_label(2);
					matrix2 = fill_matrix(scnr);
					add(matrix1, matrix2);
					break;
				case 2:
					print_label(1);
					matrix1 = fill_matrix(scnr);
					print_label(2);
					matrix2 = fill_matrix(scnr);
					multiply(matrix1, matrix2);
					break;
				case 3:
					isRunning = false;
					break;
				default:
					System.out.println("Enter either 0, 1, 2, or 3. Try again.");
			}
		}
	}

	public static void print_label(int num) { //Printing the labels for a matrix
		System.out.println("Matrix " + num);
    	System.out.println("---------------------------------------------------");
	}

	public static void print_matrix(int[][] matrix) { //Printing out a resulting matrix
		System.out.println();

		int i,j;
		for (i = 0; i < matrix.length; i++) {
	    	for (j = 0; j < matrix[i].length; j++) {
	        	System.out.print(matrix[i][j] + " ");
	    	}
	    	System.out.println();
	    }

	    System.out.println();
	}

	public static int[][] fill_matrix(Scanner scnr) { //Filling a matrix with the user's input
		System.out.println("Enter the number of rows:");
    	int rows = scnr.nextInt();
    	System.out.println("Enter the number of columns:");
    	int columns = scnr.nextInt();

		int[][] matrix = new int[rows][columns];

		int i,j;
    	for (i = 0; i < rows; i++) {
	    	for (j = 0; j < columns; j++) {
	        	System.out.println("Row " + (i+1) + " Cell " + (j+1) + ":");
	        	matrix[i][j] = scnr.nextInt();
	    	}
	    }

	    return matrix;
	}

	public static void transpose(int[][] matrix1) { //Transposing the matrix
		int[][] transposed_matrix = new int[matrix1[0].length][matrix1.length];
		
		int i,j;
		for (i = 0; i < transposed_matrix.length; i++) {
	    	for (j = 0; j < transposed_matrix[i].length; j++) {
	        	transposed_matrix[i][j] = matrix1[j][i];
	    	}
	    }

	    print_matrix(transposed_matrix);
	}

	public static void add(int[][] matrix1, int[][] matrix2) { //Adding 2 matrices
		if (matrix1.length == matrix2.length && matrix1[0].length == matrix2[0].length){
			int[][] sum_matrix = new int[matrix1.length][matrix1[0].length];

			int i,j;
			for (i = 0; i < sum_matrix.length; i++) {
	        	for (j = 0; j < sum_matrix[0].length; j++) {
	            	sum_matrix[i][j] = matrix1[i][j] + matrix2[i][j];
	        	}
	    	}

	    	print_matrix(sum_matrix);
		} else {
			System.out.println("\nThese matrices cannot be added.\n");
		}
	}

	public static void multiply(int[][] matrix1, int[][] matrix2) { //Multiplying 2 matrices
		if (matrix1[0].length == matrix2.length) {
			int[][] product_matrix = new int[matrix1.length][matrix2[0].length];
	    	
	    	int i,j,k;
	    	int product = 0;
	    	for (i = 0; i < matrix1.length; i++) {
	        	for (j = 0; j < matrix2[0].length; j++) {
	        		for (k = 0; k < matrix1[0].length; k++) {
	        			product += matrix1[i][k] * matrix2[k][j];
	        		}
	        		product_matrix[i][j] = product;
	        		product = 0;
	        	}
	        }

	        print_matrix(product_matrix);
		} else {
			System.out.println("\nThese matrices cannot be multiplied.\n");
		}
	}
}
