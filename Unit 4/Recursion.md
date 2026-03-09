## Write a method that accepts an integer and returns the result of a Fibonacci sequence up to that integer
```java
// Returns the nth Fibonacci number (0-indexed)
public static int fibonacci(int n){
    if(n <= 0) return 0;
    if(n == 1) return 1;

    return fibonacci(n - 1) + fibonacci(n - 2);
}
```

---

## Write a recursive method to traverse Strings, Arrays, and ArrayLists

```java
// Traverse a String recursively and print characters
public static void traverseString(String str, int index){
    if(index >= str.length()) return;
    System.out.println(str.charAt(index));
    traverseString(str, index + 1);
}

// Traverse an integer array recursively and print elements
public static void traverseArray(int[] arr, int index){
    if(index >= arr.length) return;
    System.out.println(arr[index]);
    traverseArray(arr, index + 1);
}

// Traverse an ArrayList recursively and print elements
import java.util.ArrayList;

public static void traverseArrayList(ArrayList<Integer> list, int index){
    if(index >= list.size()) return;
    System.out.println(list.get(index));
    traverseArrayList(list, index + 1);
}
```

---

## Write a method that implements the recursive binary search algorithm

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

## Write a method that implements the recursive merge sort algorithm to sort Arrays

```java
// Merge two sorted halves
public static void merge(int[] arr, int left, int mid, int right){
    int n1 = mid - left + 1;
    int n2 = right - mid;

    int[] L = new int[n1];
    int[] R = new int[n2];

    for(int i = 0; i < n1; i++) L[i] = arr[left + i];
    for(int j = 0; j < n2; j++) R[j] = arr[mid + 1 + j];

    int i = 0, j = 0, k = left;

    while(i < n1 && j < n2){
        if(L[i] <= R[j]){
            arr[k] = L[i];
            i++;
        } else{
            arr[k] = R[j];
            j++;
        }
        k++;
    }

    while(i < n1){
        arr[k++] = L[i++];
    }

    while(j < n2){
        arr[k++] = R[j++];
    }
}

// Recursive merge sort
public static void mergeSort(int[] arr, int left, int right){
    if(left < right){
        int mid = left + (right - left) / 2;
        mergeSort(arr, left, mid);
        mergeSort(arr, mid + 1, right);
        merge(arr, left, mid, right);
    }
}
```

---

## Write a method that implements the recursive merge sort algorithm to sort ArrayLists

```java
import java.util.ArrayList;

public static ArrayList<Integer> mergeSortList(ArrayList<Integer> list){
    if(list.size() <= 1) return list;

    int mid = list.size() / 2;
    ArrayList<Integer> left = new ArrayList<>(list.subList(0, mid));
    ArrayList<Integer> right = new ArrayList<>(list.subList(mid, list.size()));

    left = mergeSortList(left);
    right = mergeSortList(right);

    return mergeLists(left, right);
}

public static ArrayList<Integer> mergeLists(ArrayList<Integer> left, ArrayList<Integer> right){
    ArrayList<Integer> merged = new ArrayList<>();
    int i = 0, j = 0;

    while(i < left.size() && j < right.size()){
        if(left.get(i) <= right.get(j)){
            merged.add(left.get(i));
            i++;
        } else{
            merged.add(right.get(j));
            j++;
        }
    }

    while(i < left.size()){
        merged.add(left.get(i));
        i++;
    }

    while(j < right.size()){
        merged.add(right.get(j));
        j++;
    }

    return merged;
}
```
