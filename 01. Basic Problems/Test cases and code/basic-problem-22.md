## Strong number

**Problem Statement**

- Given a positive integer input, check whether the entered number is a strong number or not.

**Notes/ Formula**

- For a number to be a strong number, the sum of factorial of each digit of the number should equal to the number itself.
- Example: 145 = 1! + 4! + 5!

**Test Cases**

```
Input: 145
Output: Strong number

Input: 444
Output: Not a strong number

Input: 2
Output: Strong number
```

**Solution**

```java
import java.util.Scanner;

public class Main {

	public static void main(String args[]) {

		Scanner scan = new Scanner(System.in);

		int num = scan.nextInt();
		int temp = num, sum = 0;

		while(temp != 0) {
			int lastDigit = temp % 10;
			sum = sum + factorial(lastDigit);
			temp /= 10;
		}

		if(sum == num) {
			System.out.println("Strong number");
		} else {
			System.out.println("Not a strong number");
		}

		scan.close();
	}

	static int factorial(int number) {
		int fact = 1;
		for(int i = 1; i <= number; i++) {
			fact *= i;
		}

		return fact;
	}
}
```
