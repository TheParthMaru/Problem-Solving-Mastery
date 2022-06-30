**Problem Statement**

- Given an integer input number, write a program to calculate the sum of the digits of the given number.

**Test Cases**

```
Input: 1234
Output: 10

Input: 987654
Output: 39
```

**Solution**

```java
import java.util.Scanner;

public class Main {

	public static void main(String args[]) {

		Scanner scan = new Scanner(System.in);

		int num = scan.nextInt();
		int sum = 0;
		int temp = num;

		while(temp != 0) {
			int lastDigit = temp % 10;
			sum += lastDigit;
			temp /= 10;
		}

		System.out.println(sum);

		scan.close();
	}
}
```
