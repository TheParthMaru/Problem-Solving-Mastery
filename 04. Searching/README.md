# Searching algorithms

## Linear Search

- We are searching for an element linearly in an unsorted array.
- The `linearSearch()` method will return the index of the element to be searched.
- If the element is not found, then we need to return -1.

**Test cases**

```
Input:
n = 5
arr = 2 5 3 1 4
element = 1

Output:
3

Input:
n = 3
arr = 1 2 3
element = 9

Output:
-1
```

**Code**

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

		// Enter element to search
		int element = scan.nextInt();

		// Linear search result
		System.out.println(linearSearch(arr, element));

		scan.close();
	}

	// linearSearch() method will return the index of the element
	static int linearSearch(int[] arr, int element) {
		for(int i = 0; i < arr.length; i++) {
			if(arr[i] == element) {
				return i;
			}
		}

		return -1;
	}
}
```

**Complexity**

- Time complexity: O(n)
- Space complexity: O(1)

## Binary search

- In binary search, we are searching for an element in sorted array.
- We divide the array until we find the element and we return the index if element is found, else we return -1.

**Note**

- The array needs to be sorted.

**Test cases**

```
Input:
n = 5
arr = 1 2 3 4 5
element = 2

Output:
1

Input:
n = 5
arr = 1 2 3 4 5
element = 8

Output:
-1
```

**Code**

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

		// Enter element to search
		int element = scan.nextInt();

		// Binary search result
		System.out.println(binarySearch(arr, element));

		scan.close();
	}

	// binarySearch() method will return the index of the element
	static int binarySearch(int[] arr, int element) {
		// Setting first and last elements of the array
		int start = arr[0];
		int end = arr.length - 1;

		while(start <= end) {
			// Midpoint of the array
			int mid = start + (end - 1) / 2;

			// Checking if the middle element is the element we are searching for
			if(arr[mid] == element) {
				return mid;
			}

			/*
			 * If arr[mid] is less than the element, we need to exclude all the elements before mid
			 * and set the start element to mid + 1.
			 * Similarly if arr[mid] is greater than the element, we need to exclude all the elements after mid
			 * and set the end element to mid - 1.
			 */
			if(arr[mid] < element) {
				start = mid + 1;
			} else {
				end = mid - 1;
			}
		}

		return -1;
	}
}
```
