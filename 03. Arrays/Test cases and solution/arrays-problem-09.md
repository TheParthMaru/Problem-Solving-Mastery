## Swap alternate elements

**Problem statement**

- You have been given an array of size n. You need to swap every pair of alternate elements in the array.

**Test cases**

```
Input:
n = 6
arr = 9 3 6 12 4 32

Output:
3 9 12 6 32 4

Input:
n = 9
arr = 9 3 6 12 4 32 5 11 19

Output:
3 9 12 6 32 4 11 5 19
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

		// Input array
		for (int i = 0; i < arr.length; i++) {
			arr[i] = scan.nextInt();
		}

		// Swapping array pairs
		for (int i = 0; i < arr.length - 1; i += 2) {
			int temp = arr[i];
			arr[i] = arr[i + 1];
			arr[i + 1] = temp;
		}

		// Printing the array
		for (int i = 0; i < arr.length; i++) {
			System.out.print(arr[i] + " ");
		}

		scan.close();
	}
}
```
