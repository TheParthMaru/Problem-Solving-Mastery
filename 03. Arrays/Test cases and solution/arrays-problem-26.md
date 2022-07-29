## Sort 0, 1 and 2 without using any algorithm

**Problem statement**

- Given an array which consists of only 0s, 1s and 2s, sort the array without using any algorithm.

**Test cases**

```
Input:
5
2 1 0 1 0


Output:
0 0 1 1 2
```

**Solution**

```java
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

		sort012(arr);

		scan.close();
	}

	static void sort012(int arr[]) {
		int i = 0, j = 0, k = arr.length-1;

		while(i <= k) {
			if(arr[i] == 0) {
				swap(arr, i, j);
				i++; j++;
			} else if(arr[i] == 1) {
				i++;
			} else {
				swap(arr, i, k);
				k--;
			}
		}

		printArray(arr);
	}

	static void swap(int arr[], int i, int j) {
		int temp = arr[i];
		arr[i] = arr[j];
		arr[j] = temp;
	}

	static void printArray(int arr[]) {
		for(int i = 0; i < arr.length; i++) {
			System.out.print(arr[i] + " ");
		}
	}
}
```
