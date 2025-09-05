# AP CSA Unit 1 – Essential Knowledge

## Topic 1.1 – Introduction to Algorithms, Programming, and Compilers
- **1.1.A.1** Algorithms define step-by-step processes to follow when completing a task or solving a problem.  
- **1.1.A.2** Sequencing defines the order in which steps are completed; they occur one at a time.  
- **1.1.B.1** Code can be written in any text editor, but IDEs provide tools to write, compile, and run code.  
- **1.1.B.2** A compiler checks code for some errors, which must be fixed before running the program.  
- **1.1.C.1** A syntax error occurs when programming rules are not followed; detected by the compiler.  
- **1.1.C.2** A logic error is a mistake in the algorithm/program that causes incorrect behavior; detected through testing.  
- **1.1.C.3** A run-time error occurs during program execution and usually causes abnormal termination.  
- **1.1.C.4** An exception is a type of run-time error from an unexpected issue not detected by the compiler.  

---

## Topic 1.2 – Variables and Data Types
- **1.2.A.1** A data type is a set of values and allowed operations; types are primitive or reference.  
- **1.2.A.2** Primitive types define sets of values/operations for numbers and Boolean values.  
- **1.2.A.3** A reference type defines objects that are not primitive.  
- **1.2.B.1** The three primitive types in this course are `int`, `double`, and `boolean`.  
- **1.2.B.2** A variable stores a value that can change; each has a name and a type.  

---

## Topic 1.3 – Expressions and Output
- **1.3.A.1** `System.out.print` and `System.out.println` display output; `println` moves to a new line.  
- **1.3.B.1** A literal is a code representation of a fixed value.  
- **1.3.B.2** A string literal is a sequence of characters in double quotes.  
- **1.3.B.3** Escape sequences (e.g., `\"`, `\\`, `\n`) have special meanings in strings.  
- **1.3.C.1** Arithmetic expressions involve numeric values, variables, and operators (`int` or `double`).  
- **1.3.C.2** Arithmetic operators: `+`, `-`, `*`, `/`, `%`. Rules depend on operand types.  
- **1.3.C.3** Dividing two `int` values gives only the integer quotient; using `double` gives full quotient.  
- **1.3.C.4** `%` computes remainders.  
- **1.3.C.5** Operator precedence: `*`, `/`, `%` > `+`, `-`; evaluated left to right unless parentheses change order.  
- **1.3.C.6** Dividing an `int` by zero results in an `ArithmeticException`.  

---

## Topic 1.4 – Assignment Statements and Input
- **1.4.A.1** Variables must be assigned before use; reference types can be `null`.  
- **1.4.A.2** `=` initializes or changes a variable’s value.  
- **1.4.A.3** Expressions evaluate to a single value with a type.  
- **1.4.B.1** Input can be text, audio, visual, tactile; `Scanner` can read keyboard input.  

---

## Topic 1.5 – Casting and Range of Variables
- **1.5.A.1** `(int)` and `(double)` convert between int and double.  
- **1.5.A.2** Casting a `double` to an `int` truncates decimals.  
- **1.5.A.3** `int` values may be widened automatically to `double`.  
- **1.5.A.4** Rounding doubles: `(int)(x + 0.5)` or `(int)(x - 0.5)`.  
- **1.5.B.1** `Integer.MAX_VALUE` and `Integer.MIN_VALUE` define `int` limits.  
- **1.5.B.2** `int` values use 4 bytes, within the above range.  
- **1.5.B.3** Integer overflow occurs when results exceed `int` range, producing unexpected values.  
- **1.5.C.1** Round-off errors occur when doubles exceed precision limits; avoid by using `int`.  

---

## Topic 1.6 – Compound Assignment Operators
- **1.6.A.1** `+=`, `-=`, `*=`, `/=`, `%=` update variables by combining assignment with arithmetic.  
- **1.6.A.2** Post-increment (`x++`) and post-decrement (`x--`) adjust values by 1.  

---

## Topic 1.7 – API and Libraries
- **1.7.A.1** Libraries are collections of classes; APIs document how to use them.  
- **1.7.A.2** Attributes are data stored in variables; behaviors are defined by methods.  

---

## Topic 1.8 – Documentation with Comments
- **1.8.A.1** Comments (`/* */`, `//`, `/** */`) explain code but are ignored by the compiler.  
- **1.8.A.2** A precondition must be true before a method runs correctly.  
- **1.8.A.3** A postcondition must be true after a method finishes.  

---

## Topic 1.9 – Method Signatures
- **1.9.A.1** A method is a named block of code; procedural abstraction allows use without knowing implementation.  
- **1.9.A.2** Parameters are declared in headers; signatures consist of method name + parameter types.  
- **1.9.B.1** Void methods return nothing and aren’t used in expressions.  
- **1.9.B.2** Non-void methods return a value that must be stored or used.  
- **1.9.B.3** Arguments must match parameter type/number; passed by value.  
- **1.9.B.4** Overloaded methods share a name but have different signatures.  
- **1.9.B.5** A method call interrupts sequential execution until completed.  

---

## Topic 1.10 – Calling Class Methods
- **1.10.A.1** Class methods (static) belong to the class, not objects.  
- **1.10.A.2** Called with `ClassName.method()`, though in same class the name may be omitted.  

---

## Topic 1.11 – Math Class
- **1.11.A.1** `Math` is part of `java.lang` (imported by default).  
- **1.11.A.2** Math methods in Quick Reference:  
  - `abs(int)`, `abs(double)`  
  - `pow(double, double)`  
  - `sqrt(double)`  
  - `random()`  
- **1.11.A.3** `Math.random()` results can be modified with arithmetic/casting to produce ints or doubles in ranges.  

---

## Topic 1.12 – Objects: Instances of Classes
- **1.12.A.1** An object is an instance of a class; a class is the blueprint.  
- **1.12.A.2** Superclass/subclass relationships allow inheritance of attributes/behaviors.  
- **1.12.A.3** All classes in Java inherit from `Object`.  
- **1.12.B.1** Reference variables store object references (memory addresses).  

---

## Topic 1.13 – Object Creation and Storage
- **1.13.A.1** Classes contain constructors with same name as class.  
- **1.13.A.2** Constructor signatures: class name + parameter types.  
- **1.13.A.3** Constructors can be overloaded.  
- **1.13.B.1** Reference variables can hold an object reference or `null`.  
- **1.13.C.1** Objects are created with `new` + constructor.  
- **1.13.C.2** Constructors accept parameters to initialize attributes.  
- **1.13.C.3** Constructor arguments must match signature (by number/order/type). Passed by value.  
- **1.13.C.4** A constructor call interrupts sequential flow until finished.  

---

## Topic 1.14 – Calling Instance Methods
- **1.14.A.1** Instance methods are called on objects using the dot operator.  
- **1.14.A.2** Calling on `null` causes `NullPointerException`.  

---

## Topic 1.15 – String Manipulation
- **1.15.A.1** A `String` represents characters; created by literals or `new`.  
- **1.15.A.2** `String` belongs to `java.lang`.  
- **1.15.A.3** Strings are immutable.  
- **1.15.A.4** Strings can be concatenated with `+` or `+=`; primitives are auto-converted to Strings.  
- **1.15.A.5** Concatenating with objects calls `toString()`.  
- **1.15.B.1** String indices go from 0 to `length()-1`; accessing outside range throws `StringIndexOutOfBoundsException`.  
- **1.15.B.2** String methods (Java Quick Reference):  
  - `length()`  
  - `substring(int, int)`  
  - `substring(int)`  
  - `indexOf(String)`  
  - `equals(Object)`  
  - `compareTo(String)`  
- **1.15.B.3** `substring(index, index+1)` returns a single-character string.  
