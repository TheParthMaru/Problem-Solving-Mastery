**Problem Statement**

- Given an integer input greater than 0, write a program to check whether entered number is prime or not.

**Test Cases**

```
Input: 23
Output: Prime

Input: 2
Output: Composite
```

**Solution**

_**Approach 1: Iterative/ Brutefore approach**_

```java
import java.util.Scanner;

public class Main {

	public static void main(String args[]) {

		Scanner scan = new Scanner(System.in);

		int num = scan.nextInt();
		boolean isPrime = true;

		for (int i = 2; i * i <= num; i++) {
			if (num % i == 0) {
				isPrime = false;
				break;
			}
		}

		if (num <= 1 || !isPrime) {
			System.out.println("Composite");
		} else {
			System.out.println("Prime");
		}

		scan.close();
	}
}
```

_**Approach 2: Skipping even iterations**_

```java
import java.util.Scanner;

public class Main {

	public static void main(String args[]) {

		Scanner scan = new Scanner(System.in);

		int num = scan.nextInt();
		boolean isPrime = checkPrime(num);

		if(isPrime) {
			System.out.println("Prime");
		} else {
			System.out.println("Composite");
		}

		scan.close();
	}

	static boolean checkPrime(int num) {
		if(num <= 1) {
			return false;
		}

		// 2 is the only even prime
		if(num == 2) {
			return true;
		}

		// All even numbers except 2 are not prime numbers
		if(num % 2 == 0) {
			return false;
		}

		// Checking for odd numbers
		for(int i = 3; i * i <= num; i+=2) {
			if(num % i == 0) {
				return false;
			}
		}

		return true;
	}
}
```
