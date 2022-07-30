## Even or odd

**Problem Statement**

- Given an integer number as input, write a program to check whether the input number is even or odd.

**Test Cases**

```
Input: 11
Output: Odd

Input: -62
Output: Even

Input: 0
Output: Even
```

**Solution**

```java
import java.util.Scanner;

public class Main {
	public static void main(String[] args) {
		Scanner scan = new Scanner(System.in);

		int num = scan.nextInt();

		if(num % 2 == 0) {
			System.out.println("Even");
		} else {
			System.out.println("Odd");
		}

		scan.close();
	}
}
```
