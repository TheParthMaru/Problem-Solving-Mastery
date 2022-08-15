## Palindrome number

**Problem Statement**

- Given an integer input, write a program to check whether the number is a palindrome number or not.

**Note**

- Ignore trailing or leading zeros (001 or 1000)

**Test Cases**

```
Input: 1234
Output: Not a palindrome

Input: 13231
Output: Palindrome
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

		if(reverse == num) {
			System.out.println("Palindrome");
		} else {
			System.out.println("Not a palindrome");
		}

		scan.close();
	}
}
```
