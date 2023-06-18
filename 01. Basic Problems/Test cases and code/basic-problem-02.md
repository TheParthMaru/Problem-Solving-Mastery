## Maximum number of handshakes

**Problem statement**

- There are N persons in a room. Find the maximum number of handshakes possible given the fact that any two persons shake hand exactly once.

**Explanation**

- To maximize the number of handshakes, each person should shake hand with every other person in the room.
- For the first person, there would be N-1 handshakes.
- For second person there would N-1 person available but he had already shaken hand with the first person. So there would be N-2 handshakes and so on.
- So for every ith person, we have (N-i) handshakes.
- So, Total number of handshake = N-1 + N-2 +….+ 1 + 0, which is equivalent to ((N-1)\*N)/2.

**Test cases**

```
Input: 10
Output: 45
```

**Solution**

```java
import java.util.Scanner;

public class Main {
	public static void main(String[] args) {

		Scanner scan = new Scanner(System.in);

		int n = scan.nextInt();

		System.out.println(n * (n - 1) / 2);

		scan.close();
	}
}
```
