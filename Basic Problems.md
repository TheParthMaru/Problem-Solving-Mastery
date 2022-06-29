# Basic Problems

- The below list of problems does not need any DSA knowledge.
- Only fundamental programming knowledge in required. (data types, variables, operators, if...else, switch, loops, break, continue and methods)
- May require a bit of math.
- Main focus is to learn how to build logic and come up with a bruteforce approach.

## Problems List

[comment]: <> (Problem 1: Positive or negative numbers)

<details>
  
  <summary>1. Positive or negative number</summary>
  
  **Problem statement:** Given an integer number as input, the objective is to write a program to check if the given number is positive or negative or zero.
  
  **Test cases**
  ```
  Input: 12
  Output: Positive

Input: -76
Output: Negative

    Input: 0
    Output: Zero
    ````

**Solution**

```java
	import java.util.Scanner;

	public class Main {

		public static void main(String[] args) {
			Scanner scan = new Scanner(System.in);

			int num = scan.nextInt();

			if(num > 0) {
				System.out.println("Positive");
			} else if(num < 0) {
				System.out.println("Negative");
			} else {
				System.out.println("Zero");
			}

			scan.close();
		}
	}
```

</details>

[comment]: <> (Problem 2: Even or odd number)
**Problem 02: Even or odd number**
**Problem statement: **Given an integer number as input, the objective is the write a program to check whether the input number is even or odd.

**Test cases:**

```
Input: 11
Output: Odd

Input: -62
Output: Even

Input: 0
Output: Even
```

**Solution:**

```java
import java.util.Scanner;

  public class Main {
  	public static void main(String[] args) {
  		Scanner scan = new Scanner(System.in);

  		int num = scan.nextInt();

  		if(num % 2 == 0) {
  			System.out.println("Even");
  		} else {
  			System.out.println("Odd");
  		}

  		scan.close();
  	}
  }
```
