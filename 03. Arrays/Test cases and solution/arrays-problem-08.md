**Problem statement**

- You have been given an empty array and its size n. The only input taken from the user will be n. Your task is to populate the array using the integer values in the range 1 to n(both inclusive) in the order: 1,3,.......4,2.

**Test cases**

```
Input: 6
Output: 1 3 5 6 4 2

Input: 9
Output: 1 3 5 7 9 8 6 4 2
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

		// Populating the array
		int left = 0, right = n - 1, number = 1;

		while (left <= right) {
			if (number % 2 == 1) {
				arr[left] = number;
				number++;
				left++;
			} else {
				arr[right] = number;
				number++;
				right--;
			}
		}

		// Printing the array
		for (int i = 0; i < arr.length; i++) {
			System.out.print(arr[i] + " ");
		}

		scan.close();
	}
}
```
