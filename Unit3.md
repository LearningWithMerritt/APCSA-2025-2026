# Unit 3: Class Creation — Essential Knowledge

## Topic 3.1 — Abstraction and Program Design

* **3.1.A.1** Abstraction reduces complexity by focusing on the main idea, hiding irrelevant details, and grouping related details.
* **3.1.A.2** Data abstraction separates abstract properties of a data type from its representation. It gives data a name without referencing specific details.
* **3.1.A.3** An attribute is a data abstraction defined in a class outside methods or constructors.

  * **Instance variable**: unique to each instance.
  * **Class variable**: shared across all instances.
* **3.1.A.4** Procedural abstraction gives a name to a process and allows use of methods by knowing *what* they do, not *how*.

  * **Method decomposition** breaks behaviors into smaller methods.
  * Promotes code reuse and reduced complexity.
* **3.1.A.5** Using parameters generalizes procedures, making them reusable with different input values.
* **3.1.A.6** Procedural abstraction allows internal method changes (e.g., efficiency improvements) without affecting users if the signature and behavior remain the same.
* **3.1.A.7** Designing a class before implementation (attributes + behaviors) is helpful and can be expressed in natural language or diagrams.

---

## Topic 3.2 — Impact of Program Design

* **3.2.A.1** System reliability means a program performs as expected under stated conditions. Programmers should maximize reliability by testing under varied conditions.
* **3.2.A.2** Programs impact society, economy, and culture — both positively and negatively. Unintended harmful effects may arise.
* **3.2.A.3** Legal and intellectual property concerns arise when creating programs.

  * Open-source code can be reused freely.
  * Non-open-source code requires permission or purchase.

---

## Topic 3.3 — Anatomy of a Class

* **3.3.A.1** Data encapsulation hides implementation details. `public` and `private` control access.

  * `private` → restricted to the declaring class.
  * `public` → accessible externally.
* **3.3.A.2** In this course, classes are always `public` and declared with `class`.
* **3.3.A.3** Constructors are always `public`.
* **3.3.A.4** Instance variables belong to the object, with each object having its own copy.
* **3.3.A.5** Attributes should remain internal for encapsulation. Best practice: make instance variables `private` unless specified otherwise.
* **3.3.A.6** Behaviors (methods) may be `public` (accessible externally) or `private` (internal use only).

---

## Topic 3.4 — Constructors

* **3.4.A.1** An object’s **state** is defined by its instance variables and their values at a given time. This represents a *has-a* relationship.
* **3.4.A.2** Constructors set an object’s initial state. They allocate memory, return an object reference, and may accept parameters to initialize variables.
* **3.4.A.3** If a constructor takes a mutable object as a parameter, the instance variable should be initialized with a **copy**, not the original reference, to avoid unintended modification.
* **3.4.A.4** If no constructor is written, Java provides a **default constructor** (no parameters, variables set to default values).
* **3.4.A.5** Default values:

  * `int` → `0`
  * `double` → `0.0`
  * `boolean` → `false`
  * reference types → `null`

---

## Topic 3.5 — Methods: How to Write Them

* **3.5.A.1** A **void method** does not return a value; its header uses `void`.
* **3.5.A.2** A **non-void method** returns a single value, with the return type in the header.
* **3.5.A.3** Non-void methods use **return by value**, where an expression matching the return type is evaluated and returned.
* **3.5.A.4** `return` keyword ends method execution and returns control. Code after a `return` is never executed. `return` inside conditionals/loops ends execution early.
* **3.5.A.5** **Accessor methods** return copies of variable values (non-void).
* **3.5.A.6** **Mutator (modifier) methods** change variable values (often void).
* **3.5.A.7** Methods with parameters use arguments to accomplish tasks.
* **3.5.A.8** For primitive arguments, parameters get copies. Changes to parameters don’t affect original arguments.

---

## Topic 3.6 — Methods: Passing and Returning Object References

* **3.6.A.1** Passing an object reference as a parameter copies the reference, not the object. If the object is mutable, its state may change inside the method. Best practice: don’t modify mutable objects unless specified.
* **3.6.A.2** Returning an object reference returns the reference itself, not a copy.
* **3.6.A.3** Methods cannot access private data/methods of an object parameter unless the parameter is of the same class type.

---

## Topic 3.7 — Class Variables and Methods

* **3.7.A.1** Class methods cannot directly access instance variables or instance methods unless given an instance via a parameter.
* **3.7.A.2** Class methods can access/change class variables and call other class methods.
* **3.7.B.1** Class variables are shared by all objects of a class and are declared with `static`.
* **3.7.B.2** `public static` variables are accessed externally with `ClassName.variableName`.
* **3.7.B.3** Variables declared `final` cannot be modified.

---

## Topic 3.8 — Scope and Access

* **3.8.A.1** Local variables are declared inside methods/constructors/blocks. They can only be accessed within that block. Parameters are also local variables. They cannot be `public` or `private`.
* **3.8.A.2** If a local variable/parameter has the same name as an instance variable, it shadows the instance variable within that scope.

---

## Topic 3.9 — `this` Keyword

* **3.9.A.1** Inside an instance method/constructor, `this` holds a reference to the current object.
* **3.9.A.2** `this` can be passed as an argument in method calls.
* **3.9.A.3** Class (static) methods do not have a `this` reference.

---
