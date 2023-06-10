## Quadrants in which given coordinates lies

**Problem statement**

- Given two integer points as inputs, determine which in quadrant the given points lies.

**Test cases**

```
Input: 0 0
Output: origin

Input: 0 6
Output: y-axis

Input: 3 0
Output: x-axis

Input: 1 4
Output: Quadrant I

Input: -3 7
Output: Quadrant II

Input: -5 -6
Output: Quadrant III

Input: 2 -8
Output: Quadrant IV
```

**Solution**

```java
import java.util.Scanner;

public class Main {
	public static void main(String[] args) {

		Scanner scan = new Scanner(System.in);

		int x = scan.nextInt();
		int y = scan.nextInt();

		if (x == 0 && y == 0) {
			System.out.println("origin");
		} else if (x == 0) {
			System.out.println("y-axis");
		} else if (y == 0) {
			System.out.println("x-axis");
		} else if (x > 0 && y > 0) {
			System.out.println("Quadrant I");
		} else if (x < 0 && y > 0) {
			System.out.println("Quadrant II");
		} else if (x < 0 && y < 0) {
			System.out.println("Quadrant III");
		} else {
			System.out.println("Quadrant IV");
		}

		scan.close();
	}
}
```
