**Problem statement**

- Write a program to take n size integer array as input and reverse the array.

**Test cases**

```
Input:
5
1 2 3 4 5

Output:
5 4 3 2 1
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
		for(int i = 0; i < n; i++) {
			arr[i] = scan.nextInt();
		}

		// Reverse array
		reverseArray(arr);

		scan.close();
	}

	// Method to reverse the array
	static void reverseArray(int arr[]) {
		for(int i = 0; i < arr.length / 2; i++) {
			int temp = arr[i];
			arr[i] = arr[arr.length-i-1];
			arr[arr.length-i-1] = temp;
		}

		printArray(arr);
	}

	// Method to print the reverse array
	static void printArray(int arr[]) {
		for(int i = 0; i < arr.length; i++) {
			System.out.print(arr[i] + " ");
		}
	}
}
```
