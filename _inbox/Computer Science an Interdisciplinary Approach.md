---
aliases: []
---
Added: 202207041539
Name: 
Tags: #book
Topics: 
Author: [[Robert Sedgewick]], [[Kevin Wayne]]
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
#### Terms
- [[primitive data-type]]
- [[built-in data-type]]
- [[primitive data-type]]
- [[String]]
- [[integer data-type]]
	- [[byte]]
	- [[short]]
	- [[int]]
	- [[long]]
- [[floating point data-type]]
	- [[float]]
	- [[double]]
- [[character data-type]]
	- [[char]]
- [[Boolean data-type]]
	- [[boolean]]


#### Questions
- **Q.** Why isn't a String a primitive data-type? [[me]]
- **Q** Can non primitive data-types typically be assigned?
	- might modify [[202207251929-strings aren't primitives in Java but are often treated as if they are|202207251929]]
- **Q.** Why does Java treat Strings similiarly to primitive data-types
#### Propositions
- Strings aren't considered primitive because 
	-  they are composed of primitive data types
	- they are classes with methods
- Therefore Strings are a **composite data-type** aka **derived data-type**
- Strings are as if they are primitive in many respects:
	- Are built-in
	- Have operators
	- Can be declared as literals
- **primitive data-type** are basic set of data-types from which all others are constructed
- Java *data-type* importance- [[202207121924-must always be aware of data typed used in program written in strongly typed language|202207121924]]
	- Is this because it is *strongly typed?* (me)
- **14** in math numbers infinite, but w/ computers operations are only well defined for finite set of values within the data type
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
c = a + b; //assignment statement change value of c to a+b
```
- **Literals** represent the data-type value [[202207121947c-literals are how Java represent data-type value|202207130829]]
- **16: operators** represent operations performed on a data-type [[202207130845-operators are Java representations of operations that can be performed on data-types|202207130845]]
	- **35:** Defined only in context of *data-type*
- **16: identifiers** act as variable name [[202207130853-identifiers are Java representations for variable names|202207130853]]

- **16 variable** stores value that can be changed during the execution of a program [[202207150840-variables store data-type values that can be changed referred by name|202207150840]]
- **16: declaration statement** initializes variables and data-type to be used in program[[202207150859-declaration statements are how variables are allocated space in Java|202207150859]]
	- Why do they have to be declared before? Statically typed? (Me)
- **16: naming convention** [[202207151835-style and naming conventions are crucial for understanding complex codebases and reducing tech debt|202207151835]]
- **16: constant variable** not a truly static as all variables can be changed, but conventional to refer to variables that do not change during program execution, and indicate stylistically with all caps identifier [[202207161124-constant variables don't change during the exectiton of a progam|202207161124]]
- **17: expressions** combinations data-types  (literals and variable) and operations that are evaluated to produce a new value [[202207150901- expressions compute new values by combining entities like formulas in math|202207150901]]
- **17: Operator Precedence** ^[[[202207171358-precedence rules are conventions for the order of operations for the sequence of execution in an expression|202207171358]]]
- **17:** **assignment statement** assigned the value of a variable ^[[[202207161151- assignemnt statement associates variables with values they store|202207161151]]]
	- `=` is for assignment not indication of equality
- **18: inline initialization** variables declaration and assignment can be combined onto a single statement `int a = 1234` [[202207181227- variables can be declared and initialized at same time for efficiency|202207181227]]
- **18: trace table** used to study program behavior and how variables change with each statement over the execution of a program
- **18: type safety** data-type need to be declared for each variable to prevent mismatch errors [[202207181300- declaration of data-type required to guarentee type safety at compile time|202207181300]]
	- need to perform proper operation on proper type of data


#### Characters and Strings
- **19:** `char` represent individual alphanumeric symbols[[202207211714-characters are Java representation of characters|202207211714]]
-**19** **Strings** are sequences of characters [[202207121947a-strings in java represent sequences of characters|202207130731]]
- **19:** strings are built-in but not primitive data-type[[202207251929-strings aren't primitives in Java but are often treated as if they are|202207251929]]
- ==**19-20:** concatenation makes strings powerful type for producing complex program outputs==[[202207251946-string primitive-like treatment critical for complex computing programs|202207251946]]
- **20:** concatenation most frequently used for composing string representations of computation results for printing out put with `System.out.println()`
- **12:45** print automatically converts output to `String` https://cuvids.io/app/video/8/watch
- **21:** Strings are important for output and input in programs for all types of data
	- Result of any computation must be represented as string before being printed
##### Converting numbers to strings for output
- **21:** Java implicitly coerces other data types into strings when used in a String concatenation expression
##### Converting Strings to numbers for input
- **21:** Java provides methods for explicitly converting Strings into primitive data-types 
- **21:** Java programs can be viewed as black boxes that take string inputs for arguments and return String values as output, but with the conversion methods Strings can be the used for computations of other data-types within the black box 
- **29** arguments automatically converted to string
- can be converted to different type and manipulated with different *data-type* computations
- Strings act as a conduit for taking in and transmitting data, that can then be converted so that computations of any data-type type can be performed
- This makes Strings a valuable abstraction for transmitting data for general purpose computations
- **21:** Conversion methods mean classes can be viewed as more than black boxes that intake nd return Strings. Inside the black box the strings can be transformed into any data-type, and thus they can generalize inputs for any computation available to the pc.
- Strings are like shipping containers for data

#### Integers
- **22:** `int is Java representation of Natural numbers
- **22:** ste of values contained within 32 bits (binary digit
	- $-214683648(-2^{31})$ to $214683647(2^{31}-1)$
- **24:** *Two's complement* for negative integers
- **22:** $+,-,/,\star, \%$ are `int`  operators
	- work like normal **arithmetic operator**, except division rounds down
- **23:*** **Overflow** occurs when results truncated due to number being too large for bounds
- **24:** Several types of integer primitives, useful for different representation and memory requriements
| integer data-types | memory |set boundaries|
| ------------------ | ------ |---|
| `long`             | 64-bit |$[(-2^{64}), (2^{64}-1])$ |
| `int`              | 32-bit |$[(-2^{32}), (2^{32}-1])$ |
| `short`            | 16-bit |$[(-2^{16}), (2^{16}-1])$ |
| `byte`             | 8-bit       |$[(-2^{8}), (2^{8}-1])$ |


#### Floating-point numbers
- **24:**`double` common **floating point** data-tyoe
- **24:** **floating point** approximate real numbers (decimal points)
- **24:** **arithmetic operators** $+,-,/,\star$
- **24:** math library methods for floats
- **25:** `infinity`, `NaN`
- **26:** **floating point** multiple types of floats w/ different memory requirements and set boundaries
| floating point data-types | memory | precision|
| ------------------ | ------ |---|
| `double`             | 64-bit |15-17 digits|
| `float`              | 32-bit |6-9 digits|

- How are limits of precision worked around
- How are composition errors from truncation avoided?


#### Booleans
- **26:** `boolean` data type represents logical values with a set of values consisting of only two elements `true` and `false`
-  **26:** **Boolean operators** `&&, ||, !` representing **Boolean operations** `and`, `or`, `not` respectively 
- **26:** truth tables
| a       | b       | a&&b    | a\|\|b  |
| ------- | ------- | ------- | ------- |
| `false` | `false` | `false` | `false` |
| `false` | `true`  | `false` | `true`        |
| `true`  | `false` |      `false`   | `true`        |
| `true`  | `true`  |      `true`   | `true`        |

| a       | !a      |
| ------- | ------- |
| `true`  | `false` |
| `false` | `true`        |

- **27:** operators can be combined with parenthesis to define functions as complex as desired
	- Same function can be expressed in many ways
- **27:** **Booleans** founded in the mathematics of **Boolean algebra** and serve as the theoretical foundation for computer science as well as the physical implementation of computer hardware
- **27:** for practical purposes of program design **Boolean** expressions for conditional execution control flow logic in programs, allowing it to execute different operations for a condition depending on if it is `true` or `false`

#### Comparisons
- **27:** **mixed-type operators** take operands of one data-type and return a different data-type
- **27:** **comparison operators** are most important *mixed-type operator*
	- take other primitive data-type and return `boolean` value
- **29:** Well defined and distinct for each data-type
	- requires all operands in expression to be same data-type 
- **27:** *comparison operators* `==, !=, <, <=, >=`
- **28:** comparisons have lower operator precedence than arithmetic operators but higher precedence than Boolean operators
	- don't need parentheses but may be conducive for clarity
- **29:** Boolean logic combined with comparison operators are critical to much decision making in Java program design from **control flow conditional execution**
-  How are strings compared?

#### Library methods and APIs
- **29:** many additional methods available in libraries
- **29:** can create own libraries to reuse methods you have coded
- **30:** **API** *application programming interface* table summarizing library methods
- **30:** Java *calls/evaluates* method with given argument and *returns* a value
- **32:** `void` in `public static main void` keyword means a **method** has no return value. This means the method is purely intended to produce **side effects** like printing to a screen, but cannot pass a tangible result to memory or for other computation
- **32:** **pure methods** always return the same value for the same input and on't produce any **side-effects**
	- `Math.random()` not pure because it returns different values w/ same input
	- `System.out.print` not pure because it has side-effect of printing to console
- **32:** print methods used exclusively for**side effects**

#### Type conversion
- **32:** In order to get results of different data-types than the original operand, need to perform some type of **type conversion**
- **35:** Paying attention to appropriate type and conversion important to 
	- avoiding unintended errors
	- composing compact code
	- making intention clear for reading and understanding

##### Implicit type conversion
- **33:** Java automatically converts some data types in an expression through **coercion*
- **33:** appropriate when intent is clear and no possible loss of information


- **33:** primitives' data types can be explicitly converted to a different type by **casting**
- **33:** important for expressions where the desired conversion will cause a loss of info (like float to string)
- **33:** **Cast by prepending desired type in parentheses`(int)2.71828` converts to `2`
- **33:** Casting has higher operator precedence than arithmetic, so parentheses need to be used for expressions where **coercion** would occur later on
	- `(int) 11 * 0.25 ` becomes a float since multiplication by a float is automatically promoted
	- explicitly cast the entire expression with parentheses `` `(int)(11 * 0.25)`
- **34:** `loss of precision` error message
##### Explicit type conversion
- **35:** library methods available for explicit type conversion
	- `String` parsing to other types
	- Round `float` to `long`
- Strings need special parsing functions to be converted as they are not primitives, even if they're built in
- **REMEMBER TO PARSE STRINGS**

#### Exercises
==**Review 1.2.35 DRAGON CURVES**==


1.2.3.4 `ThreeSort`
##### My answer
```java
public class ThreeSort {

    public static void main(String[] args){
        int x = Integer.parseInt(args[0]);
        int y = Integer.parseInt(args[1]);
        int z = Integer.parseInt(args[2]);
       int first = Math.min(Math.min(x, y), Math.min(y, z));
       int third = Math.max(Math.max(x, y), Math.max(y, z));
       
       int second = 
	       Math.min(Math.min(Math.max(x, y), Math.max(y, z)), Math.max(x, z));
	       
        System.out.print(first + " " + second + " " + third);

    }

}
```

##### Author answer
Difference: Got too focused on viewing each integer as an element and didn't think it could be removed by value since they were not in an array or hash.
Oversight was that they could be added up and subtraction of min and max would leave the second value remaining in the resulting sum
```java
public class ThreeSort { 
    public static void main(String[] args) { 
        int a = Integer.parseInt(args[0]);
        int b = Integer.parseInt(args[1]);
        int c = Integer.parseInt(args[2]);

        // compute stats
        int min    = Math.min(a, Math.min(b, c));
        int max    = Math.max(a, Math.max(b, c));
        int median = a + b + c - min - max;

        // print stats
        System.out.println(min);
        System.out.println(median);
        System.out.println(max);
    }
}
```

### 1.3 Conditionals and Loops
- **51** programs need more advanced **control flow** to be able to construct more complex programs needing statements executed more than once or non-linear statement sequences
- **51** **conditional statement** permit a program to have branching execution
- **51** **loops** let programs conditionally execute statements unlimited number of times
- **control flow** allows computer to accomplish a wide variety of complex tasks and computations, truly unleashing the power of computers


#### Terms
- [[control flow]]
- [[loops]]
- [[conditional statement]]
- [[if statement]]
- [[template]]
- [[comparison operation]]
- [[statement block]]
- [[flowchart]]
- [[semantics]]
- [[while loop]]
- [[body of the loop]]
- [[accumulation functions]]
- [[for loop]]
- [[compound assignment]]
- [[scope]]
- [[compound statement]]
- [[nesting]]
- [[inner loop]]
- [[outer loop]]
- [[break statement]]
- [[simulation]]
- [[gambler's ruin]]
- [[Monte Carlo simulation]]
- [[continue statement]]
- [[switch statement]]
- [[do-while loop]]
- [[infinite loop]]
#### Propositions
- **control flow** unlocks a computer's true potential **51**
- while statements make large program possible allowing an almost unlimited number of statements to be operated. **pg 54**
- while loops become much more useful when a statement needs to be repeated many times **pg 54**
- while loops allows us to express long computations in short programs **pg54-55**
- as sophistication grows so does complexity making programs more difficult to read and understand **pg 55**
- it is important to know powers of two in computer science **pg 55**
	- $2^{10}$
	- $2^{20} \approx1,000,000,000$ 
- loops permit computer ability to theoretically compute anything that is computable making it **Turing complete** **pg 64**, [[me]] 
- Many applications are extensions or realizations of older mathematical ideas **pg 64**
- loops are necessary as many computations need to be solved by numerical approximations that repeat until a stable point is converged on
``` lisp
(newton)

```

#### Questions
- **Q.** are loops required to be **Turing complete**?[[me]]
- **Q.** what else is required?[[me]]
- **Q.** What are the details of **Newton's Method**, and how does it generalize to functions beyond the square root
	- see also [[Abelson, Sussman 1996. Structure and Interpretation of Computer Programs 2nd edition|Abelseon-Sussman-96]] **pg 21-26**
#### Examples
- **powers of two**
	- ==remember to Parse String==
- **finite sum**
- **square root**
- **number conversion**
- **factoring**



#### If statements

#### While loops

#### For loops

##### For notation

##### Compound assignment notation

##### Scope

#### Nesting

#### Applications

##### Finite sum

##### Computing the square root

##### Number conversion

##### Simulation

##### Factoring

#### Other conditional and loop constructs

##### Break statements

##### Continue statements

##### Switch statements

##### Do-while loops

#### Infinite loops

### 1.5 Input and Output
#### Terms
- [[standard input]]
#### Propositions
- while statements make large program possible allowing an almost unlimited number of statements to be operated. **pg 54**
- while loops become much more useful when a statement needs to be repeated many times **pg 54**
- while loops allows us to express long computations in short programs **pg54-55**
- as sophistication grows so does complexity making programs more difficult to read and understand **pg 55**
- it is important to know powers of two in computer science **pg 55**
	- $2^{10}$
	- $2^{20} \approx1,000,000,000$ 
- 
#### Questions
- **Q.** What does **standard input** allow programs to do beyond **command-line arguments**?
- 
#### Examples


