# Unit 4: Data Collections — Essential Knowledge

## Topic 4.1 — Ethical and Social Issues Around Data Collection

* **4.1.A.1** When using a computer, personal privacy is at risk. When developing new programs, programmers should attempt to safeguard the personal privacy of the user.
* **4.1.B.1** Algorithmic bias describes systemic and repeated errors in a program that create unfair outcomes for a specific group of users.
* **4.1.B.2** Programmers should be aware of the data set collection method and the potential for bias before using the data to extrapolate new information or draw conclusions.
* **4.1.B.3** Some data sets are incomplete or inaccurate. Using such data may cause a program to work incorrectly or inefficiently.
* **4.1.C.1** The contents of a data set may only relate to a specific question or topic, and might not be appropriate to answer other questions or topics.

---

## Topic 4.2 — Introduction to Using Data Sets

* **4.2.A.1** A data set is a collection of specific pieces of information.
* **4.2.A.2** Data sets can be manipulated and analyzed to solve problems or answer questions. Values are accessed one at a time and processed according to the desired outcome.
* **4.2.A.3** Data can be represented in a chart or table to plan algorithms for manipulating the data.

---

## Topic 4.3 — Array Creation and Access

* **4.3.A.1** An array stores multiple values of the same type (primitive or object references).
* **4.3.A.2** The length of an array is set at creation and cannot change. Access length with the `.length` attribute.
* **4.3.A.3** Arrays created with `new` initialize elements to default values:

  * `int` → `0`
  * `double` → `0.0`
  * `boolean` → `false`
  * reference types → `null`
* **4.3.A.4** Initializer lists can create and initialize arrays.
* **4.3.A.5** Square brackets `[]` are used to access or modify elements by index.
* **4.3.A.6** Valid indices are `0` through `length-1`. Using an invalid index causes an `ArrayIndexOutOfBoundsException`.

---

## Topic 4.4 — Array Traversals

* **4.4.A.1** Traversing an array means using repetition to access all or a sequence of elements.
* **4.4.A.2** Indexed `for` loops and `while` loops require access by indices.
* **4.4.A.3** An enhanced `for` loop assigns each element to a loop variable (without using indices).
* **4.4.A.4** Assigning a new value to an enhanced `for` loop variable does **not** change the array element.
* **4.4.A.5** If an array stores object references, methods can modify attributes via the loop variable, but references in the array remain unchanged.
* **4.4.A.6** Any enhanced `for` loop traversal can be rewritten with an indexed loop.

---

## Topic 4.5 — Implementing Array Algorithms

* **4.5.A.1** Standard array traversal algorithms include:

  * find min/max
  * compute sum/average
  * check if at least one element has a property
  * check if all elements have a property
  * count elements with a property
  * access consecutive pairs
  * detect duplicates
  * shift/rotate elements
  * reverse order

---

## Topic 4.6 — Using Text Files

* **4.6.A.1** A file stores data persistently, even when a program isn’t running.
* **4.6.A.2** Use `File` and `Scanner` classes to connect a file to a program.
* **4.6.A.3** A file is opened with a `File` object: `File(String str)` where `str` is the pathname.
* **4.6.A.4** Programs must handle missing/invalid files (e.g., with `throws IOException`).
* **4.6.A.5** `File` and `IOException` are in `java.io` (import required).
* **4.6.A.6** **Scanner methods (Java Quick Reference):**

  * `Scanner(File f)`
  * `int nextInt()`
  * `double nextDouble()`
  * `boolean nextBoolean()`
  * `String nextLine()`
  * `String next()`
  * `boolean hasNext()`
  * `void close()`
* **4.6.A.7** Mixing `nextLine` with other `Scanner` methods may require adjustments (excluded from AP scope).
* **4.6.A.8** `String[] split(String del)` splits a string into substrings. (Regex details excluded.)
* **4.6.A.9** Use `while(hasNext())` to loop through file contents.
* **4.6.A.10** Always close files with `close()`.

---

## Topic 4.7 — Wrapper Classes

* **4.7.A.1** `Integer` and `Double` are immutable wrapper classes in `java.lang`.
* **4.7.A.2** **Autoboxing** converts primitives → wrapper automatically.
* **4.7.A.3** **Unboxing** converts wrappers → primitives automatically.
* **4.7.A.4** `Integer.parseInt(String s)` returns an `int`.
* **4.7.A.5** `Double.parseDouble(String s)` returns a `double`.

---

## Topic 4.8 — ArrayList Methods

* **4.8.A.1** An `ArrayList` is mutable in size and stores object references.
* **4.8.A.2** Constructor: `ArrayList()` creates an empty list.
* **4.8.A.3** Use generics: `ArrayList<E>` ensures type safety. Example: `ArrayList<String> names`.
* **4.8.A.4** `ArrayList` is in `java.util` (import required).
* **4.8.A.5** **ArrayList methods (Java Quick Reference):**

  * `int size()`
  * `boolean add(E obj)`
  * `void add(int index, E obj)`
  * `E get(int index)`
  * `E set(int index, E obj)`
  * `E remove(int index)`
* **4.8.A.6** Indices range from `0` to `size()-1`.

---

## Topic 4.9 — ArrayList Traversals

* **4.9.A.1** Traversal uses iteration or recursion to access all/some elements.
* **4.9.A.2** Deleting during traversal requires care to avoid skipping elements.
* **4.9.A.3** Accessing out-of-range indices throws `IndexOutOfBoundsException`.
* **4.9.A.4** Adding/removing elements while using an enhanced `for` loop causes `ConcurrentModificationException`.

---

## Topic 4.10 — Implementing ArrayList Algorithms

* **4.10.A.1** Standard algorithms include:

  * min/max
  * sum/average
  * check at least one/all elements with a property
  * count elements with a property
  * access consecutive pairs
  * detect duplicates
  * shift/rotate
  * reverse order
  * insert elements
  * delete elements
* **4.10.A.2** Some algorithms require traversing multiple Strings, arrays, or ArrayLists simultaneously.

---

## Topic 4.11 — 2D Array Creation and Access

* **4.11.A.1** A 2D array is an array of arrays. Size is fixed at creation. Stores primitives or object references. *(Non-rectangular arrays excluded.)*
* **4.11.A.2** Arrays created with `new` initialize elements to defaults (`0`, `0.0`, `false`, or `null`).
* **4.11.A.3** Initializer lists can create/initialize 2D arrays. Example: `int[][] arr = {{1,2,3},{4,5,6}};`
* **4.11.A.4** Use `[row][col]` to access/modify elements. First index = row, second = column.
* **4.11.A.5** Access a row with one index (returns a 1D array).
* **4.11.A.6** Use `.length` for number of rows; use `array[row].length` for columns. Out-of-range indices cause `ArrayIndexOutOfBoundsException`.

---

## Topic 4.12 — 2D Array Traversals

* **4.12.A.1** Use nested iteration for traversals. Orders include row-major, column-major, or custom.
* **4.12.A.2** In enhanced `for` loops:

  * Outer loop → rows (1D arrays).
  * Inner loop → elements within a row.
  * Assigning new values to loop variables does not change array contents.

---

## Topic 4.13 — Implementing 2D Array Algorithms

* **4.13.A.1** Standard 2D array algorithms include:

  * min/max (entire array, row, column, or subsection)
  * sum/average (entire array, row, column, subsection)
  * check at least one element has property
  * check all elements have property
  * count elements with property
  * access consecutive pairs
  * detect duplicates (array, row, column, subsection)
  * shift/rotate row/column
  * reverse row/column order

---

## Topic 4.14 — Searching Algorithms

* **4.14.A.1** Linear search checks each element until a match is found or all are checked. Works for arrays, ArrayLists, and can start at either end.
* **4.14.A.2** For 2D arrays, linear search must be applied row by row.

---

## Topic 4.15 — Sorting Algorithms

* **4.15.A.1** Selection sort and insertion sort are iterative algorithms for arrays/ArrayLists.
* **4.15.A.2** **Selection sort:** repeatedly finds the smallest/largest element and swaps it into place.
* **4.15.A.3** **Insertion sort:** inserts an element into its proper position by shifting elements as needed.

---

## Topic 4.16 — Recursion

* **4.16.A.1** A recursive method calls itself, with at least one base case (stopping condition) and one recursive call.
* **4.16.A.2** Each recursive call has its own local variables/parameters. Parameter values track progress like loop control variables.
* **4.16.A.3** Any recursive solution can be rewritten iteratively, and vice versa. *(Writing recursive code is excluded from AP exam scope.)*

---

## Topic 4.17 — Recursive Searching and Sorting

* **4.17.A.1** Recursion can traverse Strings, arrays, and ArrayLists.
* **4.17.B.1** Binary search requires sorted data. It checks the middle, eliminates half each step, repeats until found or exhausted.
* **4.17.B.2** Binary search is typically more efficient than linear search. *(Other searches excluded.)*
* **4.17.B.3** Binary search can be written iteratively or recursively.
* **4.17.C.1** Merge sort is a recursive algorithm that sorts arrays/ArrayLists. *(Other sorts excluded.)*
* **4.17.C.2** Merge sort repeatedly divides arrays into subarrays of size 1, then merges them back in order.

---
