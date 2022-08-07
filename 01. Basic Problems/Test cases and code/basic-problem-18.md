## Factors of a number

**Problem Statement**

- Given a positive number as input, find its factors.

**Test Cases**

```
Input: 100
Output: 1 2 4 5 10 20 25 50 100

Input: 15
Output: 1 3 5 15
```

**Solution**

_**Approach 1: Bruteforce approach**_
- Doesn't handle negative numbers.

```java
import java.util.ScanApproach 1: Bruteforce approachner;

public class Main {
	public static void main(String[] args) {
		Scanner scan = new Scanner(System.in);
		
		int num = scan.nextInt();
		
		for(int i = 1; i <= num; i++) {
			if(num % i == 0) {
				System.out.print(i + " ");
			}
		}
		
		scan.close();
	}
}
```

_**Approach 2: Pairs of factors**_
- In this approach we find pairs of factors.
- For example consider num = 100.
- Pairs of factors will be (1, 100), (2, 50), (4, 25), (5, 20) and (10, 10).
- The repeating factor needs to be printed only once.
- This approach won't print factors in sorted order so to overcome that we can use ArrayList.
- Doesn't handle negative numbers.
```java
import java.util.Scanner;

public class Main {
	public static void main(String[] args) {

		Scanner scan = new Scanner(System.in);
		
		int num = scan.nextInt();
		
		for(int i = 1; i <= Math.sqrt(num); i++) {
			if(num % i == 0) {
				// Checking if factors are repeated
				if(num/i == i) {
					System.out.print(i);
				} else {
					System.out.print(num/i + " " + i + " ");
				}
			}
		}
		
		scan.close();
	}
}
```

_**Approach 3: Handling -ve numbers**_
- The drawback of above two approaches is that it cannot handle negative numbers.
- So to find factors of negative numbers follow the below approach.

```java
import java.util.Scanner;

public class Main {
	public static void main(String[] args) {

		Scanner scan = new Scanner(System.in);

		int num = scan.nextInt();

		if (num < 0) {
			for (int i = num; i <= Math.abs(num); i++) {
				if (i == 0) {
					continue;
				} else {
					if (num % i == 0) {
						System.out.print(i + " ");
					}
				}
			}
		} else {
			for (int i = 1; i <= Math.sqrt(num); i++) {
				if (num % i == 0) {
					if (num / i == i) {
						System.out.print(" " + i);
					} else {
						System.out.print(i + " " + num / i + " ");
					}
				}
			}
		}

		scan.close();
	}
}
```
