## Perfect number

**Problem Statement**

- Given a positive number, find whether the number is a perfect number or not.

**Notes/ Formula**

- A number where the sum of its divisors (excluding the number itself) is equal to the number itself.
- Example: 6 = 1 + 2 + 3 where 1,2 and 3 are divisors of 6

**Test Cases**

```
Input: 6
Output: Perfect number

Input: 28
Output: Perfect number

Input: 100
Output: Not a perfect number
```

**Solution**

```java
import java.util.Scanner;

public class Main {

	public static void main(String args[]) {

		Scanner scan = new Scanner(System.in);

		int num = scan.nextInt();
		int sum = 0;

		for(int i = 1; i <= num/2; i++) {
			if(num % i == 0) {
				sum += i;
			}
		}

		if(sum == num) {
			System.out.println("Perfect number");
		} else {
			System.out.println("Not a perfect number");
		}

		scan.close();
	}
}
```
