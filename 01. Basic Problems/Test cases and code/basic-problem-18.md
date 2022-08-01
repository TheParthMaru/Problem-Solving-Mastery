## Factors of a number

**Problem Statement**

- Given a positive number as input, find its factors.

**Test Cases**

```
Input: 100
Output: 1 2 4 5 10 20 25 50 100

Input: 15
Output: 1 3 5 15
```

**Solution**

```java
import java.util.Scanner;

public class Main {
	public static void main(String[] args) {
		Scanner scan = new Scanner(System.in);
		
		int num = scan.nextInt();
		
		for(int i = 1; i <= num; i++) {
			if(num == 0) {
				break;
			}
			
			if(num % i == 0) {
				System.out.print(i + " ");
			}
		}
		
		scan.close();
	}
}
```
