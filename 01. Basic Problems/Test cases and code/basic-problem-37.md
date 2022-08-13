## Calculator using switch case

**Problem statement**

- Write a program to perform all arithmetic operations using switch case.

**Solution**

```java
import java.util.Scanner;

public class Main {
	public static void main(String[] args) {

		Scanner scan = new Scanner(System.in);

		int num1 = scan.nextInt();
		int num2 = scan.nextInt();
		scan.nextLine();
		char operator = scan.nextLine().charAt(0);

		switch (operator) {
		case '+':
			System.out.println(num1 + num2);
			break;

		case '-':
			System.out.println(num1 - num2);
			break;

		case '*':
			System.out.println(num1 * num2);
			break;

		case '/':
			System.out.println(num1 / num2);
			break;

		case '%':
			System.out.println(num1 % num2);
			break;

		default:
			System.out.println("Invalid operator");
		}

		scan.close();
	}
}
```
