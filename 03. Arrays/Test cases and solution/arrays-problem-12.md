**Problem statement**

- Given two integer sorted arrays of size m and n, write a program to merge these sorted arrays.

**Test cases**

```
Input:
m = 5
arr1 = 1 4 6 10 13
n = 4
arr2 = 2 5 7 9

Output:
1 2 4 5 6 7 9 10 13
```

**Solution**

```java
import java.util.Scanner;

public class Main {
	public static void main(String[] args) {

		Scanner scan = new Scanner(System.in);

		int m = scan.nextInt();
		int[] arr1 = new int[m];

		// Input arr1
		for(int i = 0; i < arr1.length; i++) {
			arr1[i] = scan.nextInt();
		}

		int n = scan.nextInt();
		int[] arr2 = new int[n];

		// Input arr2
		for(int i = 0; i < arr2.length; i++) {
			arr2[i] = scan.nextInt();
		}

		int[] arr3 = merge(arr1, arr2);
		printArray(arr3);

		scan.close();
	}

	// Merging the arrays
	static int[] merge(int arr1[], int arr2[]) {
		int arr[] = new int[arr1.length + arr2.length];
		int i = 0, j = 0, k = 0;

		while(i < arr1.length && j < arr2.length) {
			if(arr1[i] < arr2[j]) {
				arr[k] = arr1[i];
				k++; i++;
			} else {
				arr[k] = arr2[j];
				k++; j++;
			}
		}

		while(i < arr1.length) {
			arr[k] = arr1[i];
			k++; i++;
		}

		while(j < arr2.length) {
			arr[k] = arr2[j];
			k++; j++;
		}

		return arr;
	}

	// Printing array
	static void printArray(int arr[]) {
		for(int i = 0; i < arr.length; i++) {
			System.out.print(arr[i] + " ");
		}
	}
}
```
