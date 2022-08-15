## Automorphic number

**Problem statement**

- Given an integer input, determine whether it is an automorphic number or not.

**Notes/ Formula**

- A Number that when squared ends with the number itself is known as the Automorphic Number.

**Test case**

```
Input: 5
Ouput: Yes

Input: 4
Output: No

Input: 6
Output: Yes
```

**Solution**

```java
import java.util.Scanner;

public class Main {
	public static void main(String[] args) {

		Scanner scan = new Scanner(System.in);

		int num = scan.nextInt();

		System.out.println(isAutomorphic(num) ? "Yes" : "No");

		scan.close();
	}

	static boolean isAutomorphic(int num) {
		int square = num * num;

		while(num > 0) {
			if(num % 10 != square % 10) {
				return false;
			}

			num /= 10;
			square /= 10;
		}

		return true;
	}
}
```
