## Find the second smallest element

**Problem statement**

- Given an integer array of size n, find the second smallest element in the array.

**Test cases**

```
Input:
n = 5
arr = 1 2 3 4 5

Output:
2

Input:
n = 7
arr = 70 33 46 12 9 90 69

Output:
12
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

		// Calling method to calculate second smallest element
		int secondSmallestElement = findSecondSmallestElement(arr);

		System.out.println(secondSmallestElement);
		scan.close();
	}

	// findSecondSmallestElement() method
	static int findSecondSmallestElement(int[] arr) {
		int smallest = Integer.MAX_VALUE;
		int secondSmallest = Integer.MAX_VALUE;

		for(int i = 0; i < arr.length; i++) {
			// If current element is smaller than smallest
			// first add current smallest to secondSmallest
			// then update smallest with current element
			if(arr[i] < smallest) {
				secondSmallest = smallest;
				smallest = arr[i];
			} else if(arr[i] < secondSmallest && arr[i] != smallest) {
				secondSmallest = arr[i];
			}
		}

		return secondSmallest;
	}
}
```
