**Problem Statement**

- Given two integers n1 and n2, print all the armstrong numbers between n1 and n2 inclusive.

**Test Cases**

```
Input: 1 500
Output: 1 2 3 4 5 6 7 8 9 153 370 371 407

Input: 1000 2000
Output: 1634
```

**Solution**

```java
import java.util.Scanner;

public class Main {

	public static void main(String args[]) {

		Scanner scan = new Scanner(System.in);

		int n1 = scan.nextInt();
		int n2 = scan.nextInt();

		for(int i = n1; i <= n2; i++) {
			int digits = countDigits(i);
			boolean isArmstrong = checkArmstrong(i, digits);

			if(isArmstrong) {
				System.out.print(i + " ");
			}
		}
		scan.close();
	}

	// Method to count number of digits
	static int countDigits(int num) {
		int count = 0;
		while(num != 0) {
			count++;
			num /= 10;
		}

		return count;
	}

	// Method to calculate armstrong number
	static boolean checkArmstrong(int num, int digits) {
		int sum = 0, temp = num;

		while(temp != 0) {
			int lastDigit = temp % 10;
			sum = (int) (sum + Math.pow(lastDigit, digits));
			temp /= 10;
		}

		if(sum == num) {
			return true;
		}

		return false;
	}
}
```
