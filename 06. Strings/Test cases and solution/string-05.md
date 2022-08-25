## Capitalize first and last letter of each word of a string.

**Test cases**

```
Input: parth bharat maru
Output: PartH BharaT MarU
```

**Solution**

**_Approach 1: Bruteforce using substring()_**

```java
import java.util.Scanner;

public class Main {

	public static void main(String args[]) {
		Scanner scan = new Scanner(System.in);

		String s1 = scan.nextLine();
		String s2 = "";
		String str[] = s1.split(" ");

		for(String currString : str) {
			int length = currString.length();
			String firstChar = currString.substring(0, 1);
			String lastChar = Character.toString(currString.charAt(length-1));
			String restChars = currString.substring(1, length-1);
			s2 += firstChar.toUpperCase() + restChars + lastChar.toUpperCase() + " " ;
		}

		System.out.println(s2);

		scan.close();
	}
}
```


