## Harshad Number

**Problem statement**

- Given an integer input, determine whether it is a harshad number or not.

**Notes/ Formula**

- Harshad number is a number or an integer in base 10 which is completely divisible by sum of its digits.
- Consider number 24, its digits are 2 and 4 and sum of its digits is 6 which divides 24.

**Test case**

```
Input: 24
Output: Yes

Input: 345
Output: No
```

**Solution**

```java
import java.util.Scanner;

public class Main {
	public static void main(String[] args) {

		Scanner scan = new Scanner(System.in);

		int num = scan.nextInt();

		System.out.println(isHarshad(num) ? "Harshad number" : "Not a harshad number");

		scan.close();
	}

	static boolean isHarshad(int num) {
		int sum = 0;
		for (int temp = num; temp > 0; temp /= 10) {
			sum += temp % 10;
		}
		return (num % sum == 0);
	}
}

```
