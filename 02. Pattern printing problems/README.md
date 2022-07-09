# Pattern printing problems

## Geometrical patterns

**Pattern 1**

```
* * * * *
* * * * *
* * * * *
* * * * *
* * * * *
```

**Solution**

```java
import java.util.Scanner;

public class Main {

	public static void main(String args[]) {
		Scanner scan = new Scanner(System.in);

		int n = scan.nextInt();

		for(int row = 1; row <= n; row++) {
			for(int column = 1; column <= n; column++) {
				System.out.print("*" + " ");
			}
			System.out.println();
		}

		scan.close();
	}
}
```

**Pattern 2**

```
1 2 3 4 5
1 2 3 4 5
1 2 3 4 5
1 2 3 4 5
1 2 3 4 5

```

**Solution**

```java
import java.util.Scanner;

public class Main {

	public static void main(String args[]) {
		Scanner scan = new Scanner(System.in);

		int n = scan.nextInt();

		for(int row = 1; row <= n; row++) {
			for(int column = 1; column <= n; column++) {
				System.out.print(column + " ");
			}
			System.out.println();
		}

		scan.close();
	}
}
```

**Pattern 3**

```
1 1 1 1 1
2 2 2 2 2
3 3 3 3 3
4 4 4 4 4
5 5 5 5 5
```

**Solution**

```java
import java.util.Scanner;

public class Main {

	public static void main(String args[]) {
		Scanner scan = new Scanner(System.in);

		int n = scan.nextInt();

		for(int row = 1; row <= n; row++) {
			for(int column = 1; column <= n; column++) {
				System.out.print(row + " ");
			}
			System.out.println();
		}

		scan.close();
	}
}
```

**Pattern 4**

```
A B C D
A B C D
A B C D
A B C D
```

**Solution**

```java
import java.util.Scanner;

public class Main {

	public static void main(String args[]) {
		Scanner scan = new Scanner(System.in);

		int n = scan.nextInt();

		for(int row = 1; row <= n; row++) {
      char character = 'A';
			for(int column = 1; column <= n; column++) {
				System.out.print(character + " ");
        character++;
			}
			System.out.println();
		}

		scan.close();
	}
}
```

**Pattern 5**

```
A B C D
B C D E
C D E F
D E F G
```

**Solution**

```java
import java.util.Scanner;

public class Main {

	public static void main(String args[]) {
		Scanner scan = new Scanner(System.in);

		int n = scan.nextInt();

		for(int row = 0; row < n; row++) {
      char character = 'A';
			for(int column = 0; column < n; column++) {
				System.out.print((char) (character + row + column) + " ");
			}
			System.out.println();
		}

		scan.close();
	}
}
```

**Pattern 6**

```
* * * * *
*       *
*       *
*       *
* * * * *
```

**Solution**

```java
import java.util.Scanner;

public class Main {

	public static void main(String args[]) {
		Scanner scan = new Scanner(System.in);

		int n = scan.nextInt();

		for(int row = 1; row <= n; row++) {
			for(int column = 1; column <= n; column++) {
				if(row == 1 || row == n) {
          System.out.print("*" + " ");
        } else if(column == 1 || column == n) {
          System.out.print("*" + " ");
        } else {
          System.out.print(" " + " ");
        }
			}
			System.out.println();
		}
		scan.close();
	}
}
```

**Pattern 7**

```
*
* *
* * *
* * * *
```

**Solution**

```java
import java.util.Scanner;

public class Main {

	public static void main(String args[]) {
		Scanner scan = new Scanner(System.in);

		int n = scan.nextInt();

		for(int row = 1; row <= n; row++) {
			for(int column = 1; column <= row; column++) {
			    System.out.print("*" + " ");
        }
		  	System.out.println();
			}
		scan.close();
		}
	}
```

**Pattern 8**

```
1
1 2
1 2 3
1 2 3 4
```

**Solution**

```java
import java.util.Scanner;

public class Main {

	public static void main(String args[]) {
		Scanner scan = new Scanner(System.in);

		int n = scan.nextInt();

		for(int row = 1; row <= n; row++) {
			for(int column = 1; column <= row; column++) {
			    System.out.print(column + " ");
        }
		  	System.out.println();
			}
		scan.close();
		}
	}
```

**Pattern 9**

```
* * * *
* * *
* *
*
```

**Solution**

```java
import java.util.Scanner;

public class Main {

	public static void main(String args[]) {
		Scanner scan = new Scanner(System.in);

		int n = scan.nextInt();

		for(int row = 1; row <= n; row++) {
			for(int column = 1; column <= (n - row + 1); column++) {
			    System.out.print("*" + " ");
        }
		  	System.out.println();
			}
		scan.close();
		}
	}
```

**Pattern 10**

```
1 1 1 1
2 2 2
3 3
4
```

**Solution**

```java
import java.util.Scanner;

public class Main {

	public static void main(String args[]) {
		Scanner scan = new Scanner(System.in);

		int n = scan.nextInt();

		for(int row = 1; row <= n; row++) {
			for(int column = 1; column <= (n - row + 1); column++) {
			    System.out.print(row + " ");
        }
		  	System.out.println();
			}
		scan.close();
		}
	}
```

**Problem 11**

```
      *
    * *
  * * *
* * * *
```

**Solution**

```java
import java.util.Scanner;

public class Main {

	public static void main(String args[]) {
		Scanner scan = new Scanner(System.in);

		int n = scan.nextInt();

		for(int row = 1; row <= n; row++) {
			char space = ' ';
			for(int column = 1; column <= n - row; column++) {
				System.out.print(space + " ");
			}
			for(int column = 1; column <= row; column++) {
				System.out.print("*" + " ");
			}

			System.out.println();
		}

		scan.close();
	}
}
```

**Problem 12**

```
      1
    1 2
  1 2 3
1 2 3 4
```

**Solution**

```java
import java.util.Scanner;

public class Main {

	public static void main(String args[]) {
		Scanner scan = new Scanner(System.in);

		int n = scan.nextInt();

		for(int row = 1; row <= n; row++) {
			char space = ' ';
			for(int column = 1; column <= n - row; column++) {
				System.out.print(space + " ");
			}
			for(int column = 1; column <= row; column++) {
				System.out.print(column + " ");
			}

			System.out.println();
		}

		scan.close();
	}
}
```

**Problem 13**

```
* * * *
  * * *
    * *
      *
```

**Solution**

_**Approach 1: Simplest approach**_

```java
import java.util.Scanner;

public class Main {

	public static void main(String args[]) {
		Scanner scan = new Scanner(System.in);

		int n = scan.nextInt();

		for(int row = n; row >= 1; row--) {
			char space = ' ';
			for(int column = (n - row); column >= 1; column--) {
				System.out.print(space + " ");
			}
			for(int column = row; column >= 1; column--) {
				System.out.print("*" + " ");
			}
			System.out.println();
		}

		scan.close();
	}
}
```

_**Approach 2: Logical and formula based approach**_

```java
import java.util.Scanner;

public class Main {

	public static void main(String args[]) {
		Scanner scan = new Scanner(System.in);

		int n = scan.nextInt();

		for(int row = 1; row <= n; row++) {
			char space = ' ';
			for(int column = 1; column < row; column++) {
				System.out.print(space + " ");
			}
			for(int column = 1; column <= (n - row + 1); column++) {
				System.out.print("*" + " ");
			}

			System.out.println();
		}

		scan.close();
	}
}
```

**Problem 14**

```
* * * * * *
  *       *
    *     *
      *   *
        * *
          *
```

**Solution**

```java
import java.util.Scanner;

public class Main {

	public static void main(String args[]) {
		Scanner scan = new Scanner(System.in);

		int n = scan.nextInt();

		for (int row = 1; row <= n; row++) {
			for (int column = 1; column <= n; column++) {
				char space = ' ';
				if (row == 1) {
					System.out.print("*" + " ");
				} else if (column == row || column == n) {
					System.out.print("*" + " ");
				} else {
					System.out.print(space + " ");
				}
			}
			System.out.println();
		}

		scan.close();
	}
}
```

**Problem 15**

```
*
* *
*   *
*     *
*       *
* * * * * *
```

**Solution**

```java
import java.util.Scanner;

public class Main {

	public static void main(String args[]) {
		Scanner scan = new Scanner(System.in);

		int n = scan.nextInt();

		for(int row = 1; row <= n; row++) {
			for(int column = 1; column <= n; column++) {
				char space = ' ';
				if(column == 1 || column == row) {
					System.out.print("*" + " ");
				}else if(row == n) {
					System.out.print("*" + " ");
				}else {
					System.out.print(space + " ");
				}
			}
			System.out.println();
		}

		scan.close();
	}
}
```

**Problem 16**

```
* * * * * *
*       *
*     *
*   *
* *
*
```

```java
import java.util.Scanner;

public class Main {

	public static void main(String args[]) {
		Scanner scan = new Scanner(System.in);

		int n = scan.nextInt();

		for(int row = 1; row <= n; row++) {
			for(int column = 1; column <= n; column++) {
				char space = ' ';
				if(row == 1 || column == 1) {
					System.out.print("*" + " ");
				} else if(column == (n-row+1)) {
					System.out.print("*" + " ");
				}else {
					System.out.print(space + " ");
				}
			}
			System.out.println();
		}

		scan.close();
	}
}
```

**Problem 17**

```
          *
        * *
      *   *
    *     *
  *       *
* * * * * *
```

```java
import java.util.Scanner;

public class Main {

	public static void main(String args[]) {
		Scanner scan = new Scanner(System.in);

		int n = scan.nextInt();

		for (int row = 1; row <= n; row++) {
			for (int column = 1; column <= n; column++) {
				char space = ' ';
				if (column == n || column == (n - row + 1)) {
					System.out.print("*" + " ");
				} else if (row == n) {
					System.out.print("*" + " ");
				} else {
					System.out.print(space + " ");
				}
			}
			System.out.println();
		}

		scan.close();
	}
}
```

**Problem 18**

```
1 5 10 16 23
2 7 13 20 28
3 9 16 24 33
4 11 19 28 38
5 13 22 32 43
```

```java
import java.util.Scanner;

public class Main {

	public static void main(String args[]) {
		Scanner scan = new Scanner(System.in);

		int n = scan.nextInt();

		for(int row = 1; row <= n; row++) {
			int printValue = row;
			for(int column = 1; column <= n; column++) {
				System.out.print(printValue + " ");
				printValue += row + column + 2;
			}
			System.out.println();
		}

		scan.close();
	}
}
```

**Problem 19**

```
1
2 3
4 5 6
7 8 9 10
```

```java
import java.util.Scanner;

public class Main {

	public static void main(String args[]) {
		Scanner scan = new Scanner(System.in);

		int n = scan.nextInt();
		int printValue = 1;
		for (int row = 1; row <= n; row++) {

			for (int column = 1; column <= row; column++) {
				System.out.print(printValue + " ");
				printValue++;
			}
			System.out.println();
		}

		scan.close();
	}
}
```

**Problem 20**

```
1 3 5 7 9
3 5 7 9
5 7 9
7 9
9
```

```java
import java.util.Scanner;

public class Main {

	public static void main(String args[]) {
		Scanner scan = new Scanner(System.in);

		int n = scan.nextInt();
		int startValue = 1;
		for (int row = 1; row <= n; row++) {
			int printValue = startValue;
			for (int column = 1; column <= n - row + 1; column++) {
				System.out.print(printValue + " ");
				printValue += 2;
			}
			startValue += 2;
			System.out.println();
		}

		scan.close();
	}
}
```
