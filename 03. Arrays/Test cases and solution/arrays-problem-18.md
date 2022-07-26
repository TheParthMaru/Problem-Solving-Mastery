## Sum of boundary and diagonal elements

**Problem statement**

- Given an input square matrix, find the sum of boundary elements.

**Note**

- For square matrix, rows = columns = n.

**Test cases**

```
Input:
n = 4
arr = 1 2 3 4
      1 2 3 4
      1 2 3 4
      1 2 3 4

Output:
40

Input:
n = 5
arr = 1 2 3 4 5
      6 7 8 9 10
      11 12 13 14 15
      16 17 18 19 20
      21 22 23 24 25

Output:
273
```

**Solution**

```java
import java.util.Scanner;

public class Main {

	public static void main(String args[]) {
		Scanner scan = new Scanner(System.in);

		int n = scan.nextInt();

		int arr[][] = new int[n][n];

//		Array input
		for(int i = 0; i < n; i++) {
			for(int j = 0; j < n; j++) {
				arr[i][j] = scan.nextInt();
			}
		}

		System.out.println(boundaryDiagonalSum(arr, n));

		scan.close();
	}

	static int boundaryDiagonalSum(int arr[][], int n) {
		int sum = 0;
		for(int i = 0; i < n; i++) {
			for(int j = 0; j < n; j++) {
//				Condition for diagonal element
				if(i == j|| (i+j) == n-1) {
					sum += arr[i][j];
				}

//				Condition for boundary element
				else if(i == 0 || j == 0 || j == (n-1) || i == (n-1)) {
					sum += arr[i][j];
				}
			}
		}
		return sum;
	}
}
```
