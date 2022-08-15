## Armstrong number

**Problem Statement**

- Given an integer input, check whether the given number is an armstrong number or not.

**Note/Formula**

- abcd... = a<sup>n</sup> + b<sup>n</sup> + c<sup>n</sup> + d<sup>n</sup> + ...
- Example: 153 = 1<sup>3</sup> + 5<sup>3</sup> + 3<sup>3</sup>
- Power of 3 because total number of digits in 153 = 3.
- Armstrong number cannot be negative.

**Test Cases**

```
Input: 153
Output: Armstrong number

Input: 370
Output: Armstrong number

Input: -98
Output: Invalid number

Input: 1634
Output: Armstrong number

Input: 544
Output: Not an armstrong number
```

**Solution**

```java
import java.util.Scanner;

public class Main {
	public static void main(String[] args) {

		Scanner scan = new Scanner(System.in);

		int num = scan.nextInt();

		if (num < 0) {
			System.out.println("Invalid number");
		} else if (isArmstrong(num)) {
			System.out.println("Armstrong number");
		} else {
			System.out.println("Not a armstrong number");
		}

		scan.close();
	}

	static boolean isArmstrong(int num) {
		int digits = (int) (Math.floor(Math.log10(num) + 1));
		int temp = num;
		int sum = 0;

		while (temp > 0) {
			int lastDigit = temp % 10;
			sum = (int) (sum + Math.pow(lastDigit, digits));
			temp /= 10;
		}

		if (sum == num) {
			return true;
		} else {
			return false;
		}
	}
}
```
