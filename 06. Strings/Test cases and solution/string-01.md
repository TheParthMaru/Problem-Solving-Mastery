## Length of string without using the built-in length() method

**Problem statement**

- Write a program to find the length of the given string without using the built-in length() method.

**Test cases**

```
Input: parth
Output: 5

Input: a
Output: 1

Input: parth maru
Output: 10
```

**Solution**

```java
import java.util.Scanner;

public class Main {

	public static void main(String args[]) {
		Scanner scan = new Scanner(System.in);

		String s = scan.nextLine();
		int length = 0;

		for(char c : s.toCharArray()) {
			++length;
		}

		System.out.println(length);

		scan.close();
	}
}
```
