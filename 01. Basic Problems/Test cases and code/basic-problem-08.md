## Prime number

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

		if(isPrime(num)) {
			System.out.println("Prime");
		} else {
			System.out.println("Composite");
		}

		scan.close();
	}

	static boolean isPrime(int num) {
		// 2 is the smallest prime
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

_**Approach 3: Skipping even iterations and considering large numbers**_

- In the approach given above, if the size of the given number is too large than its square root will be also very large.
- So to deal with large size input we will deal with the few numbers such as 1, 2 ,3 and the numbers which are divisible by 2 and 3 in separate cases.
- For remaining numbers, we will iterate our loop from 5 to sqrt(number) and check for each iteration whether that iteration or (iteration+2) divides number or not.
- If we find any number that divides, we return false.

```java
import java.util.Scanner;

public class Main {

	public static void main(String args[]) {
		Scanner scan = new Scanner(System.in);

		int num = scan.nextInt();

		if (isPrime(num)) {
			System.out.println("Prime");
		} else {
			System.out.println("Composite");
		}

		scan.close();
	}

	static boolean isPrime(int num) {
		// 2 is the smallest prime number
		if (num <= 1) {
			return false;
		}

		if (num == 2 || num == 3) {
			return true;
		}

		// All numbers divisible by 2 or 3
		if (num % 2 == 0 || num % 3 == 0) {
			return false;
		}

		for (int i = 5; i * i <= num; i += 6) {
			if (num % i == 0 || num % (i + 2) == 0) {
				return false;
			}
		}

		return true;
	}
}
```
