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
Class: [[01-198-205 Intro to computer science]]


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

#### Exercises
##### 1.3.5
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
				- [[column vector]] **110**
			- [[vector-matrix multiplication]] **110**
				- [[row vector]] **110**
	- [[ragged array]]
	- [[multi-dimensional array]]
	- [[tensor]]
	- [[n-dimensional space]]
- [[lattice]] **112**
- [[self-avoiding random walk]] **113**
- [[state]] **115** 
- [[Haddamard Matrix]] **123**
- [[binomial distribution]] **125**
	- [[binomial coefficient]] **125**
	- [[Pascal's Triangle]] **125**

#### Key sentences
- "Using an expression to index into an array plays a central role and enables a computation that would not otherwise be possible" **100**
	- Coupon collector
	- Sieve of Eratosthenes 
- 3 Steps Needed to Create an Array **91**
	1.  declaration
	2. creation
	3. initialization

#### Key questions
- What is done at run time
	- arrays **created** explicitly at run-time because compiler won't always know how much space to allocate at compile time 
		- Java allocates primitve variable memory at run-time as well?
		- `new` keyword is used with arrays in run time environment to reserve memory
		- variables do not need `new` keyword with memory specification as it is standard for each data type
- What is done at compile time

#### Arrays in Java
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
- *default array initialization* can be used to save time declaring, creating, and initializing an array in one line
- Automatically initialize values of elements
	- `int`  to `0`
	- `floats` to `0.0`
	- `Boolean` to  `false`
	- `Strings` to `null`
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
- **buffer overflow**
- `ArrayIndexOutOfBoundsException` runtime error
#### Setting array values at compile time
- `new` keyword unnecessary as curly braces with values in declaration implies creation **95**
- makes sense when all array values known beforehand **96**
#### Setting array values at run time
- Typical way to set value as we often want to compute the values to store in the array **96**
- array name w/ indices are used the same way as variable names in an assignment statement

#### Exchanging two values in an array
- Swapping the values of elements is useful for many situations and comes up often **97**
	- Reversing a list
	- Shuffling a deck of cards
	- Sampling without replacement
#### Shuffling an array
- Code to shuffle an array is a nuanced implementation of the swap mechanism**97**

#### Sampling without replacement
- Random sampling common statistical technique in science **97**
- Implemented similiarly to shuffling a deck of cards **97**
#### Precomputed values
- Precomputing values and storing them in an array can save compute time **100
- Important in dynamic programming **memoization** 
- Example of the **space-time tradeoff** one of the reasons it is important to understand how the program operates and what tradeoffs in design choices affect efficiency, or even make a program possible/impossible **100+**
#### Simplifying repetitive code
- Arrays can be used where previously would need many if statements or a switch statement **100**
	- arrays used where conditionals change based on the number of a variable
	- variable can be translated to the array index and the conditional return value can be the element at that index
#### Coupon collector
- implemented for cards, but type of problem of interest in science **101**
- can be used to simulate sequences like genetic sequences to se how like they are to occur at random **101**

#### Q.  Do the implementations work differently?

##### BOOK IMPLEMENTATION
```Java
public class CouponCollector {
   public static void main(String[] args){
      int n = Integer.parseInt(args[0]);
      boolean[] isCollected = new boolean[n];
      int count = 0;
      int distinct = 0;

      for(int i = 0; i < n; i++)
      {
         while(distinct < n){
            int r = (int)(Math.random()*(n);
            count++;
            
            if(!isCollected[r])
            {
               distinct++;
               isCollected[r] = true;
            }
         }
      }
      System.out.println(count + " Trials");
   }
}
```

##### MY IMPLEMENTATON
```Java
public class CouponCollector {
   public static void main(String[] args){

      int n = Integer.parseInt(args[0]);
      boolean[] isCollected = new boolean[n];
      int count = 0;

      for(int i = 0; i < n; i++)
      {
         while(isCollected[i] == false){
            int r = (int)(Math.random()*(n));
            count++;
            isCollected[r] = true;
            
         }
      }
      System.out.println(count + " Trials");
   } 
}
```

#### Sieve of Eratosthenes
- Prime numbers incredibly important in number theory, computation, and cryptography **103**
- $\pi(n)$ number of primes $\le n$ **103** 
- Naive approach, something like the example  `Factors.java` but the number of operations grows  nearly **exponentially** $\mathcal{O}(n \sqrt{n})$        
- **Sieve of Eratosthenes** is an ancient method for counting prime numbers more efficiently **103**
- Cuts down on number of redundant calculations by recording multiplication of numbers less than the square root of the the desired count limit **103**
- This is implemented in Java using an array; cuts down on number of redundant loop operations as numbers eliminated numbers can be stored and looked up immediately to verify they can be skipped as they are already know to not be prime **103**
- Tiem complexity plumets to  $\mathcal{O}(n \log{\log{n}})$        
- SIeves are common technique in number theory 
#### Two-dimensional arrays
- Often useful to organize data into a table of rows and columns where each row represents an obervation/entity and each column s a variable of interest **106**
	- Teachers keeping table of students as rows and tests scores as columns
- Mathematical abstraction for tables is a **matrix** **106**
- **Two-dimensional arrays** can be used to implement matrices in java **106**
- Many of most important applications of matrices and two-dimensional arrays involves storing and processing large volumes of data **106**
	- much like vectors and one-dimensional arrays
- notations `a[i][j]` to reefer to two dimensional array **106**
	- row i
	- columns j
-  `double[][] a = new double[m][m]` declares a new 2d array of type double with $m \text{ rows}  \times n \text{ columns}$ 
	- $m \text{ -by-}n \text{ array}$
- *two-dimensional arrays* naturally represent a *matrix* **111**
	- *matrix* common representation of problems and data in math, science, and engineering
	- *matrices* natural way to store and process data and key component in many applications like spreadsheets
	- *matrices* represented in *Cartesian-coordinates* cab ve used to model real world phenomenon 
#### Default initialization
- default initializations same for corresponding one-dimensional arrays **106**
- masks a lot more code than default for normal array as nested loops are needed **106**
- but any values desired other than default require nested loops **107**
```Java
/* defualt initilization replaces following type of nested loop
*to initializae to any value besides the default (0, 0.0, *false,Null) loopw will be needed*/

double[][] a;
a = new double[m][n];
for (int i = 0; i < m; i++){
	//initialize row i
	for (int j = 0; j < n; j++){
		//initialize row j
		a[i][j] = 0.0;
	}
}
```
- This type of nesting is the model for accessing and modifying individual elements in a 2d Array **107**

#### Output
```Java 
for (int i = 0; i < m; i++){
	for (int j = 0; j < n; j++){
		System.out.print(a[i][j] + " ");
	}
		System.out.println();
}
```

#### Memory representation
- Two-dimensional arrays represented as arrays of array **107**

#### Setting values at compile time
- The way two-dimensional arrays are represented as arrays of arrays also dictates how intiializing at compile time owkrs
```Java
double[][] a = 
	{
		{99.0, 85.0, 98.0, 0.0},
		{99.0, 85.0, 98.0, 0.0},
		{99.0, 85.0, 98.0, 0.0},
		{99.0, 85.0, 98.0, 0.0},
		{99.0, 85.0, 98.0, 0.0},
		{99.0, 85.0, 98.0, 0.0},
		{99.0, 85.0, 98.0, 0.0},
		{99.0, 85.0, 98.0, 0.0},
		{99.0, 85.0, 98.0, 0.0},
		{99.0, 85.0, 98.0, 0.0},
		{99.0, 85.0, 98.0, 0.0}
	};
```

####  Spreadsheets
- Two-dimensional arrays can be used like spreadsheets **108**
- Useful to study to understand **array processing** **108**
	- **row-major order** processing can be used for aggregate calculations by column
	- **column-major order** processing can be used for aggregate rowise calculations
#### Matrix operations
- Many scientific and engineering utilizes Linear Algebra tools for operating on matrices **109**
##### Matrix Addition

#### Matrix multiplication
#### Special cases of matrix multiplication
- Two special cases of matrix multiplication **110**
- Both involve one the matrices being only one dimension, meaning it can be represented as a vector
1. **matrix-vector multiplication**
	- **column vector**
	- column vector can be used to store weights for variables
		- each column of row contains value for the variable for that observation
2. **vector-matrix multiplication**
	- **row vector**
- can be used to succinctly express many matrix calculations **110**
	- *matrix-vector multiplication* can be used to calculate  **row averages**
	- *vector-matrix  multiplication* can be used for **column averages**

#### Ragged arrays
- *two-dimensional arrays* aren't required to have uniform rows **111**
- **ragged arrays** are arrays with rows of unequal length **111**
- more sophisticated array-processing code design required **111**

#### Multidimensional arrays
- arrays can be extended to $n$ dimension using same syntax **111**
- `double[][][] a = new double[][][]` **111**
- **tensors** are matrices generalized to *n-dimensional space*
#### Example: self-avoiding random walks
- **self-avoiding random walks** used to study random walks **112**
- set up movement on grid, goal is to escape the grid stops if surrounded by dead ends **112**
- Can study how % of times automaton gets surrounded by dead-ends vs times escaped as the grid size grows **112**
	- accuracy of approximation increases as the number of trials increased
- can be used for modeling **112**
	- materials growing until no growth possible
	- polymers
	- statistical mechanics
- program shows *example* of **guard** building exit test in `while` loop to prevent illegal operation **112**
	- while loops exit *guards* against out of bounds array access checking whether the automaton escaped the grid as the stopping condition (`x` and `y` checked against the grid boundaries)
- Big enough grid almost certain to get trapped **113**
- *self-avoiding random walks* open problem without mathematical solution **113**
- no succinct mathematical expression for the **escape probability**, **average path length** and most other important parameters **113**

#### Summary
4 elements found in almost every language:
1. Assignments
2. Conditionals
3. Loops
4. Arrays

- Arrays allow for a large increase in the programs **state** **115**
- **state** of program is the information needed to understand what it is doing **115**
- more challenging to track state as the number of variables arrays can store makes tracing very difficult **115**
- exist in almost every language **115**
- used explicitly for many software problems **115**
- used implicitly all the time since computer memory is essentially constructed as arrays **115**
- Natural representation for *matrices* and *vector* which are used to model many problems science, engineering, and mathematics **115**
- provide succinct notation for manipulating large volumes of data in uniform way, making them critical for any application that involves processing large volumes of data **115**
#### to-do
- [ ] **1.** *problem*  **pg**
- [ ] **2** *problem*  **pg**
- [ ] **3.** *problem*  **pg**
- [ ] **4.** *problem*  **pg**
- [ ] **5.** *problem*  **pg**
- [ ] **6.** *problem*  **pg**
- [ ] **7** *problem*  **pg**
- [ ] **8.** *problem*  **pg**
- [ ] **9.** *problem*  **pg**
- [ ] **10.** *problem*  **pg**
- [ ] **11.** *problem*  **pg**
- [x] **1.4.12.** *Discrete Distribution*  **pg*119*
	- ==What is being calculated here?==
	- [ ] test with probability trials
- [x] **1.4.13.** *Copy matrices*  **pg 119**
	- [x] **a.** *Square Matrix*
	- [x] **b.** *Rectangular Matrix*
	- [x] **c.** *Ragged array*
		- this works by creating each subarray individually, with length of corresponding initial nested array 
- [x] **1.4.14.** *Transpose Matrix*  **pg 120**
- [x] **1.4.15.** *Transpose Square Matrix*  **pg 120**
- [x] **==1.4.16.** *RelativelyPrime* use a prime number sieve to determine if cli arguments `i` and `j` are *relatively prime*  (`RelativelyPrimeSieve.java)`**pg 120**==
		- [x] ==Could this be more efficient w/ **ragged array**?==
	 ![[1.4.16-RELATIVELY-PRIME-SIEVE-WORK-PG120.JPG]]![[1.4.16-RELATIVELY-PRIME-SIEVE-WORK-INITIALIZATION-PG120.JPG]]![[1.4.16-RELATIVELY-PRIME-SIEVE-WORK-2-PG120.JPG]]
- [ ] ==POTENTIAL NEW APPORACH TO TRY WITH SIEVE, FACTOR AS THE OUTER LOOPS==
- [x] **17.** *1.4.17*  use weights with **matrix-vector** multiplication to find average grades  **pg 120**
- [ ] **18.** *problem*  **pg**
- [ ] **19.** *problem*  **pg**
- [x] **1.4.20.** *SelfAvoidingWalk* calculate average length of dead end and escape paths  **pg 120**
- [x] **1.4.21.** *SelfAvoidingWalk* calculate average area of smallest *axis-aligned rectangle* enclosing dead end paths  **pg 120**
	- [ ] Check variable scope understanding for `deadEndArea`
- [x] **1.4.22.** *DiceSim*  **pg 121**
	- [ ] ==formalize 3 sig fig approx text== 
- [x] **1.4.23.** *LongestPlateau*  **pg 121**
- [x] **1.4.24.** *Empirical Shuffle*  test accuracy of shuffling by approximating frequencies over n trials  **pg 121**
- [x] **1.4.25.** *BadShuffle*  run the shuffle test where card is not removed from shuffle deck (porbability for (0 , n-1) not (j, n-1) ) **pg 121**
	- [ ] double check against online answer
- [x] **1.4.26.** *MusicShuffle*  create program to estimate likelihood of having at least one sequential pair of songs when shuffling a playlist of length n**pg 121**
	- [ ] ==Analytical solution?==
- [x] **1.4.27.** *Permutations Minima* find average number of left-right minima in random shuffles  **pg 122**
- [x] **1.4.28.** *Inverse Permutation*  **pg 122**
- [ ] **1.4.29.** *Hadamard matrix*   **pg 122**
- [x] **1.4.30.** *Rumors*  estimate likelihood of rumors fully propgating a party with n guests, if each guest spread to one person and any guest that has heard the rumor before will cease to propagate **pg 123**
	- [ ] How does this related to population growth?
	- [ ] ==How would this be affected if 1 person spreads it to multiple people?==
		- [ ] how to account for multiple independent spreaders?
	- [ ] ==Alternatively how long does it take for spread with multiple spreaders?==
- [x] **1.4.31.** *Sieve Comparison*  **pg 123**
- [x] **32.** *MineSweeper*  **pg 123**
- [ ] **33.** *problem*  **pg**
- [x] **1.4.34.** *SelfAvoidingRanomWalk* find what average steps are if grid size unlimited **pg 124**
	- [ ] Try to set stop on program that actually terminates
	- **HYPOTHESIS** as grid size approaches infinity it becomes almost statistically impossible to escape grid and average step count converges toward the dead end average, which should be mostly stable once an adequate grid size is reached
- [x] **1.4.35.** *3D Random Walk*  fin average escape probability with a 3d grid **pg 124**
- [ ] **1.4.36.** *N Random walkers* how many steps on average does it take to fill a grid with n random walkers starting from same point  **pg 124**
- [ ] **37.** *problem*  **pg**
- [x] **38.** *Birthday Paradox* what is the average number of people needed to have a duplicate birthday in a group  **pg 124**
- [x] **1.4.39.** *Coupon Collector*  **pg 124**
	- [ ] why does $n\sum \frac{1}{n}$ equal average number of draws before all combos will be seen?
- [ ] **1.40.** *RiffleShuffle* **pg 125**
- [x] **1.4.41.** *Binomial coefficient*  **pg 125**

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
#### Examples
#### to-do
- [x] **1.5.1** *MaxMin* find maz and min integers in a user input stream **pg 162**
- [ ] **2** *problem*  **pg**
- [x] **1.5.3** *DescriptiveStats*  Take user ploating punt inptu and sample size and calculate mean and sample deviation for input **pg 162**
	- ==Is there a more elegant approach?== 
- [ ] ==**1.5.4** *zScoreFilter* use previously calculated descriptive stats and print out all numbers in sample that are more than 1.5 deviations from mean **pg 162**==
- [x] **1.5.5** *LongestRun* create program that takes integer input and returns the integer with the longest consecutive input stream along with said integer  **pg 162**
- [ ] **6.** *problem*  **pg**
- [ ] **7** *problem*  **pg**
- [ ] ==**1.5.8** *EuclideanMeans* calculate **harmonic mean** and **geometric mean** from floating point input stream **pg 162**==
- [x] **1.5.9** *Dragon* determine what program that takes dragon curve input wilk do when supplied starting point and self referential input   **pg 162 - 163**
	- Adaptation of program **1.2.35 pg 49**
	- ==how would this be rewritten **recursively**==
- [ ] **10.** *problem*  **pg**
- [x] **1.5.11** *WordCount* create program that takes input from a text file and count the number of word strings withing **pg 163**
- [ ] **12.** *problem*  **pg**
- [ ] **13.** *problem*  **pg**
- [ ] **14.** *problem*  **pg**
- [ ] **15.** *problem*  **pg**
- [ ] **1.5.16** *Centroids*  **pg**
- [ ] **17.** *problem*  **pg**
- [ ] **1.5.18** *problem*  **pg 165**
- [ ] **1.5.19** *problem*  **pg 165**
- [ ] **1.5.20** *problem* **pg 165**
- [ ] **1.5.21** *problem*  **pg 165**
- [ ] **22.** *problem*  **pg**
- [ ] **23.** *problem*  **pg**
- [ ] **24.** *problem*  **pg**
- [ ] **1.5.25** *problem*  **pg 166**
- [ ] **26.** *problem*  **pg**
- [ ] **1.5.27** *problem*  **pg 167**
- [ ] **1.5.28** *problem*  **pg 167**
- [ ] **1.529** *problem*  **pg 167**
- [ ] **1.5.30** *problem*  **pg 167**
- [ ] **31.** *problem*  **pg**
- [ ] **32.** *problem*  **pg**
- [ ] **33.** *problem*  **pg**
- [ ] **1.5.34** *problem*  **pg 168**
- [ ] **1.5.35** *problem*  **pg 168**
- [ ] **1.5.36** *problem*  **pg 168**
- [ ] **1.5.37** *problem*  **pg 168**



### 1.6 Case Study: Random Web-Surfer
#### Terms
#### Propositions
#### Questions
#### to-do
- [ ] **1.** *problem*  **pg**
- [ ] **2** *problem*  **pg**
- [ ] **3.** *problem*  **pg**
- [ ] **4.** *problem*  **pg**
- [ ] **5.** *problem*  **pg**
- [ ] **6.** *problem*  **pg**
- [ ] **7** *problem*  **pg**
- [ ] **8.** *problem*  **pg**
- [ ] **9.** *problem*  **pg**
- [ ] **10.** *problem*  **pg**
- [ ] **11.** *problem*  **pg**
- [ ]  **12.** *problem*  **pg**
- [ ] **13.** *problem*  **pg**
- [ ] **14.** *problem*  **pg**
- [ ] **15.** *problem*  **pg**
- [ ] **16.** *problem*  **pg**
- [ ] **17** *problem*  **pg**
- [ ] **18.** *problem*  **pg**
- [ ] **19.** *problem*  **pg**
- [ ] **20.** *problem*  **pg**
- [ ]  **21.** *problem*  **pg**
- [ ] **22** *problem*  **pg**
- [ ] **23.** *problem*  **pg**
- [ ] **24.** *problem*  **pg**
- [ ] **25.** *problem*  **pg**
- [ ] **26.** *problem*  **pg**
- [ ] **27** *problem*  **pg**
- [ ] **28.** *problem*  **pg**
- [ ] **29.** *problem*  **pg**
- [ ] **30.** *problem*  **pg**
- [ ] **31.** *problem*  **pg**
- [ ] **32** *problem*  **pg**
- [ ] **33.** *problem*  **pg**
- [ ] **34.** *problem*  **pg**
- [ ] **35.** *problem*  **pg**
- [ ] **36.** *problem*  **pg**
- [ ] **37** *problem*  **pg**
- [ ] **38.** *problem*  **pg**
- [ ] **39.** *problem*  **pg**
- [ ] **40.** *problem*  **pg**


## Chapter 2: Functions and Modules
### 2.1 Defining functions
#### Learning Objectives
**(7.1a)** Explain the **meaning** and **use** of *static methods* in Java.
**(7.1b)** Use pre-existing functions/modules when writing program code.
**(7.1c)** Define and use **static methods** *with and without **parameters*** in program code.
**(7.1d)** Define and use **static methods** *with and without **return values*** in program code.
**(7.1e)** Define and use **static methods** that include ***arrays** as **parameters** or **return types**.*
**(7.1f)** *Explain and illustrate* the **call stack** for a program that includes multiple method calls.
**(7.1g)** Trace and write programs that include methods having multiple return statements.
**(7.1h)** Write program code that includes calls to Java Library methods. 
**(7.1i)** Describe the meaning of each part of a method signature.
**(7.1j)** Identify the scope of variables in a program that includes multiple methods.
**(7.1k)** Explain the difference between local variables and parameter variables.
**(7.1l)** Explain the difference between a method implementation and a method call.
**(7.1m)** Trace and write programs involving overloaded methods.
**(7.1n)** Identify the scope of a variables in a program with multiple methods and method calls.
**(7.1o)** Use debugging tools to step through code in order to identify errors at various stages of program development.

#### Terms
- [[static method]]
- [[modularity]] **193**
- [[encapsulation]] **205**
#### Propositions
- *whenever you can clearly separate tasks within programs you should do so*
- variable **scope** should be as limited as possible **200**
- **static methods** make debugging easier by limiting variable scope **200**
#### Questions
#### Static methods
- static methods change a program's control flow **193**
- can define separate static methods to separate tasks **193**
- **modularity** whenever you can clearly separate tasks within programs you should do so **193**
##### Control flow
- despite physical placement within a class, java executes `main` method first... always **193**
- from main java can **call** on another static method causing **transfer of control** to the called method **193**
	- this can even be called from other classes
- a variable can be passed from calling method as argument for parameter in called method **194**
- **static methods** work as standalone functions and are not tied to an object 
##### Function-call 

##### Terminology
- **parameter variable** is a placeholder for an input value that will be substituted much like $x$ in a mathematical function **196**
	- **arguments** are the input value for which the function is to be evaluated 
##### Static method definition
- method's **signature** **196**
	- first line of static method
	- provides
		- method name
		- parameter variable names
		- method return type
		- parameter variable type
		- keywords 
			- `public`
			- `static`
			- `return type`
```Java
public static double harmonic(int n)
```
- method **body** follows signature
	- enclosed in curly braces
	- includes statements that implement method's functionality
	- **return statement** transfers control back to point where static methods took over.
		- typically provides a **return value** as well
		- **void** return types methods don't return a value, but often still include a return statement to formalize return of control, or add conditional return of control
			- not necessary though
	- **local variables** declared in body of function are scoped to  function and can only be used within the method in which they are declared
##### Function calls
- method calls are **expressions** that can be used to compose more complex expressions **197**
- **arguments** are also expressions and Java will evaluate the expression before passing it to the method
	- `Math.exp(-x*x/2)/Math.sqrt(2*Math.PI)` are perfectly valid arguments to pass, Java will evaluate the result and pass it to the parameter variable
##### Multiple arguments
- methods can take multiple arguments and can have multiple parameter variables defined
- parameter variables can be of different types
- parameter variables declared in signature and separated by commas
``` Java
public static double hypotenuse(double a, double b)
{
	return Math.sqrt(a*a + b*b);
}
```
##### Multiple methods
- can define as many methods as needed **197**
- methods are independent and can be organized in any order
- **static** methods can call any other **static** methods in the same file or in another library that it has access to (eg `Math` library)
```Java
public static double square(double a)
{
	return a*a;	
}

public static hypotenuse(double a, double b)
{
	return Math.sqrt(square(a) + square(b));
}
```
- static methods can call static methods from other `.java` files as long as it has access
- static methods can use **recursion** and even call themselves

##### Overloading
-  **Static methods** are considered ditinct as long as they have *different signatures* **198**
- this means that even methods with the same name can be treated as distinct methods
```Java
/*
 *OVERLOADING method name, performing same operation for 
 *different data types
 */
public static int abs(int x)
{
	if (x < 0) return -x;
	else       return  x;
}

public static double abs(double x)
{
	if (x < 0.0) return -x;
	else       return  x;
}
```
- **Overloading** is common practice when same name is used for methods with distinct signatures
	- useful when same methods are sufficiently similiar to warrant same name
		- eg Java math library using same name to perform same operation on different data types
			- `Math.max(), Math.min(), Math.abs()` etc.
	- also commonly used to define two versions of same method , but one has a variable argument while the other uses a **default value** for that argument 
##### Multiple return statements
- `return` statements can be placed anywhere they are needed in a method **198**
- control returned to calling program as soon as first return statement is executed
	- only one value returned, even if there are multiple return statements
- some problems naturally expressed with multiple return statements that are typically designed to execute conditionally
```Java
public static boolean isPrime(int n)
{
	if(n < 2) return false;
	for (int i = 2; i <= n/i; i++)
		if (n % i == 0) return false;
	return true;
}
```
##### Single return value
- a method only returns a **single** value to calling program **200**
	- must be of same data type value
- java data types can be returned, containing more info than a primitive return type
	- **arrays** can be used as return values for example

##### Scope
- **scope** of a variable is the parts of the program that can use that variable **200**
- A variable declared is usually scoped local to the code block in which it was declared
	- variables declared within static methods cannot be used by other methods
	- variables declared within nested block, cannot be accessed by containing block
- local scoping lets same variable names be reused by independent code blocks as the name allowing independent variables to share a name provided they don't share a scope
- *principle of good software design is to make a variable's scope as small as possible*
- **static methods limit ease debugging by limiting scope**
##### Side effects
- **pure functions** take arguments and input and return a single value **201**
	- similar to mathematical functions which can take multiple inputs and map them to a single outputs
- pure functions don't produce any **side effects**
- Often useful to have functions that produce side effects like printing and drawing
- `void` functions are designed only for it's side effects
	- can include but don't require a `return` statement as control returned to the caller after last statement executed

#### Implementing mathematical functions
##### Closed form
##### No closed form
#### Using static methods to organize code
- Ability to calculate output values based on an input value is important for organizing complex control flow **205**
- essential to taking advantage of **modularity** in organization of code **205**
- separating distinct task into their own methods allows us to change specific method without have to worry about impact on other methods **205**
- using static methods allows for specific function to be **encapsulated**
#### Passing arguments and returning values
##### Pass by value
- **pass by value** allows parameter variables to be used anywhere within the method the same way as a **local variable** **207**
	- only difference is that a parameter argument is evaluated by java calling the code and initializing it as the return value
- works with value of arguments rather than argument itself
- changing parameter variable within the static method has no effect on calling code
	- doesn't change the input variable outside the method
##### Arrays as arguments
- When an arrays are passed as arguments for functions that need to work on an arbitrary amount of inputs of the same *data-type* **208**
- Array arguments are passed as references, rather that copies **217**

##### Side effects with arrays
- Since arrays are passed as references, a method that takes an array argument causes as **side-effect** when it works on the array, as it works on the original not an array copy
- this is because copying an array would be potentially incredibly memory since arrays can be of arbitrary value **217**
	- Most languages are designed this way, although some like `Matlab` do create an arrays copy
- Passing arrays as arguments is **call by value** wrt the array reference but **call by reference** for the array elements **210**
	- A method doesn't change the arrays itself (memory location, length, and type are same when array created)
	- Method can assign different values to be assigned to the elements of the array
##### Arrays as return values
- methods that modify an array can be `void` as they do not require a return value **210**
	- sorting, shuffling etc,
- other array procedures it may be useful to `return ` and array
	- `tone` functuion samples a sine wave and returns it as a new array
		- this is useful since pure sounds waves can be combined through **superposition** by adding and scaling sound waves allowing arbitrily complex sounds
#### Importance of Functions
- **static methods** give ability to extend java language within a program
- ability to use functions as if they're part of the changes understanding of programs as sequence of statements to **sequence of static methods**
	- programs now have higher level control flow defined by method calls and returns
- can now conceive operations beyond the simple primitives built in
- **Clearly separate tasks within program wherever possible**
- Benefits of modularization with static methods
	- Divide long sequences of statements into independent parts
	- Easy reuse of code w/out copying
	- Able to define and work with higher level concepts (like sound waves)
- Code will be easier to understand, maintain and debug

#### to-do
- [ ] **1.** *problem*  **pg**
- [ ] **2** *problem*  **pg**
- [ ] **3.** *problem*  **pg**
- [ ] **4.** *problem*  **pg**
- [ ] **5.** *problem*  **pg**
- [ ] **6.** *problem*  **pg**
- [ ] **7** *problem*  **pg**
- [ ] **8.** *problem*  **pg**
- [ ] **9.** *problem*  **pg**
- [ ] **10.** *problem*  **pg**
- [ ] **11.** *problem*  **pg**
- [ ]  **12.** *problem*  **pg**
- [ ] **13.** *problem*  **pg**
- [ ] **14.** *problem*  **pg**
- [ ] **15.** *problem*  **pg**
- [ ] **16.** *problem*  **pg**
- [ ] **17** *problem*  **pg**
- [ ] **18.** *problem*  **pg**
- [ ] **19.** *problem*  **pg**
- [ ] **20.** *problem*  **pg**
- [ ]  **21.** *problem*  **pg**
- [ ] **22** *problem*  **pg**
- [ ] **23.** *problem*  **pg**
- [ ] **24.** *problem*  **pg**
- [ ] **25.** *problem*  **pg**
- [ ] **26.** *problem*  **pg**
- [ ] **27** *problem*  **pg**
- [ ] **28.** *problem*  **pg**
- [ ] **29.** *problem*  **pg**
- [ ] **30.** *problem*  **pg**
- [ ] **31.** *problem*  **pg**
- [ ] **32** *problem*  **pg**
- [ ] **33.** *problem*  **pg**
- [ ] **34.** *problem*  **pg**
- [ ] **35.** *problem*  **pg**
- [ ] **36.** *problem*  **pg**
- [ ] **37** *problem*  **pg**
- [ ] **38.** *problem*  **pg**
- [ ] **39.** *problem*  **pg**
- [ ] **40.** *problem*  **pg**

### 2.2 Libraries and Clients (226)
- Ability to reference methods in other programs
	- allows for code reuse
	- allows  **modular programming**programs to be divided and organized into files based on application need
- **modular programming** important level of abstraction
	- allows parts of programs to be developed, compiled, and debugged independent of other parts, allowing us to ignore those parts that haven't been developed yet
	- programs can be developed one piece at a time, with no need to worry about independent components not currently being worked on
- can now progress to understanding of program as **set of classes, each of which is an independent module composed of a set of methods**
- All code can interact as network of methods calling each other, grouped together in classes
- allows management of complexity by decomposing tasks into separate classes that can be iimplemented and tested independently

#### Terms
#### Propositions
#### Questions

#### Using static methods in other programs(227)
- Can access static methods in other program
- call method prepended with class name
- make sure client and library class are accessible to java
- with **modular programming** we define multiple files each a different class composed of multiple methods
	- independently develop and debug methods that can be used at a  later time
	- profoundly changes how we can develop programs
- this allows us to think of programs astools that can be usefule later, meaning every computational problem is improving our computational environment **(229)**
- **every program should** *be written by  dividing computation into sperate parts of manageable size implementing each part as if* **someone will use it later ***(229)***
	- this someone is often **you**
	- this will save a large amount of effort in debugging and rewriting code
##### The public keyword (228)
- `public` identifies methods as being for general use by any other program with access to the file
- other ways to identify methods like `private` and some others
##### Each module is a class (228)
- **module** refers to all code with a file
- each module is a class contained within single file with `.java` extension with matching class and file names
##### The . class file (228)
- compiled `.class` files are the java program translated into machine friendly language
- any method can be run with only `.class`, but won't be able to make any changes if there is a bug without the source code `.java` file
##### Compile when necessary (229)
- Java only what is necessary when compiling a new file (wrt methods called)
- If methods called form other classes, java checks if any changes were made since last time it was compiled.
	- if so java will recompile the file that is being called
- This is helpful, as all classes calling a function will be propagated with new code, meaning any bug fixes will be applied to all dependencies

##### Multiple main methods (229)
- multiple classes can have `main()` methods
- `main()` will be included in most classes to test and debug included methods
####  Libraries (230)
- a **library** is a module whose methods are primarily intended for use by other programs
- **user-defined libraries** are classes that contain sets of *related* methods for use by other programs
- many predefined `Java` libraires exist, but no library contains all methods needed for all computations
- ability to create your own libraries as needed crucial to developing complex programs
##### Clients (230)
- **client** is the program that calls a library method
- when class contains a method that is a client method in another class then the first class is a client of the second class
- example `Sat` is a client of `Guassian`
- a class can have multiple clients
	- all classes that call `Math.random()` and `Math.sqrt()` are clients of the `Math` class
##### APIS (230)
- **API**s define the contract between the client and implementation, with what the method is meant for clearly specified
- *provide to clients the methods they need and no others*
- APIs allow users to understand and use the code, without needing to examine the implementation. This us allows us to limit the contract of what the library will do only to the API specification, not the implementation
##### Implementations 231
- **Implementation** is code that implements the methods in an API
- Every Java program is implementation of some API and no API is of use without an implementation
- goal of implementations is to **honor the terms of the contract**
- separating client code from implementation provides freedom to substitute new and improved implementations, since there be many ways to do so, and optimal may not be clear at the outset
- *provide client programmers the info they need and no more*
- any unnecessary information implicitly extends the contract, which is not desirable
- implementation should not be checked for understanding utilization, only should go off API contract
##### Unit testing (235)
- even if a class is implemented without reference to any particular client it is good practice to include a `main()` method for **unit testing** and debugging methods in the library
- `main()` should minimally
	- exercise all code
	- provide some assurance code is working
	- take command line arguments for further testing
##### Stress testing (236)
- extensively used libraries should be subject to robust **stress testing**
- make sure it doesn't crash if client doesn't follow contract or makes assumptions no covered explicitly in API
- each line of code should be questioned carefully for any conditions that may cause issues or **edge/corner cases**
#### Input and output for arrays (237)
- `StdArrayIO` contains static methods for reading primitivize type arrays from standard input and printing them to standard output 
	- `double[] readDouble1d()`
	- `double[][] readDouble2d`
	- `void print(double([] a)`
	- `void print(double[][] a)`
- `StdArrayIO` notes
	- need to settle on file format
	- print methods are overloaded
- implementing this library with arrays processing methods from section 1.4 prevents us from having to think about the implementation details for basic array processing and printing
#### Modular programming (252)
- library implementations demonstrate value of **modular programming**, instead of writing new program self-contained within own file to address new problem we break up each task into smaller more manageable subtasks, then implement and debug code that addresses each subtask
- *whenever you can clearly separate tasks within a program, you should do so*
- **module** typically refers to code that can be compiled and run independently
- in java each class is a module
- **dependency graph** maps the relationship between modules in a modular program
- advantages of modular program have become **crucial** in modern programming
	- allows us to keep program to a **reasonable size** even in large systems
	- **debugging** contained to small pieces of code
	- code can be **reused** without needing re-implementation
	- **maintaining** and improving code is simpler
##### Reasonable size programs (252)
- no large task is so complex that it cannot be broken down into subtasks
- no hard and fast rule for module size
- tradeoff between having too many small modules or too few inflexible modules
- questions to consider as for **monolithic modules**
	- Are there subtasks that can be and make sense to implement separately?
	- Could some subtask be logically grouped into a separate library?
	- Would it be useful for other clients use code in the future?
- question to consider for **large number of tiny modules**
	- Is there some group of subtasks that should logically belong to the same module?
	- Is each separate module really likely to be useful to other clients?
##### Debugging (253)
- tracing becomes more difficult with more statements and variable interactions
- with modular programming and containing the scope of variable local to the modules dramatically cut down on number of possibilities to consider when debugging
- **contract** between client and implementation, once we're satisfied implementation is meeting contract all of its clients can be debugged under that assumptions

##### Code reuse (253)
- once a library is written we don't need to worry about implementing those methods again, they can just be called from their module
- any module can refer to any public method in any other available module

##### Maintenance and improvement (253)
- modular programming facilitates **continuous improvement**
- improving module improves all of its clients
- several different approaches to a problem may be available
- modular programming allows implementation of each one independently
- also important is if a bug is noticed with modular programming fixing the bug also fixes the bug in the module's clients

#### sharing static methods extends programming model in two ways
1. allows code reuse without having to maintain multiple copies
2. supports message of *whenever you can clearly separate tasks in programs, you should do so* by allowing us to organize programs into files of manageable size that can be independently debugged and compiled






#### to-do
- [ ] **1.** *problem*  **pg**
- [ ] **2** *problem*  **pg**
- [ ] **3.** *problem*  **pg**
- [ ] **4.** *problem*  **pg**
- [ ] **5.** *problem*  **pg**
- [ ] **6.** *problem*  **pg**
- [ ] **7** *problem*  **pg**
- [ ] **8.** *problem*  **pg**
- [ ] **9.** *problem*  **pg**
- [ ] **10.** *problem*  **pg**
- [ ] **11.** *problem*  **pg**
- [ ]  **12.** *problem*  **pg**
- [ ] **13.** *problem*  **pg**
- [ ] **14.** *problem*  **pg**
- [ ] **15.** *problem*  **pg**
- [ ] **16.** *problem*  **pg**
- [ ] **17** *problem*  **pg**
- [ ] **18.** *problem*  **pg**
- [ ] **19.** *problem*  **pg**
- [ ] **20.** *problem*  **pg**
- [ ]  **21.** *problem*  **pg**
- [ ] **22** *problem*  **pg**
- [ ] **23.** *problem*  **pg**
- [ ] **24.** *problem*  **pg**
- [ ] **25.** *problem*  **pg**
- [ ] **26.** *problem*  **pg**
- [ ] **27** *problem*  **pg**
- [ ] **28.** *problem*  **pg**
- [ ] **29.** *problem*  **pg**
- [ ] **30.** *problem*  **pg**
- [ ] **31.** *problem*  **pg**
- [ ] **32** *problem*  **pg**
- [ ] **33.** *problem*  **pg**
- [ ] **34.** *problem*  **pg**
- [ ] **35.** *problem*  **pg**
- [ ] **36.** *problem*  **pg**
- [ ] **37** *problem*  **pg**
- [ ] **38.** *problem*  **pg**
- [ ] **39.** *problem*  **pg**
- [ ] **40.** *problem*  **pg**

### 2.3 Recursion (262)
- **recursions** functions have the ability to call themselves
- recursion can be a useful way to describe the natural world
	- recursive trees
- recursion plays central role in CS
	- provides a simple computational model embracing anything that can be computed with any computer
	- helps organize and analyze programs
	- key to many critical types of applications including
		- combinatorial search
		- tree data structures for information processing
		- **Fast Fourier Transform** for signal processing
- through the proof technique of **mathematical induction** recursion provides straightforward way to build mathematical models that can be used to prove important facts about programs




#### Terms
1. [[recursion]] (262)
2. [[mathematical induction]] (262)
3. [[induction step]] 
4. [[reduction step]]
5. [[recurrence relations]] (272)
6. [[exponential time]] (272)
7. [[H-tree]] (277)
8. [[fractal]] (278)
9. [[fractional Brownian motion]] (278)
10. [[Brownian bridge]] (278)
11. [[midpoint displacement method]] (279)
12. [[Hurst exponent]] (280)
13. [[infinite recursion]] (281)
14. [[call stack]] (281)
15. [[stack overflow]] (281)
16. [[dynamic programming]] 283
17. [[memoization]] (284)
18. [[static variable]] (284)

#### Propositions
#### Questions

#### Your first recursive program (264)
- `factorial` is `hello world` for recursion
- two main components **required** of every recursive function
	1. **base case** comes first and defines the stopping condition for the calls
	2. **reduction step** or **induction step** is the central piece of the recursion, relating the value of a function at one or more arguments to the value at one or more other arguments 
- *sequence of argument values **must converge** to the base case*
- base case is place first with a `return` instead of using an `else` clause as it adds unnecessary complexity to larger programs
	- rest of code dedicated to reduction step
- small recursive functions are useful for calculating finite sums
	- this type of recursion acts like a loop in disguise


#### Mathematical Induction (265)
- recursive programming directly related to **mathematical induction** which is used for many proofs about the **natural numbers**
- proving statement involving integer $n$ for infinitely many values of $n$ with mathematical induction involves 
	1. **base case:** prove true for specific value of values of $n$ typically $1$ or $0$
	2. **induction step:** assume statement is true for all positive integers $< n$, then use to prove it is true for all $n$
- this type of proof showing statement is true for infinitely many values of $n$
	- can start at base case and use proof to establish statement is true for each larger value of $n$ one-by-one
- every time we write a recursive program we need mathematical induction to be convinced it will produce desired effect (266)
- clear line between induction and recursion (266)
- difference in nomenclature (*induction vs reduction*) indicates the different outlook (266)
	- with recursion we are trying to get a computation done by *reducing* it to a smaller problem so use a **reduction step**
	- with *inductive proofs* we are trying to establish truth of statement for larger problems so use an **induction step** (266)
- with recursive programs we don't always write a formal proof, but we are dependent that such a proof exits (266)
- often rely on an **informal proof** like with `factorial`
##### Proof Sum of Positive integers <= n = n(n+1)/2 (266)
$1+ 2 + 3 + ... + (n-1) + n = n(n+1)/2$
it is true for base case $n=1 = 1(1+1)/2$
assume true for all positive integers less than $n$ with $n-1$ in particular
$1+ 2 + 3 + ... + (n-1)= (n-1)(n)/2$
add $n$ to both sides and simplify to get desired equation (*induction step*)
$1+ 2 + 3 + ... + (n-1) + n= \frac{(n^2-n)}{2} +n$
$1+ 2 + 3 + ... + (n-1) + n = \frac{(n^2+n)}{2}$
$1+ 2 + 3 + ... + (2n-1) = \frac{n(n+1)}{2}$
**QED**

##### Euclid's algorithm (268)

##### Towers of Hanoi (269)

#### Function-call trees (269)
- each method call represented as a **tree-node**
- tracing function of recursive program may indicate ways to develop non-recursively like with `Towers of Hanoi`
- **trees** are quintessential recursive object
- trees play essential role as abstract mathematical object in many programs

#### Exponential time (272)
- advantage of using recursion is it often allows us to develop mathematical models to prove important facts about behavior of recursive program (like disc movement patterns in `Towers of Hanoi`) 
	- or the amount of time before it finishes
- this is important to help us avoid writing programs that take an intractably long time to compute
- **recurrence relations** naturally arise in recursice programs. These are used in *discrete mathematics* and can often be used to develop a **closed form expression** for quantity of interest
- `Towers of Hanoi` must satisfy recurrence $T(n) = 2T(n-1) +1 \text{ for } n>1, \text{ with } T(1) = 1$
	- $T(n)$ is the number of disc move needed
	- *base case:* $T(1) = 2^n-1=1$
	- *induction step:* 
- therefore $t(N) = 2^n -1$ for all inputs $n>0$ 
- **exponential growth** can quickly exceed capacity for computer to finish program in reasonable amount of time
*beware of programs that might require exponential time*

##### Gray codes (273)

#### Recursive graphics (276)
- simple recursive schemes can create remarkably intricate image output
- examples like **H-trees** have practical applications
	- H-trees can be used for running cable, planning number of centers in the region, running cable through connecting each home to a center
##### Brownian bridge (278)
- **H-tree** is a a type of **fractal**, a geometric shape that can be divided into parts, each of which is approximately a reduced size copy of the original
- fractals are naturally expressed recrusively
- fractals useful for fields as diverse as art, econ, and scientific analysis
- fractals can be used to build compact models of complex shapes, that otherwise defy description
- **Fractional Brownian motion** is a mathematical model for creating realistic fractal models, often used in
	- computational finance
	- study of phenomena like ocean waves and nerve membranes
- **Brownian bridge**
- **midpoint displacement method**
- **Hurst exponent** controls smoothness of curve

#### Pitfalls of recursion (281)
- pitfalls can be overcome, but need to be careful to recognize
##### Missing base case (281)
- without a base case the program will not terminate resulting in an **infinite recursion**
- infinite recursion differs from infinite loops as the system keeps track of each recursive call in the **call stack**
- this eventually exceeds the system memory resulting in a `StackOverflowError` at *run time*
- can use an informal argument using mathematical induction to make sure recursion has desired effect, this can uncover a missing base case

##### No guarantee of convergence (281)
- recursion design might not reduce meaning base case will not be reached, resulting in an infinite recursion
- can sometimes be difficult to identify, depending on complexity of code

##### Excessive memory requirements (282)
- functions that call themselves excessively may exceed memory and overflow the call stack
##### Excessive recomputation (282)
- use of recursion to simply solve problem must be weighed against understanding if it will take *exponential time
- naive implementation of recursive **Fibonacci** sequence incredibly inefficient as same numbers are being computed repeatedly, growing exponentially with `n`
- **dynamic programming** can be used to prevent recomputation of values already computed

#### Dynamic programming (284)
- Idea of **dynamic programming** is **divide-and-conquer** strategy
	- recursively divide complex problems into smaller subproblems
	- store the answer to each subproblem
	- use stored answers to solve original problem
- for `fibonacci` can store calculations then use them to solve when values need to be computed again


##### Top-down dynamic programming (284)
- **top-down** we store or **cache** result of computations
- next time same computation is needed, stored value can be used 
- in Java we use a `static` variable aka **class variable** or **global variable** declared outside method
- top-down DP also known as **memoization**

##### Bottom-up dynamic programming (285)
- **bottom-up dynamic programming** 
	- compute solutions of all subproblems, starting with simplest
	- gradually build up more complicated subproblems
- to solve this ways subproblems must be *ordered* so each subsequent subproblem, can be solved by combining subproblems earlier in the order
- 
##### Longest common subsequence problem (285)

##### Longest common subsequence recurrence (286)

##### Dynamic programming solution (286)

#### Perspective (289)
- not using recursion miss out on some advantages
	1. compact solutions to complex problems
	2. Recursive solutions embody argument that program works as intended
- recursion illustrates power of carefully articulated abstraction
- essential to understanding and exploiting computation and understanding role of computational models in natural phenomena
- 

#### to-do
- [ ] **1.** *problem*  **pg**
- [ ] **2** *problem*  **pg**
- [ ] **3.** *problem*  **pg**
- [ ] **4.** *problem*  **pg**
- [ ] **5.** *problem*  **pg**
- [ ] **6.** *problem*  **pg**
- [ ] **7** *problem*  **pg**
- [ ] **8.** *problem*  **pg**
- [ ] **9.** *problem*  **pg**
- [ ] **10.** *problem*  **pg**
- [ ] **11.** *problem*  **pg**
- [ ]  **12.** *problem*  **pg**
- [ ] **13.** *problem*  **pg**
- [ ] **14.** *problem*  **pg**
- [ ] **15.** *problem*  **pg**
- [ ] **16.** *problem*  **pg**
- [ ] **17** *problem*  **pg**
- [ ] **18.** *problem*  **pg**
- [ ] **19.** *problem*  **pg**
- [ ] **20.** *problem*  **pg**
- [ ]  **21.** *problem*  **pg**
- [ ] **22** *problem*  **pg**
- [ ] **23.** *problem*  **pg**
- [ ] **24.** *problem*  **pg**
- [ ] **25.** *problem*  **pg**
- [ ] **26.** *problem*  **pg**
- [ ] **27** *problem*  **pg**
- [ ] **28.** *problem*  **pg**
- [ ] **29.** *problem*  **pg**
- [ ] **30.** *problem*  **pg**
- [ ] **31.** *problem*  **pg**
- [ ] **32** *problem*  **pg**
- [ ] **33.** *problem*  **pg**
- [ ] **34.** *problem*  **pg**
- [ ] **35.** *problem*  **pg**
- [ ] **36.** *problem*  **pg**
- [ ] **37** *problem*  **pg**
- [ ] **38.** *problem*  **pg**
- [ ] **39.** *problem*  **pg**
- [ ] **40.** *problem*  **pg**

### 2.4 Case Study: Percolation
#### Terms
#### Propositions
#### Questions
#### to-do
- [ ] **1.** *problem*  **pg**
- [ ] **2** *problem*  **pg**
- [ ] **3.** *problem*  **pg**
- [ ] **4.** *problem*  **pg**
- [ ] **5.** *problem*  **pg**
- [ ] **6.** *problem*  **pg**
- [ ] **7** *problem*  **pg**
- [ ] **8.** *problem*  **pg**
- [ ] **9.** *problem*  **pg**
- [ ] **10.** *problem*  **pg**
- [ ] **11.** *problem*  **pg**
- [ ]  **12.** *problem*  **pg**
- [ ] **13.** *problem*  **pg**
- [ ] **14.** *problem*  **pg**
- [ ] **15.** *problem*  **pg**
- [ ] **16.** *problem*  **pg**
- [ ] **17** *problem*  **pg**
- [ ] **18.** *problem*  **pg**
- [ ] **19.** *problem*  **pg**
- [ ] **20.** *problem*  **pg**
- [ ]  **21.** *problem*  **pg**
- [ ] **22** *problem*  **pg**
- [ ] **23.** *problem*  **pg**
- [ ] **24.** *problem*  **pg**
- [ ] **25.** *problem*  **pg**
- [ ] **26.** *problem*  **pg**
- [ ] **27** *problem*  **pg**
- [ ] **28.** *problem*  **pg**
- [ ] **29.** *problem*  **pg**
- [ ] **30.** *problem*  **pg**
- [ ] **31.** *problem*  **pg**
- [ ] **32** *problem*  **pg**
- [ ] **33.** *problem*  **pg**
- [ ] **34.** *problem*  **pg**
- [ ] **35.** *problem*  **pg**
- [ ] **36.** *problem*  **pg**
- [ ] **37** *problem*  **pg**
- [ ] **38.** *problem*  **pg**
- [ ] **39.** *problem*  **pg**
- [ ] **40.** *problem*  **pg**

## Chapter 3: Object Oriented Programming

### 3.1 Using Data Types
#### Terms
#### Propositions
#### Questions
#### to-do
- [ ] **1.** *problem*  **pg**
- [ ] **2** *problem*  **pg**
- [ ] **3.** *problem*  **pg**
- [ ] **4.** *problem*  **pg**
- [ ] **5.** *problem*  **pg**
- [ ] **6.** *problem*  **pg**
- [ ] **7** *problem*  **pg**
- [ ] **8.** *problem*  **pg**
- [ ] **9.** *problem*  **pg**
- [ ] **10.** *problem*  **pg**
- [ ] **11.** *problem*  **pg**
- [ ]  **12.** *problem*  **pg**
- [ ] **13.** *problem*  **pg**
- [ ] **14.** *problem*  **pg**
- [ ] **15.** *problem*  **pg**
- [ ] **16.** *problem*  **pg**
- [ ] **17** *problem*  **pg**
- [ ] **18.** *problem*  **pg**
- [ ] **19.** *problem*  **pg**
- [ ] **20.** *problem*  **pg**
- [ ]  **21.** *problem*  **pg**
- [ ] **22** *problem*  **pg**
- [ ] **23.** *problem*  **pg**
- [ ] **24.** *problem*  **pg**
- [ ] **25.** *problem*  **pg**
- [ ] **26.** *problem*  **pg**
- [ ] **27** *problem*  **pg**
- [ ] **28.** *problem*  **pg**
- [ ] **29.** *problem*  **pg**
- [ ] **30.** *problem*  **pg**
- [ ] **31.** *problem*  **pg**
- [ ] **32** *problem*  **pg**
- [ ] **33.** *problem*  **pg**
- [ ] **34.** *problem*  **pg**
- [ ] **35.** *problem*  **pg**
- [ ] **36.** *problem*  **pg**
- [ ] **37** *problem*  **pg**
- [ ] **38.** *problem*  **pg**
- [ ] **39.** *problem*  **pg**
- [ ] **40.** *problem*  **pg**

### 3.2 Creating Data Types
#### Terms
#### Propositions
#### Questions
#### to-do
- [ ] **1.** *problem*  **pg**
- [ ] **2** *problem*  **pg**
- [ ] **3.** *problem*  **pg**
- [ ] **4.** *problem*  **pg**
- [ ] **5.** *problem*  **pg**
- [ ] **6.** *problem*  **pg**
- [ ] **7** *problem*  **pg**
- [ ] **8.** *problem*  **pg**
- [ ] **9.** *problem*  **pg**
- [ ] **10.** *problem*  **pg**
- [ ] **11.** *problem*  **pg**
- [ ]  **12.** *problem*  **pg**
- [ ] **13.** *problem*  **pg**
- [ ] **14.** *problem*  **pg**
- [ ] **15.** *problem*  **pg**
- [ ] **16.** *problem*  **pg**
- [ ] **17** *problem*  **pg**
- [ ] **18.** *problem*  **pg**
- [ ] **19.** *problem*  **pg**
- [ ] **20.** *problem*  **pg**
- [ ]  **21.** *problem*  **pg**
- [ ] **22** *problem*  **pg**
- [ ] **23.** *problem*  **pg**
- [ ] **24.** *problem*  **pg**
- [ ] **25.** *problem*  **pg**
- [ ] **26.** *problem*  **pg**
- [ ] **27** *problem*  **pg**
- [ ] **28.** *problem*  **pg**
- [ ] **29.** *problem*  **pg**
- [ ] **30.** *problem*  **pg**
- [ ] **31.** *problem*  **pg**
- [ ] **32** *problem*  **pg**
- [ ] **33.** *problem*  **pg**
- [ ] **34.** *problem*  **pg**
- [ ] **35.** *problem*  **pg**
- [ ] **36.** *problem*  **pg**
- [ ] **37** *problem*  **pg**
- [ ] **38.** *problem*  **pg**
- [ ] **39.** *problem*  **pg**
- [ ] **40.** *problem*  **pg**

### 3.3 Designing Data Types
#### Terms
#### Propositions
#### Questions
#### to-do
- [ ] **1.** *problem*  **pg**
- [ ] **2** *problem*  **pg**
- [ ] **3.** *problem*  **pg**
- [ ] **4.** *problem*  **pg**
- [ ] **5.** *problem*  **pg**
- [ ] **6.** *problem*  **pg**
- [ ] **7** *problem*  **pg**
- [ ] **8.** *problem*  **pg**
- [ ] **9.** *problem*  **pg**
- [ ] **10.** *problem*  **pg**
- [ ] **11.** *problem*  **pg**
- [ ]  **12.** *problem*  **pg**
- [ ] **13.** *problem*  **pg**
- [ ] **14.** *problem*  **pg**
- [ ] **15.** *problem*  **pg**
- [ ] **16.** *problem*  **pg**
- [ ] **17** *problem*  **pg**
- [ ] **18.** *problem*  **pg**
- [ ] **19.** *problem*  **pg**
- [ ] **20.** *problem*  **pg**
- [ ]  **21.** *problem*  **pg**
- [ ] **22** *problem*  **pg**
- [ ] **23.** *problem*  **pg**
- [ ] **24.** *problem*  **pg**
- [ ] **25.** *problem*  **pg**
- [ ] **26.** *problem*  **pg**
- [ ] **27** *problem*  **pg**
- [ ] **28.** *problem*  **pg**
- [ ] **29.** *problem*  **pg**
- [ ] **30.** *problem*  **pg**
- [ ] **31.** *problem*  **pg**
- [ ] **32** *problem*  **pg**
- [ ] **33.** *problem*  **pg**
- [ ] **34.** *problem*  **pg**
- [ ] **35.** *problem*  **pg**
- [ ] **36.** *problem*  **pg**
- [ ] **37** *problem*  **pg**
- [ ] **38.** *problem*  **pg**
- [ ] **39.** *problem*  **pg**
- [ ] **40.** *problem*  **pg**

### 3.4 Case Study: N-Body Simulation
#### Terms
#### Propositions
#### Questions
#### to-do
- [ ] **1.** *problem*  **pg**
- [ ] **2** *problem*  **pg**
- [ ] **3.** *problem*  **pg**
- [ ] **4.** *problem*  **pg**
- [ ] **5.** *problem*  **pg**
- [ ] **6.** *problem*  **pg**
- [ ] **7** *problem*  **pg**
- [ ] **8.** *problem*  **pg**
- [ ] **9.** *problem*  **pg**
- [ ] **10.** *problem*  **pg**
- [ ] **11.** *problem*  **pg**
- [ ]  **12.** *problem*  **pg**
- [ ] **13.** *problem*  **pg**
- [ ] **14.** *problem*  **pg**
- [ ] **15.** *problem*  **pg**
- [ ] **16.** *problem*  **pg**
- [ ] **17** *problem*  **pg**
- [ ] **18.** *problem*  **pg**
- [ ] **19.** *problem*  **pg**
- [ ] **20.** *problem*  **pg**
- [ ]  **21.** *problem*  **pg**
- [ ] **22** *problem*  **pg**
- [ ] **23.** *problem*  **pg**
- [ ] **24.** *problem*  **pg**
- [ ] **25.** *problem*  **pg**
- [ ] **26.** *problem*  **pg**
- [ ] **27** *problem*  **pg**
- [ ] **28.** *problem*  **pg**
- [ ] **29.** *problem*  **pg**
- [ ] **30.** *problem*  **pg**
- [ ] **31.** *problem*  **pg**
- [ ] **32** *problem*  **pg**
- [ ] **33.** *problem*  **pg**
- [ ] **34.** *problem*  **pg**
- [ ] **35.** *problem*  **pg**
- [ ] **36.** *problem*  **pg**
- [ ] **37** *problem*  **pg**
- [ ] **38.** *problem*  **pg**
- [ ] **39.** *problem*  **pg**
- [ ] **40.** *problem*  **pg**

## Chapter 4: Algorithms and Data Structures

### 4.1 Performance
#### Terms
#### Propositions
#### Questions
#### to-do
- [ ] **1.** *problem*  **pg**
- [ ] **2** *problem*  **pg**
- [ ] **3.** *problem*  **pg**
- [ ] **4.** *problem*  **pg**
- [ ] **5.** *problem*  **pg**
- [ ] **6.** *problem*  **pg**
- [ ] **7** *problem*  **pg**
- [ ] **8.** *problem*  **pg**
- [ ] **9.** *problem*  **pg**
- [ ] **10.** *problem*  **pg**
- [ ] **11.** *problem*  **pg**
- [ ]  **12.** *problem*  **pg**
- [ ] **13.** *problem*  **pg**
- [ ] **14.** *problem*  **pg**
- [ ] **15.** *problem*  **pg**
- [ ] **16.** *problem*  **pg**
- [ ] **17** *problem*  **pg**
- [ ] **18.** *problem*  **pg**
- [ ] **19.** *problem*  **pg**
- [ ] **20.** *problem*  **pg**
- [ ]  **21.** *problem*  **pg**
- [ ] **22** *problem*  **pg**
- [ ] **23.** *problem*  **pg**
- [ ] **24.** *problem*  **pg**
- [ ] **25.** *problem*  **pg**
- [ ] **26.** *problem*  **pg**
- [ ] **27** *problem*  **pg**
- [ ] **28.** *problem*  **pg**
- [ ] **29.** *problem*  **pg**
- [ ] **30.** *problem*  **pg**
- [ ] **31.** *problem*  **pg**
- [ ] **32** *problem*  **pg**
- [ ] **33.** *problem*  **pg**
- [ ] **34.** *problem*  **pg**
- [ ] **35.** *problem*  **pg**
- [ ] **36.** *problem*  **pg**
- [ ] **37** *problem*  **pg**
- [ ] **38.** *problem*  **pg**
- [ ] **39.** *problem*  **pg**
- [ ] **40.** *problem*  **pg**

### 4.2 Sorting and Searching
#### Terms
#### Propositions
#### Questions
#### to-do
- [ ] **1.** *problem*  **pg**
- [ ] **2** *problem*  **pg**
- [ ] **3.** *problem*  **pg**
- [ ] **4.** *problem*  **pg**
- [ ] **5.** *problem*  **pg**
- [ ] **6.** *problem*  **pg**
- [ ] **7** *problem*  **pg**
- [ ] **8.** *problem*  **pg**
- [ ] **9.** *problem*  **pg**
- [ ] **10.** *problem*  **pg**
- [ ] **11.** *problem*  **pg**
- [ ]  **12.** *problem*  **pg**
- [ ] **13.** *problem*  **pg**
- [ ] **14.** *problem*  **pg**
- [ ] **15.** *problem*  **pg**
- [ ] **16.** *problem*  **pg**
- [ ] **17** *problem*  **pg**
- [ ] **18.** *problem*  **pg**
- [ ] **19.** *problem*  **pg**
- [ ] **20.** *problem*  **pg**
- [ ]  **21.** *problem*  **pg**
- [ ] **22** *problem*  **pg**
- [ ] **23.** *problem*  **pg**
- [ ] **24.** *problem*  **pg**
- [ ] **25.** *problem*  **pg**
- [ ] **26.** *problem*  **pg**
- [ ] **27** *problem*  **pg**
- [ ] **28.** *problem*  **pg**
- [ ] **29.** *problem*  **pg**
- [ ] **30.** *problem*  **pg**
- [ ] **31.** *problem*  **pg**
- [ ] **32** *problem*  **pg**
- [ ] **33.** *problem*  **pg**
- [ ] **34.** *problem*  **pg**
- [ ] **35.** *problem*  **pg**
- [ ] **36.** *problem*  **pg**
- [ ] **37** *problem*  **pg**
- [ ] **38.** *problem*  **pg**
- [ ] **39.** *problem*  **pg**
- [ ] **40.** *problem*  **pg**

### 4.3 Stacks and Queues
#### Terms
#### Propositions
#### Questions
#### to-do
- [ ] **1.** *problem*  **pg**
- [ ] **2** *problem*  **pg**
- [ ] **3.** *problem*  **pg**
- [ ] **4.** *problem*  **pg**
- [ ] **5.** *problem*  **pg**
- [ ] **6.** *problem*  **pg**
- [ ] **7** *problem*  **pg**
- [ ] **8.** *problem*  **pg**
- [ ] **9.** *problem*  **pg**
- [ ] **10.** *problem*  **pg**
- [ ] **11.** *problem*  **pg**
- [ ]  **12.** *problem*  **pg**
- [ ] **13.** *problem*  **pg**
- [ ] **14.** *problem*  **pg**
- [ ] **15.** *problem*  **pg**
- [ ] **16.** *problem*  **pg**
- [ ] **17** *problem*  **pg**
- [ ] **18.** *problem*  **pg**
- [ ] **19.** *problem*  **pg**
- [ ] **20.** *problem*  **pg**
- [ ]  **21.** *problem*  **pg**
- [ ] **22** *problem*  **pg**
- [ ] **23.** *problem*  **pg**
- [ ] **24.** *problem*  **pg**
- [ ] **25.** *problem*  **pg**
- [ ] **26.** *problem*  **pg**
- [ ] **27** *problem*  **pg**
- [ ] **28.** *problem*  **pg**
- [ ] **29.** *problem*  **pg**
- [ ] **30.** *problem*  **pg**
- [ ] **31.** *problem*  **pg**
- [ ] **32** *problem*  **pg**
- [ ] **33.** *problem*  **pg**
- [ ] **34.** *problem*  **pg**
- [ ] **35.** *problem*  **pg**
- [ ] **36.** *problem*  **pg**
- [ ] **37** *problem*  **pg**
- [ ] **38.** *problem*  **pg**
- [ ] **39.** *problem*  **pg**
- [ ] **40.** *problem*  **pg**

### 4.4 Symbol Tables
#### Terms
#### Propositions
#### Questions
#### to-do
- [ ] **1.** *problem*  **pg**
- [ ] **2** *problem*  **pg**
- [ ] **3.** *problem*  **pg**
- [ ] **4.** *problem*  **pg**
- [ ] **5.** *problem*  **pg**
- [ ] **6.** *problem*  **pg**
- [ ] **7** *problem*  **pg**
- [ ] **8.** *problem*  **pg**
- [ ] **9.** *problem*  **pg**
- [ ] **10.** *problem*  **pg**
- [ ] **11.** *problem*  **pg**
- [ ]  **12.** *problem*  **pg**
- [ ] **13.** *problem*  **pg**
- [ ] **14.** *problem*  **pg**
- [ ] **15.** *problem*  **pg**
- [ ] **16.** *problem*  **pg**
- [ ] **17** *problem*  **pg**
- [ ] **18.** *problem*  **pg**
- [ ] **19.** *problem*  **pg**
- [ ] **20.** *problem*  **pg**
- [ ]  **21.** *problem*  **pg**
- [ ] **22** *problem*  **pg**
- [ ] **23.** *problem*  **pg**
- [ ] **24.** *problem*  **pg**
- [ ] **25.** *problem*  **pg**
- [ ] **26.** *problem*  **pg**
- [ ] **27** *problem*  **pg**
- [ ] **28.** *problem*  **pg**
- [ ] **29.** *problem*  **pg**
- [ ] **30.** *problem*  **pg**
- [ ] **31.** *problem*  **pg**
- [ ] **32** *problem*  **pg**
- [ ] **33.** *problem*  **pg**
- [ ] **34.** *problem*  **pg**
- [ ] **35.** *problem*  **pg**
- [ ] **36.** *problem*  **pg**
- [ ] **37** *problem*  **pg**
- [ ] **38.** *problem*  **pg**
- [ ] **39.** *problem*  **pg**
- [ ] **40.** *problem*  **pg**

### 4.5 Case Study: Small World
#### Terms
#### Propositions
#### Questions
#### to-do
- [ ] **1.** *problem*  **pg**
- [ ] **2** *problem*  **pg**
- [ ] **3.** *problem*  **pg**
- [ ] **4.** *problem*  **pg**
- [ ] **5.** *problem*  **pg**
- [ ] **6.** *problem*  **pg**
- [ ] **7** *problem*  **pg**
- [ ] **8.** *problem*  **pg**
- [ ] **9.** *problem*  **pg**
- [ ] **10.** *problem*  **pg**
- [ ] **11.** *problem*  **pg**
- [ ]  **12.** *problem*  **pg**
- [ ] **13.** *problem*  **pg**
- [ ] **14.** *problem*  **pg**
- [ ] **15.** *problem*  **pg**
- [ ] **16.** *problem*  **pg**
- [ ] **17** *problem*  **pg**
- [ ] **18.** *problem*  **pg**
- [ ] **19.** *problem*  **pg**
- [ ] **20.** *problem*  **pg**
- [ ]  **21.** *problem*  **pg**
- [ ] **22** *problem*  **pg**
- [ ] **23.** *problem*  **pg**
- [ ] **24.** *problem*  **pg**
- [ ] **25.** *problem*  **pg**
- [ ] **26.** *problem*  **pg**
- [ ] **27** *problem*  **pg**
- [ ] **28.** *problem*  **pg**
- [ ] **29.** *problem*  **pg**
- [ ] **30.** *problem*  **pg**
- [ ] **31.** *problem*  **pg**
- [ ] **32** *problem*  **pg**
- [ ] **33.** *problem*  **pg**
- [ ] **34.** *problem*  **pg**
- [ ] **35.** *problem*  **pg**
- [ ] **36.** *problem*  **pg**
- [ ] **37** *problem*  **pg**
- [ ] **38.** *problem*  **pg**
- [ ] **39.** *problem*  **pg**
- [ ] **40.** *problem*  **pg**

# Chapter 5: Theory of Computing

## 5.1 Formal Languages
#### Terms
#### Propositions
#### Questions
#### to-do
- [ ] **1.** *problem*  **pg**
- [ ] **2** *problem*  **pg**
- [ ] **3.** *problem*  **pg**
- [ ] **4.** *problem*  **pg**
- [ ] **5.** *problem*  **pg**
- [ ] **6.** *problem*  **pg**
- [ ] **7** *problem*  **pg**
- [ ] **8.** *problem*  **pg**
- [ ] **9.** *problem*  **pg**
- [ ] **10.** *problem*  **pg**
- [ ] **11.** *problem*  **pg**
- [ ]  **12.** *problem*  **pg**
- [ ] **13.** *problem*  **pg**
- [ ] **14.** *problem*  **pg**
- [ ] **15.** *problem*  **pg**
- [ ] **16.** *problem*  **pg**
- [ ] **17** *problem*  **pg**
- [ ] **18.** *problem*  **pg**
- [ ] **19.** *problem*  **pg**
- [ ] **20.** *problem*  **pg**
- [ ]  **21.** *problem*  **pg**
- [ ] **22** *problem*  **pg**
- [ ] **23.** *problem*  **pg**
- [ ] **24.** *problem*  **pg**
- [ ] **25.** *problem*  **pg**
- [ ] **26.** *problem*  **pg**
- [ ] **27** *problem*  **pg**
- [ ] **28.** *problem*  **pg**
- [ ] **29.** *problem*  **pg**
- [ ] **30.** *problem*  **pg**
- [ ] **31.** *problem*  **pg**
- [ ] **32** *problem*  **pg**
- [ ] **33.** *problem*  **pg**
- [ ] **34.** *problem*  **pg**
- [ ] **35.** *problem*  **pg**
- [ ] **36.** *problem*  **pg**
- [ ] **37** *problem*  **pg**
- [ ] **38.** *problem*  **pg**
- [ ] **39.** *problem*  **pg**
- [ ] **40.** *problem*  **pg**

## 5.2 Turing Machines
#### Terms
#### Propositions
#### Questions
#### to-do
- [ ] **1.** *problem*  **pg**
- [ ] **2** *problem*  **pg**
- [ ] **3.** *problem*  **pg**
- [ ] **4.** *problem*  **pg**
- [ ] **5.** *problem*  **pg**
- [ ] **6.** *problem*  **pg**
- [ ] **7** *problem*  **pg**
- [ ] **8.** *problem*  **pg**
- [ ] **9.** *problem*  **pg**
- [ ] **10.** *problem*  **pg**
- [ ] **11.** *problem*  **pg**
- [ ]  **12.** *problem*  **pg**
- [ ] **13.** *problem*  **pg**
- [ ] **14.** *problem*  **pg**
- [ ] **15.** *problem*  **pg**
- [ ] **16.** *problem*  **pg**
- [ ] **17** *problem*  **pg**
- [ ] **18.** *problem*  **pg**
- [ ] **19.** *problem*  **pg**
- [ ] **20.** *problem*  **pg**
- [ ]  **21.** *problem*  **pg**
- [ ] **22** *problem*  **pg**
- [ ] **23.** *problem*  **pg**
- [ ] **24.** *problem*  **pg**
- [ ] **25.** *problem*  **pg**
- [ ] **26.** *problem*  **pg**
- [ ] **27** *problem*  **pg**
- [ ] **28.** *problem*  **pg**
- [ ] **29.** *problem*  **pg**
- [ ] **30.** *problem*  **pg**
- [ ] **31.** *problem*  **pg**
- [ ] **32** *problem*  **pg**
- [ ] **33.** *problem*  **pg**
- [ ] **34.** *problem*  **pg**
- [ ] **35.** *problem*  **pg**
- [ ] **36.** *problem*  **pg**
- [ ] **37** *problem*  **pg**
- [ ] **38.** *problem*  **pg**
- [ ] **39.** *problem*  **pg**
- [ ] **40.** *problem*  **pg**

## 5.3 Universality
#### Terms
#### Propositions
#### Questions
#### to-do
- [ ] **1.** *problem*  **pg**
- [ ] **2** *problem*  **pg**
- [ ] **3.** *problem*  **pg**
- [ ] **4.** *problem*  **pg**
- [ ] **5.** *problem*  **pg**
- [ ] **6.** *problem*  **pg**
- [ ] **7** *problem*  **pg**
- [ ] **8.** *problem*  **pg**
- [ ] **9.** *problem*  **pg**
- [ ] **10.** *problem*  **pg**
- [ ] **11.** *problem*  **pg**
- [ ]  **12.** *problem*  **pg**
- [ ] **13.** *problem*  **pg**
- [ ] **14.** *problem*  **pg**
- [ ] **15.** *problem*  **pg**
- [ ] **16.** *problem*  **pg**
- [ ] **17** *problem*  **pg**
- [ ] **18.** *problem*  **pg**
- [ ] **19.** *problem*  **pg**
- [ ] **20.** *problem*  **pg**
- [ ]  **21.** *problem*  **pg**
- [ ] **22** *problem*  **pg**
- [ ] **23.** *problem*  **pg**
- [ ] **24.** *problem*  **pg**
- [ ] **25.** *problem*  **pg**
- [ ] **26.** *problem*  **pg**
- [ ] **27** *problem*  **pg**
- [ ] **28.** *problem*  **pg**
- [ ] **29.** *problem*  **pg**
- [ ] **30.** *problem*  **pg**
- [ ] **31.** *problem*  **pg**
- [ ] **32** *problem*  **pg**
- [ ] **33.** *problem*  **pg**
- [ ] **34.** *problem*  **pg**
- [ ] **35.** *problem*  **pg**
- [ ] **36.** *problem*  **pg**
- [ ] **37** *problem*  **pg**
- [ ] **38.** *problem*  **pg**
- [ ] **39.** *problem*  **pg**
- [ ] **40.** *problem*  **pg**

## 5.4 Computability
#### Terms
#### Propositions
#### Questions
#### to-do
- [ ] **1.** *problem*  **pg**
- [ ] **2** *problem*  **pg**
- [ ] **3.** *problem*  **pg**
- [ ] **4.** *problem*  **pg**
- [ ] **5.** *problem*  **pg**
- [ ] **6.** *problem*  **pg**
- [ ] **7** *problem*  **pg**
- [ ] **8.** *problem*  **pg**
- [ ] **9.** *problem*  **pg**
- [ ] **10.** *problem*  **pg**
- [ ] **11.** *problem*  **pg**
- [ ]  **12.** *problem*  **pg**
- [ ] **13.** *problem*  **pg**
- [ ] **14.** *problem*  **pg**
- [ ] **15.** *problem*  **pg**
- [ ] **16.** *problem*  **pg**
- [ ] **17** *problem*  **pg**
- [ ] **18.** *problem*  **pg**
- [ ] **19.** *problem*  **pg**
- [ ] **20.** *problem*  **pg**
- [ ]  **21.** *problem*  **pg**
- [ ] **22** *problem*  **pg**
- [ ] **23.** *problem*  **pg**
- [ ] **24.** *problem*  **pg**
- [ ] **25.** *problem*  **pg**
- [ ] **26.** *problem*  **pg**
- [ ] **27** *problem*  **pg**
- [ ] **28.** *problem*  **pg**
- [ ] **29.** *problem*  **pg**
- [ ] **30.** *problem*  **pg**
- [ ] **31.** *problem*  **pg**
- [ ] **32** *problem*  **pg**
- [ ] **33.** *problem*  **pg**
- [ ] **34.** *problem*  **pg**
- [ ] **35.** *problem*  **pg**
- [ ] **36.** *problem*  **pg**
- [ ] **37** *problem*  **pg**
- [ ] **38.** *problem*  **pg**
- [ ] **39.** *problem*  **pg**
- [ ] **40.** *problem*  **pg**

## 5.5 Intractability
#### Terms
#### Propositions
#### Questions
#### to-do
- [ ] **1.** *problem*  **pg**
- [ ] **2** *problem*  **pg**
- [ ] **3.** *problem*  **pg**
- [ ] **4.** *problem*  **pg**
- [ ] **5.** *problem*  **pg**
- [ ] **6.** *problem*  **pg**
- [ ] **7** *problem*  **pg**
- [ ] **8.** *problem*  **pg**
- [ ] **9.** *problem*  **pg**
- [ ] **10.** *problem*  **pg**
- [ ] **11.** *problem*  **pg**
- [ ]  **12.** *problem*  **pg**
- [ ] **13.** *problem*  **pg**
- [ ] **14.** *problem*  **pg**
- [ ] **15.** *problem*  **pg**
- [ ] **16.** *problem*  **pg**
- [ ] **17** *problem*  **pg**
- [ ] **18.** *problem*  **pg**
- [ ] **19.** *problem*  **pg**
- [ ] **20.** *problem*  **pg**
- [ ]  **21.** *problem*  **pg**
- [ ] **22** *problem*  **pg**
- [ ] **23.** *problem*  **pg**
- [ ] **24.** *problem*  **pg**
- [ ] **25.** *problem*  **pg**
- [ ] **26.** *problem*  **pg**
- [ ] **27** *problem*  **pg**
- [ ] **28.** *problem*  **pg**
- [ ] **29.** *problem*  **pg**
- [ ] **30.** *problem*  **pg**
- [ ] **31.** *problem*  **pg**
- [ ] **32** *problem*  **pg**
- [ ] **33.** *problem*  **pg**
- [ ] **34.** *problem*  **pg**
- [ ] **35.** *problem*  **pg**
- [ ] **36.** *problem*  **pg**
- [ ] **37** *problem*  **pg**
- [ ] **38.** *problem*  **pg**
- [ ] **39.** *problem*  **pg**
- [ ] **40.** *problem*  **pg**

# Chapter 6: A Computing Machine

## 6.1 Representing Information
#### Terms
#### Propositions
#### Questions
#### to-do
- [ ] **1.** *problem*  **pg**
- [ ] **2** *problem*  **pg**
- [ ] **3.** *problem*  **pg**
- [ ] **4.** *problem*  **pg**
- [ ] **5.** *problem*  **pg**
- [ ] **6.** *problem*  **pg**
- [ ] **7** *problem*  **pg**
- [ ] **8.** *problem*  **pg**
- [ ] **9.** *problem*  **pg**
- [ ] **10.** *problem*  **pg**
- [ ] **11.** *problem*  **pg**
- [ ]  **12.** *problem*  **pg**
- [ ] **13.** *problem*  **pg**
- [ ] **14.** *problem*  **pg**
- [ ] **15.** *problem*  **pg**
- [ ] **16.** *problem*  **pg**
- [ ] **17** *problem*  **pg**
- [ ] **18.** *problem*  **pg**
- [ ] **19.** *problem*  **pg**
- [ ] **20.** *problem*  **pg**
- [ ]  **21.** *problem*  **pg**
- [ ] **22** *problem*  **pg**
- [ ] **23.** *problem*  **pg**
- [ ] **24.** *problem*  **pg**
- [ ] **25.** *problem*  **pg**
- [ ] **26.** *problem*  **pg**
- [ ] **27** *problem*  **pg**
- [ ] **28.** *problem*  **pg**
- [ ] **29.** *problem*  **pg**
- [ ] **30.** *problem*  **pg**
- [ ] **31.** *problem*  **pg**
- [ ] **32** *problem*  **pg**
- [ ] **33.** *problem*  **pg**
- [ ] **34.** *problem*  **pg**
- [ ] **35.** *problem*  **pg**
- [ ] **36.** *problem*  **pg**
- [ ] **37** *problem*  **pg**
- [ ] **38.** *problem*  **pg**
- [ ] **39.** *problem*  **pg**
- [ ] **40.** *problem*  **pg**

## 6.2 TOY Machine
#### Terms
#### Propositions
#### Questions
#### to-do
- [ ] **1.** *problem*  **pg**
- [ ] **2** *problem*  **pg**
- [ ] **3.** *problem*  **pg**
- [ ] **4.** *problem*  **pg**
- [ ] **5.** *problem*  **pg**
- [ ] **6.** *problem*  **pg**
- [ ] **7** *problem*  **pg**
- [ ] **8.** *problem*  **pg**
- [ ] **9.** *problem*  **pg**
- [ ] **10.** *problem*  **pg**
- [ ] **11.** *problem*  **pg**
- [ ]  **12.** *problem*  **pg**
- [ ] **13.** *problem*  **pg**
- [ ] **14.** *problem*  **pg**
- [ ] **15.** *problem*  **pg**
- [ ] **16.** *problem*  **pg**
- [ ] **17** *problem*  **pg**
- [ ] **18.** *problem*  **pg**
- [ ] **19.** *problem*  **pg**
- [ ] **20.** *problem*  **pg**
- [ ]  **21.** *problem*  **pg**
- [ ] **22** *problem*  **pg**
- [ ] **23.** *problem*  **pg**
- [ ] **24.** *problem*  **pg**
- [ ] **25.** *problem*  **pg**
- [ ] **26.** *problem*  **pg**
- [ ] **27** *problem*  **pg**
- [ ] **28.** *problem*  **pg**
- [ ] **29.** *problem*  **pg**
- [ ] **30.** *problem*  **pg**
- [ ] **31.** *problem*  **pg**
- [ ] **32** *problem*  **pg**
- [ ] **33.** *problem*  **pg**
- [ ] **34.** *problem*  **pg**
- [ ] **35.** *problem*  **pg**
- [ ] **36.** *problem*  **pg**
- [ ] **37** *problem*  **pg**
- [ ] **38.** *problem*  **pg**
- [ ] **39.** *problem*  **pg**
- [ ] **40.** *problem*  **pg**

## 6.3 Machine Language Programming
#### Terms
#### Propositions
#### Questions
#### to-do
- [ ] **1.** *problem*  **pg**
- [ ] **2** *problem*  **pg**
- [ ] **3.** *problem*  **pg**
- [ ] **4.** *problem*  **pg**
- [ ] **5.** *problem*  **pg**
- [ ] **6.** *problem*  **pg**
- [ ] **7** *problem*  **pg**
- [ ] **8.** *problem*  **pg**
- [ ] **9.** *problem*  **pg**
- [ ] **10.** *problem*  **pg**
- [ ] **11.** *problem*  **pg**
- [ ]  **12.** *problem*  **pg**
- [ ] **13.** *problem*  **pg**
- [ ] **14.** *problem*  **pg**
- [ ] **15.** *problem*  **pg**
- [ ] **16.** *problem*  **pg**
- [ ] **17** *problem*  **pg**
- [ ] **18.** *problem*  **pg**
- [ ] **19.** *problem*  **pg**
- [ ] **20.** *problem*  **pg**
- [ ]  **21.** *problem*  **pg**
- [ ] **22** *problem*  **pg**
- [ ] **23.** *problem*  **pg**
- [ ] **24.** *problem*  **pg**
- [ ] **25.** *problem*  **pg**
- [ ] **26.** *problem*  **pg**
- [ ] **27** *problem*  **pg**
- [ ] **28.** *problem*  **pg**
- [ ] **29.** *problem*  **pg**
- [ ] **30.** *problem*  **pg**
- [ ] **31.** *problem*  **pg**
- [ ] **32** *problem*  **pg**
- [ ] **33.** *problem*  **pg**
- [ ] **34.** *problem*  **pg**
- [ ] **35.** *problem*  **pg**
- [ ] **36.** *problem*  **pg**
- [ ] **37** *problem*  **pg**
- [ ] **38.** *problem*  **pg**
- [ ] **39.** *problem*  **pg**
- [ ] **40.** *problem*  **pg**

## 6.4 TOY Virtual Machine
#### Terms
#### Propositions
#### Questions
#### to-do
- [ ] **1.** *problem*  **pg**
- [ ] **2** *problem*  **pg**
- [ ] **3.** *problem*  **pg**
- [ ] **4.** *problem*  **pg**
- [ ] **5.** *problem*  **pg**
- [ ] **6.** *problem*  **pg**
- [ ] **7** *problem*  **pg**
- [ ] **8.** *problem*  **pg**
- [ ] **9.** *problem*  **pg**
- [ ] **10.** *problem*  **pg**
- [ ] **11.** *problem*  **pg**
- [ ]  **12.** *problem*  **pg**
- [ ] **13.** *problem*  **pg**
- [ ] **14.** *problem*  **pg**
- [ ] **15.** *problem*  **pg**
- [ ] **16.** *problem*  **pg**
- [ ] **17** *problem*  **pg**
- [ ] **18.** *problem*  **pg**
- [ ] **19.** *problem*  **pg**
- [ ] **20.** *problem*  **pg**
- [ ]  **21.** *problem*  **pg**
- [ ] **22** *problem*  **pg**
- [ ] **23.** *problem*  **pg**
- [ ] **24.** *problem*  **pg**
- [ ] **25.** *problem*  **pg**
- [ ] **26.** *problem*  **pg**
- [ ] **27** *problem*  **pg**
- [ ] **28.** *problem*  **pg**
- [ ] **29.** *problem*  **pg**
- [ ] **30.** *problem*  **pg**
- [ ] **31.** *problem*  **pg**
- [ ] **32** *problem*  **pg**
- [ ] **33.** *problem*  **pg**
- [ ] **34.** *problem*  **pg**
- [ ] **35.** *problem*  **pg**
- [ ] **36.** *problem*  **pg**
- [ ] **37** *problem*  **pg**
- [ ] **38.** *problem*  **pg**
- [ ] **39.** *problem*  **pg**
- [ ] **40.** *problem*  **pg**

# Chapter 7: Building a Computing Device

## 7.1 Boolean Logic
#### Terms
#### Propositions
#### Questions
#### to-do
- [ ] **1.** *problem*  **pg**
- [ ] **2** *problem*  **pg**
- [ ] **3.** *problem*  **pg**
- [ ] **4.** *problem*  **pg**
- [ ] **5.** *problem*  **pg**
- [ ] **6.** *problem*  **pg**
- [ ] **7** *problem*  **pg**
- [ ] **8.** *problem*  **pg**
- [ ] **9.** *problem*  **pg**
- [ ] **10.** *problem*  **pg**
- [ ] **11.** *problem*  **pg**
- [ ]  **12.** *problem*  **pg**
- [ ] **13.** *problem*  **pg**
- [ ] **14.** *problem*  **pg**
- [ ] **15.** *problem*  **pg**
- [ ] **16.** *problem*  **pg**
- [ ] **17** *problem*  **pg**
- [ ] **18.** *problem*  **pg**
- [ ] **19.** *problem*  **pg**
- [ ] **20.** *problem*  **pg**
- [ ]  **21.** *problem*  **pg**
- [ ] **22** *problem*  **pg**
- [ ] **23.** *problem*  **pg**
- [ ] **24.** *problem*  **pg**
- [ ] **25.** *problem*  **pg**
- [ ] **26.** *problem*  **pg**
- [ ] **27** *problem*  **pg**
- [ ] **28.** *problem*  **pg**
- [ ] **29.** *problem*  **pg**
- [ ] **30.** *problem*  **pg**
- [ ] **31.** *problem*  **pg**
- [ ] **32** *problem*  **pg**
- [ ] **33.** *problem*  **pg**
- [ ] **34.** *problem*  **pg**
- [ ] **35.** *problem*  **pg**
- [ ] **36.** *problem*  **pg**
- [ ] **37** *problem*  **pg**
- [ ] **38.** *problem*  **pg**
- [ ] **39.** *problem*  **pg**
- [ ] **40.** *problem*  **pg**

## 7.2 Basic Circuit Model
#### Terms
#### Propositions
#### Questions
#### to-do
- [ ] **1.** *problem*  **pg**
- [ ] **2** *problem*  **pg**
- [ ] **3.** *problem*  **pg**
- [ ] **4.** *problem*  **pg**
- [ ] **5.** *problem*  **pg**
- [ ] **6.** *problem*  **pg**
- [ ] **7** *problem*  **pg**
- [ ] **8.** *problem*  **pg**
- [ ] **9.** *problem*  **pg**
- [ ] **10.** *problem*  **pg**
- [ ] **11.** *problem*  **pg**
- [ ]  **12.** *problem*  **pg**
- [ ] **13.** *problem*  **pg**
- [ ] **14.** *problem*  **pg**
- [ ] **15.** *problem*  **pg**
- [ ] **16.** *problem*  **pg**
- [ ] **17** *problem*  **pg**
- [ ] **18.** *problem*  **pg**
- [ ] **19.** *problem*  **pg**
- [ ] **20.** *problem*  **pg**
- [ ]  **21.** *problem*  **pg**
- [ ] **22** *problem*  **pg**
- [ ] **23.** *problem*  **pg**
- [ ] **24.** *problem*  **pg**
- [ ] **25.** *problem*  **pg**
- [ ] **26.** *problem*  **pg**
- [ ] **27** *problem*  **pg**
- [ ] **28.** *problem*  **pg**
- [ ] **29.** *problem*  **pg**
- [ ] **30.** *problem*  **pg**
- [ ] **31.** *problem*  **pg**
- [ ] **32** *problem*  **pg**
- [ ] **33.** *problem*  **pg**
- [ ] **34.** *problem*  **pg**
- [ ] **35.** *problem*  **pg**
- [ ] **36.** *problem*  **pg**
- [ ] **37** *problem*  **pg**
- [ ] **38.** *problem*  **pg**
- [ ] **39.** *problem*  **pg**
- [ ] **40.** *problem*  **pg**

## 7.3 Combinational Circuits
#### Terms
#### Propositions
#### Questions
#### to-do
- [ ] **1.** *problem*  **pg**
- [ ] **2** *problem*  **pg**
- [ ] **3.** *problem*  **pg**
- [ ] **4.** *problem*  **pg**
- [ ] **5.** *problem*  **pg**
- [ ] **6.** *problem*  **pg**
- [ ] **7** *problem*  **pg**
- [ ] **8.** *problem*  **pg**
- [ ] **9.** *problem*  **pg**
- [ ] **10.** *problem*  **pg**
- [ ] **11.** *problem*  **pg**
- [ ]  **12.** *problem*  **pg**
- [ ] **13.** *problem*  **pg**
- [ ] **14.** *problem*  **pg**
- [ ] **15.** *problem*  **pg**
- [ ] **16.** *problem*  **pg**
- [ ] **17** *problem*  **pg**
- [ ] **18.** *problem*  **pg**
- [ ] **19.** *problem*  **pg**
- [ ] **20.** *problem*  **pg**
- [ ]  **21.** *problem*  **pg**
- [ ] **22** *problem*  **pg**
- [ ] **23.** *problem*  **pg**
- [ ] **24.** *problem*  **pg**
- [ ] **25.** *problem*  **pg**
- [ ] **26.** *problem*  **pg**
- [ ] **27** *problem*  **pg**
- [ ] **28.** *problem*  **pg**
- [ ] **29.** *problem*  **pg**
- [ ] **30.** *problem*  **pg**
- [ ] **31.** *problem*  **pg**
- [ ] **32** *problem*  **pg**
- [ ] **33.** *problem*  **pg**
- [ ] **34.** *problem*  **pg**
- [ ] **35.** *problem*  **pg**
- [ ] **36.** *problem*  **pg**
- [ ] **37** *problem*  **pg**
- [ ] **38.** *problem*  **pg**
- [ ] **39.** *problem*  **pg**
- [ ] **40.** *problem*  **pg**

## 7.4 Sequential Circuits
#### Terms
#### Propositions
#### Questions
#### to-do
- [ ] **1.** *problem*  **pg**
- [ ] **2** *problem*  **pg**
- [ ] **3.** *problem*  **pg**
- [ ] **4.** *problem*  **pg**
- [ ] **5.** *problem*  **pg**
- [ ] **6.** *problem*  **pg**
- [ ] **7** *problem*  **pg**
- [ ] **8.** *problem*  **pg**
- [ ] **9.** *problem*  **pg**
- [ ] **10.** *problem*  **pg**
- [ ] **11.** *problem*  **pg**
- [ ]  **12.** *problem*  **pg**
- [ ] **13.** *problem*  **pg**
- [ ] **14.** *problem*  **pg**
- [ ] **15.** *problem*  **pg**
- [ ] **16.** *problem*  **pg**
- [ ] **17** *problem*  **pg**
- [ ] **18.** *problem*  **pg**
- [ ] **19.** *problem*  **pg**
- [ ] **20.** *problem*  **pg**
- [ ]  **21.** *problem*  **pg**
- [ ] **22** *problem*  **pg**
- [ ] **23.** *problem*  **pg**
- [ ] **24.** *problem*  **pg**
- [ ] **25.** *problem*  **pg**
- [ ] **26.** *problem*  **pg**
- [ ] **27** *problem*  **pg**
- [ ] **28.** *problem*  **pg**
- [ ] **29.** *problem*  **pg**
- [ ] **30.** *problem*  **pg**
- [ ] **31.** *problem*  **pg**
- [ ] **32** *problem*  **pg**
- [ ] **33.** *problem*  **pg**
- [ ] **34.** *problem*  **pg**
- [ ] **35.** *problem*  **pg**
- [ ] **36.** *problem*  **pg**
- [ ] **37** *problem*  **pg**
- [ ] **38.** *problem*  **pg**
- [ ] **39.** *problem*  **pg**
- [ ] **40.** *problem*  **pg**

## 7.5 Digital Devices
#### Terms
#### Propositions
#### Questions
#### to-do
- [ ] **1.** *problem*  **pg**
- [ ] **2** *problem*  **pg**
- [ ] **3.** *problem*  **pg**
- [ ] **4.** *problem*  **pg**
- [ ] **5.** *problem*  **pg**
- [ ] **6.** *problem*  **pg**
- [ ] **7** *problem*  **pg**
- [ ] **8.** *problem*  **pg**
- [ ] **9.** *problem*  **pg**
- [ ] **10.** *problem*  **pg**
- [ ] **11.** *problem*  **pg**
- [ ]  **12.** *problem*  **pg**
- [ ] **13.** *problem*  **pg**
- [ ] **14.** *problem*  **pg**
- [ ] **15.** *problem*  **pg**
- [ ] **16.** *problem*  **pg**
- [ ] **17** *problem*  **pg**
- [ ] **18.** *problem*  **pg**
- [ ] **19.** *problem*  **pg**
- [ ] **20.** *problem*  **pg**
- [ ]  **21.** *problem*  **pg**
- [ ] **22** *problem*  **pg**
- [ ] **23.** *problem*  **pg**
- [ ] **24.** *problem*  **pg**
- [ ] **25.** *problem*  **pg**
- [ ] **26.** *problem*  **pg**
- [ ] **27** *problem*  **pg**
- [ ] **28.** *problem*  **pg**
- [ ] **29.** *problem*  **pg**
- [ ] **30.** *problem*  **pg**
- [ ] **31.** *problem*  **pg**
- [ ] **32** *problem*  **pg**
- [ ] **33.** *problem*  **pg**
- [ ] **34.** *problem*  **pg**
- [ ] **35.** *problem*  **pg**
- [ ] **36.** *problem*  **pg**
- [ ] **37** *problem*  **pg**
- [ ] **38.** *problem*  **pg**
- [ ] **39.** *problem*  **pg**
- [ ] **40.** *problem*  **pg**

# Context
##### Java libraries
##### Programming environments
##### Scientific computing
##### Apps and cloud computing
##### Computer systems
##### Theory of computing
##### Machine learning