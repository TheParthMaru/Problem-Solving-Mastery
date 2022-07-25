## Print sum row wise

**Problem statement**

- Given a 2-d m x n integer array, print sum of the rows.

**Test cases**

```
Input:
rows = 4
columns = 2

arr = 1 2
      3 4
      5 6
      7 8

Output:
3 7 11 15
```

**Solution**

```java
package main;

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

		printSum(arr);

		scan.close();
	}

	static void printSum(int arr[][]) {
		int rows = arr.length;
		int cols = arr[0].length;

		for(int i = 0; i < rows; i++) {
			int sum = 0;
			for(int j = 0; j < cols; j++) {
				sum += arr[i][j];
			}
			System.out.print(sum + " ");
		}
	}
}
```
