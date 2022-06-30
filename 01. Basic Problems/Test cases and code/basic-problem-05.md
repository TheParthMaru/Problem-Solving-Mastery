**Problem Statement**

- Given two integer inputs n1 and n2, write a program to find the greatest of the two numbers.

**Test Cases**

```
Input: 2 5
Output: 5

Input: -10 10
Output: 10

Input: 99 99
Output: Equal
```

**Solution**

```java
import java.util.Scanner;

public class Main {
	public static void main(String[] args) {
		Scanner scan = new Scanner(System.in);

		int n1 = scan.nextInt();
		int n2 = scan.nextInt();

		if(n1 > n2) {
			System.out.println(n1);
		} else if(n1 < n2) {
			System.out.println(n2);
		} else {
			System.out.println("Equal");
		}

		scan.close();
	}
}
```
