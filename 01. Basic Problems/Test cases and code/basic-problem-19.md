**Problem Statement**

- Given a positive integer number as an input, print all prime factors of the number.

**Test Cases**

```
Input: 48
Output: 2 2 2 2 3

Input: 12
Output: 2 2 3

Input: 90
Output: 2 3 3 5
```

**Solution**

```java
import java.util.Scanner;

public class Main {

	public static void main(String args[]) {

		Scanner scan = new Scanner(System.in);

		int num = scan.nextInt();
		int divisor = 2;

		while (num != 1) {
			if (isPrime(divisor)) {
				if (num % divisor == 0 && num >= divisor) {
					System.out.print(divisor + " ");
					num /= divisor;
				} else {
					divisor++;
				}
			} else {
				divisor++;
			}
		}

		scan.close();
	}

  // Method to check whether divisor is prime or not
	static boolean isPrime(int divisor) {

		for (int i = 2; i * i <= divisor; i++) {
			if (divisor % i == 0) {
				return false;
			}
		}

		return true;
	}
}
```
