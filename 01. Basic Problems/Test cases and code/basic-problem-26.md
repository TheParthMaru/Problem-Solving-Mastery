**Problem statement**

- Given a positive number as input n, write a program to find the sum of all its even digits and odd digits seperately.

**Test cases**

```
Input:
n = 1234

Output:
sumEven = 6 sumOdd = 4

Input:
552245

Output:
8 15
```

**Solution**

```java
import java.util.Scanner;

public class Main {
	public static void main(String[] args) {
		Scanner scan = new Scanner(System.in);

		int num = scan.nextInt();
		int sumEven = 0, sumOdd = 0;

		while(num > 0) {
			int lastDigit = num % 10;
			if(lastDigit % 2 == 0) {
				sumEven += lastDigit;
			} else {
				sumOdd += lastDigit;
			}

			num /= 10;
		}

		System.out.println(sumEven + " " + sumOdd);

		scan.close();
	}
}
```
