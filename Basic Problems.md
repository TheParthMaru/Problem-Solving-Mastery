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

<details>
  
  <summary>2. Even or odd number</summary>
  
  **Problem statement:** Given an integer number as input, the objective is the write a program to check whether the input number is even or odd.
  
  **Test cases**
  ```
  Input: 11
  Output: Odd

Input: -62
Output: Even

Input: 0
Output: Even

````

**Solution**

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

</details>
````
