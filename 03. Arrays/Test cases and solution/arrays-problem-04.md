## Rotate array left by k elements

**Problem statement**

- Given an integer array of size n, rotate the array left by k elements.

**Test cases**

```
Input:
n = 5
arr = 1 2 3 4 5
k = 1

Output:
2 3 4 5 1

Input:
3
1 2 3
2

Output:
3 1 2
```

**Solution**

_Approach 1: Bruteforce approach_

```java
import java.util.Scanner;

public class Main {

	public static void main(String args[]) {
		Scanner scan = new Scanner(System.in);

		// Input size of the array
		int n = scan.nextInt();

		// Array of size n
		int[] arr = new int[n];

		// Input array elements
		for (int i = 0; i < n; i++) {
			arr[i] = scan.nextInt();
		}

		// Rotate by k elements
		int k = scan.nextInt();

		// Calling rotateLeft() method
		rotateLeft(arr, k);
		scan.close();
	}

	// Method to rotate array left by k elements
	static void rotateLeft(int arr[], int k) {
		for(int i = 1; i <= k; i++) {
			// Storing the first element
			int firstElement = arr[0];
			for(int j = 0; j < arr.length - 1; j++) {
				// Shifting elements
				arr[j] = arr[j+1];
			}

			// Adding the first element to the end
			arr[arr.length-1] = firstElement;
		}

		printArray(arr);
	}

	// Method to print the array
	static void printArray(int[] arr) {
		for(int i = 0; i < arr.length; i++) {
			System.out.print(arr[i] + " ");
		}
	}
}
```

_Approach 2: Reversing the array_

```java
import java.util.Scanner;

public class Main {
	public static void main(String[] args) {
		Scanner scan = new Scanner(System.in);

		// Input size of array
		int n = scan.nextInt();

		// Declare array of size n
		int arr[] = new int[n];

		// Input elements in array
		for(int i = 0; i < n; i++) {
			arr[i] = scan.nextInt();
		}

		// Input k
		int k = scan.nextInt();

		// Calling rotateArray method
		rotateArray(arr, k);
	}

	static void rotateArray(int arr[], int k) {
		int n = arr.length;

		// Reverse the whole array
		reverseArray(arr, 0, n-1);

		// Reverse first n-k elements
		reverseArray(arr, 0, n-k-1);

		// Reverse the remaining k elements
		reverseArray(arr, n-k, n-1);

		// Printing result
		for(int i = 0; i < n; i++) {
			System.out.print(arr[i] + " ");
		}
	}

	static void reverseArray(int arr[], int start, int end) {
		while(start < end) {
			int temp = arr[start];
			arr[start] = arr[end];
			arr[end] = temp;
			start++; end--;
		}
	}

}
```
