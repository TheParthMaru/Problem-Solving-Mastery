## Vowel or not

**Problem statement**

- Write a program to input an alphabet and determine whether it is a vowel or not.

**Test case**

```
Input: A
Output: Yes

Input: Z
Output: no
```

**Solution**
_**Approach 1: If-else**_

```java
import java.util.Scanner;

public class Main {
	public static void main(String[] args) {

		Scanner scan = new Scanner(System.in);

		char alphabet = scan.next().charAt(0);

		alphabet = (char) (alphabet + 32);

		if (alphabet == 'a' || alphabet == 'e' || alphabet == 'i' || alphabet == 'o' || alphabet == 'u') {
			System.out.println("Yes");
		} else {
			System.out.println("No");
		}

		scan.close();
	}
}
```

_**Approach 2: Switch case**_

```java
import java.util.Scanner;

public class Main {
	public static void main(String[] args) {

		Scanner scan = new Scanner(System.in);

		char alphabet = scan.next().charAt(0);

		switch (alphabet) {
		case 'A':
		case 'a':
		case 'E':
		case 'e':
		case 'I':
		case 'i':
		case 'O':
		case 'o':
		case 'U':
		case 'u':
			System.out.println("Yes");
			break;
		default:
			System.out.println("No");


		}

		scan.close();
	}
}
```
