**Problem Statement**

- Given an integer input, check whether the given number is an armstrong number or not.

**Note/Formula**

- abcd... = a<sup>n</sup> + b<sup>n</sup> + c<sup>n</sup> + d<sup>n</sup> + ...
- Example: 153 = 1<sup>3</sup> + 5<sup>3</sup> + 3<sup>3</sup>
- Power of 3 because total number of digits in 153 = 3.

**Test Cases**

```
Input: 153
Output: Armstrong number

Input: 370
Output: Armstrong number

Input: 1634
Output: Armstrong number

Input: 544
Output: Not an armstrong number
```

**Solution**

```java
import java.util.Scanner;

public class Main {

	public static void main(String args[]) {

		Scanner scan = new Scanner(System.in);

		int num = scan.nextInt();
		int digits = 0, temp = num;

		// Counting number of digits
		while(temp != 0) {
			digits++;
			temp /= 10;
		}

		// Re-initializing temp with num as it was reduced in above loop
		temp = num;
		int sum = 0;

		// Calculating armstrong number
		while(temp != 0) {
			int lastDigit = temp % 10;
			// Casting as Math.pow returns Double
			sum = (int) (sum + Math.pow(lastDigit, digits)); // Casting as Math.pow returns Double
			temp /= 10;
		}

		if(sum == num) {
			System.out.println("Armstrong number");
		} else {
			System.out.println("Not an armstrong number");
		}

		scan.close();
	}
}
```
