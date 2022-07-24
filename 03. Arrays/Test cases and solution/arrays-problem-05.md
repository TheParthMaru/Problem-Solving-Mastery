**Problem statement**

- Given an integer array of size n, rotate the array right by k elements.

**Test cases**

```
Input:
n = 5
arr = 1 2 3 4 5
k = 1

Output:
5 1 2 3 4

Input:
3
1 2 3
2

Output:
2 3 1
```

**Solution**

```java
import java.util.Scanner;

public class Main {

	public static void main(String args[]) {
		Scanner scan = new Scanner(System.in);

		// Input size of the array
		int n = scan.nextInt();

		// Array of size n
		int[] arr = new int[n];

		// Taking inputs
		for (int i = 0; i < n; i++) {
			arr[i] = scan.nextInt();
		}

		// rotate by k elements
		int k = scan.nextInt();

		// Calling rotateRight() method
		rotateRight(arr, k);
		scan.close();
	}

	// Method to rotate array right by k elements
	static void rotateRight(int arr[], int k) {
		for (int i = 1; i <= k; i++) {
			// Storing the last element
			int lastElement = arr[arr.length - 1];
			for (int j = arr.length-1; j > 0; j--) {
				// Shifting elements
				arr[j] = arr[j - 1];
			}

			// Adding the last element to start
			arr[0] = lastElement;
		}

		printArray(arr);
	}

	// Method to print the array
	static void printArray(int[] arr) {
		for (int i = 0; i < arr.length; i++) {
			System.out.print(arr[i] + " ");
		}
	}
}
```
