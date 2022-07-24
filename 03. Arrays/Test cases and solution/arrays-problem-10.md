## Print all pairs

**Problem statement**

- Given an integer input array of size n, write a program to print all no repeting integers.

**Test cases**

```
Input:
n = 3
arr = 1 2 3

Output:
{1,2} {1,3} {2,3}

Explanation:
- Pair shouldn't have repeting elements: {1,1} {2,2} {3,3}
- {1,2} and {2,1} is considered as same so avoid having such repetition also.

Input:
5
1 2 3 4 5

Output:
{1,2} {1,3} {1,4} {1,5} {2,3} {2,4} {2,5} {3,4} {3,5} {4,5}
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

		printAllPairs(arr);

		scan.close();
	}

	static void printAllPairs(int[] arr) {
		for(int i = 0; i < arr.length - 1; i++) {
			for(int j = i+1; j < arr.length; j++) {
				System.out.print("{" + arr[i] + "," + arr[j] + "}" + " ");
			}
		}
	}
}
```
