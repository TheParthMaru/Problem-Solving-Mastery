**Problem statement**

- Write a program to take n size integer array as input and print the minimum and maximum element in it.

**Test cases**

```
Input:
5
1 2 3 4 5

Output:
Minimum = 1
Maximum = 5

Input:
3
3 1 3

Output:
Minimum = 1
Maximum = 3

Input:
1
2

Output:
Minimum = 2
Maximum = 2
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

		// Finding minimum and maximum
		int minimum, maximum;
		if (n == 1) {
			minimum = arr[0];
			maximum = arr[0];
			printMinMax(minimum, maximum);
			return;
		}

		if(arr[0] < arr[1]) {
			minimum = arr[0];
			maximum = arr[1];
		} else {
			maximum = arr[0];
			minimum = arr[1];
		}

		for(int i = 2; i < arr.length; i++) {
			if(arr[i] < minimum) {
				minimum = arr[i];
			}
			if(arr[i] > maximum) {
				maximum = arr[i];
			}
		}

		printMinMax(minimum, maximum);
		scan.close();
	}

	// Printing minmax
	static void printMinMax(int min, int max) {
		System.out.println("Minimum = " + min);
		System.out.println("Maximum = " + max);
	}
}
```
