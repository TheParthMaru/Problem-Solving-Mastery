## Palindrome

**Problem statement**

- Given an input string, check whether it is palindrome or not.

**Test cases**

```
Input: madam
Output: yes

Input: aloo
Output: no
```

**Solution**
**_Approach 1_**: Bruteforce

```java
import java.util.Scanner;

public class Main {

	public static void main(String args[]) {
		Scanner scan = new Scanner(System.in);

		String s = scan.nextLine();
		String s1 = "";

		for(int i = s.length()-1; i >= 0; i--) {
			s1 += s.charAt(i);
		}

		if(s.equalsIgnoreCase(s1)) {
			System.out.println("yes");
		} else {
			System.out.println("no");
		}

		scan.close();
	}
}
```
