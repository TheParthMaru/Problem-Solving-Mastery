## Perfect Square

**Problem statement**

- Given an integer input, determine whether it is a perfect square or not.

**Test case**

```
Input: 64
Output: Yes

Input: 97
Output: No

```

**Solution**

```java
import java.util.Scanner;

public class Main {
	public static void main(String[] args) {

		Scanner scan = new Scanner(System.in);

		int num = scan.nextInt();

		if (isPerfectSquare(num)) {
			System.out.println("Yes");
		} else {
			System.out.println("No");
		}

		scan.close();
	}

	static boolean isPerfectSquare(int num) {
		if (num >= 0) {
			int squareRoot = (int) Math.sqrt(num);
			return ((squareRoot * squareRoot) == num);
		}
		return false;
	}
}
```
