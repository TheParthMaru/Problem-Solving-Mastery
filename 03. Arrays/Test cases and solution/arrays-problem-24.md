## Search an element in matrix

**Problem statement**

- Given a 2d array of size mxn, write a program to search an element in it.

**Test case**

```
Input:
m = 3
n = 4

arr = 0 1 12 3
      4 5 6  7
      8 9 10 11

element = 6

Output:
(1,2)
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

		for (int i = 0; i < rows; i++) {
			for (int j = 0; j < cols; j++) {
				arr[i][j] = scan.nextInt();
			}
		}

		int element = scan.nextInt();

		searchElement(arr, rows, cols, element);

		scan.close();
	}

	static void searchElement(int arr[][], int rows, int cols, int element) {
		int flag = 0;

		for(int i = 0; i < rows; i++) {
			for(int j = 0; j < cols; j++) {
				if(arr[i][j] == element) {
					System.out.println("(" + i + "," + j + ")");
					flag = 1;
					break;
				}
			}
			if(flag == 1) {
				break;
			}
		}

		if(flag == 0) {
			System.out.println(-1);
		}

	}
}
```
