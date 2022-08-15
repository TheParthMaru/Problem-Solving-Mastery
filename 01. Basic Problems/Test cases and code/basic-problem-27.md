## Count the number of digits in the integer

**Problems statement**

- Given an integer input, calculate the number of digits present in the integer.

**Test cases**

```
Input: 345
Output: 3

Input: 10001
Output: 5

Input: 1000
Output: 4
```

**Solution**

_**Approach 1: Iterative/ Bruteforce approach**_

**Note**

- In this approach numbers with leading 0s will result in incorrect output.
- 0001 will give answer as 1 instead of 4.
- You can use string based approach to overcome this edge case.

```java
import java.util.Scanner;

public class Main {

	public static void main(String args[]) {
		Scanner scan = new Scanner(System.in);

		int num = scan.nextInt();
		int digits = 0;

		while(num != 0) {
			++digits;
			num /= 10;
		}

		System.out.println(digits);

		scan.close();
	}
}
```

_**Approach 2: Log based approach**_

- `Math.log10()` return type is double
- `Math.log10(1) → 0.0`
- `Math.log10(9) → 0.954...`
- `Math.log10(10) → 1.0`
- `Math.log10(99) → 1.995...`
- This implies that `Math.log10(1)` to `Math.log10(9)` will result in 0.something.
- `Math.log10(10)` to `Math.log10(99)` will result in 1.something.
- So we can say that for single digit `Math.log10()` → 0, double digits → 1, triple digits → 2 and so on.
- Therefore, `Math.log(1234) = 3` and we can add 1 which gives us the total number of digits → 4.
- `log` is not defined for -ve nos so make sure to convert the +ve to -ve and then check.
- Even this approach won't work for test cases with leading 0s.

```java
import java.util.Scanner;

public class Main {

	public static void main(String args[]) {
		Scanner scan = new Scanner(System.in);

		int num = scan.nextInt();

    // Converting -ve numbers to +ve
		if(num < 0) {
			num *= -1;
		}

		// Log based approach
		int digits = (int) Math.floor(Math.log10(num) + 1);


		System.out.println(digits);

		scan.close();
	}
}
```
