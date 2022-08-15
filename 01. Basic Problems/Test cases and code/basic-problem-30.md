## Nth armstrong number

**Problem statement**

- Given an integer input n, find the nth armstrong number.

**Test case**

```
Input: 10
Output: 153

Input: 13
Output: 407
```

**Solution**

```java
import java.util.Scanner;

public class Main {

	public static void main(String args[]) {
		Scanner scan = new Scanner(System.in);

		int n = scan.nextInt();

		System.out.println(nthArmstrong(n));

		scan.close();
	}

	static int nthArmstrong(int n) {
		int count = 0;
		for(int i = 1; i <= Integer.MAX_VALUE; i++) {
			int num = i;
			int digits = (int) Math.floor(Math.log10(num) + 1);

			if(checkArmstrong(num, digits)) {
				++count;
			}

			if(count == n) {
				return i;
			}
		}
		return n;
	}

	static boolean checkArmstrong(int num, int digits) {
		int temp = num, sum = 0;
		while(temp != 0) {
			int lastDigit = temp % 10;
			sum = (int) (sum + Math.floor(Math.pow(lastDigit, digits)));
			temp /= 10;
		}

		if(sum == num) {
			return true;
		}

		return false;
	}
}
```
