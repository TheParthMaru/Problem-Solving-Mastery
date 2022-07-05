**Problem Statement**

- Given a positive binary number, find its equivalent decimal number.

**Test Cases**

```
Input: 1011
Output: 11

Input: 10101001
Output: 169
```

**Solution**

```java
import java.util.Scanner;

public class Main {

	public static void main(String args[]) {
		Scanner scan = new Scanner(System.in);

		int binary = scan.nextInt();
		int decimal  = 0, temp = binary;

		int base = 1; // 2 ^ 0

		while(temp != 0) {
			int lastDigit = temp % 10;
			decimal += lastDigit *  base;
			base *= 2;
			temp /= 10;
		}

		System.out.println(decimal);
		scan.close();
	}
}
```
