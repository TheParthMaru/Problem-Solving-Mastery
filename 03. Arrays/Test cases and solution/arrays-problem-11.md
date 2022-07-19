**Problem statement**

- Given an integer input array of size containing all 0s and 1s, sort this array with only one scan and no extra array.

**Test cases**

```
Input:
5
1 0 1 1 0

Output:
0 0 1 1 1

Input:
3
1 1 0

Output:
0 1 1
```

**Solution**

```java
import java.util.Scanner;

public class Main {
	public static void main(String[] args) {
		Scanner scan = new Scanner(System.in);

		// No. of elements in array
		int n = scan.nextInt();

		// Input array of size n
		int[] arr = new int[n];

		// Taking array input
		for(int i = 0; i < n; i++) {
			arr[i] = scan.nextInt();
		}

		sort(arr);

		scan.close();
	}

	static void sort(int[] arr) {
		int nextZero = 0;

		for(int i = 0; i < arr.length; i++) {
			if(arr[i] == 0) {
				int temp = arr[nextZero];
				arr[nextZero] = arr[i];
				arr[i] = temp;
				nextZero++;
			}
		}

		printArray(arr);
	}

	static void printArray(int[] arr) {
		for(int i = 0; i < arr.length; i++) {
			System.out.print(arr[i] + " ");
		}
	}
}
```
