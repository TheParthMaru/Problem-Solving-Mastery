**Problem statement**

- Given an integer array of size n, write a program to push all 0s to the end of the arry.

**Test cases**

```
Input:
n = 6
arr = 2 0 0 1 3 0 0

Output:
2 1 3 0 0 0 0
```

**Solution**

```java
import java.util.Scanner;

public class Main {
	public static void main(String[] args) {
		Scanner scan = new Scanner(System.in);

		int n = scan.nextInt();
		int arr[] = new int[n];

		for(int i = 0; i < arr.length; i++) {
			arr[i] = scan.nextInt();
		}

		pushZeroesToEnd(arr);
		scan.close();
	}

	static void pushZeroesToEnd(int arr[]) {
		int nonZero = 0;
		for(int i = 0; i < arr.length; i++) {
			if(arr[i] != 0) {
				int temp = arr[i];
				arr[i] = arr[nonZero];
				arr[nonZero] = temp;
				nonZero++;
			}
		}

		printArray(arr);
	}

	static void printArray(int arr[]) {
		for(int i = 0; i < arr.length; i++) {
			System.out.print(arr[i] + " ");
		}
	}
}
```
