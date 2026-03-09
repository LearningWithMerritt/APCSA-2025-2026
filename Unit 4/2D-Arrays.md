## Create and initialize a 2D Array

```java
public class Main{
    public static void main(String[] args){

        // Create and initialize a 2D Array
        int[][] matrix = {
            {1, 2, 3},
            {4, 5, 6},
            {7, 8, 9}
        };

        // OR

        int[][] matrix = new int[3][3];
        /* -->
        {
            {0,0,0},
            {0,0,0},
            {0,0,0}
        }
        */

    }
}
```

---

## Demonstrate accessing a row from a 2D Array

```java
public class Main{
    public static void main(String[] args){
        int[][] matrix = {
            {1, 2, 3},
            {4, 5, 6},
            {7, 8, 9}
        };

        // Access a row from a 2D Array
        int[] firstRow = matrix[0];     //--> {1, 2, 3}
        int[] secondRow = matrix[1];    //--> {4, 5, 6}
        int[] thirdRow = matrix[2];     //--> {7, 8, 9}

    }
}
```

---

## Demonstrate accessing an element from a 2D Array by index

```java
public class Main{
    public static void main(String[] args){

        int[][] matrix = {
            {1, 2, 3},
            {4, 5, 6},
            {7, 8, 9}
        };

        // Access elements by index
        int firstRowFirstElement = matrix[0][0];    //--> 1
        int secondRowSecondElement = matrix[1][1];  //--> 5
        int thirdRowThirdElement = matrix[2][2];    //--> 9

    }
}
```

---

## Demonstrate modifying an element from a 2D Array by index

```java
public class Main{
    public static void main(String[] args){

        int[][] matrix = {
            {1, 2, 3},
            {4, 5, 6},
            {7, 8, 9}
        };

        // Modify elements
        matrix[0][1] = 25;
        matrix[1][2] = 50;
        matrix[2][0] = 75;

    }
}
```

---

## Demonstrate using length to return the number of rows

```java
public class Main{
    public static void main(String[] args){

        int[][] matrix = {
            {1, 2, 3},
            {4, 5, 6},
            {7, 8, 9}
        };

        // Number of rows
        int rows = matrix.length; // --> 3

        System.out.println(rows);

    }
}
```

---

## Demonstrate using length to return the number of columns

```java
public class Main{
    public static void main(String[] args){

        int[][] matrix = {
            {1, 2, 3},
            {4, 5, 6},
            {7, 8, 9}
        };

        // Number of columns
        int cols = matrix[0].length; // --> 3

        System.out.println(cols);

    }
}
```

---

## Use a for loop to traverse a 2D Array

```java
public class Main{
    public static void main(String[] args){

        int[][] matrix = {
            {1, 2, 3},
            {4, 5, 6},
            {7, 8, 9}
        };

        for(int r = 0; r < matrix.length; r++){
            for(int c = 0; c < matrix[r].length; c++){
                System.out.print(matrix[r][c] + " ");
            }
            System.out.println();
        }

    }
}
```

---

## Use a while loop to traverse a 2D Array

```java
public class Main{
    public static void main(String[] args){

        int[][] matrix = {
            {1, 2, 3},
            {4, 5, 6},
            {7, 8, 9}
        };

        int r = 0;

        while(r < matrix.length){
            int c = 0;

            while(c < matrix[r].length){
                System.out.print(matrix[r][c] + " ");
                c++;
            }

            System.out.println();
            r++;
        }

    }
}
```

---

## Use an enhanced for loop (for-each) to traverse a 2D Array

```java
public class Main{
    public static void main(String[] args){

        int[][] matrix = {
            {1, 2, 3},
            {4, 5, 6},
            {7, 8, 9}
        };

        for(int[] row : matrix){
            for(int value : row){
                System.out.print(value + " ");
            }
            System.out.println();
        }

    }
}
```

# Algorithms

## Write a method that returns the minimum value
* The entire array
* Each row
* Each column
* A subsection of the Array
```java
// Minimum value of the entire array
public static int minArray(int[][] arr){
    int min = arr[0][0];
    for(int r = 0; r < arr.length; r++){
        for(int c = 0; c < arr[r].length; c++){
            if(arr[r][c] < min) min = arr[r][c];
        }
    }
    return min;
}

// Minimum of a specific row
public static int minRow(int[][] arr, int row){
    int min = arr[row][0];
    for(int c = 1; c < arr[row].length; c++){
        if(arr[row][c] < min) min = arr[row][c];
    }
    return min;
}

// Minimum of a specific column
public static int minCol(int[][] arr, int col){
    int min = arr[0][col];
    for(int r = 1; r < arr.length; r++){
        if(arr[r][col] < min) min = arr[r][col];
    }
    return min;
}

// Minimum of a subsection of the array (rowStart, rowEnd, colStart, colEnd inclusive)
public static int minSubsection(int[][] arr, int rowStart, int rowEnd, int colStart, int colEnd){
    int min = arr[rowStart][colStart];
    for(int r = rowStart; r <= rowEnd; r++){
        for(int c = colStart; c <= colEnd; c++){
            if(arr[r][c] < min) min = arr[r][c];
        }
    }
    return min;
}
```

---

## Write a method that returns the maximum value
* The entire array
* Each row
* Each column
* A subsection of the Array
```java
// Maximum value of the entire array
public static int maxArray(int[][] arr){
    int max = arr[0][0];
    for(int r = 0; r < arr.length; r++){
        for(int c = 0; c < arr[r].length; c++){
            if(arr[r][c] > max) max = arr[r][c];
        }
    }
    return max;
}

// Maximum of a specific row
public static int maxRow(int[][] arr, int row){
    int max = arr[row][0];
    for(int c = 1; c < arr[row].length; c++){
        if(arr[row][c] > max) max = arr[row][c];
    }
    return max;
}

// Maximum of a specific column
public static int maxCol(int[][] arr, int col){
    int max = arr[0][col];
    for(int r = 1; r < arr.length; r++){
        if(arr[r][col] > max) max = arr[r][col];
    }
    return max;
}

// Maximum of a subsection of the array
public static int maxSubsection(int[][] arr, int rowStart, int rowEnd, int colStart, int colEnd){
    int max = arr[rowStart][colStart];
    for(int r = rowStart; r <= rowEnd; r++){
        for(int c = colStart; c <= colEnd; c++){
            if(arr[r][c] > max) max = arr[r][c];
        }
    }
    return max;
}
```

---

## Write a method that returns the sum
* The entire array
* Each row
* Each column
* A subsection of the Array
```java
// Sum of the entire array
public static int sumArray(int[][] arr){
    int sum = 0;
    for(int r = 0; r < arr.length; r++){
        for(int c = 0; c < arr[r].length; c++){
            sum += arr[r][c];
        }
    }
    return sum;
}

// Sum of a specific row
public static int sumRow(int[][] arr, int row){
    int sum = 0;
    for(int c = 0; c < arr[row].length; c++){
        sum += arr[row][c];
    }
    return sum;
}

// Sum of a specific column
public static int sumCol(int[][] arr, int col){
    int sum = 0;
    for(int r = 0; r < arr.length; r++){
        sum += arr[r][col];
    }
    return sum;
}

// Sum of a subsection
public static int sumSubsection(int[][] arr, int rowStart, int rowEnd, int colStart, int colEnd){
    int sum = 0;
    for(int r = rowStart; r <= rowEnd; r++){
        for(int c = colStart; c <= colEnd; c++){
            sum += arr[r][c];
        }
    }
    return sum;
}
```

---

## Write a method that returns the average
* The entire array
* Each row
* Each column
* A subsection of the Array
```java
public static double averageArray(int[][] arr){
    int sum = sumArray(arr);
    return (double) sum / (arr.length * arr[0].length);
}

public static double averageRow(int[][] arr, int row){
    return (double) sumRow(arr, row) / arr[row].length;
}

public static double averageCol(int[][] arr, int col){
    return (double) sumCol(arr, col) / arr.length;
}

public static double averageSubsection(int[][] arr, int rowStart, int rowEnd, int colStart, int colEnd){
    int sum = sumSubsection(arr, rowStart, rowEnd, colStart, colEnd);
    int count = (rowEnd - rowStart + 1) * (colEnd - colStart + 1);
    return (double) sum / count;
}
```

---

## Write a method to check if at least one element has property
```java
// At least one element satisfies property (e.g., even)
public static boolean anyEven(int[][] arr){
    for(int[] row : arr){
        for(int val : row){
            if(val % 2 == 0) return true;
        }
    }
    return false;
}
```
## Write a method to check all elements have property

```java
// All elements satisfy property
public static boolean allEven(int[][] arr){
    for(int[] row : arr){
        for(int val : row){
            if(val % 2 != 0) return false;
        }
    }
    return true;
}

```

## Write a method to count elements with property
```java
// Count elements satisfying property
public static int countEven(int[][] arr){
    int count = 0;
    for(int[] row : arr){
        for(int val : row){
            if(val % 2 == 0) count++;
        }
    }
    return count;
}
```

---

## Write a method to access consecutive pairs

```java
public static void printConsecutivePairs(int[][] arr){
    for(int r = 0; r < arr.length; r++){
        for(int c = 0; c < arr[r].length - 1; c++){
            System.out.println("(" + arr[r][c] + ", " + arr[r][c+1] + ")");
        }
    }
}
```

---

## Write a method to detect duplicates:
* The entire array
* Each row
* Each column
* A subsection of the Array 
```java
// Entire array
public static boolean hasDuplicatesArray(int[][] arr){
    for(int r1 = 0; r1 < arr.length; r1++){
        for(int c1 = 0; c1 < arr[r1].length; c1++){
            for(int r2 = r1; r2 < arr.length; r2++){
                int startCol = (r2 == r1) ? c1 + 1 : 0;
                for(int c2 = startCol; c2 < arr[r2].length; c2++){
                    if(arr[r1][c1] == arr[r2][c2]) return true;
                }
            }
        }
    }
    return false;
}

// Row duplicates
public static boolean hasDuplicatesRow(int[][] arr, int row){
    for(int i = 0; i < arr[row].length; i++){
        for(int j = i + 1; j < arr[row].length; j++){
            if(arr[row][i] == arr[row][j]) return true;
        }
    }
    return false;
}

// Column duplicates
public static boolean hasDuplicatesCol(int[][] arr, int col){
    for(int i = 0; i < arr.length; i++){
        for(int j = i + 1; j < arr.length; j++){
            if(arr[i][col] == arr[j][col]) return true;
        }
    }
    return false;
}

// Subsection duplicates
public static boolean hasDuplicatesSubsection(int[][] arr, int rowStart, int rowEnd, int colStart, int colEnd){
    for(int r1 = rowStart; r1 <= rowEnd; r1++){
        for(int c1 = colStart; c1 <= colEnd; c1++){
            for(int r2 = r1; r2 <= rowEnd; r2++){
                int startC = (r2 == r1) ? c1 + 1 : colStart;
                for(int c2 = startC; c2 <= colEnd; c2++){
                    if(arr[r1][c1] == arr[r2][c2]) return true;
                }
            }
        }
    }
    return false;
}
```

---

## Write a method to shift/rotate:
* rows
* columns
```java
// Shift rows down by 1
public static void shiftRows(int[][] arr){
    if(arr.length == 0) return;
    int[] lastRow = arr[arr.length - 1];
    for(int r = arr.length - 1; r > 0; r--){
        arr[r] = arr[r-1];
    }
    arr[0] = lastRow;
}

// Shift columns right by 1
public static void shiftCols(int[][] arr){
    if(arr[0].length == 0) return;
    for(int r = 0; r < arr.length; r++){
        int last = arr[r][arr[r].length - 1];
        for(int c = arr[r].length - 1; c > 0; c--){
            arr[r][c] = arr[r][c-1];
        }
        arr[r][0] = last;
    }
}
```

---

## Write a method to reverse:
* The row order
* The column order
```java
// Reverse the order of rows
public static void reverseRows(int[][] arr){
    int top = 0;
    int bottom = arr.length - 1;
    while(top < bottom){
        int[] temp = arr[top];
        arr[top] = arr[bottom];
        arr[bottom] = temp;
        top++;
        bottom--;
    }
}

// Reverse the order of columns in each row
public static void reverseCols(int[][] arr){
    for(int r = 0; r < arr.length; r++){
        int left = 0;
        int right = arr[r].length - 1;
        while(left < right){
            int temp = arr[r][left];
            arr[r][left] = arr[r][right];
            arr[r][right] = temp;
            left++;
            right--;
        }
    }
}
```
