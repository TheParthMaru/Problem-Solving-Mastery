## Finding the number of times x digit occurs in a given input

**Problem statement**

- For a given integer number, count number of times x digits occurs in the input number.

**Test cases**

```
Input: 889889 8
Output: 4

Input: 97986 6
Output: 1

Input: 1234 9
Output: 0

Input: 20000 0
Output: 4
```

**Solution**

_**Approach 1: Iterative approach**_

- This approach will not provide correct answers for leading 0s.

```java
import java.util.Scanner;

public class Main {
	public static void main(String[] args) {

		Scanner scan = new Scanner(System.in);

		int num = scan.nextInt();
		int x = scan.nextInt();
		int count = 0;

		while(num > 0) {
			int lastDigit = num % 10;
			if(lastDigit == x) {
				count++;
			}
			num /= 10;
		}

		System.out.println(count);

		scan.close();
	}
}
```
