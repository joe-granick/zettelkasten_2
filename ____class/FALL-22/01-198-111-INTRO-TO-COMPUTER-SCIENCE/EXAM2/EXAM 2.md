#### Practice exam
- [x] type conversion
	- [x] explicit
	- [x] implicit
- [x]  command line input
- [ ] translate psuedocode to java
- [x] `break` statement
- [ ] scope of variable declaration
- [ ] array declaration
- [x] array compile time errors
- [x] array runtimerrors
- [x] `arrayIndexOutOfBoundsErrors`
- [ ] array output
- [ ] array indices at 0
- [ ] 

#### Topics
- [ ] **1.5** terminating input
- [ ] **1.2** type conversion
- [ ] command line input
- [ ] translate psuedocode to java
- [ ] **1.4** creating an array
	- [ ] array declaration
	- [ ] array initialization
	- [ ] `new` keyword
	- [ ] arrays size
- [ ] **1.4** array initialization
	- [ ] default initialization
		- [ ] default values
	- [ ] initialize with list
	- [ ] `Arrays.fill()`
- [ ] How arrays are analogous to system memory
- [ ] How are arrays stored in memory
	- [ ] indices start at 0
	- [ ] given the index `i` finding value of `a[i]` is very efficient $\mathcal{O}(1)$
	- [ ] assigning new identifier to an array does not copy array, only adds a reference
- [ ] array storage of **primitive** vs **non-primitive** types in memory
	- [ ] contiguous values vs contiguous references
- [ ] **1.4** [[array bounds]]
	![[5.1eQ identify whether element access is within array boundary.png]]
- [ ] **1.4** Array errors
	- [ ] [[array index out of bounds]]
		- [ ] `ArrayIndexOutOfBoundsExceptions`
	- [ ] [[uninitialized array]]
	- [ ] [[undeclared array variable]]
	- [ ] Identify run-time vs compile-time
- [ ] **1.4** array manipulation (1D 2D)
	- [ ]  [[array copy]]
		- [ ] can't just assign array to new identifier
	- [ ] comparing [[array equality]]
		- [ ] needs to be compared on an element level
		- [ ] checking array directly is only checking if both identifiers refer to same memory address
	- [ ] [[traverse array]] and [[print array elements]] 
		- [ ] in order
		- [ ] reverse order
	![[51gQ traverse array.png]]
- [ ] [[reverse array elements]]
		- [ ] temp variable
	![[5.1gQ reverse array elements.png]]
	![[Pasted image 20221109184112.png]]
	- [ ] find [[array min]] and [[array max]] elements
		- [ ] report index
![[Pasted image 20221109180339.png]]
![[Pasted image 20221109180413.png]]
- [ ] calculate [[array average]]
- [ ] **exchange** values of elements in array
- [ ]  **shift** elements to right or left
![[Pasted image 20221109180717.png]]
![[Pasted image 20221109180743.png]]
- [ ] [[manipulate array]]
![[Pasted image 20221109184220.png]]
- [ ] **count** elements
- [ ] **conditionally remove** elements
- [ ] **dedup** elements in array
- [ ] [[shuffle array]]
	- [ ] [[deck shuffling]]
	- [ ] [[shuffle and random selection from an array]]
![[Pasted image 20221109184335.png]]

- [ ] **sample** from array
- [ ] [[command line arguments in array]]
- [ ] [[create array with N random values]]
- [ ] [[for each loops]] with arrays
![[Pasted image 20221109181056.png]]
	- [ ] 1d array
	- [ ] 2d array
	- [ ] when can't `for each1 be used?
- [ ] [[ragged array]]
- [ ] [[two dimensional array]]
- [ ] [[array representation of a deck of cards]]
![[Pasted image 20221109181820.png]]
![[Pasted image 20221109181908.png]]
![[Pasted image 20221109181928.png]]
![[Pasted image 20221109182001.png]]
![[Pasted image 20221109182142.png]]

**2D array deck**
![[Pasted image 20221109185316.png]]
![[Pasted image 20221109185341.png]]

[[shuffle array]] [[deck shuffling]] [[shuffle and random selection from an array]]
![[Pasted image 20221110070134.png]]
![[Pasted image 20221109184526.png]]

[[sampling from an array]] 

2Da
## 1.4 Arrays
- compile vs runtime errors
	- `arrayIndexOutOfBounds`
- declaring an array
- 2D Arrays

## Learning Objectives
#### 5.1a Declare, create, and initialize one-dimensional(1D) and two-dimensional (2D) arrays.

##### Lecture Videos

##### Slides
- [[data structure]] arrangement ebavke efficient processing by a program
- [[array]]s 
	- **Purpose:** storage and manifpulation of Data
	- *indexed* sequence of values
	- values are same [[data-type]]
![[LO 5.1A declare create initialize arrays.png]]
	- arrays means we don't need to create individual variables each time we store value
		- necessity when arbitrarily large amount of data of same type needs to be stored
	- **declaration** `<data type> [] arrayName;`
	- length of array needs to specified `arrayName = new <data type>[arraySize]`
		- `new` keyword

##### Book

##### Book Website

> **Array Creation**
> Making an array in a Java program involves three distinct steps:
	-   Declare the array name.
	-   Create the array.
	-   Initialize the array values.
```Java
double[] a;                    // declare the array
a = new double[n];             // create the array
for (int i = 0; i < n; i++)    // elements indexed from 0 to n-1
   a[i] = 0.0;                 // initialize all elements to 0.0
```

>  [[zero-based indexing]]_ We always refer to the first element of an array a[] as a[0], the second as a[1], and so forth. It might seem more natural to you to refer to the first element as a[1], the second value as a[2], and so forth, but starting the indexing with 0 has some advantages and has emerged as the convention used in most modern programming languages. ^[ https://introcs.cs.princeton.edu/java/14array/]

>[[array length]] Once we create an array, its length is fixed. You can refer to the length of an a[] in your program with the code `a.length`^[ https://introcs.cs.princeton.edu/java/14array/]

#### Book videos


#### 5.1b Explain Java’s default array initialization. 5.1c Describe and implement initializer lists to initialize arrays.

![[LO 5.1b java default array initialization.png]]

![[5.1b java default array initialization values.png]]
- Java assigns default values upon initialization
	- `boolean[] false`
	- `int[] 0`
	- `double[] 0.0`
	- `char[] '\u0000'`
	- `String[] null`


![[5.1c Initialize array at compile with list.png]]
- [[initialize array with list]] is done at compile time assigning values at compile time
	- constants can **only!** be used as initialization
![[5.1c lists can only be assigned to arrays at initialization.png]]
[[Arrays.fill(array, val)]]
- `java.util.Arrays.fill` can be used to assign array elements same specific value
![[5.1c Arrays.fill().png]]

![[5.1bc arrays in Java language.png]]

##### Book


#### Book videos

##### Book Website


>[[default array initialization]]. For economy in code, we often take advantage of Java's default array initialization convention. For example, the following statement is equivalent to the four lines of code at the top of this page:

```Java
double[] a = new double[n];
```
  [[setting array values at compile time]] alternatively arrays can be initialized with assigned literal values set at compile time
 ```Java
 String[] SUITS = {
    "Clubs", "Diamonds", "Hearts", "Spades"
}; 

String[] RANKS = {
    "2", "3", "4", "5", "6", "7", "8", "9", "10",
    "Jack", "Queen", "King", "Ace"
};
```

#### 5.1d Describe and illustrate memory representation and allocation involving array implementations in Java.
- array structure is analogous to how computer memory works
	- both are *indexed sequences of values of same data type*
	- each **primitive** type stored in fixed number of locations
	- arrays values are stored in **contiguous locations**
 ![[5.1d array memory representation.png]]
- array identifier points to starting address in memory for array, where first element is stored
- primitive types are stored in contiguous memory

![[5.1d memory for array primitive elements.png]]

- non-primitive references are stored in contiguous memory, which point to memory address where actual values are stored, but the reference addresses are not contiguous
![[5.1d array memory addresses for non-primitive data-type.png]]

##### Lecture Videos

##### Slides

##### Book

##### Book Website

> [[array memory representation]] Java represents a two-dimensional array as an array of arrays. A matrix with m rows and n columns is actually an array of length m, each entry of which is an array of length n. In a two-dimensional Java array, we can use the code `a[i]` to refer to the ith row (which is a one-dimensional array). Enables **ragged arrays**.


> [[new keyword]] and [[memory representation]]. When you use `new` to create an array, Java reserves space in memory for it (and initializes the values). This process is called _memory allocation_.

#### Book videos



#### 5.1e Distinguish between valid and invalid array index references in code segments. 5.1f Identify ArrayIndexOutOfBoundsExceptions in program code segments.

##### Lecture Videos

##### Slides


[[array index out of bounds]]
![[Pasted image 20221109093839.png]]
[[uninitialized array]]
![[Pasted image 20221109093850.png]]
[[undeclared array variable]]
![[Pasted image 20221109093911.png]]

[[array bounds]]
- array of size `n` has `n` elements to store data
- element index range from `0` to `n-1`
![[Pasted image 20221109094638.png]]
- if trying to access index element outside range `ArrayIndexOutOfBoundsException` thrown
![[Pasted image 20221109094213.png]]
![[5.1eA identify whether element access is within array boundary.png]]
##### Book

##### Book Website

#### Book videos

#### 5.1g Implement Java code to manipulate 1D arrays including, but not limited to, the following tasks:

- Copy arrays
- Check array equivalence
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

##### Lecture Videos

##### Slides

[[exchange array elements]]
![[Pasted image 20221110070016.png]]

- [[array copy]] need to **copy** arrays by element
	- assigning whole array *only assigns reference*
![[5.1g copying an array.png]]
![[5.1g copy array2.png]]
![[Pasted image 20221109093407.png]]
![[Pasted image 20221109093441.png]]
- [[array equality]] arrays considered are equal if
	- both have same number of elements
	- all elements at correspond indices have same value
- equality needs to be checked at the element level
	- directly comparing array identifiers only evaluates whether references are to same memory address
![[5.1g array equality.png]]

[[array representation of a deck of cards]]
![[Pasted image 20221109181749.png]]
- remember loop structure
- `suit[4]`: clubs, diamons, hearts, spade
- `rank [12`]: 2-10
- deck needs to range from elements 0 - 51
- `deck[i+13*j] = rank[i] = suit[j]
**2D Array Representation**
![[Pasted image 20221109185602.png]]


[[command line arguments in array]]
  ![[Pasted image 20221109093022.png]]

[[create array with N random values]]
![[Pasted image 20221109093125.png]]

[[array average]]
![[Pasted image 20221109093202.png]]

[[print array elements]]
![[Pasted image 20221109093239.png]]
![[Pasted image 20221109093359.png]]
![[Pasted image 20221109093433.png]]
[[array max]]
![[Pasted image 20221109093304.png]]

[[traverse array]]
![[5.1gA traverse array.png]]

![[Pasted image 20221109183438.png]]
[[manipulate array]]
![[Pasted image 20221109183857.png]]

![[Pasted image 20221109183949.png]]

[[reverse array elements]]
![[5.1gA reverse array elements.png]]
![[Pasted image 20221109184017.png]]

[[array min]] [[array max]] and [[return array index]]![[Pasted image 20221109180509.png]]
[[shift array elements]]
![[Pasted image 20221109180558.png]]
##### Book

##### Book Website
#### Book videos

#### 5.1h Demonstrate the use of the enhanced for loop (for-each) when writing code involving arrays.
[[for each loops]]
![[Pasted image 20221109181139.png]]
![[Pasted image 20221109180948.png]]

#### 5.1i Distinguish between situations that can and that cannot utilize an enhanced for loop.

##### slides
- cannot use `for each` if you need to return or use the index reference 
- cannot use `for each` if you need to access array in non-linear order starting from left
![[Pasted image 20221109181226.png]]
#### 5.1j Determine the result of program code that traverses and manipulates the elements in a 2D array.
[[2D array default initialization]]
![[Pasted image 20221110060901.png]]

[[single statement declare create initialize 2D array]]
![[Pasted image 20221110061049.png]]
![[Pasted image 20221110061419.png]]
[[list initialization 2D arrays]]
![[Pasted image 20221110061139.png]]

[[2D array length]]
![[Pasted image 20221110061248.png]]
![[Pasted image 20221110061814.png]]
[[2D arrays are arrays of references to  1D arrays]]
![[Pasted image 20221110061348.png]]
- This means that each element can be a reference to an array of a different length [[ragged arrays]]
![[Pasted image 20221110061644.png]]
![[Pasted image 20221110061737.png]]

[[2D array iteration]]
![[Pasted image 20221110061914.png]]
- **outer loop** loops over rows
- **inner loop** loops over columns

[[row-major order]]
- traverse matrix by row-by-row 
- traverse elements in until all elements of row have been processed
- move to first element in next row
[[row-major sum]]
```java
m = 10
n = 10
int arr[][] matrix = new int[m][n]

//traverse in row major order and retrun row sums
for(int i = 0; i < arr.length; i ++){
	int sum = 0; //for each new row reset sum to 0
	for(int j = 0; j < arr[i].length; i++)
		sum + = arr[i][j]; //sum all elements in row
	
	//when all c's in row are in sum, print and move to next line 
	System.out.prinln(sum);  line

}

```

[[row-major average]]

[[column-major order]]
- traverse matrix column by column
- move from element of same column index number for every row
- once element at that index has been processed for all rows move to next column index 
- repeat until all column indexes have been processed for all rows
[[column-major sum]]
```java
int m = 10;
int n = 10
int arr[][] = new int[m][n];
//traverse matrix in column-major order
for (int j = 0; j < arr[0].length; j++){
	
	int sum = 0; // reset sum for reach new col
	for(int i = 0; arr.length; i++)//loop over r's arr[i:n][j] 
		sum + arr[i][j]; // add element [r=i][c=j] to sum
	
	// when all rows in sum, print and move to next line
	System.out.println(sum);
}
```

[[column-major average]]

[[ragged array row-major order]]
[[ragged array column-major order]]


##### slides

card deck with 2D array
![[Pasted image 20221109185623.png]]

5.1k Trace and implement code to traverse and manipulate 2D arrays in row-major and column-major order.
[[2d Array Traversal]]

[[ragged arrays]]
![[Pasted image 20221109192756.png]]
- use a for loop to traverse a 2D array
- 
## 1.5 Input Output

[[command-line input]]
![[Pasted image 20221110170629.png]]
![[Pasted image 20221110170648.png]]
![[Pasted image 20221110170757.png]]
![[Pasted image 20221110170821.png]]

[[standard input and standard output]]
![[Pasted image 20221110172205.png]]
![[Pasted image 20221110172149.png]]
[[standard input operations]]
![[Pasted image 20221110172355.png]]
![[Pasted image 20221110172313.png]]
![[Pasted image 20221110172440.png]]
![[Pasted image 20221110172422.png]]


[[standard input stream]]
![[Pasted image 20221110172549.png]]
![[Pasted image 20221110172528.png]]
![[Pasted image 20221110172659.png]]
![[Pasted image 20221110172714.png]]
- What is an standard input stream
	- it provides an abstraction for an infinite input sequence
- how does it differ from command line input?
	- arguments can be provided while program is executing
	- no limit to amount of data input
	- type conversion handled explicitly
[[piping]]
![[Pasted image 20221110172828.png]]
- piping allows for infinite input stream form program to program
what is the critical advantage of piping
 ![[Pasted image 20221110172800.png]]

[[file redirection]]
![[Pasted image 20221110173026.png]]
![[Pasted image 20221110172939.png]]
![[Pasted image 20221110172959.png]]

[[standard output]]
![[Pasted image 20221110172058.png]]
[[StdIn library methods]]
![[Pasted image 20221110171930.png]]
![[Pasted image 20221110171946.png]]
![[Pasted image 20221110172000.png]]
https://introcs.cs.princeton.edu/java/stdlib/javadoc/StdIn.html
![[Pasted image 20221110171408.png]]

[[StdOut library methods]]
![[Pasted image 20221110172024.png]]
https://introcs.cs.princeton.edu/java/stdlib/javadoc/StdOut.html
![[Pasted image 20221110171529.png]]

[[StdDraw library methods]]
![[Pasted image 20221110173216.png]]
![[Pasted image 20221110173358.png]]
https://introcs.cs.princeton.edu/java/stdlib/javadoc/StdDraw.html
![[Pasted image 20221110171732.png]]
![[Pasted image 20221110171752.png]]

[[standard draw]]
- now allows output of drawing shapes to screen

![[Pasted image 20221110173312.png]]
![[Pasted image 20221110173245.png]]

![[Pasted image 20221110173545.png]]
![[Pasted image 20221110173517.png]]

![[Pasted image 20221110173713.png]]
![[Pasted image 20221110173610.png]]

![[Pasted image 20221110173740.png]]
![[Pasted image 20221110173805.png]]

![[Pasted image 20221110174102.png]]

- (6.1a) Use command line arguments to provide input values to programs.
- (6.1b) Explain the meaning and functioning of `String args[]` as a parameter to main.
- (6.1c) Explain the need for `Integer.parseInt()` and `Double.parseDouble()` when using command line input.
- (6.1d) Use standard output in programs: 
	- `System.out.print()`, 
	- `System.out println()`
- (6.1e) Use the following methods of `StdIn` in programs to read individual tokens from standard input: 
	- `isEmpty()`, 
	- `readInt()`, 
	- `readDouble()`, 
	- `readBoolean()`, 
	- `readString()`
- (6.1f) Use the following methods of `StdIn` in programs for reading characters from standard input: 
	- `hasNextChar()`, 
	- `readChar()`
- (6.1g) Use the following methods of `StdIn` in programs for reading lines from standard input: 
	- `hasNextLine()`, 
	- `readLine()`, 
	- `readAll()`
- (6.1h) Use the following methods of `StdIn` in programs for reading from standard input to arrays:
	- `readAllInts()`, 
	- `readAllDoubles()`, 
	- `readAllBooleans()`,
	- ` readAllStrings()`, 
	- `readAllLines()`
- (6.1i) Explain and implement an **end-of-file sequence** to end user input.
- (6.1j) Redirect standard output to a file when executing a program.
- (6.k) Redirect from a file to standard input when executing a program.
- (6.1l) Demonstrate piping the output of one program to the input of another
## 2.1 Static Methods & 2.2 Libraries and Clients

##### questions
###### static methods
[[static methods]]
- What are static methods?
	- Java's implementation of a function
	- [[pure functions]] return same out put for different input
	- [[void functions]] can produce side effects
![[Pasted image 20221111163902.png]]
![[Pasted image 20221111163926.png]]

![[Pasted image 20221111164001.png]]
![[Pasted image 20221111164125.png]]

![[Pasted image 20221111164231.png]]
![[Pasted image 20221111164302.png]]

![[Pasted image 20221111164402.png]]
![[Pasted image 20221111164429.png]]

![[Pasted image 20221111164459.png]]
![[Pasted image 20221111164521.png]]

###### methods signature
[[method signature]]
![[Pasted image 20221111162939.png]]
###### method definition
[[method definition]]
![[Pasted image 20221111163057.png]]
![[Pasted image 20221111163040.png]]
###### array parameters
[[array parameters]]
![[Pasted image 20221111163329.png]]
![[Pasted image 20221111163421.png]]

![[Pasted image 20221111163257.png]]

![[Pasted image 20221111163340.png]]

###### array return values
[[array return value]]
implement a method called `create` that returns a `double` array of length `n` where each element value equals the value of it's index
![[Pasted image 20221111163530.png]]

###### function calls
[[function calls]]
![[Pasted image 20221111164633.png]]
![[Pasted image 20221111164708.png]]
Q. In what order are methods executed from the call stack?
A. Last-in-First-out [[LIFO]]

![[Pasted image 20221111164918.png]]
![[Pasted image 20221111165212.png]]
###### modular programming
[[modular programming]]
implement a library of the following methods
![[Pasted image 20221111165440.png]]
![[Pasted image 20221111165806.png]]
##### LO
- (7.1a) Explain the meaning and use of static methods in Java.
- (7.1b) Use pre-existing functions/modules when writing program code.
- (7.1c) Define and use static methods with and without parameters in program code.
- (7.1d) Define and use static methods with and without return values in program code.
- (7.1e) Define and use static methods that include arrays as parameters or return types.
- (7.1f) Explain and illustrate the call stack for a program that includes multiple method calls.
- (7.1g) Trace and write programs that include methods having multiple return statements.
- (7.1h) Write program code that includes calls to Java Library methods. 
- (7.1i) Describe the meaning of each part of a method signature.
- (7.1j) Identify the scope of variables in a program that includes multiple methods.
- (7.1k) Explain the difference between local variables and parameter variables.
- (7.1l) Explain the difference between a method implementation and a method call.
- (7.1m) Trace and write programs involving overloaded methods.
- (7.1n) Identify the scope of a variables in a program with multiple methods and method calls.
- (7.1o) Use debugging tools to step through code in order to identify errors at various stages of program development

## 2.3 Recursion

##### questions
###### recursion
Q. write a method for converting decimal to binary
Hint:
![[Pasted image 20221111170500.png]]
![[Pasted image 20221111170514.png]]

use [[Euclid's algorithm]] to find [[greatest common factor]] of two integers
![[Pasted image 20221111170625.png]]
![[Pasted image 20221111170641.png]]

[[recursion trace]]
![[Pasted image 20221111170951.png]]

![[Pasted image 20221111171018.png]]

[[recursion vs iteration]]
- are there methods that can be created in recursion that cannot be implemented iteratively"

[[recursion pitfalls]]
Q. what is the error with this code
![[Pasted image 20221112130054.png]]
![[Pasted image 20221112130210.png]]
Q. what is the issue with this code 
![[Pasted image 20221112130316.png]]
![[Pasted image 20221112130339.png]]

[[recursive sum]]
Q. implement a method that calculate the sum of an integer array of elements recursively
![[Pasted image 20221112130646.png]]

[[recursive min]]
Q. implement a function that recursively finds the minimum of element in an array specified as follows
![[Pasted image 20221112131052.png]]
![[Pasted image 20221112131113.png]]

[[recursive array search]]
Q. Given an array of ints, compute recursively the number of times that the value 11 appears in the array. We‘ll use the convention of considering only the part of the array that begins at the given index. In this way, a recursive call can pass index+1 to move down the array. The initial call will pass in index as 0.
![[Pasted image 20221112131424.png]]
![[Pasted image 20221112131436.png]]

[[recursive bunny ears]]
**Q.** We have bunnies standing in a line, numbered 1, 2, ... The odd bunnies (1, 3, ..) have the normal 2 ears. The even bunnies (2, 4, ..) we‘ll say have 3 ears, because they each have a raised foot. Recursively return the number of “ears” in the bunny line 1, 2, ... n (without loops or multiplication).
![[Pasted image 20221112131626.png]]
![[Pasted image 20221112131723.png]]

[[towers of hanoi]]
![[Pasted image 20221112131815.png]]
![[Pasted image 20221112131846.png]]
![[Pasted image 20221112131902.png]]
![[Pasted image 20221112131919.png]]
![[Pasted image 20221112132147.png]]

##### LO
- (8.1a) Determine the purpose or output of a recursive method by tracing the program code.
- (8.1b) Compare the readability and efficiency of iterative and recursive solutions to the same problem.
- (8.1c) Identify the **base case** and **general case** for a recursive solution.
- (8.1d) Design and implement a recursive method to solve a problem.
- (8.1e) Explain and illustrate the **call stack** developed in a recursive solution to a problem.
- (8.1f) Check and test a recursive method for correctness.
- (8.1g) Use debugging tools to step through code in order to identify errors at various stages of program development.