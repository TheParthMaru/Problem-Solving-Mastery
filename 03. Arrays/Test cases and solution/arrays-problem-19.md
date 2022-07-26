## Wave print

**Problem statement**

- Given an integer array of size mxn, print the elements in wave form.

**Test cases**

```
Input:
3 3
1 2 3
4 5 6
7 8 9

Output:
1 4 7 2 5 8 3 6 9
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

		wavePrint(arr, rows, cols);

		scan.close();
	}

	static void wavePrint(int arr[][], int rows, int cols) {
		for(int j = 0; j < cols; j++) {
			if(j % 2 == 0) {
				for(int i = 0; i < rows; i++) {
					System.out.print(arr[i][j] + " ");
				}
			} else {
				for(int i = rows-1; i >= 0; i--) {
					System.out.print(arr[i][j] + " ");
				}
			}
		}
	}
}
```
