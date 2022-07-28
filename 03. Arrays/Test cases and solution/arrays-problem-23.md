## Replace each element by its rank given in array

**Problem statement**

- Given an integer array of size n, write a problem to replace each element of the array by its rank.

**Test cases**

```
Input:
5
100 2 70 12 90

Output:
5 1 3 2 4
```

**Solution**

```java
import java.util.Arrays;
import java.util.Scanner;

public class Main {

	public static void main(String args[]) {
		Scanner scan = new Scanner(System.in);

//		Input size of array
		int n = scan.nextInt();

//		Define an array of size n
		int arr[] = new int[n];

//		Input elements into array
		for(int i = 0; i < arr.length; i++) {
			arr[i] = scan.nextInt();
		}

		replaceElement(arr);

		scan.close();
	}

	static void replaceElement(int arr[]) {
//		Copy the original array into new array
		int newArray[] = Arrays.copyOfRange(arr, 0, arr.length);

//		Sort the newArray[] in ascending order
		Arrays.sort(newArray);

		for(int i = 0; i < arr.length; i++) {
			for(int j = 0; j < arr.length; j++) {
				if(newArray[j] == arr[i]) {
					arr[i] = j+1;
					break;
				}
			}
		}

		printArray(arr);
	}

	static void printArray(int arr[]) {
		for(int i = 0; i < arr.length; i++) {
			System.out.print(arr[i] + " ");
		}
	}
}
```

**Note**

- Another approach will be using hashmap
