---
aliases: []
---
Added: 202207041539
Name: 
Tags: #book
Topics: 
Author: 
Publisher: 
Date: 
Year: 
Edition:
URL: https://introcs.cs.princeton.edu/java/home/
Class: [[Intro to computer science]]


## What kind of book is this?

## What is this book about?

## What are the major topics and how are they organized, related, and/or independent?

## Chapter 1 : Elements of Programming
Topic:
### 1.1 Your First Java Program: Hello World
 compiler translates program from Java to machine code
**errors**
- *compile-time errors* prevent compiler from translating to machine code, caught at compile time
- *run-time errors* occur when program is executed due to invalid operation
- *logical errors* produces wrong answers and bugs when program is executed. Doesn't prevent program from running nd needs to be caught by programmer

### 1.2 Built-In Types of Data
- Java *data-type* importance- [[202207121924-must always be aware of data typed used in program written in strongly typed language|202207121924]]
	- Is this because it is *strongly typed?* (me)
- **14** in math numbers infinite, but w/ computers operations are only well deifnied for finite set of values within the data type
- **14** java 8 primitive data types
	1. int **35**
	2. short **35**
	3. long **35**
	4. double **35**
	5. float **35**
	6. char **35**
	7. byte **35**
	8. boolean **35**
- **14:** strings are non-primitive critical for input and output, and Java treats them differently than the other, primitive, data types
- **37:** Strings stored as sequences of characters encoded with Unicode

| type    | values                 | operators    |
| ------- | ---------------------- | ------------ |
| int     | integers               | $+,-,*,/,\%$ |
| double  | floating-point numbers | $+,-,*,/$    |
| boolean | boolean values         |   $\&\&, \|\|, !$           |
| char    | characters             |              |
| String  | character sequence     | +            |

#### Terminology
``` java
int a,b,c; //declaration statement
a = 1234 //assignment statement change value of a to 1234
b = 99; //assignment statement change value of b to 99
c = a + b //assignment statement change value of c to a+b
```
- **Literals** represent the data-type value [[202207130829-literals are how Java represent data-type value|202207130829]]
- **16: operators** represent operations performed on a data-type [[202207130845-operators are Java representations of operations that can be performed on data-types|202207130845]]
- **16: identifiers** act as variable name [[202207130853-identifiers are Java representations for variable names|202207130853]]

- **16 variable** assigned data-type value that can be changed during the execution of a program 
	- can be referred to by name
	- created with *declaration statements*
	- used for computation in *expressions*
- **16: declaration statement** initializes variables and their data types to be used in program
	- Why do they have to be declared before? Statically typed? (Me)
- **16: naming convention** 
- **16: constant variable** not a truly static as all variables can be changed, but conventional to refer to variables that do not change during program execution, and indicate stylistically with all caps identifier
- **17: expressions** combinations data-types  (literals and variable) and operations that are evaluated to produce a new value
	- directive to perform sequence of operations
	- representation of resulting value
- **17: Operator Precedence**
- **17:** **assignment statement** assigne the value of a variable
	- `=` is for assignment not indication of equality
- **18: inline initialization** variables declaration and assigbnment can be combined onto a single statement `int a = 1234`
- **18: trace table** used to study program behavior and how variables change with each statement over the execution of a program
- **18: type safety** data-type need to be declared for each variable to prevent mismatch errors 
	- need to perform proper operation on proper type of data