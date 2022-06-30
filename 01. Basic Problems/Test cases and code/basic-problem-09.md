**Problem Statement**

- Given two integer inputs n1 and n2, write a program to display all the prime numbers between n1 and n2 inclusive.

**Test Cases**

```
Input: 2 10
Output: 2 3 5 7

Input: 11 50
Output: 11 13 17 19 23 29 31 37 41 43 47
```

**Solution**

```java
import java.util.Scanner;

public class Main {

	public static void main(String args[]) {

		Scanner scan = new Scanner(System.in);

		int n1 = scan.nextInt();
		int n2 = scan.nextInt();

		for (int i = n1; i <= n2; i++) {
			// Prime numbers start from 2
			if (i <= 1) {
				continue;
			}

			boolean isPrime = checkPrime(i);

			if (isPrime) {
				System.out.print(i + " ");
			}
		}

		scan.close();
	}

	static boolean checkPrime(int num) {
		for (int i = 2; i * i <= num; i++) {
			if (num % i == 0) {
				return false;
			}
		}

		return true;
	}
}
```
