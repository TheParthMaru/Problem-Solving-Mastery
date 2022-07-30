## Prime numbers in a given range

**Problem Statement**

- Given two integer inputs n1 and n2, write a program to display all the prime numbers between n1 and n2 inclusive.

**Test Cases**

```
Input: 2 10
Output: 2 3 5 7

Input: 11 50
Output: 11 13 17 19 23 29 31 37 41 43 47
```

**Solution**

```java
import java.util.Scanner;

public class Main {
	public static void main(String[] args) {
		Scanner scan = new Scanner(System.in);
		
		int n1 = scan.nextInt();
		int n2 = scan.nextInt();
		
		for(int i = n1; i <= n2; i++) {
			if(isPrime(i)) {
				System.out.print(i + " ");
			}
		}
		
		scan.close();
	}
	
	static boolean isPrime(int num) {
		// Eliminates all -ve numbers and 1
		if(num <= 1) {
			return false;
		}
		
		// 2 is the only even prime and 2 and 3 are the only consecutive primes
		if(num == 2 || num == 3) {
			return true;
		}
		
		// Most of the numbers are divisible by 2 and 3 so avoiding all those numbers
		if(num % 2 == 0 || num % 3 == 0) {
			return false;
		}
		
		// All the rest numbers
		for(int divisor = 5; divisor * divisor <= num; divisor += 6) {
			if(num % divisor == 0 || num % (divisor+2) == 0) {
				return false;
			}
		}
		
		return true;
	}
}
```
