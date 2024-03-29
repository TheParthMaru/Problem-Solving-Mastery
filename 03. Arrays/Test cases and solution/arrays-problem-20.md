## Spiral print

**Problem statement**

- Given an integer array of size mxn, print the elements in spiral form.

**Test cases**

```
Input:
4 4
1 2 3 4
5 6 7 8
9 10 11 12
13 14 15 16

Output:
1 2 3 4 8 12 16 15 14 13 9 5 6 7 11 10
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
		for (int i = 0; i < rows; i++) {
			for (int j = 0; j < cols; j++) {
				arr[i][j] = scan.nextInt();
			}
		}

		spiralPrint(arr);

		scan.close();
	}

	static void spiralPrint(int arr[][]) {
		int top = 0;
		int down = arr.length - 1;
		int left = 0;
		int right = arr[0].length - 1;

		int dir = 0;
		int i;

		while (top <= down && left <= right) {
			if (dir == 0) {
				for (i = left; i <= right; i++) {
					System.out.print(arr[top][i] + " ");
				}
				top++;
			} else if (dir == 1) {
				for (i = top; i <= down; i++) {
					System.out.print(arr[i][right] + " ");
				}
				right--;
			} else if (dir == 2) {
				for (i = right; i >= left; i--) {
					System.out.print(arr[down][i] + " ");
				}
				down--;
			} else if (dir == 3) {
				for (i = down; i >= top; i--) {
					System.out.print(arr[i][left] + " ");
				}
				left++;
			}
			dir = (dir + 1) % 4;
		}
	}
}
```
