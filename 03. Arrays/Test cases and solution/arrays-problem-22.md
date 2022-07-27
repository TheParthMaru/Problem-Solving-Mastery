## Count even and odd elements

**Problem statement**

- Given an array of size n, count the number of even elements and odd elements present in the array.

**Test cases**

```
Input:
7
1 20 60 31 75 40 80

Output:
Even: 4
Odd: 3
```

**Solution**

```java
import java.util.Scanner;

public class Main {

	public static void main(String args[]) {
		Scanner scan = new Scanner(System.in);

		int n = scan.nextInt();

		int arr[] = new int[n];

		for(int i = 0; i < n; i++) {
			arr[i] = scan.nextInt();
		}

		int countEven = 0, countOdd = 0;

		for(int i = 0; i < n; i++) {
			if(arr[i] % 2 == 0) {
				countEven++;
			} else {
				countOdd++;
			}
		}

		System.out.println("Even: " + countEven);
		System.out.println("Odd: " + countOdd);

		scan.close();
	}
}
```
