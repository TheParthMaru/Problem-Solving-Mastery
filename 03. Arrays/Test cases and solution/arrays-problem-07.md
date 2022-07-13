**Problem statement**

- Given an integer array of size n, find the sum of all the elements in the array.

**Test cases**

```
Input:
n = 5
arr = 1 2 3 4 5

Output:
15

Input:
6
12 13 1 10 34 10

Output:
80
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

		// Sum of all elements
		int sum = 0;
		for (int i = 0; i < arr.length; i++) {
			sum += arr[i];
		}

		System.out.println(sum);
		scan.close();
	}
}
```
