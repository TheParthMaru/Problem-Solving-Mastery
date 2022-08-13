## Swap two numbers

**Problem statement**

- Given two integer inputs, swap two inputs.

**Test cases**

```
Input: 5 10
Output: 10 5

Input: 2 -3
Output: -3 2
```

**Solution**
_**Approach 1: Using temporary variable**_

```java
import java.util.Scanner;

public class Main {
	public static void main(String[] args) {

		Scanner scan = new Scanner(System.in);

		int num1 = scan.nextInt();
		int num2 = scan.nextInt();

		int temp = num1;
		num1 = num2;
		num2 = temp;

		System.out.println(num1 + " " + num2);
		scan.close();
	}
}
```

_**Approach 2: Not using temporary variable**_

```java
import java.util.Scanner;

public class Main {
	public static void main(String[] args) {

		Scanner scan = new Scanner(System.in);

		int num1 = scan.nextInt();
		int num2 = scan.nextInt();

		num1 = num1 + num2;
		num2 = num1 - num2;
		num1 = num1 - num2;

		System.out.println(num1 + " " + num2);
		scan.close();
	}
}
```
