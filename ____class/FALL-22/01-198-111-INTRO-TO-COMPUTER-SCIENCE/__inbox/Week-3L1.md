---
aliases: []
---
Added: 202209141415
Professor:
TA:
Tags: #class
Topics: 
Textbooks:
Resources:
Assignments:
Dates:
Exams:
Pre-Requistes:
Pre-Requisites to:
Grades:

# Monday 2022-09-19
**Learning Objectives**
**3.1** **Java Programs**
https://youtu.be/1wee9uiyrhk
-   (3.1a) Edit, compile, and run a program
-   (3.1b) Find and correct errors in a 
- (8:20) **public** class like bathrooms
- name of file must be same as name of class
- filename ending in **.java**
- **main method** 
- What does it take to run a java program?
	-  Have to compile before running**s15**
	- **compiler** is just a program that checks syntax before running
	- **syntax errors** 
		- misspelled keywords
		- missing semicolons/braces etc.
	- java program is **input** for compiler
	- **compiler** takes source code as input and outputs the **byte code**
	- **byte code** is closer to the machine code, and is difficult for humans to understand
	- **how to compile
		- `javac Fileame.java`
		- produces class file `filename.class`
	- **Interpreter** takes bytecode and executes **one line at the time**	
		- 	- **Interpreter** takes bytecode and executes **one line at the time**
		- **java virtual machine (*JVM*)** command called with `java`
		- follow with class method you want to call and any input arguments `java classMethod args`
	- comments not executed
		- used for explanation/reminder for programmers

**3.2 Built In Data Types**
https://youtu.be/f4jBh9OfCds
-   **(3.2a)** Identify the four primitive types in Java and operations on those primitive types.
	- `Integer`: `+,-,*,/,% `
	- `Float`: `+,-,*,/`
	- `Boolean`: `&&, ||, !`
	- `Char`: 
-   **(3.2b)** Declare and assign values to variables.
-   **(3.2c)** Use Java identifier conventions (camel-case).
-   **(3.2d)** Evaluate results of assignment statements involving arithmetic operations.
-   **(3.2e)** Write and evaluate statements involving compound assignment operators (+=, -=, etc.).
-   **(3.2f)** Evaluate given expressions that involve the primitive types and/or  Strings and operations performed on them.
- **data type** is a set of values and a set of operations on those values
	- related to **domain** and **range**
- **variables** have a data type and the corresponding set of operations that can be performed on that type of data
- **primitive data types**
-  `int`: `+,-,*,/,% `
	- `double: `+,-,*,/`
	- `boolean`: `&&, ||, !`
	- `char`: 
- **strings** are a special data type. They are not a primitive type, but are a **basic data type** and is syntactically treated similarly
	- `String` data-type variables **declared** and **assigned** like primitve data type variables
	- Have built in **concatenation** operation utilize with `+` operators 
	- They are built in but not primitive as they are just a composition of the built in primitive `char` data-type
- variables can be declared and assigned at same time
- **declaration** declare data type and identifier for variable
- **assignment** store value of corresponding data type in variable
- use **camel case** for naming variables (and methods later on)
- 
**3.3 Input and Output**
https://youtu.be/CPvJjbmowwg
-   (3.3a) Use _System.out.println(…)_ method to output information as a String in a Java program.
-   (3.3b) Use command-line arguments for input to a Java program.
-   (3.3c) Convert the command-line String arguments to **_ints_** using **_parseInt_** method.
**3.4 Booleans And Logical Operators**
https://youtu.be/rkupNx7V8cE
-   (3.4a) Evaluate and construct complex Boolean expressions using the logical operators (&&, ||, !).
-   (3.4b) Construct truth tables to evaluate complex Boolean expressions.
-   (3.4c) Compare and contrast equivalent Boolean expressions.
**3.5 The Math Class**
https://youtu.be/u9YjV9P4KQI
- Methods are just Java's implementation of functions
-   (3.5a) Use the following constants and methods in Java _Math_ class to write solutions to problems.
    -   _Constants:__PI_
    -   _Methods: abs, ceil, floor, max, min, pow, random, round, sqrt_
**3.6 Casting**
https://youtu.be/kE3tQEuqQWM
- can cast when data is in one primitive data type and you need it in another
	- **Implicit** some casts Java does automatically
	- **Explicit**
-   (3.6a) Evaluate expressions involving implicit type conversions.
-   (3.6b) Identify cases where explicit casting is needed.
-   (3.6c) Determine the results of executing program segments involving implicit type conversions and/or explicit casting.
-   (3.6d) Write solutions to problems involving explicit casts.
-   (3.6e) Identify progr
**3.7 Relational Operators**
https://youtu.be/IUQlbMgyP1s
-   (3.7a) Evaluate and write expressions using the relational operators (<, >, =, <=, >=, !=).
-   (3.7b) Explain the dangers in comparing double values with == or !=.
-   (3.7c) Write, compile and execute programs in Java.
-   (3.7d) Find and correct errors in a program.
-   (3.7e) Determine the most appropriate data type for a particular specification.
-   (3.7f) Determine the solution to Boolean expressions.

## Example program 5
- If error condition need to check
- If precondition, no need to check (contract w/ user)
- Cant's always cover every test case
## Quiz
- `(x>2)`Boolean expression
- Expression
- Variable
- Variable
- Boolean expression
- Statement
## Quiz Identify Input, Output, Error Condition
- Hello world
- Larger of 3 negative numbers
## 2. Algorithm Implementation and counting
### From design to implementation
**Algorithms can be expressed as**
- flow-charts- good for visual expression
- psuedocode- express using psuedo instructions
- program code
### Adding control flow
- program can conditionally break sequential executions
### Basic control flow
- **IF-ELSE:** Branch based on condition
- **WHILE:** Iterative execution while condition is true
### Constructing test cases
- How many test cases are needed?
### Counting operations
- **Always** count `or` as multiple operations even if first condition evaluates `True`

### Extra example
SET count TO 1
WHILE count < n
	IF COUNT%2 is 0
		DISPLAY even
	ELSE
		DISPLAY odd
	ENDIF
	ADD 1 to count
ENDWHILE

SET count TO 0 (1)
WHILE count <= n (n+2)
	DISPLAY count (n+1)
	COMPUTE count AS count + 1 (n+1)
ENDWHILE

### MEasuring performance
- **Counting operations**
- **Each Operation** take some computer time (CPU cycles)
- **Algorithm performance** (dpending on many varables, including processor speed, best measured by number of operations as actual speed depends on many other factors outside the program design)
- **Algorith performance** based on some variable (like data size n)