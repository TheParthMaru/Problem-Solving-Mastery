## Sum of first n natural numbers

**Problem Statement**

- Given an integer input, write a program to find the sum of first n natural numbers.

**Test Cases**

```
Input: 5
Output: 15

Input: 10
Output: 55
```

**Solution**

_**Approach 1: Using loop**_

```java
import java.util.Scanner;

public class Main {

	public static void main(String[] args) {
		Scanner scan = new Scanner(System.in);

		int n = scan.nextInt();
		int sum = 0;

		for(int i = 1; i <= n; i++) {
			sum += i;
		}

		System.out.println(sum);

		scan.close();
	}
}
```

_**Approach 2: Using formula**_

```java
import java.util.Scanner;

public class Main {

	public static void main(String[] args) {
		Scanner scan = new Scanner(System.in);

		int n = scan.nextInt();
		int result = (n * (n + 1)) / 2;

		System.out.println(result);
		scan.close();
	}
}
```
