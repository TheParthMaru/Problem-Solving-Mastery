## Remove vowels from string

**Problem statement**

- Given an input string, remove all the vowels present in it.

**Test cases**

```
Input: parth
Output: prth

Input: vaidehi
Output: vdh
```

**Solution**

\_**Approach 1:**\_Bruteforce approach

```java
import java.util.Scanner;

public class Main {

	public static void main(String args[]) {
		Scanner scan = new Scanner(System.in);

		String s = scan.nextLine();
		String s1 = "";

		for(int i = 0; i < s.length(); i++) {
			if(s.charAt(i) == 'A' || s.charAt(i) == 'a' ||s.charAt(i) == 'E' ||s.charAt(i) == 'e' ||s.charAt(i) == 'I' ||s.charAt(i) == 'i' ||s.charAt(i) == 'O' ||s.charAt(i) == 'o' ||s.charAt(i) == 'U' ||s.charAt(i) == 'u') {
				continue;
			} else {
				s1 += s.charAt(i);
			}
		}

		System.out.println(s1);

		scan.close();
	}
}
```

**_Approach 2: Regex based_**
