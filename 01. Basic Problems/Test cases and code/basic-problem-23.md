**Problem Statement**

- Given two positive numbers num1 and num2, calculate its lcm.

**Test Cases**

```
Input: 10 11
Output: 110

Input: 12 14
Output: 84

Input: 1 10
Output: 10

Input: 0 1
Output: 0
```

**Solution**

````java
import java.util.Scanner;

public class Main {

	public static void main(String args[]) {

		Scanner scan = new Scanner(System.in);

		int num1 = scan.nextInt();
		int num2 = scan.nextInt();

		int lcm;

		if (num1 == 0 || num2 == 0) {
			lcm = 0;
		} else {
			lcm = (num1 * num2) / gcd(num1, num2);
		}

		System.out.println(lcm);

		scan.close();
	}

	static int gcd(int num1, int num2) {
		while (num1 != num2) {
			if (num1 > num2) {
				num1 -= num2;
			} else {
				num2 -= num1;
			}
		}
		return num1;
	}
}```
````
