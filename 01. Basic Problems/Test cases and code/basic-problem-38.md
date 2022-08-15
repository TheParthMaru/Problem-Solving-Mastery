## Add two fractions

**Problem statement**

- Take first fraction input as numerator1 and denominator1. Take second fraction input as numerator2 and denominator2. Add fraction 1 and 2 and the print the result in simplified form.

**Test case**

```
Input:
num1 = 5
deno1 = 3
num2 = 2
deno2 = 3

Output:
7/3

Input:
num1 = 1
deno1 = 500
num2 = 2
deno2 = 1500

Output:
1/300
```

**Solution**

```java
import java.util.Scanner;

public class Main {
	public static void main(String[] args) {

		Scanner scan = new Scanner(System.in);

		// First fraction
		int num1 = scan.nextInt();
		int deno1 = scan.nextInt();

		// Second fraction
		int num2 = scan.nextInt();
		int deno2 = scan.nextInt();

		// Result of addition will be one fraction
		int num, deno;

		// If denominator of fraction 1 and 2 is same
		if (deno1 == deno2) {
			num = num1 + num2;
			deno = deno1;
			calculateGcd(num, deno);
		} else {
			num = num1 * deno2 + num2 * deno1;
			deno = deno1 * deno2;
			calculateGcd(num, deno);
		}
		scan.close();
	}

	// GCD is used to simplify the fraction
	static void calculateGcd(int num, int deno) {
		int gcd = 1;

		for (int i = 1; i <= num || i <= deno; i++) {
			if (num % i == 0 && deno % i == 0) {
				gcd = i;
			}
		}

		// Simplifying the fraction values
		num /= gcd;
		deno /= gcd;

		System.out.println(num + "/" + deno);
	}
}
```
