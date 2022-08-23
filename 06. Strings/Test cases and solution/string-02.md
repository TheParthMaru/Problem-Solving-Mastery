## Toggle character case

**Problem statement**

- Given a string as input, write a program to change each character case in the string. If the character is in uppercase, change it to lowercase and vice-versa.

**Test cases**

```
Input: pARtH
Output: ParTh
```

**Solution**

```java
import java.util.Scanner;

public class Main {

	public static void main(String args[]) {
		Scanner scan = new Scanner(System.in);

		String s = scan.nextLine();
		String s1 = "";

		for(int i = 0; i < s.length(); i++) {
			if(Character.isUpperCase(s.charAt(i))) {
				s1 += Character.toLowerCase(s.charAt(i));
			} else {
				s1 += Character.toUpperCase(s.charAt(i));
			}
		}

		System.out.println(s1);
		scan.close();
	}
}
```
