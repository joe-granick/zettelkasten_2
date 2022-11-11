---
aliases: []
---
Added: 202206201838
Professor:
TA:
Tags: #class
Topics: 
Textbooks:
Resources: https://introcs.cs.rutgers.edu/lectures/
Assignments: https://introcs.cs.rutgers.edu/assignments/
Dates:
Exams:
Pre-Requistes:
Pre-Requisites to:
- [[01-198-112 Data Structures]]
Grades:
URL: https://www.cs.rutgers.edu/academics/undergraduate/course-synopses/course-details/01-198-111-introduction-to-computer-science

# Exams
## Exam 1
- 100% Week 1-4
- 10/12

### Week 1 Algorithmic Thinking
- [ ] Review video lectures
	- [ ] [**(1.1)**](https://youtu.be/h48IOPWXuEE) Given a problem specification, determine the **inputs, outputs and error conditions** of the algorithmic solution to the problem.
	- [ ] [**(1.2)**](https://youtu.be/g-gU30e44DM) Develop algorithms involving sequential control
	- [ ] [**(1.3)**](https://youtu.be/VmPNdkeW2QI) Develop algorithms involving selection control: **_IF, IF-THEN-ELSE_**
	- [ ] [**(1.4)**](https://youtu.be/68vPATfr92c) Write algorithms that include decision statements using Boolean expressions with relational and logical operators
	- [ ] [**(1.5)**](https://youtu.be/oIxgLZuy-do) Develop an appropriate algorithm to solve a problem or accomplish a task involving sequential and selection control.
	- [ ] [**(1.6)**](https://youtu.be/2P9O3g2Zie8) Count the number of operations executed in an algorithm involving decision statements.

### Week 2 Algorithmic Thinking and Analysis
- [ ] Review counting operations examples (Lecture slides 2)
- [ ] Review video lectures
	- [ ] **(2.1)** Given a problem specification, determine the inputs, outputs and error conditions of the algorithmic solution to the problem
	- [ ] [**(2.2)**](https://youtu.be/OyAbVnnZAlw) Analyze algorithms by counting operations executed in the algorithm
	- [ ] [**(2.3)**](https://youtu.be/BTsRuG1EDlo) Develop algorithms involving iteration using a WHILE loop
	- [ ] [**(2.4)**](https://rutgers.box.com/s/a03thnyni6sqd8x7yfhggpddadkny83n) Count the number of operations executed in an algorithm that involves iteration
- [x] Scarlet Placement Exam 
- [ ] HW1 Psuedocode Open: 9/16 Due: 9/23
- [x] **Recitation PreQuiz Due: 9/16**
- [ ] **Recitation PostQuiz Due:9/17**
- [[Week-2L1]]
#### Currently unlcear
**Identify** (*precise definition needed*)
- variable
- constant
- expression
	- combination of **variables**, **operators**, and/or **literals** that evaluates to a value
- Boolean expression 	- 
	- Includes relational operator
- Statement
**Difference between**
- Statement and expression?
#### Quiz
##### Print HelloWorld
[[LECTURE 1 QUIZ-2A]]
**INPUT:** None
**Output:** display phrase "Hello, World"
**Error:** None
```
DISPLAY "Hello, World"
```
##### Add two positive  numbers
**Input:** Two numbers >= 0
**Output:** sum of both numbers added
**Error:** Negative number input, non-number type input
```
READ num1 R
READ num2
IF num1 < 0 OR num2 < 0
	DISPLAY "Error negative input"
ELSE
	COMPUTE sum AS num1 + num2
	DISPLAY sum
```
##### Find max of two numbers
**Input:** two numbers 
**Output:** the large of the two input numbers
**Error:** non-number type input
```
```
##### Find max of 3 negative numbers
**Input:** 3 numbers with values <0
**Output:** the largest of the 3 numbers
**Error:** Non-negative numbers input, Non-number input
```
```

##### Find area of a circle given radius
**Input:** Given radius of a circle
**Output:** Area of resulting circle
**Error:** Non-numeric input
```
READ radius
COMPUTE area AS PI*(radius*radius)
DISPLAY area
```

##### Print even numbers from 1 - 100
**Input:** None
**Output:** all even number between 1 and 100
**Error:** 
```
SET n TO 2
WHILE(n <= 100)
	DISPLAY n
	COMPUTE n AS n+2
ENDWHILE
```

##### Design ATM machine accepting deposits/withdrawals
**Input:** 
**Output:** 
**Error:** 
```
```

### Week 3 Algorithm Implementation, Basic Java
- [ ] **HW1 Psuedocode Open: 9/16 Due: 9/23**
- [ ] HW2 Hello World Open: 9/23 Due: 9/30
- [ ] Review lecture videos
	- [ ] **[(3.1)](https://youtu.be/1wee9uiyrhk) Java Programs**
		-   (3.1a) Edit, compile, and run a program
		-   (3.1b) Find and correct errors in a program
	- [ ] **[(3.2)](https://youtu.be/f4jBh9OfCds) Built In Data Types**
		-   (3.2a) Identify the four primitive types in Java and operations on those primitive types.
		-   (3.2b) Declare and assign values to variables.
		-   (3.2c) Use Java identifier conventions (camel-case).
		-   (3.2d) Evaluate results of assignment statements involving arithmetic operations.
		-   (3.2e) Write and evaluate statements involving compound assignment operators (+=, -=, etc.).
		-   (3.2f) Evaluate given expressions that involve the primitive types and/or  Strings and operations performed on them.
	- [ ] **[(3.3)](https://youtu.be/CPvJjbmowwg) Input And Output**
		-   (3.3a) Use _System.out.println(…)_ method to output information as a String in a Java program.
		-   (3.3b) Use command-line arguments for input to a Java program.
		-   (3.3c) Convert the command-line String arguments to **_ints_** using **_parseInt_** method.
	- [ ] **[(3.4)](https://youtu.be/rkupNx7V8cE) Booleans And Logical Operators**
		-   (3.4a) Evaluate and construct complex Boolean expressions using the logical operators (&&, ||, !).
		-   (3.4b) Construct truth tables to evaluate complex Boolean expressions.
		-   (3.4c) Compare and contrast equivalent Boolean expressions.
	- [ ] **[(3.5)](https://youtu.be/u9YjV9P4KQI) The Math Class**
		-   (3.5a) Use the following constants and methods in Java _Math_ class to write solutions to problems.
		    -   _Constants:__PI_
		    -   _Methods: abs, ceil, floor, max, min, pow, random, round, sqrt_
	- [ ] **[(3.6)](https://youtu.be/kE3tQEuqQWM) Casting**  
		-   (3.6a) Evaluate expressions involving implicit type conversions.
		-   (3.6b) Identify cases where explicit casting is needed.
		-   (3.6c) Determine the results of executing program segments involving implicit type conversions and/or explicit casting.
		-   (3.6d) Write solutions to problems involving explicit casts.
-   (3.6e) Identify program errors due to incorrect type assignments.
- [ ] **[(3.7)](https://youtu.be/IUQlbMgyP1s) Relational Operators**
		-   (3.7a) Evaluate and write expressions using the relational operators (<, >, =, <=, >=, !=).
		-   (3.7b) Explain the dangers in comparing double values with == or !=.
		-   (3.7c) Write, compile and execute programs in Java.
		-   (3.7d) Find and correct errors in a program.
		-   (3.7e) Determine the most appropriate data type for a particular specification.
		-   (3.7f) Determine the solution to Boolean expressions.
-   Textbook reading 1.1, 1.2
-   [Lecture slides](https://rutgers.box.com/s/no7pcx03ikfh6ybm9fdu9kdw1zvrnjck)
-   [Book video](https://www.cubits.ai/collections/41/modules/1/?key=c9be4c54-e487-4648-b149-cb2281e95fc9)
-   Java reference sheet
-   [Tools installation](https://introcs.cs.rutgers.edu/tools/)

### Week 4 Array Data Structure
- [ ] Review lectures
	- [ ] [(5.1a)](https://youtu.be/z3BD06vzzaI) Declare, create, and initialize one-dimensional(1D) and two-dimensional (2D) arrays.
	- [ ] [(5.1b)](https://youtu.be/z3BD06vzzaI) Explain Java’s default array initialization.
	- [ ] [(5.1c)](https://youtu.be/z3BD06vzzaI) Describe and implement initializer lists to initialize arrays.
	- [ ] [(5.1d)](https://youtu.be/gubYfF-5-Qg) Describe and illustrate memory representation and allocation involving array implementations in Java.
	- [ ] [(5.1e)](https://youtu.be/wOgJXSfAPvo) Distinguish between valid and invalid array index references in code segments.
	- [ ] [(5.1f)](https://youtu.be/wOgJXSfAPvo) Identify _ArrayIndexOutOfBoundsExceptions_ in program code segments.
	- [ ] [(5.1g)](https://youtu.be/88VVS0q-LS4) Implement Java code to manipulate 1D arrays including, but not limited to, the following tasks:
		- Traverse and display the elements in an array in order and in reverse order.
	    -   Reverse the elements in an array.
	    -   Find and report the minimum/maximum value in an array.
	    -   Find and report the index of the minimum/maximum value in an array.
	    -   Find the average of numerical values in an array.
	    -   Exchange values of two elements in an array.
	    -   Shift elements in array to the right/left as specifications describe.
	    -   Count the number of elements in an array satisfying given specifications.
	    -   Remove elements that satisfy certain conditions from an array.
	    -   Remove duplicate values from an array.
- [ ] [(5.1h)](https://youtu.be/A3pMviCH1_A) Demonstrate the use of the enhanced for loop (for-each) when writing code involving arrays.
- [ ] (5.1i) Distinguish between situations that can and that cannot utilize an enhanced for loop.
- [ ] [(5.1j)](https://youtu.be/tSdlNF92Wxw) Determine the result of program code that traverses and manipulates the elements in a 2D array.
- [ ] [(5.1k)](https://youtu.be/tSdlNF92Wxw) Trace and implement code to traverse and manipulate 2D arrays in **row-major** and **column-major order.**
-   Textbook reading 1.4
-   [Lecture slides](https://rutgers.box.com/s/80akhq416iechgxbmd44outsp3ya4j3m)
-   [Book video](https://www.cubits.ai/collections/41/modules/3/?key=c9be4c54-e487-4648-b149-cb2281e95fc9)

## Exam 2
- 25% Week 1-4
- 75% Week 5-8
- 11/16
### Week 5
### Week 6
### Week 7 
### Week 8
## Exam 3 (Final)
- 5% Week 1-4
- 20% Week 5-8
- 75% Week 9-14
### Week 9
### Week 10
### Week 11
### Week 13
### Week 14
# Week 1: Algorithmic Thinking
## 1.1: Given a problem specification, determine the inputs, outputs and error conditions of the algorithmic solution to the problem.
**input** what is read by computer
**output** what is displayed or returned by program
**error** anything that can be wrong with input that needs to be handled by algorithm