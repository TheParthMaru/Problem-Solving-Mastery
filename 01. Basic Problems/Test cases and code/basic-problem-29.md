## nPr

**Problem statement**

- Given input as n and r, write a program to compute nPr.

**Test cases**

```
Input: 9 0
Output: 1

Input: 3 2
Output: 6
```

**Solution**

```java
import java.util.Scanner;

public class Main {

	public static void main(String args[]) {
		Scanner scan = new Scanner(System.in);

		int n = scan.nextInt();
		int r = scan.nextInt();
		
		System.out.println(calculateNPR(n, r));
		
		scan.close();
	}
	
	static int calculateNPR(int n, int r) {
		int nCr = calculateFactorial(n) / calculateFactorial(n-r);
		
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
