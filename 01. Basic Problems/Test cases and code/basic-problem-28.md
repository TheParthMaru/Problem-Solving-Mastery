## nCr

**Problem statement**

- Given input as n and r, write a program to compute nCr.

**Test cases**

```
Input: 12 5
Output: 792

Input: 5 0
Output: 1
```

**Solution**

```java
import java.util.Scanner;

public class Main {

	public static void main(String args[]) {
		Scanner scan = new Scanner(System.in);

		int n = scan.nextInt();
		int r = scan.nextInt();

		System.out.println(calculateNCR(n, r));

		scan.close();
	}

	static int calculateNCR(int n, int r) {
		int nCr = calculateFactorial(n) / (calculateFactorial(r) * calculateFactorial(n-r));

		return nCr;
	}

	static int calculateFactorial(int num) {
		int factorial = 1;

		for(int i = 1; i <= num; i++) {
			factorial = factorial * i;
		}

		return factorial;
	}
}
```
