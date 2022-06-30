**Problem Statement**

- Given two integer inputs n1 and n2, write a program to find the sum of all the numbers between the given interval.

**Test Cases**

```
Input: 2 5
Output: 14

Input: -10 10
Output: 0

Input: 1 10
Output: 55
```

**Solution**

_**Approach 1: Iterative approach**_

```java
import java.util.Scanner;

public class Main {
	public static void main(String[] args) {
		Scanner scan = new Scanner(System.in);

		int n1 = scan.nextInt();
		int n2 = scan.nextInt();
		int sum = 0;

		for(int i = n1; i <= n2; i++) {
			sum += i;
		}

		System.out.println(sum);

		scan.close();
	}
}
```

_**Approach 2: Formula**_

```java
/*
 Formula: b*(b+1)/2 - a*(a+1)/2 + a
*/

import java.util.Scanner;

public class Main {
	public static void main(String[] args) {
		Scanner scan = new Scanner(System.in);

		int n1 = scan.nextInt();
		int n2 = scan.nextInt();
		int sum = (n2 * (n2 + 1) / 2) - (n1 * (n1 + 1) / 2) + n1;

		System.out.println(sum);

		scan.close();
	}
}
```
