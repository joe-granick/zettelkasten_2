## Week 1 - Algorithmic Thinkin
### 1.1 Inputs, Outputs, and Error Conditions for specified program
- https://www.youtube.com/watch?v=h48IOPWXuEE
### 1.2 Sequential control in algorithms
- https://www.youtube.com/watch?v=g-gU30e44DM
### 1.3 Error Handling and Control Flow in algorithms
- https://www.youtube.com/watch?v=VmPNdkeW2QI
- **IF, IF-THEN- Else**
- **Nesting**
### 1.4 conditional execution and comparison
- https://www.youtube.com/watch?v=68vPATfr92c
- **Relational Operator**
- **Logical Operatior**
- **Truth Tables**
- **Boolean expressions**
### 1.5 Algorithm that involves sequential control and selection control
- https://www.youtube.com/watch?v=oIxgLZuy-do
### 1.6 Counting Operations
- https://www.youtube.com/watch?v=2P9O3g2Zie8

## Week 2

### 2.1 Given a problem specification, determine the inputs, outputs and error conditions of the algorithmic solution to the problem
### 2.2 Analyze algorithms by counting operations executed in the algorithm
### 2.3 Develop algorithms involving iteration using a WHILE loop
### 2.4 Count the number of operations executed in an algorithm that involves iteration

## Week 3 - Algorithm Implementation: Basic Java
### 3.1 Java Programs
#### 3.1a Edit, compile, and run a program
#### 3.1b Find and correct errors in a program
### 3.2 Built In Data Types
#### 3.2a Identify the four primitive types in Java and operations on those primitive types.
#### 3.2b Declare and assign values to variables.
#### (3.2c) Use Java identifier conventions (camel-case).
#### (3.2d) Evaluate results of assignment statements involving arithmetic operations.
#### (3.2e) Write and evaluate statements involving compound assignment operators (+=, -=, etc.).
#### (3.2f) Evaluate given expressions that involve the primitive types and/or  Strings and operations performed on them.
### (3.3) Input And Output
#### (3.3a) Use System.out.println(…) method to output information as a String in a Java program.
#### (3.3b) Use command-line arguments for input to a Java program.
#### (3.3c) Convert the command-line String arguments to ints using parseInt method.
### (3.4) Booleans And Logical Operators
#### (3.4a) Evaluate and construct complex Boolean expressions using the logical operators (&&, ||, !).
#### (3.4b) Construct truth tables to evaluate complex Boolean expressions.
#### (3.4c) Compare and contrast equivalent Boolean expressions.
### (3.5) The Math Class
#### (3.5a) Use the following constants and methods in Java Math class to write solutions to problems.
- **Constants:** `PI`
- **Methods:** `abs`, `ceil`, `floor`, `max`, `min`, `pow`, `random`, `round`, `sqrt`
### (3.6) Casting  
#### (3.6a) Evaluate expressions involving implicit type conversions.
#### (3.6b) Identify cases where explicit casting is needed.
#### (3.6c) Determine the results of executing program segments involving implicit type conversions and/or explicit casting.
#### (3.6d) Write solutions to problems involving explicit casts.
#### (3.6e) Identify program errors due to incorrect type assignments.
### (3.7) Relational Operators
#### (3.7a) Evaluate and write expressions using the relational operators (<, >, =, <=, >=, !=).
#### (3.7b) Explain the dangers in comparing double values with == or !=.
#### (3.7c) Write, compile and execute programs in Java.
#### (3.7d) Find and correct errors in a program.
#### (3.7e) Determine the most appropriate data type for a particular specification.
#### (3.7f) Determine the solution to Boolean expressions.

## Week 4 - Algorithm Implementation: Conditionals and Loops
Topics: [[program design]], [[programming in Java]]
### 4.1 Conditionals And Loops involving if, if-else, while, for, do-while
**todo**
- [ ] *additional reading* **SCOPE OF VARIABLES**
<font style="color:red"><b>CLARIFY</b></font>
- **LO4.1[(c)]** are all parts of the initializing statements within a for loops considered to be part of **conditional statement**?
	- if not is there a specific name for this
- **LO4.1[(i),(e)]* how are **infinite loops** related to the following?
	- **infinite recursion** 
	- **The Halting Problem**
	- **Turing Machines**
- **LO4.1[(e)]** how does the difference in **iteration** order between a **for loop** and **while loop** impact the execution of the **iteration variable**
	- does this have any impact on the occurrence of an **infinite** loop due unnecessary inclusion of a semi-colon?
	- how about the likelihood of a logical error in variable iteration?
- **LO4.1[(n)]** what other variables are constrained by a **scope** conditions?
	- how does this related to?
		- **encapsulation**
		- **modularization**
		- **OOP**
		- **methods/functions**
		- **libraries/APIs**

#### 4.1a Write program code to satisfy program specifications using expressions, conditional statements, and iterative statements.
https://www.youtube.com/watch?v=ST9UcMZGlYI
- **Conditionals**
```
if (cakeSize <= 0)
{
System.out.println("Error: Cakes size must be greater than")
}
else {
	if (cakeSize <= 5){
		price = 10;
		}
}
```
- do not use semi-colon after if statement, as additional statements that will be executed conditional to the if need to be included
	- ends with braces
	- same as with **loops**
- *conditionals* allow you to execute different code, based on meeting different conditions that can be specified for different program states
#### 4.1b Determine how many times a program segment will execute.
https://www.youtube.com/watch?v=ByH95Lr_3W8
- **loops** type of conditional that continues to execute block of code as long as condition remains true
- **counting operations** same rule set for *Psuedocode*
- **remember**: conditional executes one extra time than the rest of the block when the execution is `false` as it evaluates the **Truthiness** of the condition and executes all statements when `True`, but when the condition executes to `false` the code following the conditional doesn't execute, but the conditional statement already was. So *for every* `n` *times the program executes the **conditional block** it executes the preceding **conditional statement***  `n+1` times
	- careful of this  when tracing with print statements
	- will always evaluate to `false` once ("if not stuck in infinite loop")
#### 4.1c Determine if two or more code segments result with the same outcomes.
https://www.youtube.com/watch?v=DYkIAqgaBc4
- **for loop** alternative **repetition structure**is equivalent computationally to **while loop** but afford more compact syntax that can be a more natural way to express certain operations
- consists of 3 parts:
	1. Evaluate **initialization statement**
	2. Evaluate **boolean expression** for conditional
	3. `if true` execute **body of loop** and **increment statement** 
- for loop is just a while loop written more concisely
<h4><font style="color:gray">4.1d Describe the behavior of code segments involving control structures</font></h>
#### 4.1e Describe why a given code segment does not work as intended.
<font style="color:red"><b>missing semi-colon</b></font>   after *conditional statement* 
- in a *while loop* the *body of loop* from executing, and therefore any code written to change the condition 
- Since the condition never changes it will never evaluate to `false`
- An **infinite loop** results when a loop's condition cannot evaluate to false, the loop continually executes preventing **transfer of control** to rest of program
	- sometimes the code block continually executes as well depending on how the error manifests
	- The *infinite loop* above is cause by a <font style="color:red"><b>syntax error</b></font>  where the semi-colon prevents the *body-of-the-loop* from exacting resulting in only the conditional being infinitely evaluated
	- a <font style="color:red"><b>logical error</b></font> can also be the source of an infinite loop, where all code is executed, but the *body-of-the-loop* code doesn't appropriately specify operations to change the variables of evaluation in a process by which the stop condition will be reached
		- may be simple as a missing iterator
		- may be complexity to interactions where condition may not be met under certain conditions
		- see **infinite recursion**
		- see **halting problem**
 <font style="color:red"><b>missing braces</b></font> around body-of-loop
 - syntactically braces aren't required
 - if braces aren't included the first statement following the conditional  will be executed as long as the loop condition evaluates to true
 - however any statement following the first will only be expected once, meaning code won't work as intended if intention was to executed more statements within the same loop condition 
- ==would there be any difference in operation of a **for loop** since **iterating variable** *is incremented within the conditional* statement *rather than the* *body-of-the loop* like in a *while loop?==*
<h4><font style="color:gray">4.1f Determine the most appropriate selection/control control structures for a particular specification.</font></h>
<h4><font style="color:gray">4.1g Implement and trace code involving compound assignment idioms within loops (i++).</font></h>
#### 4.1h Implement and trace code involving break and continue
- `break` and `continue statements` are ways to modify behavior of both for and while loops
- **break statement** exits the loop, returning control to next sequence in the program
	- careful with nesting and which loops are being broken out of
	- [7:03] may be a potential example problem
- **continue statement** skips execution of any following statements in *body-of-loop* for iteration returning to next iteration of the conditional statement
#### 4.1i Recognize conditions that would result in an infinite loop scenario.
- See **LO4.1e** error with unnecessary placement of semi-colon after while condition
#### 4.1j Describe the process and result of nesting control structures.
https://www.youtube.com/watch?v=ALnbRzZSs-0
- 
#### 4.1k Trace program segments involving nested control structures.
#### 4.1l Write program code involving nested control structures.
https://www.youtube.com/watch?v=8ggvoTkDC2s
- putting an **if conditional** inside a **while loop**
- `i++` is a more concise way to increment a variable equivalent to `i= i+1` 
	- typically used for **iteration** in the for loop conditional statement
- **iteration** each individual execution of while loop<h4><font style="color:gray">4.1m Create appropriate test cases for if statements and test if statements in a comprehensive manner.</font></h>

#### 4.1n Identify the scope of variables within a program involving loops and conditionals.
https://youtu.be/s3jCMKDZ_s4
- any variable initialized within a loop  the **scope** is limited to the inside of the loop
	- a variable's **scope** is defined by the elements of a program that can utilize the variable 
	- this is a **local variable** because it is only available *locally* to the section of the program in which it is *encapsulated*
	- contrast this with a **global variable** which can be accessed *globally* by all parts of the program
- trying to use a variable <font style="color:red">outside of scope</font> like trying to use one initialized in an **inner loop** within the **outer loop** causes a <font style="color:red"><b>compile time error</b></font>
	- compiler doesn't know where to find variable, as no matching *identifiers* are initialized within that loop's **scope** initialized within that part of the program
	- rest of program can't use **local variable** in nested loop either

#### 4.1o Count the number of operations executed in program or program segment.
https://youtu.be/rABgH9d1dio
- counting operations follows *same principle as pseudocode*
- 
<h4><font style="color:gray">4.1l Use debugging tools to step through code in order to identify errors at various stages of program development.</font></h>
## Week 5 - The Array Data Structure
Topics : [[program design]], [[Arrays]]
### 5.1 Arrays in Java
#### (5.1a) Declare, create, and initialize one-dimensional(1D) and two-dimensional (2D) arrays.
https://youtu.be/z3BD06vzzaI
#### (5.1b) Explain Java’s default array initialization.
https://youtu.be/z3BD06vzzaI
#### (5.1c) Describe and implement initializer lists to initialize arrays.
https://youtu.be/z3BD06vzzaI
#### (5.1d) Describe and illustrate memory representation and allocation involving array implementations in Java.
https://youtu.be/gubYfF-5-Qg
#### (5.1e) Distinguish between valid and invalid array index references in code segments.
https://youtu.be/wOgJXSfAPvo
#### (5.1f) Identify ArrayIndexOutOfBoundsExceptions in program code segments.
https://youtu.be/wOgJXSfAPvo
#### (5.1g) Implement Java code to manipulate 1D arrays including, but not limited to, the following tasks:
https://youtu.be/88VVS0q-LS4
- Traverse and display the elements in an array in order and in reverse order.
- Reverse the elements in an array.
- Find and report the minimum/maximum value in an array.
- Find and report the index of the minimum/maximum value in an array.
- Find the average of numerical values in an array.
- Exchange values of two elements in an array.
- Shift elements in array to the right/left as specifications describe.
- Count the number of elements in an array satisfying given specifications.
- Remove elements that satisfy certain conditions from an array.
- Remove duplicate values from an array.
#### (5.1h) Demonstrate the use of the enhanced for loop (for-each) when writing code involving arrays.
https://youtu.be/A3pMviCH1_A
#### (5.1i) Distinguish between situations that can and that cannot utilize an enhanced for loop.
#### (5.1j) Determine the result of program code that traverses and manipulates the elements in a 2D array.
https://youtu.be/tSdlNF92Wxw
#### (5.1k) Trace and implement code to traverse and manipulate 2D arrays in row-major and column-major order.
https://youtu.be/tSdlNF92Wxw

## Week 6 - Input and Output
### (6.1a) Use command line arguments to provide input values to programs.
https://www.youtube.com/watch?v=MGC_oiGtQOA
- 
### (6.1b) Explain the meaning and functioning of String args[] as a parameter to main.

### (6.1c) Explain the need for Integer.parseInt() and Double.parseDouble when using command line input.

### (6.1d) Use standard output in programs: System.out.print(), System.out println()

### (6.1e) Use the following methods of StdIn in programs to read individual tokens from standard input: isEmpty(), readInt(), readDouble(), readBoolean(), readString()
https://www.youtube.com/watch?v=mzN7_pvmGZQ
- **standard input** is keyboard
- `StdIn.readInt()` waits until user inputs an integer number
- `StdIn.isEmpty()` checks if standard input is empty
- 

### (6.1f) Use the following methods of StdIn in programs for reading characters from standard input: hasNextChar(), readChar()

### (6.1g) Use the following methods of StdIn in programs for reading lines from standard input: hasNextLine(), readLine(), readAll()

### (6.1h) Use the following methods of StdIn in programs for reading from standard input to arrays: readAllInts(), readAllDoubles(), readAllBooleans(), readAllStrings(), readAllLines()

### (6.1i) Explain and implement an end-of-file sequence to end user input.

### (6.1j) Redirect standard output to a file when executing a program.

### (6.k) Redirect from a file to standard input when executing a program.

### (6.1l) Demonstrate piping the output of one program to the input of another