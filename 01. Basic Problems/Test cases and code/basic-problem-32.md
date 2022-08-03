## Automorphic number

**Solution**

```java
import java.util.Scanner;

public class Main {
	public static void main(String[] args) {

		Scanner scan = new Scanner(System.in);

		int num = scan.nextInt();

		System.out.println(isAutomorphic(num) ? "Automorphic number" : "Not an automorphic number");

		scan.close();
	}

	static boolean isAutomorphic(int num) {
		int square = num * num;

		while(num > 0) {
			if(num % 10 != square % 10) {
				return false;
			}

			num /= 10;
			square /= 10;
		}

		return true;
	}
}
```
