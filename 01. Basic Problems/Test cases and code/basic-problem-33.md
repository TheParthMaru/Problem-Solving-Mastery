## Harshad Number

```java
import java.util.Scanner;

public class Main {
	public static void main(String[] args) {

		Scanner scan = new Scanner(System.in);

		int num = scan.nextInt();

		System.out.println(isHarshad(num) ? "Harshad number" : "Not a harshad number");

		scan.close();
	}

	static boolean isHarshad(int num) {
		int sum = 0;
		for (int temp = num; temp > 0; temp /= 10) {
			sum += temp % 10;
		}
		return (num % sum == 0);
	}
}

```
