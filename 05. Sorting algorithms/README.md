# Sorting algorithms

## Terminologies:

- **In-place sorting:** Algorithms that do not require additional space for sorting the array. The array is sorted in constant space O(n).
- **Internal sorting:** When all data is placed in the main memory or internal memory then sorting is called internal sorting. Here, the problem cannot take input beyond its size. Example: heap sort, bubble sort, selection sort, quick sort, shell sort, insertion sort.
- **External sorting:** When all data that needs to be sorted cannot be placed in memory at a time, the sorting is called external sorting. External Sorting is used for the massive amount of data. Merge Sort and its variations are typically used for external sorting. Example: Merge sort, Tag sort, Polyphase sort, Four tape sort, External radix sort, Internal merge sort, etc.
- **Stable sorting:** When two same data appear in the same order in sorted data without changing their position is called stable sort. Example: merge sort, insertion sort, bubble sort.
- **Unstable sorting:** When two same data appear in the different order in sorted data it is called unstable sort. Example: quick sort, heap sort, shell sort.

## Selection sort

- For n elements, we perform n-1 rounds.
- We start by moving the minimum element at 0th position and continue until it is sorted.

**Working**

- Consider the following array: `arr[] = {64, 25, 12, 22, 11}`
  _First pass:_

  - The outer array will traverse from 0 to n-2 and the inner array will traverse from outer array's index + 1 to n - 1.
  - The first element will be compared with all the rest element and if any element is smaller than the element at 0, then swap both the elements
  - Thus, 64 and 11 will be swapped.
    `arr = {11, 25, 12, 22, 64}`

  _Second pass:_

  - Now, start with index 1 and traverse the array and check if any element is smaller than element present at index 1.
  - If yes, then swap.
  - Thus, 25 and 12 will be swapped.
    `arr = {11, 12, 25, 22, 64}`

  _Third pass:_

  - Starting index will be 2 and traverse the array and follow the same step.
  - Thus, 25 and 22 will be swapped.
    `arr = {11, 12, 22, 25, 64}`

  _Fourth pass:_

  - Now the starting index will be 3 and check the same.
  - Although the array is sorted still we check.

**Code**

```java
import java.util.Scanner;

public class Main {
	public static void main(String[] args) {
		Scanner scan = new Scanner(System.in);

		// Size of input array
		int n = scan.nextInt();

		// Array of size n
		int[] arr = new int[n];

		// Input elements in the array
		for(int i = 0; i < n; i++) {
			arr[i] = scan.nextInt();
		}

		// Calling the selectionSort method
		selectionSort(arr);

		scan.close();
	}

// Selection sort algorithm
	static void selectionSort(int[] arr) {
		for(int i = 0; i < arr.length - 1; i++) {
			for(int j = i+1; j < arr.length; j++) {
				if(arr[j] < arr[i]) {
					int temp = arr[i];
					arr[i] = arr[j];
					arr[j] = temp;
				}
			}
		}

		printArray(arr);
	}

	// Method to print array
	static void printArray(int[] arr) {
		for(int i = 0; i < arr.length; i++) {
			System.out.print(arr[i] + " ");
		}
	}
}
```

**Complexity**

- Time complexity: O(n<sup>2</sup>)

## Bubble sort

- Bubble Sort is the simplest sorting algorithm that works by repeatedly swapping the adjacent elements if they are in the wrong order.
- This algorithm is not suitable for large data sets as its average and worst-case time complexity is quite high.

**Working**
_First Pass:_

- Bubble sort starts with very first two elements, comparing them to check which one is greater.
  ( 5 1 4 2 8 ) –> ( 1 5 4 2 8 ), Here, algorithm compares the first two elements, and swaps since 5 > 1.
  ( 1 5 4 2 8 ) –> ( 1 4 5 2 8 ), Swap since 5 > 4
  ( 1 4 5 2 8 ) –> ( 1 4 2 5 8 ), Swap since 5 > 2
  ( 1 4 2 5 8 ) –> ( 1 4 2 5 8 ), Now, since these elements are already in order (8 > 5), algorithm does not swap them.

_Second Pass:_

- Now, during second iteration it should look like this:
  ( 1 4 2 5 8 ) –> ( 1 4 2 5 8 )
  ( 1 4 2 5 8 ) –> ( 1 2 4 5 8 ), Swap since 4 > 2
  ( 1 2 4 5 8 ) –> ( 1 2 4 5 8 )
  ( 1 2 4 5 8 ) –> ( 1 2 4 5 8 )

_Third Pass:_

- Now, the array is already sorted, but our algorithm does not know if it is completed.
- The algorithm needs one whole pass without any swap to know it is sorted.
  ( 1 2 4 5 8 ) –> ( 1 2 4 5 8 )
  ( 1 2 4 5 8 ) –> ( 1 2 4 5 8 )
  ( 1 2 4 5 8 ) –> ( 1 2 4 5 8 )
  ( 1 2 4 5 8 ) –> ( 1 2 4 5 8 )

**Code**

```java
import java.util.Scanner;

public class Main {
	public static void main(String[] args) {
		Scanner scan = new Scanner(System.in);

		// Size of input array
		int n = scan.nextInt();

		// Array of size n
		int[] arr = new int[n];

		// Input elements in the array
		for(int i = 0; i < n; i++) {
			arr[i] = scan.nextInt();
		}

		// Calling the bubbleSort method
		bubbleSort(arr);

		scan.close();
	}

// Bubble sort algorithm
	static void bubbleSort(int[] arr) {
		for(int i = 0; i < arr.length - 1; i++) {
			for(int j = 0; j < (arr.length - i - 1); j++) {
				if(arr[j] > arr[j+1]) {

					// Swap arr[j] and arr[j+1]
					int temp = arr[j];
					arr[j] = arr[j+1];
					arr[j+1] = temp;
				}
			}
		}

		printArray(arr);
	}

	// Method to print array
	static void printArray(int[] arr) {
		for(int i = 0; i < arr.length; i++) {
			System.out.print(arr[i] + " ");
		}
	}
}
```

**Complexity**

- Time complexity: O(n<sup>2</sup>)
