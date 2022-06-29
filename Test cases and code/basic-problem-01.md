**Problem Statement**

- Given an integer number as input, the objective is to write a program to check if the given number is positive or negative or zero.

**Test Cases**

```
Input: 12
Output: Positive

Input: -76
Output: Negative

Input: 0
Output: Zero
```

**Solution**

```java
import java.util.Scanner;

public class Main {
	public static void main(String[] args) {
		Scanner scan = new Scanner(System.in);

		int num = scan.nextInt();

		if(num > 0) {
			System.out.println("Positive");
		} else if(num < 0) {
			System.out.println("Negative");
		} else {
			System.out.println("Zero");
		}

		scan.close();

		}
	}
```
