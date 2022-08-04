## Quadrants in which given coordinates lies

**Test cases**

```
Input: 0 0
Output: Origin

Input: 1 6
Output: 1

Input: -6 3
Output: 2

Input: -5 -5
Output: 3

Input: 1 -1
Output: 4
```

```java
import java.util.Scanner;

public class Main {
	public static void main(String[] args) {

		Scanner scan = new Scanner(System.in);

		int x = scan.nextInt();
		int y = scan.nextInt();

		if (x == 0 && y == 0) {
			System.out.println("Origin");
		} else {
			System.out.println(findQuadrant(x, y));
		}
		scan.close();
	}

	static int findQuadrant(int x, int y) {

		if (x > 0 && y > 0) {
			return 1;
		} else if (x < 0 && y > 0) {
			return 2;
		} else if (x < 0 && y < 0) {
			return 3;
		} else {
			return 4;
		}
	}
}
```
