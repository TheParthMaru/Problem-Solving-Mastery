## Perfect Square

**Solution**

_**Approach 1**_

```java
import java.util.Scanner;

public class Main {
	public static void main(String[] args) {

		Scanner scan = new Scanner(System.in);

		int num = scan.nextInt();

		if (isPerfectSquare(num)) {
			System.out.println("Perfect square");
		} else {
			System.out.println("Not a perfect square");
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
