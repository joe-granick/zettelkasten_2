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
#### Keywords
- [[primitive data-type]]
- [[built-in data-type]]
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
	- [[Boolean]]
- [[dragon curve]]


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
- Java *data-type* importance- [[202207121924a1--must always be aware of data typed used in program written in strongly typed language|202207121924]]
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
- [x] ==**Review 1.2.35 DRAGON CURVES**==
	- Reconsider how path works mathematically
	- How would we modify this to be recursive?


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
- [[infinite loop]]
- [[finite sum]]
- [[harmonic number]]
- [[index variable]]
- [[accumulation variable]]
- [[computational approximation]]
	- [[Taylor series expansion]]
	- [[Newton's method]]
- [[number conversion]]
-  [[simulation]]
	- [[gambler's ruin]]
	- [[Monte Carlo simulation]]
- [[factoring]]
	- [[prime number]]
-  [[break statement]]
- [[continue statement]]
- [[switch statement]]
- [[do-while loop]]
- [[Marsaglia's method]]
- [[fecundity parameter]]
#### Propositions
- **control flow** unlocks a computer's true potential **51**
- computers can't generate truly random numbers, but programs can produce **pseudorandom** numbers that have many properties as random **52**numbers ()
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
- **if statement** allow different actions based for different conditions **(50)**
- evaluates **Boolean expression** and executes code in following **statement block**  $iff$ `true` **(51)**
- `if(<boolean expression>){statement block}` **(50)**
	- braces optional if statement block only one statement

```Java
if (x < 0) x = -x;//single sequence statement block

if (x > y)  //multi sequence statement block w/ braces
{
	int t = x;
	x = y;
	y = t;
}
```
- **else clause** can be added to create a branching statement that executes if the **Boolean expression** evaluates false **(51)**
`if(<boolean expression){ <statements T> }`
`else                   { <statements F> }`
```Java
if (x > y) max = x;
else       max = y;
```

#### While loops
- Many computations are repetitive, requiring multiple executions of the same lines of code
- **while loops** allow continuous execution of a block of code as long as the condition remains true
- structured with a **Boolean expression** and a statement block and executing the statement block (*body of the loop*) like an **if statement**, but where an **if statement** executes only once, the while loop will continue to execute the statement until the **Boolean expression** evaluates `false` **(53)**
	- works like repeated sequence of **if statements**
`while (<boolean expression>){<satetements>}`
- require a condition that changes and will eventually evaluate to false at the correct time, otherwise loop will continue infinitely **(54)**
	- common to use integer value that changes over the course of the execution (rule defined in body of loop) and is evaluated in the **Boolean expression**, which stops execution once it evaluates to `false`
```Java
int power = 1;
while(power <= n/2){
	power = 2*power;
}
```

- By allowing executions to be repeated an arbitrary number of times specified by condition **while loops** open up a world of computation that would be impossible without computers **(56)**

**Accumulation/index pattern**
```Java
public class PowerOfTwo {
    public static void main(String[] args){
        int n = Integer.parseInt(args[0]);
        int power = 1;
        int i = 0;
        while(i <= n){
        System.out.println(i + " " + power);
        power = 2*result;
        i++;
        }
        System.out.println(result);
    }    
}

```
- `PowersOfTwo` uses common loop computational pattern with two variables: **(64)**
	- **index variable** that controls the loop
	- **accumulation variable** that aggregates a computational result over each loop iteration
**Reasoning through while loop (58)**
```Java
public class PowerTwoLessThan {
    public static void main(String[] args){
        int n = Integer.parseInt(args[0]);
        int power = 1;
        while(power <= n/2){
            power = 2*result;
        }
        System.out.println(result);
    }    
}
```
- `power` is always a power of two
- `power` is never greater than `n`
- `power` increase each loop iteration and will eventually exceed stopping condition guaranteeing termination
- After termination `2*power` is greater than or equal to `n` 


#### For loops
- **for loops** are functionally the same as **while loops**, but the extra flexibility provided by the syntax allows for more compact code in some situations **(59)**

##### For notation
- Many **while loops** structured:
	- initialize index variable
	- test continuation condition
	- increment index variable
```Java
<initialize>;
while (<boolean expression>){
	<statements>;
	<increment>;
}

```

- This pattern can be expressed directly with an **for loop**
```Java
for (<initialize>; <boolean expression>; <increment>){
	<statements>;
}
```

##### Compound assignment notation
- Java and many other programming languages have built in shorthand for modifying a variable since it is such a common task **(60)**
- all of the following increment the variable `i` by 1
```Java
i = i+1; // standard assignment
i += 1;// compund assignemnt
i++; // iteration specific
++i; // iteration specific
```

- **compound assignment** like `power *=2` can be used any primitive operator **(60)**

##### Scope
- a variable's **scope** determines which parts of the program can access that variable **(60)**
- Scope typically contains the statements in the same block as the variable after it has been declared **(60)**
- This has different implications with respect to the `<increment>` variable in **for loops** vs **while loops** since in a for loop it is not part of the statement block, it is not available for use in the statement, which may be a reason the use a while loop over a for loop for certain applications **60**

#### Nesting
- `if`, `while`, and `for` statements have same priority as any other type of statements and can be used anywhere a statement is required **62**
- that means additional **control flow** statements can be used in the **statement** block to create **compound statements** **(62)**
- A compound statement of loops can be **nesting** where the **inner loop** iterates through all executions at each iteration of the **outer loop** **(62)**
- **if statements** can be nested by chaining together **if statements** and **else clauses** nesting the statements to test whether one of the designated *mutually exclusive* conditions is true and executing that statement **(64)**
```Java
if (income <           0) rate = 0.00;
else if (income <   8925) rate = 0.10;
else if (income <  36250) rate = 0.15;
else if (income <  87850) rate = 0.23;
else if (income < 183250) rate = 0.28;
else if (income < 398350) rate = 0.33;
else if (income < 400000) rate = 0.35;
else                      rate = 0.396;
```
#### Applications
- loops open full computational capability
- many computational methods utilized and implemented by computers are based on mathematical theories and discoveries going back centuries
##### Finite sum

##### Computing the square root
```Java
public class NewtonsMethodSqrt{
	public static void main(String[] args){
		double c = Double.parseDouble(args[0]);
		double EPSILON = 1e-15;
		double t = c;
		while (Math.abs((t*t)-c) > EPSILON){
			t =  ((c/t) +t)/2.0;
		}
		System.out.println(t);
	}
}


```

##### Number conversion
```Java
public class Binary {
    //pattern here is counting up then unraveling
    //first number will always be 1
    //for ones reduce bhyh the bit
    public static void main(String[] args){
        int n = Integer.parseInt(args[0]);
        int bit = 1;
        int i = 0;
        String code = "";

        while(bit <= n/2){
            i++;
            bit*=2;
            System.out.println("value: "+ bit + " power: " + i);
        } 
        while (bit > 0){
            if (n<bit){     code+="0";}
            else      {code+="1";
                        n = (n - bit);}
            bit = bit/2; //since it's an int 1/2 rounds to 0
                       }       
                       System.out.println(code);
    }        
}
```
###### Generalized number conversion (HW 1.3.21)
```Java
public class Kary {
    public static void main(String[] args){
        int n = Integer.parseInt(args[0]);
        int k = Integer.parseInt(args[1]);
        int bit = 1;
        int i = 0;

        while(bit <= n/k){
            i++;
            bit*=k;
            System.out.println("value: "+ bit + " power: " + i);
        }

        String code = "";
        int multiple = k-1; 
        while (bit > 0){
                while (n < multiple*bit){
                    multiple--;
                    }

            code += multiple;    
            n = n-multiple*bit;
            bit = bit/k;
            multiple = k-1; //since it's an int 1/2 rounds to 0
                       }       
                       System.out.println(code);
    }        
}
```

##### Simulation **69 - 71**
- Common application of computers to solve real world problems is by using them to simulate what will happen in real world in order to make informed decisions **69**
- Questions to consider when building a simulation: **70**
	- Is it an accurate model for the real life event it is simulating?
	- How many trials are needed to get an accurate answer?
	- What are the computational limits of the simulation?
- Simulations used in many applied fields and these questions are important to their models
	- Economics
	- Science
	- Engineering
- Simulation and analysis go hand-in-hand to validate each other
- Simulations can approximate answers that may be too difficult to solve analytically
	- What's the expected take away with an upper limit on bets?
		- Why is this difficult to solve analytically?

##### Factoring

#### Other conditional and loop constructs

##### Break statements

##### Continue statements

##### Switch statements

##### Do-while loops

#### Infinite loops

### Exercises
#### 1.3.5
Write program `RollLoadedDie` that prints result of rolling a loaded die such that probability of getting `1,2,3,4,5` is $\frac{1}{8}$ and getting `6` is $\frac{3}{8}$ **(81)**

```Java
public class RollLoadedDie {
    //rolls die where probability of rolling 1-5 is 1/6 and getting a 6 is 5/6
    public static void main(String[] args){
        double roll = Math.random();
        double prob = (1.0/6.0);
        int dice;

        if(roll <= (1.0 * prob))      dice = 1;
        else if(roll <= (2.0 * prob)) dice = 2;
        else if(roll <= (3.0 * prob)) dice = 3;
        else if(roll <= (4.0 * prob)) dice = 4;
        else if(roll <= (5.0 * prob)) dice = 5;
        else                          dice = 6;
        System.out.print(dice);
    } 
}

```
**Remember:** Print a variable instead of writing separate print statements

#### to-do
- [x] **1.3.5**: *Loaded die* **81**
- [x] **1.3.10**: *Uniform Random Average* **82**
- [x] ==**1.3.19**: *Newton's method* differentiable **83** ==
- [x] **1.3.20**: *Newton's method* for any root **83**
- [x] **1.3.21:** *Binary conversion* any change of base **83**
- [ ] **1.3.23:** *Gambler's ruin* double nested loops **84**
- [x] **1.3.24:** *Gambler's ruin* visualization **84**
- [x] **1.3.25:** *Gambler's ruin* specify probability **84**
- [x] **1.3.26:** *Gambler's ruin* 3 outcomes/expected value **84**
- [x] **1.3.27:** *Factors*  **85**
	- [ ] Write proof of Factors 1.3.9 pg 73
- [ ] **1.3.28** Factors modified efficiency
- [x] **1.3.29:** *Checkerboard*  **85**
- [x] **1.3.30:** *GCD*  **85**
- [x] **1.3.31:** *Relatively prime*  **85**
- [ ] **1.3.32** `PowersOfK` **85** 
- [x] **1.3.33:** *Marsaglia's method*  **85**
- [x] **1.3.34:** *Ramanujan's taxi*  **86**
	- [ ] **Check answer:** https://introcs.cs.princeton.edu/java/13flow/Ramanujan.java.html
- [x] **1.3.35:** *Checksum*  **86**
	- [ ] **Check answer:** https://introcs.cs.princeton.edu/java/13flow/ISBN.java.html
- [x] ==**1.3.36:** *Counting primes*  **86**==
	- *try to find better approach*
	- why can we assume a number is prime if for 3 through j for all `j * j < i` for an odd number j
	- Explanation [[202208111024- Checking primes with square of a factor|202208111024]]
- [x] **1.3.37:** *2D Random Walk*  **86**
- [x] **1.3.38:** *Exponential Taylor expansion*  **87**
	- ==Is there a better way to prevent overflows==
	- [x] Check book solution
		-  This converges to the point where an additional expansion doesn't change it so stop condition arrives when a new term doesn't change existing term
- [ ] **1.3.39:** *Trig function Taylor expansion*  **88**
- [ ] **1.3.40:** *Experimental analysis of `Math.exp()` Taylor expansion*  **88**
- [ ] **1.3.41:** *Pepy's problem*  **88**
- [x] **1.3.42:** *Monte Hall simulation*  **88**

```Java
public class MontyHall {
   public static void main(String[] args){
    int n = Integer.parseInt(args[0]); // number of rounds to play
    int switchY = 0; // increment if switching doors after the door is checked wins
    int switchN = 0; // increment if sticking with original choice wins
    //int checkDoor;

    for(int i = 0; i < n; i++){
        int  door = (int)(3.0*Math.random());
        int choice = (int)(3.0*Math.random());
        if (door == choice) switchN++;
        if (door != choice) switchY++;
        System.out.println("stay: " + switchN + " " + "change: " + switchY);
        /*
        *do{
        *    checkDoor = (int)(3.0*Math.random());
        *   } while(checkDoor == door || checkDoor == choice);
        */
    }
    
    System.out.println("stay: " + ((double)switchN/n) + " " + "change: " + ((double)switchY/n));
   } 
}

```

- [ ] **Check answer:** https://introcs.cs.princeton.edu/java/13flow/MonteHall.java.html
- [x] **implementation:** naive, doesn't simulate check door but this might not make a difference
	- [ ] ==**Idea:** check if you can write a mathematical proof of the above conjecture===
- Is there a deterministic way to do this with combinatorics?
- Is there a way to do this by simulating door change
	- ==**Idea:** hypothetically shouldn't make a difference, but can additional data be gathered from the additional `checkDoor` simulation?==
- can this be done differently with arrays?
- [x] **1.3.43:** *5-number median*  **89**
	- [x] double check assumptions
	- [ ] Check for < 7 comparison **solution** https://stackoverflow.com/questions/480960/how-do-i-calculate-the-median-of-five-in-c
	
> 	 An interesting thread here: http://www.ocf.berkeley.edu/~wwu/cgi-bin/yabb/YaBB.cgi?board=riddles_cs;action=display;num=1061827085
> 	
> 	Quote from thread:
> 	
> 	Put the numbers in an array.
> 	
> 	Use three comparisons and shuffle around the numbers so that a[1] < a[2], a[4] < a[5], and a[1] < a[4].
> 	
> 	If a[3] > a[2], then the problem is fairly easy. If a[2] < a[4], the median value is the smaller of a[3] and a[4]. If not, the median value is the smaller of a[2] and a[5].
> 	
> 	So a[3] < a[2]. If a[3] > a[4], then the solution is the smaller of a[3] and a[5]. Otherwise, the solution is the smaller of a[2] and a[4].
- [ ] **1.3.44:** *3 num sort* **89**
- [x] **1.3.45:** *Chaos* **89**
	- [ ] look into population growth formulations
	- [ ] [[fecundity parameter]]
- [ ] **1.3.46:** *Euler's sum of powers* **89**


### 1.4 Arrays
- **data structures** are abstractions that organize data, and are critical to complex programs **(90)**
- **arrays** are data structures meant to store and manipulate large volumes of data efficiently **(90)**
> [!Related] 
 > *vectors*
 > *matrices* 

- **one-dimensional array** stores sequence of **elements** of same type **(90)**
	- **elements** are the components/ values that are stored within an array
- **indexing** done to reference element in array **(90)**
- For array of n elements each element indexed from 0 - n-1 **(90)**
	- how it works in system memory
- **two-dimensional array** an array of one-dimensional arrays **(90**
	- **two-number** index
- arrays often used to store real-world representations of data that can be organized as the same type, often involving large number of values to be stored **(90)**
> [!Real World dat that can be represented by arrays] 
 > - Exam Scores
 > - Stock Prices
 > - DNA Nucleotides
 > - Characters in a book
 > 

#### Keywords
- [[array]] **90**
	- [[one-dimensional array]]
	- [[two dimensional array]]
	- [[ragged array]] **111**
	- [[multidimensional array]] **111**
- [[vector]]**90**
- [[element]]
- [[indexing]] **90**
- [[dot product]]
- [[zero-based index]]
- [[null]]
- [[memory address]]
- [[pointer]]
- [[memory allocation]]
- [[buffer overflow]]
- [[precomputed value]]
- [[space-time tradeoff]]
- [[coupon collector problem]]
- [[Sieve of Eratosthenes]] **103**
- [[spreadsheet]] **108**
- [[row-major order]] **108**
- [[column-major order]] **108**
-  [[matrix]] **106**
	- [[matrix operations]] **109**
		- [[matrix addition]] **109**
		- [[matrix multiplication]] **109**
			- [[matrix-vector multiplication]] **110**
			- [[vector-matrix multiplication]] **110**
		- [[columnar vector]] **110**

- [[lattice]] **112**
- [[self-avoiding random walk]] **113**
- [[state]] **115** 
- [[binomial distribution]] **125**
	- [[binomial coefficient]] **125**
	- [[Pascal's Triangle]] **125**

### Key sentences
- "Using an expression to index into an array plays a central role and enables a computation that would not otherwise be possible" **100**
	- Coupon collector
	- Sieve of Eratosthenes 

### Arrays in Java
- 3 Steps to make array in Java **(91)**
	1. **Declare** array with data type and *indentfier*
	2. **Create array** specify length*
	3. **Initialize** array by assigning values to each elements
```Java
double[] a;                   // declare array
a = new double[n];            // create array
for(int i = 0; i < n; n++){   // initialize arry
	a[n] = 0.0;
}
```
- declaring array similar to declaring primitive of same type **(91)**
- `new` keyword required to allocate memory upon creation of all *non-primitive*  data-types including **arrays** **(91)**
	- specifies number of elements to free up memory for
- arrays allow a program to define many variables without the need to explicitly name each one **(91)** 
	- complex programs with many variables would be practically impossible to write if each one needed to be designated individually
	- now easy to define even millions of variable
- Variables can be used as **array index** meaning an arbirtrarily large number of variables can be processed using a loop and an *index variable*
``` Java
for (int i = 1; i < n; i++){
	a[i] = 0.0;
}
```
- Each array element can be treated like an individual variable **(91)**
- **Example** arrays as vectors, calculating the **dot product** **(91)**
```Java
double dotProduct = 0.0;
for (int i = 0; i < n; i++;
	 dotProuduct += vectorX[i] * vectorY[i];
```
- Simplicity of calculations like this are what make arrays useful for many applications **(91)**
	- ==How would this look without arrays?==
	- ==What other data structures could be used here?==

##### Examples: Array Processing
###### Create new array with random values
```Java
double[] a = new double[n];
for(int i = 0; i < n; i++){
	a[i] = Math.random();
}
```
###### Print array values one line at a time
```Java
for(int i = 0; i <n; i++){
	System.out.println(a[i]);
}
```

###### Find max array value
```Java
double maxVal = Double.NEGATIVE_INFINITY;
for(int i = 0; i < n; i++){
	if(a[i] > maxVal) maxVal = a[i];
}
```
###### Calculate average of array values
```Java
double sum = 0.0;
for(int i = 0; i <n; i++){
	sum += a[i];

}
double avg = sum/n;
```

###### Reverse array values
```Java
int t;
for (int i, i < n/2; i++){
	t = a[i];
	a[i] = a[(n-1-i)]; // n = a.length()
	a[(n-1-i)] = t;
}
```
###### Copy array to another array
```Java
double b[] = new double[n];
for(int i = 0; i < n; i++){
b[i] = a[i];
}
```

#### Zero-based indexing
- *Array indexes start at 0* in Java similar standard to indexing most objects in most languages **92**
- **off-by-one errors** can occur if the indexing is not understood **92**

#### Array length
- Array length is fixed upon creation **92**
- Arrays need to be explicitly created at run time because Java compiler can't know how much memory to reserve at compile time (since length isn't known until run time) **92**
- Variables vs array memory allocation **92**
- `a.length` can be used to refer to the size of an array
	- last array element is always `a[a.length-1]` **92**

#### Default array initialization
- *default array initialization* can be used to save time declaring, creating, adn initializing an array in one line
- Automatically initialize values of elements
	- Numeric arrays  0
	- Boolean arrays: `false`
	- String arrays `null`
```Java
double[] a = new double a[n];
```
 
 #### Memory representation
- Arrays directly correspond tp system memory for practically any computer **94**
- Memory can be modeled as a giant array **94**
	- sequence of memory location accessed by index
- Array elements are sequences of memory locations accessed by index as well **94**
- Location's index in computer memory is it's **address** **94**
- Arrays store address of first element along with length in another location  **94**
	- address points to referenced memory location, in this capacity it is a **pointer** **94**
- if array is stored in memory location `523 -530`
	- accessing `a[4]` Java would find stored address `523` - index for, accessing memory location `523 + 4 = 527`
- Accessing element of array by index is efficient requiring only two steps:
	1. Adding two integers
	2. Referencing memory location
#### Memory allocation
- **memory allocation** is process whereby Java reserved space in memory to store specified number of elements **92**
	- For arrays done when using `new` to create an arrays 
	- 
- blocks of memory allocated for n sequence starting with the address of first element **94**
#### Bounds checking

#### Setting array values at compile time

#### Setting array values at run time

#### Exchanging two values in an array

#### Shuffling an array

#### Sampling without replacement

#### Precomputed values

#### Simplifying repetitive code

### Coupon collector

### Sieve of Eratosthenes

### Two-dimensional arrays

#### Default initialization

#### Output

#### Memory representation

#### Setting values at compile time

#### Matrix operations

#### Special cases of matrix multiplication

#### Ragged arrays

#### Multidimensional arrays

### Example: self-avoiding random walks

### Summary



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


