## Greatest of three numbers

**Problem Statement**

- Given two integer inputs n1, n2 and n3, write a program to find the greatest of the three numbers.

**Test Cases**

```
Input: 2 5 7
Output: 7

Input: -10 10 0
Output: 10

Input: 3 5 2
Output: 5
```

**Solution**

_**Approach 1: Using if else**_

```java
import java.util.Scanner;

public class Main {

	public static void main(String args[]) {

		Scanner scan = new Scanner(System.in);

		int n1 = scan.nextInt();
		int n2 = scan.nextInt();
		int n3 = scan.nextInt();

		if(n1 >= n2 && n1 >= n3) {
			System.out.println(n1);
		} else if(n2 >= n3) {
			System.out.println(n2);
		} else {
			System.out.println(n3);
		}

		scan.close();
	}
}
```

_**Approach 2: Using ternary operator**_

```java
import java.util.Scanner;

public class Main {

	public static void main(String args[]) {
		Scanner scan = new Scanner(System.in);

		int num1 = scan.nextInt();
		int num2 = scan.nextInt();
		int num3 = scan.nextInt();

		int result = (num1 >= num2) ? (num1 >= num3 ? num1 : num3) : (num2 >= num3 ? num2 : num3);
		System.out.println(result);

		scan.close();
	}
}
```
