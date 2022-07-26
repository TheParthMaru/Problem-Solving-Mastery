## Largest column sum

**Problem statement**

- Given a 2d array of size m x n, find the largest sum of all the columns.

**Test cases**

```
Input:
rows = 2
cols = 3
arr = 1 2 3
      6 5 7

Output:
10
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

		System.out.println(largestColumnSum(arr, rows, cols));

		scan.close();
	}

	static int largestColumnSum(int arr[][], int rows, int cols) {
		int largestSum = Integer.MIN_VALUE;

		for(int j = 0; j < cols; j++) {
			int sum = 0;
			for(int i = 0; i < rows; i++) {
				sum += arr[i][j];
			}
			if(sum > largestSum) {
				largestSum = sum;
			}
		}

		return largestSum;
	}
}
```
