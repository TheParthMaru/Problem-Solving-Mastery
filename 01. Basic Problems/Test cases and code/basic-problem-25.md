## Octal to decimal

**Problem Statement**

- Given a positive octal number, find its equivalent decimal number.

**Test Cases**

```
Input: 20
Output: 16

Input: 2001
Output: 1025
```

**Solution**

```java
public class Main {

	public static void main(String args[]) {
		Scanner scan = new Scanner(System.in);

		int octal = scan.nextInt();
		int decimal  = 0, temp = octal;

		int base = 1; // 2 ^ 0

		while(temp != 0) {
			int lastDigit = temp % 10;
			decimal += lastDigit *  base;
			base *= 8;
			temp /= 10;
		}

		System.out.println(decimal);
		scan.close();
	}
}
```
