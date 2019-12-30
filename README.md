# Transpose Matrix

### Implementation

```java
import java.util.Arrays;

public class App {

	public static void main(String[] args) {
		int[][] mat = { 
				        { 1, 2, 3 }, 
				        { 4, 5, 6 } 
				      };
		
		for (int[] row : transpose(mat)) {
			System.out.println(Arrays.toString(row));
		}
	}

	private static int[][] transpose(int[][] A) {
		int row = A.length;
		int column = A[0].length;
		int[][] transpose = new int[column][row];
		for (int i = 0; i < row; i++) {
			for (int j = 0; j < column; j++) {
				transpose[j][i] = A[i][j];
			}
		}
		return transpose;

	}
}

```
The above implementation have runtime complexity of O(m * n) and space complexity of O(m * n), where m is number of rows in input matrix and n is the number of columns in the input matrix.

```
Runtime Complexity = O(m*n)
Space Complexity   = O(m*n)
```
