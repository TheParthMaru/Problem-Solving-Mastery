**Problem Statement**

- Given two integer inputs num and exponent, calculate num to the power of exponent (num<sup>exponent</sup>).

**Test Cases**

```
Input: 2 5
Output: 32

Input: 5 3
Output: 125

Input: 11 0
Output: 1

Input: 0 1
Output: 0
```

**Solution**

```java
import java.util.Scanner;

public class Main {

	public static void main(String args[]) {

		Scanner scan = new Scanner(System.in);

		int num = scan.nextInt();
		int exponent = scan.nextInt();
		int result = 1;

		while(exponent != 0) {
			result *= num;
			exponent--;
		}

		System.out.println(result);

		scan.close();
	}

}
```
