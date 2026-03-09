# Searching Algorithms

## Implement an iterative linear search method for integers, Arrays, and ArrayLists
```java
import java.util.ArrayList;

// Linear search for an array
public static int linearSearch(int target, int[] arr){
    for(int i = 0; i < arr.length; i++){
        if(arr[i] == target) return i;
    }
    return -1; // not found
}

// Linear search for an ArrayList
public static int linearSearch(int target, ArrayList<Integer> list){
    for(int i = 0; i < list.size(); i++){
        if(list.get(i) == target) return i;
    }
    return -1; // not found
}
```

---

## Implement an iterative binary search method for integers

```java
// Assumes array is sorted in ascending order
public static int binarySearchIterative(int[] arr, int target){
    int left = 0;
    int right = arr.length - 1;

    while(left <= right){
        int mid = left + (right - left) / 2;

        if(arr[mid] == target) return mid;
        else if(arr[mid] < target) left = mid + 1;
        else right = mid - 1;
    }

    return -1; // not found
}
```

---

## Implement a recursive binary search method for integers

```java
// Assumes array is sorted in ascending order
public static int binarySearchRecursive(int[] arr, int target, int left, int right){
    if(left > right) return -1; // not found

    int mid = left + (right - left) / 2;

    if(arr[mid] == target) return mid;
    else if(arr[mid] < target) return binarySearchRecursive(arr, target, mid + 1, right);
    else return binarySearchRecursive(arr, target, left, mid - 1);
}
```


```java
// Assumes array is sorted in ascending order
public static int binarySearch(int[] arr, int target, int left, int right){
    if(left > right) return -1; // not found

    int mid = left + (right - left) / 2;

    if(arr[mid] == target) return mid;
    else if(arr[mid] < target) return binarySearch(arr, target, mid + 1, right);
    else return binarySearch(arr, target, left, mid - 1);
}
```

---




