## Leap year

**Problem Statement**

- Given an integer input "year", write a program to find whether the given year is a leap year or not.

**Note**

- A year is leap when either
  - The year must be divisible by 400.
  - The year must be divisible by 4 but not 100.

**Test Cases**

```
Input: 2019
Output: Not a leap year

Input: 2016
Output: Leap year
```

**Solution**

```java
import java.util.Scanner;

public class Main {

	public static void main(String args[]) {

		Scanner scan = new Scanner(System.in);

		int year = scan.nextInt();

		if ((year % 400 == 0) || ((year % 4 == 0) && (year % 100 != 0))) {
			System.out.println("Leap year");
		} else {
			System.out.println("Not a leap year");
		}

		scan.close();
	}
}
```
