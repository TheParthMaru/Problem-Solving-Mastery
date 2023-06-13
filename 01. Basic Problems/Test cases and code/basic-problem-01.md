## Swap two numbers

**Problem statement**

- Given two integer inputs, swap two inputs.

**Test cases**

```
Input: 5 10
Output: 10 5

Input: 2 -3
Output: -3 2
```

**Solution**

<details>
	<summary>Java solution</summary>

_**Approach 1: Using temporary variable**_

```java
import java.util.Scanner;

public class Main {
	public static void main(String[] args) {

		Scanner scan = new Scanner(System.in);

		int num1 = scan.nextInt();
		int num2 = scan.nextInt();

		int temp = num1;
		num1 = num2;
		num2 = temp;

		System.out.println(num1 + " " + num2);
		scan.close();
	}
}
```

_**Approach 2: Not using temporary variable**_

```java
import java.util.Scanner;

public class Main {
	public static void main(String[] args) {

		Scanner scan = new Scanner(System.in);

		int num1 = scan.nextInt();
		int num2 = scan.nextInt();

		num1 = num1 + num2;
		num2 = num1 - num2;
		num1 = num1 - num2;

		System.out.println(num1 + " " + num2);
		scan.close();
	}
}
```

</details>

<details>
	<summary>Javascript solution</summary>

_**Approach 1: Using temporary variable**_

```js
"use strict";

let num1 = 5;
let num2 = 10;

let temp = num1;
num1 = num2;
num2 = temp;

console.log(num1, num2);
```

_**Approach 2: Not using temporary variable**_

```js
"use strict";

let num1 = 5;
let num2 = 10;

num1 = num1 + num2;
num2 = num1 - num2;
num1 = num1 - num2;

console.log(num1, num2);
```

_**Approach 3: Using destructuring**_

```js
"use strict";

let num1 = 5;
let num2 = 10;

[num1, num2] = [num2, num1];
console.log(num1, num2);
```

</details>
