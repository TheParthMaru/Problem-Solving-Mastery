# Basic problems

1. Positive or negative numbers ✔
2. Even or odd ✔
3. Sum of first n natural numbers ✔

- Formula approach ✔
- Iterative approach ✔

4. Sum of numbers in a given range ✔

- Formula approach ✔
- Iterative approach ✔

5. Greatest of two numbers

- Using if else ✔
- Using ternary operator ✔

6. Greatest of three numbers

- Using if else ✔
- Using ternary operator ✔

7. Leap year ✔
8. Prime number ✔

- Iterative approach ✔
- Approach with skiping even iterations ✔
- Approach with considering large numbers ✔

9. Prime numbers in a given range ✔
10. Sum of digits of a number ✔
11. Reverse digits of a number ❌

- Ignoring leading and trailing 0s ✔
- Approach using strings ❌
- Recursive approach ❌
- Handling -ve numbers(Required for recursive approach) ❌

12. Palindrome number ❌

- Iterative approach ✔
- Recursive approach ❌
- Check [gfg](https://www.geeksforgeeks.org/check-if-a-number-is-palindrome/) for string approaches.

13. Calculate the number of digits in the integer ❌

- Iterative approach ✔
- Recursive approach ❌
- Log based approach ✔
- [String based approach](https://www.geeksforgeeks.org/program-count-digits-integer-3-different-methods/) ❌

14. Armstrong number ❌

- Iterative approach ✔
- Recursive approach ❌
- [Arrays/Strings based approach](https://www.geeksforgeeks.org/program-for-armstrong-numbers/) ❌

15. Armstrong number in a given range ✔
16. Fibonacci series upto n terms ❌

- Iterative approach ✔
- Recursive approach ❌
- Approach using arrays/ dynamic programming ❌

17. Find the nth term of fibonacci series ❌

- Check [gfg](https://www.geeksforgeeks.org/program-for-nth-fibonacci-number/)

18. Factorial of a number ❌

- Iterative approach ✔
- Recursive approach ❌

19. Power of a number ✔
20. Factors of a number ❌

- Iterative approach ✔
- Handling -ve numbers approach ❌
- Check [gfg](https://www.geeksforgeeks.org/find-divisors-natural-number-set-1/)

21. Finding Prime Factors of a number ❌

- Iterative approach ✔
- Check [gfg](https://www.geeksforgeeks.org/print-all-prime-factors-of-a-given-number/) for other approaches.

22. Strong number ❌

- Iterative approach ✔
- Recursive approach ❌

23. Perfect number ❌

- Iterative approach ✔
- Recursive approach ❌

24. Perfect Square ❌

- Not solved yet
- Refer [gfg](https://www.geeksforgeeks.org/check-if-given-number-is-perfect-square-in-cpp/)

25. Automorphic number ❌

- Not solved yet
- Refer [gfg](https://www.geeksforgeeks.org/automorphic-number/)

26. Harshad number ❌

- Not solved yet
- Refer [gfg](https://www.geeksforgeeks.org/harshad-or-niven-number/)

27. Abundant number ❌

- Not solved yet
- Refer [gfg](https://www.geeksforgeeks.org/harshad-or-niven-number/)

28. Friendly pair ❌

- Not solved yet
- Refer [gfg](https://www.geeksforgeeks.org/check-given-two-number-friendly-pair-not/)

29. GCD or HCF ❌

- Approach 1: Iterative approach ✔
- Approach 2: Euclidean Algorithm: Repeated Subtraction ✔
- Approach 3: Recursive Euclidean Algorithm: Repeated Subtraction ❌
- Approach 4: Modulo Recursive Euclidean Algorithm: Repeated Subtraction ❌
- Approach 5: Handling Negative Numbers in HCF ❌
- Refer [gfg](https://www.geeksforgeeks.org/java-program-to-compute-gcd/)

30. LCM ❌

- Approach 1: A linear way to calculate LCM ❌
- Approach 2: Modified interval Linear way ❌
- Approach 3: Simple usage of HCF calculation to determine LCM ✔
- Approach 4: Repeated subtraction to calculate HCF and determine LCM ❌
- Approach 5: Recursive repeated subtraction to calculate HCF and determine LCM ❌
- Approach 6: Modulo Recursive repeated subtraction to calculate HCF and determine LCM ❌

31. Binary to decimal ❌

- Iterative approach ✔
- Refer [gfg](https://www.geeksforgeeks.org/program-binary-decimal-conversion/)

32. Octal to decimal ❌

- Iterative approach ✔
- Refer [gfg](https://www.geeksforgeeks.org/java-program-to-convert-octal-to-decimal/)

33. Hexadecimal to decimal ❌

- String concept required.

34. Decimal to binary ❌

- Not solved
- Approach is using array.
- Refer [gfg](https://www.geeksforgeeks.org/java-program-for-decimal-to-binary-conversion/)

35. Decimal to octal ❌

- Not solved yet as array approach required.
- Refer [gfg](https://www.geeksforgeeks.org/java-program-for-decimal-to-octal-conversion/)

36. Decimal to hexadecimal ❌

- Not solved yet as array approach required.
- Refer [gfg](https://www.geeksforgeeks.org/java-program-for-decimal-to-octal-conversion/)

37. Binary to octal ❌

- Not solved yet as array approach required. ❌
- Refer [gfg](https://www.geeksforgeeks.org/java-program-to-convert-binary-to-octal/)

38. Octal to binary ❌

- Not solved yet as array approach required.
- Refer [gfg](https://www.geeksforgeeks.org/java-program-to-convert-octal-to-binary/)

39. Quadrants in which a given coordinate lies ❌

- Not solved yet.
- Refer [gfg](https://www.geeksforgeeks.org/program-determine-quadrant-cartesian-plane/)

40. nCr ❌
41. nPr ❌
42. Maximum number of handshakes ❌
43. Addition of two fractions ❌
44. Replace all 0s with 1s in the given integer ❌
45. Count possible decoding of a given digit sequence ❌
46. Convert digit/ number to words ❌
47. Counting number of days in a given month of a year ❌
48. Finding the number of times x digit occurs in a given input. ❌
49. Finding number of integers which has exactly x divisors. ❌
50. Finding roots of a quadratic equation. ❌

## Additional Questions
1. Find the nth armstrong number
```java
import java.util.Scanner;

public class Main {

	public static void main(String args[]) {
		Scanner scan = new Scanner(System.in);

		int n = scan.nextInt();
		
		System.out.println(nthArmstrong(n));
		
		scan.close();
	}
	
	static int nthArmstrong(int n) {
		int count = 0;
		for(int i = 1; i <= Integer.MAX_VALUE; i++) {
			int num = i;
			int digits = (int) Math.floor(Math.log10(num) + 1);
			
			if(checkArmstrong(num, digits)) {
				++count;
			}
			
			if(count == n) {
				return i;
			}
		}
		return n;
	}
	
	static boolean checkArmstrong(int num, int digits) {
		int temp = num, sum = 0;
		while(temp != 0) {
			int lastDigit = temp % 10;
			sum = (int) (sum + Math.floor(Math.pow(lastDigit, digits)));
			temp /= 10;
		}
		
		if(sum == num) {
			return true;
		}
		
		return false;
	}
}
```
2. [Sum of even and odd digits of an integer](https://github.com/TheParthMaru/Problem-Solving-Mastery/blob/main/01.%20Basic%20Problems/Test%20cases%20and%20code/basic-problem-26.md)
