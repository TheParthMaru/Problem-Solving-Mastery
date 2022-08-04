## Counting number of days in a given month of a year

**Solution**

```java
import java.util.Scanner;

public class Main {
	public static void main(String[] args) {

		Scanner scan = new Scanner(System.in);

		int month = scan.nextInt();
		int year = scan.nextInt();

		switch (month) {
		// Cases for 31 days
		case 1:
		case 3:
		case 5:
		case 7:
		case 8:
		case 10:
		case 12:
			System.out.println(31);
			break;

		// Cases for 30 days
		case 4:
		case 6:
		case 9:
		case 11:
			System.out.println(30);
			break;

		// Case for 28/29 days
		case 2:
			if ((year % 400 == 0) || ((year % 4 == 0) && (year % 100 != 0))) {
				System.out.println(29);
			} else {
				System.out.println(28);
			}
			break;

		// Invalid month
		default:
			System.out.println("Invalid month");
			break;
		}
		scan.close();
	}
}
```
