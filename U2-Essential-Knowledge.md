# Unit 2: Selection and Iteration — Essential Knowledge

## Topic 2.1 — Algorithms with Selection and Repetition

* **2.1.A.1** The building blocks of algorithms include sequencing, selection, and repetition.
* **2.1.A.2** Algorithms can contain selection, through decision making, and repetition, via looping.
* **2.1.A.3** Selection occurs when a choice of how the execution of an algorithm will proceed is based on a true or false decision.
* **2.1.A.4** Repetition is when a process repeats itself until a desired outcome is reached.
* **2.1.A.5** The order in which sequencing, selection, and repetition are used contributes to the outcome of the algorithm.

---

## Topic 2.2 — Boolean Expressions

* **2.2.A.1** Values can be compared using the relational operators `==` and `!=` to determine whether the values are the same. With primitive types, this compares actual primitive values. With reference types, this compares object references.
* **2.2.A.2** Numeric values can be compared using `<`, `>`, `<=`, and `>=` to determine the relationship between values.
* **2.2.A.3** An expression involving relational operators evaluates to a Boolean value.

---

## Topic 2.3 — if Statements

* **2.3.A.1** Selection statements change the sequential execution of statements.
* **2.3.A.2** An `if` statement is a type of selection statement that affects the flow of control by executing different segments of code based on the value of a Boolean expression.
* **2.3.A.3** A **one-way selection** (`if` statement) executes its body only when the Boolean expression is true.
* **2.3.A.4** A **two-way selection** (`if-else` statement) executes one segment when the expression is true, and another when it is false.

---

## Topic 2.4 — Nested if Statements

* **2.4.A.1** Nested if statements consist of `if`, `if-else`, or `if-else-if` statements inside other `if`, `if-else`, or `if-else-if` statements.
* **2.4.A.2** The Boolean expression of an inner nested `if` statement is evaluated only if the outer `if` condition is true.
* **2.4.A.3** A **multiway selection** (`if-else-if`) is used when there are multiple conditions. At most one block executes — the first true condition’s block. If none are true and there is a trailing `else`, that block executes.

---

## Topic 2.5 — Compound Boolean Expressions

* **2.5.A.1** Logical operators `!` (not), `&&` (and), and `||` (or) are used with Boolean expressions.

  * `!a` is true if `a` is false.
  * `a && b` is true if both `a` and `b` are true.
  * `a || b` is true if either or both are true.
  * Operator precedence: `!` > `&&` > `||`.
* **2.5.A.2** **Short-circuit evaluation** occurs when `&&` or `||` can be resolved by evaluating only the first expression.

---

## Topic 2.6 — Comparing Boolean Expressions

* **2.6.A.1** Two Boolean expressions are **equivalent** if they evaluate to the same value in all cases. Truth tables can prove equivalence.
* **2.6.A.2** **De Morgan’s Law**:

  * `!(a && b)` ⇔ `!a || !b`
  * `!(a || b)` ⇔ `!a && !b`
* **2.6.B.1** Two variables can reference the same object. References can be compared using `==` and `!=`.
* **2.6.B.2** Object references can be compared with `null` to check if they reference an object.
* **2.6.B.3** Classes often define their own `equals` method to specify equivalency between objects (usually based on attributes).

---

## Topic 2.7 — while Loops

* **2.7.A.1** Iteration changes flow of control by repeating code zero or more times as long as the loop condition is true.
* **2.7.A.2** An **infinite loop** occurs if the loop condition always evaluates to true.
* **2.7.A.3** A loop body does not execute if the condition is initially false.
* **2.7.A.4** **Off-by-one errors** occur when loops run one time too many or too few.
* **2.7.B.1** In a `while` loop, the condition is checked before each iteration. If true, the body executes, repeating until false.

---

## Topic 2.8 — for Loops

* **2.8.A.1** A `for` loop has three parts: initialization, Boolean expression, and update.
* **2.8.A.2** Initialization runs once, then the condition is checked. After each iteration, the update executes before re-checking the condition.
* **2.8.A.3** A `for` loop can be rewritten as an equivalent `while` loop (and vice versa).

---

## Topic 2.9 — Implementing Selection and Iteration Algorithms

* **2.9.A.1** Standard algorithms include:

  * Checking if an integer is divisible by another.
  * Extracting digits from an integer.
  * Counting occurrences of a condition.
  * Finding a minimum or maximum.
  * Computing a sum or average.

---

## Topic 2.10 — Implementing String Algorithms

* **2.10.A.1** Standard string algorithms include:

  * Checking if substrings have certain properties.
  * Counting substrings that meet criteria.
  * Creating a reversed string.

---

## Topic 2.11 — Nested Iteration

* **2.11.A.1** **Nested iteration statements** are loops inside loops. The inner loop completes all iterations before the outer loop continues.

---

## Topic 2.12 — Informal Run-Time Analysis

* **2.12.A.1** A **statement execution count** indicates how many times a statement runs in a program. These counts are often determined through tracing and analyzing loops.

---