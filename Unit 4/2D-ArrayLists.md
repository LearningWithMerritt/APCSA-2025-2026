## Create and initialize a 2D ArrayList

```java
import java.util.ArrayList;

public class Main{
    public static void main(String[] args){

        // Create a 2D ArrayList
        ArrayList<ArrayList<Integer>> matrix = new ArrayList<>();

        ArrayList<Integer> row1 = new ArrayList<>();
        row1.add(1);
        row1.add(2);
        row1.add(3);

        ArrayList<Integer> row2 = new ArrayList<>();
        row2.add(4);
        row2.add(5);
        row2.add(6);

        ArrayList<Integer> row3 = new ArrayList<>();
        row3.add(7);
        row3.add(8);
        row3.add(9);

        matrix.add(row1);
        matrix.add(row2);
        matrix.add(row3);

    }
}
```

---

## Demonstrate accessing a row from a 2D ArrayList

```java
import java.util.ArrayList;

public class Main{
    public static void main(String[] args){

        ArrayList<ArrayList<Integer>> matrix = new ArrayList<>();

        matrix.add(new ArrayList<>());
        matrix.add(new ArrayList<>());
        matrix.add(new ArrayList<>());

        // Access rows
        ArrayList<Integer> firstRow = matrix.get(0);
        ArrayList<Integer> secondRow = matrix.get(1);
        ArrayList<Integer> thirdRow = matrix.get(2);

    }
}
```

---

## Demonstrate accessing an element from a 2D ArrayList by index

```java
import java.util.ArrayList;

public class Main{
    public static void main(String[] args){

        ArrayList<ArrayList<Integer>> matrix = new ArrayList<>();

        matrix.add(new ArrayList<>());
        matrix.get(0).add(1);
        matrix.get(0).add(2);
        matrix.get(0).add(3);

        // Access element
        int value = matrix.get(0).get(1); // --> 2

    }
}
```

---

## Demonstrate modifying an element from a 2D ArrayList by index

```java
import java.util.ArrayList;

public class Main{
    public static void main(String[] args){

        ArrayList<ArrayList<Integer>> matrix = new ArrayList<>();

        matrix.add(new ArrayList<>());
        matrix.get(0).add(1);
        matrix.get(0).add(2);
        matrix.get(0).add(3);

        // Modify element
        matrix.get(0).set(1, 25); // replaces 2 with 25

    }
}
```

---

## Demonstrate using size() to return the number of rows

```java
import java.util.ArrayList;

public class Main{
    public static void main(String[] args){

        ArrayList<ArrayList<Integer>> matrix = new ArrayList<>();

        matrix.add(new ArrayList<>());
        matrix.add(new ArrayList<>());
        matrix.add(new ArrayList<>());

        int rows = matrix.size(); // --> 3

        System.out.println(rows);

    }
}
```

---

## Demonstrate using size() to return the number of columns

```java
import java.util.ArrayList;

public class Main{
    public static void main(String[] args){

        ArrayList<ArrayList<Integer>> matrix = new ArrayList<>();

        ArrayList<Integer> row = new ArrayList<>();
        row.add(1);
        row.add(2);
        row.add(3);

        matrix.add(row);

        int cols = matrix.get(0).size(); // --> 3

        System.out.println(cols);

    }
}
```

---

## Use a for loop to traverse a 2D ArrayList

```java
import java.util.ArrayList;

public class Main{
    public static void main(String[] args){

        ArrayList<ArrayList<Integer>> matrix = new ArrayList<>();

        for(int i = 0; i < 3; i++){
            matrix.add(new ArrayList<>());
            for(int j = 0; j < 3; j++){
                matrix.get(i).add(j + 1);
            }
        }

        for(int r = 0; r < matrix.size(); r++){
            for(int c = 0; c < matrix.get(r).size(); c++){
                System.out.print(matrix.get(r).get(c) + " ");
            }
            System.out.println();
        }

    }
}
```

---

## Use a while loop to traverse a 2D ArrayList

```java
import java.util.ArrayList;

public class Main{
    public static void main(String[] args){

        ArrayList<ArrayList<Integer>> matrix = new ArrayList<>();

        matrix.add(new ArrayList<>());
        matrix.get(0).add(1);
        matrix.get(0).add(2);
        matrix.get(0).add(3);

        int r = 0;

        while(r < matrix.size()){
            int c = 0;

            while(c < matrix.get(r).size()){
                System.out.print(matrix.get(r).get(c) + " ");
                c++;
            }

            System.out.println();
            r++;
        }

    }
}
```

---

## Use an enhanced for loop (for-each) to traverse a 2D ArrayList

```java
import java.util.ArrayList;

public class Main{
    public static void main(String[] args){

        ArrayList<ArrayList<Integer>> matrix = new ArrayList<>();

        ArrayList<Integer> row = new ArrayList<>();
        row.add(1);
        row.add(2);
        row.add(3);

        matrix.add(row);

        for(ArrayList<Integer> r : matrix){
            for(Integer value : r){
                System.out.print(value + " ");
            }
            System.out.println();
        }

    }
}
```

---

# Algorithms

## Write a method that returns the minimum value of:
* The entire ArrayList
* Each row
* Each column
* A subsection of the ArrayList

```java
import java.util.ArrayList;

// Minimum of the entire 2D ArrayList
public static int minArrayList(ArrayList<ArrayList<Integer>> list){
    int min = list.get(0).get(0);
    for(ArrayList<Integer> row : list){
        for(int val : row){
            if(val < min) min = val;
        }
    }
    return min;
}

// Minimum of a specific row
public static int minRowList(ArrayList<ArrayList<Integer>> list, int row){
    int min = list.get(row).get(0);
    for(int val : list.get(row)){
        if(val < min) min = val;
    }
    return min;
}

// Minimum of a specific column
public static int minColList(ArrayList<ArrayList<Integer>> list, int col){
    int min = list.get(0).get(col);
    for(int r = 1; r < list.size(); r++){
        if(list.get(r).get(col) < min) min = list.get(r).get(col);
    }
    return min;
}

// Minimum of a subsection (rowStart to rowEnd, colStart to colEnd inclusive)
public static int minSubsectionList(ArrayList<ArrayList<Integer>> list, int rowStart, int rowEnd, int colStart, int colEnd){
    int min = list.get(rowStart).get(colStart);
    for(int r = rowStart; r <= rowEnd; r++){
        for(int c = colStart; c <= colEnd; c++){
            if(list.get(r).get(c) < min) min = list.get(r).get(c);
        }
    }
    return min;
}
```

--- 

## Write a method that returns the maximum value of: 
* The entire ArrayList
* Each row
* Each column
* A subsection of the ArrayList

```java
import java.util.ArrayList;

// Maximum of the entire 2D ArrayList
public static int maxArrayList(ArrayList<ArrayList<Integer>> list){
    int max = list.get(0).get(0);
    for(ArrayList<Integer> row : list){
        for(int val : row){
            if(val > max) max = val;
        }
    }
    return max;
}

// Maximum of a specific row
public static int maxRowList(ArrayList<ArrayList<Integer>> list, int row){
    int max = list.get(row).get(0);
    for(int val : list.get(row)){
        if(val > max) max = val;
    }
    return max;
}

// Maximum of a specific column
public static int maxColList(ArrayList<ArrayList<Integer>> list, int col){
    int max = list.get(0).get(col);
    for(int r = 1; r < list.size(); r++){
        if(list.get(r).get(col) > max) max = list.get(r).get(col);
    }
    return max;
}

// Maximum of a subsection (rowStart to rowEnd, colStart to colEnd inclusive)
public static int maxSubsectionList(ArrayList<ArrayList<Integer>> list, int rowStart, int rowEnd, int colStart, int colEnd){
    int max = list.get(rowStart).get(colStart);
    for(int r = rowStart; r <= rowEnd; r++){
        for(int c = colStart; c <= colEnd; c++){
            if(list.get(r).get(c) > max) max = list.get(r).get(c);
        }
    }
    return max;
}

```

--- 

## Write a method that returns the sum of:
* The entire ArrayList
* Each row
* Each column
* A subsection of the ArrayList

```java
import java.util.ArrayList;

// Sum of the entire 2D ArrayList
public static int sumArrayList(ArrayList<ArrayList<Integer>> list){
    int sum = 0;
    for(ArrayList<Integer> row : list){
        for(int val : row){
            sum += val;
        }
    }
    return sum;
}

// Sum of a specific row
public static int sumRowList(ArrayList<ArrayList<Integer>> list, int row){
    int sum = 0;
    for(int val : list.get(row)){
        sum += val;
    }
    return sum;
}

// Sum of a specific column
public static int sumColList(ArrayList<ArrayList<Integer>> list, int col){
    int sum = 0;
    for(int r = 0; r < list.size(); r++){
        sum += list.get(r).get(col);
    }
    return sum;
}

// Sum of a subsection (rowStart to rowEnd, colStart to colEnd inclusive)
public static int sumSubsectionList(ArrayList<ArrayList<Integer>> list, int rowStart, int rowEnd, int colStart, int colEnd){
    int sum = 0;
    for(int r = rowStart; r <= rowEnd; r++){
        for(int c = colStart; c <= colEnd; c++){
            sum += list.get(r).get(c);
        }
    }
    return sum;
}
```

--- 

## Write a method that returns the average of:
* The entire ArrayList
* Each row
* Each column
* A subsection of the ArrayList

```java
import java.util.ArrayList;

// Average of the entire 2D ArrayList
public static double averageArrayList(ArrayList<ArrayList<Integer>> list){
    int totalElements = 0;
    int sum = 0;
    for(ArrayList<Integer> row : list){
        totalElements += row.size();
        for(int val : row){
            sum += val;
        }
    }
    return (double) sum / totalElements;
}

// Average of a specific row
public static double averageRowList(ArrayList<ArrayList<Integer>> list, int row){
    int sum = 0;
    ArrayList<Integer> rowList = list.get(row);
    for(int val : rowList){
        sum += val;
    }
    return (double) sum / rowList.size();
}

// Average of a specific column
public static double averageColList(ArrayList<ArrayList<Integer>> list, int col){
    int sum = 0;
    for(int r = 0; r < list.size(); r++){
        sum += list.get(r).get(col);
    }
    return (double) sum / list.size();
}

// Average of a subsection (rowStart to rowEnd, colStart to colEnd inclusive)
public static double averageSubsectionList(ArrayList<ArrayList<Integer>> list, int rowStart, int rowEnd, int colStart, int colEnd){
    int sum = 0;
    int count = 0;
    for(int r = rowStart; r <= rowEnd; r++){
        for(int c = colStart; c <= colEnd; c++){
            sum += list.get(r).get(c);
            count++;
        }
    }
    return (double) sum / count;
}
```

---


## Write a method to check if at least one element has property
## Write a method to check all elements have property
## Write a method to count elements with property
## Write a method to access consecutive pairs

```java
import java.util.ArrayList;

// Check if at least one element is even
public static boolean anyEvenList(ArrayList<ArrayList<Integer>> list){
    for(ArrayList<Integer> row : list){
        for(int val : row){
            if(val % 2 == 0) return true;
        }
    }
    return false;
}

// Check if all elements are even
public static boolean allEvenList(ArrayList<ArrayList<Integer>> list){
    for(ArrayList<Integer> row : list){
        for(int val : row){
            if(val % 2 != 0) return false;
        }
    }
    return true;
}

// Count elements that are even
public static int countEvenList(ArrayList<ArrayList<Integer>> list){
    int count = 0;
    for(ArrayList<Integer> row : list){
        for(int val : row){
            if(val % 2 == 0) count++;
        }
    }
    return count;
}

// Access and print consecutive pairs in each row
public static void printConsecutivePairsList(ArrayList<ArrayList<Integer>> list){
    for(ArrayList<Integer> row : list){
        for(int c = 0; c < row.size() - 1; c++){
            System.out.println("(" + row.get(c) + ", " + row.get(c+1) + ")");
        }
    }
}
```

## Write a method to detect duplicates:
* The entire ArrayList
* Each row
* Each column
* A subsection of the ArrayList 

```java
import java.util.ArrayList;

// Detect duplicates in the entire ArrayList
public static boolean hasDuplicatesList(ArrayList<ArrayList<Integer>> list){
    for(int r1 = 0; r1 < list.size(); r1++){
        for(int c1 = 0; c1 < list.get(r1).size(); c1++){
            for(int r2 = r1; r2 < list.size(); r2++){
                int startCol = (r2 == r1) ? c1 + 1 : 0;
                for(int c2 = startCol; c2 < list.get(r2).size(); c2++){
                    if(list.get(r1).get(c1).equals(list.get(r2).get(c2))) return true;
                }
            }
        }
    }
    return false;
}

// Detect duplicates in a specific row
public static boolean hasDuplicatesRowList(ArrayList<ArrayList<Integer>> list, int row){
    ArrayList<Integer> rowList = list.get(row);
    for(int i = 0; i < rowList.size(); i++){
        for(int j = i + 1; j < rowList.size(); j++){
            if(rowList.get(i).equals(rowList.get(j))) return true;
        }
    }
    return false;
}

// Detect duplicates in a specific column
public static boolean hasDuplicatesColList(ArrayList<ArrayList<Integer>> list, int col){
    for(int i = 0; i < list.size(); i++){
        for(int j = i + 1; j < list.size(); j++){
            if(list.get(i).get(col).equals(list.get(j).get(col))) return true;
        }
    }
    return false;
}

// Detect duplicates in a subsection (rowStart to rowEnd, colStart to colEnd inclusive)
public static boolean hasDuplicatesSubsectionList(ArrayList<ArrayList<Integer>> list, int rowStart, int rowEnd, int colStart, int colEnd){
    for(int r1 = rowStart; r1 <= rowEnd; r1++){
        for(int c1 = colStart; c1 <= colEnd; c1++){
            for(int r2 = r1; r2 <= rowEnd; r2++){
                int startC = (r2 == r1) ? c1 + 1 : colStart;
                for(int c2 = startC; c2 <= colEnd; c2++){
                    if(list.get(r1).get(c1).equals(list.get(r2).get(c2))) return true;
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
import java.util.ArrayList;

// Shift rows down by 1
public static void shiftRowsList(ArrayList<ArrayList<Integer>> list){
    if(list.size() <= 1) return;

    ArrayList<Integer> lastRow = list.get(list.size() - 1);
    for(int r = list.size() - 1; r > 0; r--){
        list.set(r, list.get(r - 1));
    }
    list.set(0, lastRow);
}

// Shift columns right by 1
public static void shiftColsList(ArrayList<ArrayList<Integer>> list){
    if(list.size() == 0 || list.get(0).size() == 0) return;

    int cols = list.get(0).size();
    for(int r = 0; r < list.size(); r++){
        ArrayList<Integer> row = list.get(r);
        int last = row.get(cols - 1);
        for(int c = cols - 1; c > 0; c--){
            row.set(c, row.get(c - 1));
        }
        row.set(0, last);
    }
}
```

--- 

## Write a method to reverse:
* The row order
* The column order

```java
import java.util.ArrayList;

// Reverse the order of rows
public static void reverseRowsList(ArrayList<ArrayList<Integer>> list){
    int top = 0;
    int bottom = list.size() - 1;
    while(top < bottom){
        ArrayList<Integer> temp = list.get(top);
        list.set(top, list.get(bottom));
        list.set(bottom, temp);
        top++;
        bottom--;
    }
}

// Reverse the order of columns in each row
public static void reverseColsList(ArrayList<ArrayList<Integer>> list){
    for(ArrayList<Integer> row : list){
        int left = 0;
        int right = row.size() - 1;
        while(left < right){
            int temp = row.get(left);
            row.set(left, row.get(right));
            row.set(right, temp);
            left++;
            right--;
        }
    }
}
```

---


