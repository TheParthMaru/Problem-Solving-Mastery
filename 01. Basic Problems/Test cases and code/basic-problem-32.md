## Factorial of a number

**Problem Statement**

- Given an integer number as input, calculate its factorial.

**Test Cases**

```
Input: 5
Output: 120

Input: 0
Output: 1
```

**Solution**

```java
import java.util.Scanner;

public class Main {

	public static void main(String args[]) {

		Scanner scan = new Scanner(System.in);

		int num = scan.nextInt();
		int fact = 1;

		for (int i = 1; i <= num; i++) {
			fact *= i;
		}

		System.out.println(fact);

		scan.close();
	}

}
```
