## Print duplicate elements

**Problem statement**

- Write a program to input n size integer array and print the duplicate elements.
- First input will be n, then the array elements.

**Test cases**

```
Input:
9
1 2 3 4 2 7 8 8 3
Output:
2 3 8
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

		// Finding duplicates
		for(int i = 0; i < arr.length - 1; i++) {
			for(int j = i+1; j < arr.length; j++) {
				if(arr[i] == arr[j]) {
					System.out.print(arr[i] + " ");
				}
			}
		}

		scan.close();
	}
}
```
