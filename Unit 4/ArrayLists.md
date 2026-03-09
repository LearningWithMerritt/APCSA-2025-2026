
## Import the ArrayList class
```java
import java.util.ArrayList;

public class Main{
    public static void main(String[] args){

    }
}
```

---

## Create and initialize a 1D ArrayList

```java
import java.util.ArrayList;

public class Main{
    public static void main(String[] args){

        // Create and initialize a 1D ArrayList
        ArrayList<Integer> numbers = new ArrayList<>();

        numbers.add(1);
        numbers.add(2);
        numbers.add(3);

    }
}
```

---

## Produce and handle (try-catch) a ConcurrentModificationException

```java
import java.util.ArrayList;
import java.util.ConcurrentModificationException;

public class Main{
    public static void main(String[] args){

        ArrayList<Integer> numbers = new ArrayList<>();

        numbers.add(1);
        numbers.add(2);
        numbers.add(3);

        try{
            for(Integer num : numbers){
                if(num == 2){
                    numbers.remove(num); // causes ConcurrentModificationException
                }
            }
        }
        catch(ConcurrentModificationException e){
            System.out.println("ConcurrentModificationException caught!");
        }

    }
}
```


## Write a method that returns the minimum value of any ArrayList
```java
import java.util.ArrayList;

public static int findMin(ArrayList<Integer> list){
    int min = list.get(0);

    for(int i = 1; i < list.size(); i++){
        if(list.get(i) < min){
            min = list.get(i);
        }
    }

    return min;
}
```

---


## Write a method that returns the minimum value of any ArrayList
```java
import java.util.ArrayList;

public static int findMin(ArrayList<Integer> list){
    int min = list.get(0);

    for(int i = 1; i < list.size(); i++){
        if(list.get(i) < min){
            min = list.get(i);
        }
    }

    return min;
}
```

---

## Write a method that returns the maximum value of any ArrayList

```java
import java.util.ArrayList;

public static int findMax(ArrayList<Integer> list){
    int max = list.get(0);

    for(int i = 1; i < list.size(); i++){
        if(list.get(i) > max){
            max = list.get(i);
        }
    }

    return max;
}
```

---

## Write a method to compute the sum of any ArrayList of integers

```java
import java.util.ArrayList;

public static int findSum(ArrayList<Integer> list){
    int sum = 0;

    for(int i = 0; i < list.size(); i++){
        sum += list.get(i);
    }

    return sum;
}
```

---

## Write a method to compute the average of any ArrayList of integers

```java
import java.util.ArrayList;

public static double findAverage(ArrayList<Integer> list){
    int sum = 0;

    for(int i = 0; i < list.size(); i++){
        sum += list.get(i);
    }

    return (double) sum / list.size();
}
```

---

## Write a method to check if all elements of an ArrayList have a certain property

```java
import java.util.ArrayList;

public static boolean allEven(ArrayList<Integer> list){
    for(int num : list){
        if(num % 2 != 0){
            return false;
        }
    }
    return true;
}
```

---

## Write a method to count the number of elements in an ArrayList that have a certain property

```java
import java.util.ArrayList;

public static int countEven(ArrayList<Integer> list){
    int count = 0;
    for(int num : list){
        if(num % 2 == 0){
            count++;
        }
    }
    return count;
}
```

---

## Write a method to access consecutive pairs of elements

```java
import java.util.ArrayList;

public static void printConsecutivePairs(ArrayList<Integer> list){
    for(int i = 0; i < list.size() - 1; i++){
        System.out.println("(" + list.get(i) + ", " + list.get(i + 1) + ")");
    }
}
```

---

## Write a method to detect duplicate values in an ArrayList
```java
import java.util.ArrayList;

public static boolean hasDuplicates(ArrayList<Integer> list){

    for(int i = 0; i < list.size(); i++){
        for(int j = i + 1; j < list.size(); j++){
            if(list.get(i).equals(list.get(j))){
                return true; // duplicate found
            }
        }
    }

    return false; // no duplicates
}
```
```java
import java.util.ArrayList;
import java.util.HashSet;

public static boolean hasDuplicates(ArrayList<Integer> list){
    HashSet<Integer> set = new HashSet<>();
    for(int num : list){
        if(!set.add(num)){
            return true;
        }
    }
    return false;
}
```

---

## Write a method to shift/rotate elements in an ArrayList

```java
import java.util.ArrayList;

public static void shiftLeft(ArrayList<Integer> list){
    if(list.size() == 0) return;

    int first = list.remove(0);
    list.add(first);
}

public static void shiftRight(ArrayList<Integer> list){
    if(list.size() == 0) return;

    int last = list.remove(list.size() - 1);
    list.add(0, last);
}
```

---

## Write a method to reverse the order of elements in an ArrayList

```java
import java.util.ArrayList;

public static void reverseList(ArrayList<Integer> list){
    int left = 0;
    int right = list.size() - 1;

    while(left < right){
        int temp = list.get(left);
        list.set(left, list.get(right));
        list.set(right, temp);

        left++;
        right--;
    }
}
```


     





