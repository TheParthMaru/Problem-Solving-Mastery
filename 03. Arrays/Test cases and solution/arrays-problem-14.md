## Print all possible pairs

**Problem statement**

- Given an integer array of size n, find all possible pairs of the element including repetition of pairs.

**Test cases**

```
Input:
n = 2
arr = {1, 2}

Output:
(1, 1) (1, 2) (2, 1) (2, 2)
```

**Solution**

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

		printPairs(arr);
	}

	// Method to print all possible pairs
	static void printPairs(int arr[]) {
		for(int i = 0; i < arr.length; i++) {
			for(int j = 0; j < arr.length; j++) {
				System.out.print("(" + arr[i] + ", " + arr[j] + ") ");
			}
		}
	}
}
```
