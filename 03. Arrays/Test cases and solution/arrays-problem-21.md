## Frequency of elements

**Problem statement**

- Given an array of size n, find the frequency of all the elements in it.

**Test cases**

```
Input:
6
5 8 5 7 8 10

Output:
5 : 2
7 : 1
8 : 2
10 : 1

Input:
8
10 30 10 20 10 20 30 10

Output:
10 : 4
30 : 2
20 : 2
```

**Solution**

_Approach 1: Bruteforce approach_

```java
import java.util.Arrays;
import java.util.Scanner;

public class Main {

	public static void main(String args[]) {
		Scanner scan = new Scanner(System.in);

		int n = scan.nextInt();

		int arr[] = new int[n];

		for(int i = 0; i < n; i++) {
			arr[i] = scan.nextInt();
		}

		countFrequency(arr);

		scan.close();
	}

	static void countFrequency(int arr[]) {
		boolean visited[] = new boolean[arr.length];

		Arrays.fill(visited, false);

		for(int i = 0; i < arr.length; i++) {
			// Skip this element if already processed
			if(visited[i] == true) {
				continue;
			}

			// Count frequency
			int count = 1;
			for(int j = i+1; j < arr.length; j++) {
				if(arr[i] == arr[j]) {
					visited[j] = true;
					count++;
				}
			}
			System.out.println(arr[i] + " : " + count);
		}
	}
}
```

_Approach 2: Using hashmap_

- Will implement after learning hashmap
