## Count uppercase, lowercase and digits

**Problem statement**

- Write a program to read a character until a \* is encountered. Also, count the number of uppercase, lowercase and nuumbers entered.

**Test case**

```
Input:
1
2
3
4
A
C
D
s
x
*

Output:
Uppercase: 3
Lowercase: 2
Numbers: 4
```

**Solution**

```java
import java.util.Scanner;

public class Main {
	public static void main(String[] args) {

		Scanner scan = new Scanner(System.in);

		char character = scan.nextLine().charAt(0);

		int lowercase = 0, uppercase = 0, numbers = 0;

		do {

			if (character >= 'A' && character <= 'Z') {
				uppercase++;
			} else if (character >= 'a' && character <= 'z') {
				lowercase++;
			} else if (character >= '0' && character <= '9') {
				numbers++;
			}
			character = scan.nextLine().charAt(0);
		} while (character != '*');

		System.out.println("Uppercase: " + uppercase);
		System.out.println("Lowercase: " + lowercase);
		System.out.println("Numbers: " + numbers);

		scan.close();
	}
}
```
