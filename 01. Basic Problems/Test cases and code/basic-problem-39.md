## Convert alphabet case

**Problem statement**

- Write a program to enter any alphabet. If the entered alphabet is in lower case then convert it into upper case and if it is an upper case alphabet then convert it into lower case.

**Test case**

```
Input: l
Output: L

Input: Z
Output: z

Input: 5
Output: Invalid alphabet
```

**Solution**

```java
import java.util.Scanner;

public class Main {
	public static void main(String[] args) {

		Scanner scan = new Scanner(System.in);

		char alphabet = scan.next().charAt(0);

		if (alphabet >= 'A' && alphabet <= 'Z') {
			System.out.println((char) (alphabet + 32));
		} else if (alphabet >= 'a' && alphabet <= 'z') {
			System.out.println((char) (alphabet - 32));
		} else {
			System.out.println("Invalid alphabet");
		}

		scan.close();
	}
}
```
