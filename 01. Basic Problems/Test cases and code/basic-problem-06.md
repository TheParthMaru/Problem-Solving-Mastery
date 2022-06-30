**Problem Statement**

- Given two integer inputs n1, n2 and n3, write a program to find the greatest of the two numbers.

**Test Cases**

```
Input: 2 5 7
Output: 7

Input: -10 10 0
Output: 10

Input: 3 5 2
Output: 5
```

**Solution**

```java
import java.util.Scanner;

public class Main {

	public static void main(String args[]) {

		Scanner scan = new Scanner(System.in);

		int n1 = scan.nextInt();
		int n2 = scan.nextInt();
		int n3 = scan.nextInt();

		if(n1 >= n2 && n1 >= n3) {
			System.out.println(n1);
		} else if(n2 >= n3) {
			System.out.println(n2);
		} else {
			System.out.println(n3);
		}

		scan.close();
	}
}
```
