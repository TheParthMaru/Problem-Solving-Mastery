**Problem Statement**

- Given an integer number as input, find its factors.

**Test Cases**

```
Input: 100
Output: 1 2 4 5 10 20 25 50 100

Input: 15
Output: 1 3 5 15
```

**Solution**

```java
import java.util.Scanner;

public class Main {

	public static void main(String args[]) {

		Scanner scan = new Scanner(System.in);

		int num = scan.nextInt();

		for(int i = num; i <= Math.abs(num); i++) {
			if(i == 0) {
				continue;
			} else {
				if(num % i == 0) {
					System.out.print(i + " ");
				}
			}
		}
		scan.close();
	}
}
```
