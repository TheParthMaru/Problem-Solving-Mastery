## Fibonacci series upto n terms

**Problem Statement**

- Given an integer input n, print fibonacci series upto n terms.

**Test Cases**

```
Input: 4
Output: 0 1 1 2

Input: 15
Output: 0 1 1 2 3 5 8 13 21 34 55 89 144 233 377
```

**Solution**

```java
import java.util.Scanner;

public class Main {

	public static void main(String args[]) {

		Scanner scan = new Scanner(System.in);

		int n = scan.nextInt();
		int termA = 0, termB = 1;
		System.out.print(termA + " " + termB + " ");


		// Starting from 3 because first two terms are fixed that is 0 and 1
		for (int i = 3; i <= n; i++) {
			int nextTerm = termA + termB;
			System.out.print(nextTerm + " ");
			termA = termB;
			termB = nextTerm;
		}
		scan.close();
	}
}
```
