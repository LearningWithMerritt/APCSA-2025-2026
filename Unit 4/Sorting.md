
# Sorting Algorithms

## Implement an iterative selection sort method for Arrays and ArrayLists
```java
import java.util.ArrayList;

// Selection sort for array
public static void selectionSort(int[] arr){
    for(int i = 0; i < arr.length - 1; i++){
        int minIndex = i;
        for(int j = i + 1; j < arr.length; j++){
            if(arr[j] < arr[minIndex]){
                minIndex = j;
            }
        }
        int temp = arr[i];
        arr[i] = arr[minIndex];
        arr[minIndex] = temp;
    }
}

// Selection sort for ArrayList
public static void selectionSort(ArrayList<Integer> list){
    for(int i = 0; i < list.size() - 1; i++){
        int minIndex = i;
        for(int j = i + 1; j < list.size(); j++){
            if(list.get(j) < list.get(minIndex)){
                minIndex = j;
            }
        }
        int temp = list.get(i);
        list.set(i, list.get(minIndex));
        list.set(minIndex, temp);
    }
}
```

---

## Implement an iterative insertion sort method for Arrays and ArrayLists

```java
import java.util.ArrayList;

// Insertion sort for array
public static void insertionSort(int[] arr){
    for(int i = 1; i < arr.length; i++){
        int key = arr[i];
        int j = i - 1;

        while(j >= 0 && arr[j] > key){
            arr[j + 1] = arr[j];
            j--;
        }

        arr[j + 1] = key;
    }
}

// Insertion sort for ArrayList
public static void insertionSort(ArrayList<Integer> list){
    for(int i = 1; i < list.size(); i++){
        int key = list.get(i);
        int j = i - 1;

        while(j >= 0 && list.get(j) > key){
            list.set(j + 1, list.get(j));
            j--;
        }

        list.set(j + 1, key);
    }
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