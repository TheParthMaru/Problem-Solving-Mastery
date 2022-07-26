## Largest row or column

**Problem statement**

- For a given two-dimensional integer array of size (mxn), find out which row or column has the largest sum (sum of all the elements in a row/column) amongst all the rows and columns.

**Note**

- If there are more than one rows/columns with maximum sum, consider the row/column that comes first and if ith row and jth column has the same largest sum, consider the ith row as answer.

Output Format :

- For each test case, if row sum is maximum, then print: "row" <row_index> <row_sum> or if column sum is maximum, then print: "column" <col_index> <col_sum>.

**Test cases**

```
Input:
2 2
1 1
1 1

Output:
row 0 2

Input:
3 3
3 6 9
1 4 7
2 8 9

Output:
column 2 25
```

**Solution**

```java
import java.util.Scanner;

public class Main {

	public static void main(String args[]) {
		Scanner scan = new Scanner(System.in);

		int rows = scan.nextInt();
		int cols = scan.nextInt();

		int arr[][] = new int[rows][cols];

//		Array input
		for(int i = 0; i < rows; i++) {
			for(int j = 0; j < cols; j++) {
				arr[i][j] = scan.nextInt();
			}
		}

		largestRowOrCol(arr, rows, cols);

		scan.close();
	}

	static void largestRowOrCol(int arr[][], int rows, int cols) {
		int largestRowSum = Integer.MIN_VALUE;
		int largestColSum = Integer.MIN_VALUE;
		int index = 0;

//		Calculating largestRowSum
		for(int i = 0; i < rows; i++) {
			int sum = 0;
			for(int j = 0; j < cols; j++) {
				sum += arr[i][j];
			}
			if(sum > largestRowSum) {
				largestRowSum = sum;
				index = i;
			}
		}

//		Calculating largestColSum
		for(int j = 0; j < cols; j++) {
			int sum = 0;
			for(int i = 0; i < rows; i++) {
				sum += arr[i][j];
			}
			if(sum > largestColSum) {
				largestColSum = sum;
				index = j;
			}
		}

//		Determining whether row has largest sum or column
		if(largestRowSum >= largestColSum) {
			System.out.println("row" + " " + index + " " + largestRowSum);
		} else {
			System.out.println("column" + " " + index + " " + largestColSum);
		}
	}
}
```
