## Sort first half in ascending order and second half in descending order

**Problem statement**

- Given an integer array of size n as input, write a program to sort the first half of the array in ascending order and the later half in descending order.

**Test cases**

```
Input:
8
3 2 4 1 10 30 40 20

Output:
1 2 3 4 40 30 20 10
```

**Solution**

```java
import java.util.Arrays;
import java.util.Scanner;

public class Main {

	public static void main(String args[]) {
		Scanner scan = new Scanner(System.in);

		// Input the size of array
		int n = scan.nextInt();

		// Define array of size n
		int arr[] = new int[n];

		// Input array elements
		for (int i = 0; i < n; i++) {
			arr[i] = scan.nextInt();
		}

		sortArray(arr);
		scan.close();
	}

	static void sortArray(int arr[]) {

		// Sorting entire array in ascending order
		Arrays.sort(arr);

		// Sorting the right half of the array in descending order
		for (int i = arr.length / 2; i < arr.length - 1; i++) {
			for(int j = i+1; j < arr.length; j++) {
				if (arr[i] < arr[j]) {
					int temp = arr[i];
					arr[i] = arr[j];
					arr[j] = temp;
				}
			}

		}

		printArray(arr);
	}

	static void printArray(int arr[]) {
		for (int i = 0; i < arr.length; i++) {
			System.out.print(arr[i] + " ");
		}
	}
}
```
