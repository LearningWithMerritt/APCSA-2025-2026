
## Create and initialize a 1D Array
```java

public static void main(String[] args){

    // Create and initialize a 1D Array
    int[] numbers = {1, 2, 3, 4, 5};
    // OR
    int[] number = new int[3]; //--> {0,0,0}

}

```

---

## Write a method that returns the minimum value of any Array
```java

public static int findMinimum(int[] array){

    int min = arr[0];

    for(int i = 1; i < arr.length; i++){
        if(arr[i] < min){
            min = arr[i];
        }
    }
    return min;
}

```
---

## Write a method that returns the maximum value of any Array
```java
public static int findMax(int[] arr){

    int max = arr[0];

    for(int i = 1; i < arr.length; i++){
        if(arr[i] > max){
            max = arr[i];
        }
    }

    return max;
}
```
---

## Write a method to compute the sum of any Array of integers
```java
public static int findSum(int[] arr){

    int sum = 0;

    for(int i = 0; i < arr.length; i++){
        sum += arr[i];
    }

    return sum;
}
```

---

## Write a method to compute the average of any Array of integers
```java
public static double findAverage(int[] arr){

    int sum = 0;

    for(int i = 0; i < arr.length; i++){
        sum += arr[i];
    }

    return (double) sum / arr.length;
}
```

---


## Write a method to check if all elemets of a Array have a certain property
* loop through each element
* check if it has a property
* if one element doesn't return false
```java
public static boolean hasLetterA(String[] arr){
    for(int i = 0; i < arr.length; i++){
        String elem = arr[i];

        // Checking if they all have the letter "a"
        if(!elem.contains("a")){
            return False
        }
    }
}
```

---

## Write a method to count the number of elements in an Array that have a certain property.
```java
public static int countLetterA(String[] arr){
    int count = 0;
    for(int i = 0; i < arr.length; i++){
        String elem = arr[i];

        // Checking if they all have the letter "a"
        if(elem.contains("a")){
            count += 1
        }
    }
    return count;
}
```

---

## Write a method to access consecutve pairs of elements.
* watch out for index out of bounds!
```java
public static void workWithPairs(String[] arr){
    for(int i = 0; i < arr.length-1; i++){
        String first = arr[i];
        String second = arr[i+1];

    }
}
```

---

## Write a method to detect duplicate values in an Array
```java
public static boolean hasDuplicates(int[] arr){

    for(int i = 0; i < arr.length; i++){
        for(int j = i + 1; j < arr.length; j++){
            if(arr[i] == arr[j]){
                return true; // duplicate found
            }
        }
    }

    return false; // no duplicates
}
```
```java
import java.util.HashMap;

public static boolean altHasDuplicates(int[] arr){
    HashMap<Integer,Integer> map = new HashMap<>();
    for(int i = 0; i < arr.length; i++){
        int elem = arr[i];

        if(map.containsKey(elem)){
            return true;
        }
        else{
            map.put(elem,1);
        }

    }
    return false;
}
```

---

## Write a method to shift/rotate elements in an Array.
```java
public static void shiftLeft(String[] arr){

    if(arr.length == 0) return;

    //shifting the array in place
    String first = arr[0];
    for(int i = 0; i < arr.length-1; i++){
         arr[i] = arr[i+1];
    }

    arr[arr.length-1] = first;        
}

```
```java
public static void shiftRight(String[] arr){
    if(arr.length == 0) return;

    //shifting the array in place
    String last = arr[arr.length-1];
    for(int i = arr.length-1; i > 0;i--){
        arr[i] = arr[i-1];
    }

    arr[0] = last;
}
```

---

## Write a method to reverse the order of elements in an Array
```java
public static void reverseArray(int[] arr){
    int left = 0;
    int right = arr.length - 1;

    while(left < right){
        // Swap elements
        int temp = arr[left];
        arr[left] = arr[right];
        arr[right] = temp;

        left++;
        right--;
    }
}

