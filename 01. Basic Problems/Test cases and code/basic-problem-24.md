## Reverse digits of a number

**Problem Statement**

- Given a integer input, write the program to reverse the given number.

**Note**

- Ignore trailing or leading zeros (001 or 1000)

**Test Cases**

```
Input: 1234
Output: 4321

Input: 13233
Output: 33231
```

**Solution**

```java
import java.util.Scanner;

public class Main {

	public static void main(String args[]) {

		Scanner scan = new Scanner(System.in);

		int num = scan.nextInt();
		int reverse = 0;
		int temp = num;

		while(temp != 0) {
			int lastDigit = temp % 10;
			reverse =  reverse * 10 + lastDigit;
			temp /= 10;
		}

		System.out.println(reverse);

		scan.close();
	}
}
```
