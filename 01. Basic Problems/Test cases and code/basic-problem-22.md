**Problem Statement**

- Given two positive numbers num1 and num2, calculate its gcd or hcf.

**Test Cases**

```
Input: 8 12
Output: 4

Input: 18 12
Output: 6

Input: 36 60
Output: 12

Input: 5 7
Output: 1
```

**Solution**
_**Approach 1: **_ Bruteforce

```java
import java.util.Scanner;

public class Main {

	public static void main(String args[]) {

		Scanner scan = new Scanner(System.in);

		int num1 = scan.nextInt();
		int num2 = scan.nextInt();
		int gcd = 1;

		for(int i = 1; i <= num1 || i <= num2; i++) {
			if(num1 % i == 0 && num2 % i == 0) {
				gcd = i;
			}
		}

		System.out.println(gcd);

		scan.close();
	}
}
```

_**Approach 2: **_ Euclidean algorithm - repetitive subtraction

```java
import java.util.Scanner;

public class Main {

	public static void main(String args[]) {

		Scanner scan = new Scanner(System.in);

		int num1 = scan.nextInt();
		int num2 = scan.nextInt();

		while (num1 != num2) {
			if (num1 > num2) {
				num1 -= num2;
			} else {
				num2 -= num1;
			}
		}

		System.out.println(num1);

		scan.close();
	}
}
```
