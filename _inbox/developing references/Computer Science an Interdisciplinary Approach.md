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
[[object-oriented programming]] (330)
[[String data-type]] (330)
[[constructor method]] (331)
[[reference data-type]] (334)
[[static methods]] (340)
[[instance methods]] (340)
[[color data-type]] (341)
#### Propositions
#### Questions

- [[object-oriented programming]] (**OOP**)organizes data for processing using abstract data-types know n as [[reference types]]
	- OOP is a programming paradigm facilitating organizing and processing data
- extensive libraries of reference types supplements primitive data-types including the [[String data-type]]
- with the ability to use and create reference types we are not only limited to operations on primitive types (mostly numeric), or even the built -in string and [[color data-type]]
#### Basic definitions (331)
- *do not need to know how a data-type is implemented to be able to use it*
- data-types defined by values and operations, but when using a data-type the focus is on the **operations**
##### The String data-type (331)
- String processing is critical to many applications
	- lie at heart of ability to compile and run programs
	- basis of info processing apps crucial to business systems
	- people use them to communicate
		- blogs
		- chat
		- email
		- documents for publication
	- important to scientific advancements especially in molecular biology
- Strings are an object and have separate operations for *declaring variables*, *creating objects* to hold data-type values and *invoking instance methods* associated with data-type to perform operations
	- they are the only object that have shortcuts for operations so they can by used in a similar way to primitive data-types
	- reference data type declaration, creation, and operations are used differently from primitive types, but corresponding mechanisms perform similar functions
##### API (332)
- Java classes can be used to define reference data types
- like any class of methods the API contract can specify what a user needs to know and allows us to guarantee that *data -types can be used even if a user is ignorant of the implementation details**
- API purpose is to provide information needed to be able to utilize data type appropriately in a client program calling the class
- a [[constructor]] is a special method, it is the first class entry  has same name as the class and no return type
- class entries are [[instance methods]] that can take arguments and return values for objects of the reference data-type
	- similar to [[static method]]s  but are only associated with objects the reference data-type
	- `string.length()` returns number of characters in a string
	- `string.charAt(i)` returns character at index if of a string objects
- [[string]]s are indexed similar to arrays

##### Declaring variables (333)
- Declare reference data-type same ways as a primitive data-type
	- `String s;`
	- Convention is for reference data-types to be declared with a capitalized data-type and primitive data-types use lower case `int, double, char etc.`
- Doesn't create anything just declares that the identifier will be used for an object of that type
- 
##### Creating objects (333)
- `String s = new String("Hello, world");`
##### Invoking instance methods (334)
- each data-type value is tored in a na object
- when [[constructor method]] called by a client, Java instantiates a new instance of the object
- `s = new String("Hello, World);"`
- declaration and instantaiation can be called in the same line
- `String s = new String("Hello, World);"`
- An unlimited number of objects can be created from the same data class
- each object has same identity and values that can be manipulated independently
```Java
//3 Differente string objects (even s1 and s3)
String s1 = new String("Cat");
String s2 = new String("Dog");
String s3 = new String("Cat");
```


##### Invoking instance methods (334)
-    biggest difference between primitive and reference data-types is how op-erations are invoked
	- [[primitive data-type operations]]
		- `+,-,/,*` etc.
	- [[reference data-type]] variables themselves are sued to invoke instance methods
- similar to calling a static method except the method is associated with the object itself as well as the method class like with a [[static method]]
	- typically use object name instead of class name when identifying instance method
- `s.chartAt(1)` invokes the instance method to find the character at index 1 on the string object `s`
##### Strings shortcuts (335)
- Strings are only reference data type with shortcuts resembling primitive data-type operations
- These are just shortcuts for corresponding long form operations like a traditional object method call
``` Java
String s = "abc";
String s = new String("abc");

String t = r + s;
String t = r.concat(s);
```
- String class has many more operations for processing Strings
- String API good example of developing and abstract model and separating the code that implements the abstraction from the code that uses it
- [[object-oriented programming]] is built around this idea, where programs are based on defining and invoking methods that implement abstractions through data-type operations
#### String-processing application: [[genomics]] (336)
- String's useful for working with gene models
- Biologists model [[DNA]] using  *A, C, G, T* as the four bases in DNA of living organisms
	- one for each [[chromosome]]
- building blocks appear in long sequence known as a [[genome]]
- Genome for many living creatures is known allowing scientists to compose programs to study the structure
- String processing critical to molecular biology for both experimental and coputational purposes, especially since a specie's genome can be massive
	- human genome made up of a sequence of 3,000,000,000 bases
##### Gene prediction (336)
- [[gene]] is a substring of a genome that represents a functional unit for life processes
- genes are made up of a sequence of [[codons]], made up of 3 bases representing an amino acid
- [[start codon]] *ATG* marks beggining
- [[stop codon]] *TAG, TAA, TGA* mark the end
- first step in analyzing genome is a [[String processing]] task
	- sued to identify potential genes by making sure sequences comply with the conditions specified below
		- length must be multiple of 3
		- starts with *start codon*
		- ends with an *end codon*
		- no *stop codon*s appear in between
##### Program 3.1.1 Identifying potential gene
###### Methods used
```Java
length()
charAt()
startsWith()
endsWith()
substring()
equals()
```
#### Properties of reference types and objects 
##### Object references (338)
- [[constructor]] creates object returns reference to the object
- `new` assigns memory space to hold object's [[data-type value]] and return's a [[pointer]] to memory address 
	- memory address associated with object is the [[object's identity]]
- *Why is address returned rather than object itself?*
	- data-type values consume a lot memory
	- if object is large it would be very costly to copy and move all data every time an object is passed as an argument to a method
	- same reasoning as with arrays because **arrays are objects**
- primitive types are natural to represent in memory so doesn't make sense to use references

##### Using objects (338)
- variable names can be used similar to variables for primitive types
	- as arguments or return values in methods
	- in array assignments statements
	- in arrays
- Additionally **object** variable names can be used to *invoke instance methods defined for the object type*
	- not available for primitive variables as operations are built into the language

##### Uninitialized variables (339)
- variables that are declared but not assigned a value are [[uninitialized]]
- Using uninitialized objects variables returns a *compile-time error* like using unitialized primitive variables
##### Type conversion (339)
- need to write code if you want to convert an object of one type to the other
- often not necessary as object data-types are so different conversion wouldn't make sense
	- what does it mean to convert a String to a Color object
- `toString()` is one conversion that is worthwhile
	- details of conversion are up to implementation
	- usually implemented where String encodes object value
- Java automatically calls `toString()` for certain situations like
	- [[string concatenation]]
	- printing to console

##### Accessing a reference data type (339)
- similar to [[static methods]] code implementing class 
	- stored in file of same name
	- needs to be accessible to java to utilize in client code

##### Distinction between instance methods and static methods (340)
- purpose of [[static methods]] is to implement functions
- purpose of [[instance methods]] is to implement [[data-type operations]]
- visual difference
	- static methods typically start with class name
	- instance methods starts with object name
|              | instance method                     | static method    |
| ------------ | ----------------------------------- | ---------------- |
| sample call  | `s.startsWith("Hello")`               | `Math.sqrt(2.0)` |
| invoked with | object name/object reference        | class name       |
| parameters   | reference to invoking object + args | args             |
| purpose      |manipulate an object's value         |compute a return value  |

##### OOP Summary (340)
- **Data type:** is set of values and operations defined on those values
	- data types are implemented in modules which client programs can use
- **Object:** is an *instance* of a data-type
- **Objects** characterized by 3 properties
	1. [[state]]: value from an object's data type
	2. [[behavior]]: defined by object's [[data-type operations]] 
	3. [[identity]]: object's memory location
- Invoke [[constructor method]] to create objects
- Invoke [[instance method]] to modify object state
- Objects are manipulated via [[object references]]

#### Color (341)
- [[color]] is a widely used abstraction in computer graphics
- representing and using color is a complex task and depends heavily on publication format
- Java provides a color reference type allowing for separation between designer's problem of specifying a color and the system's problem of representing it accurately
- `import java.awt.Color` allows us to explicitly list which libraries to use to avoid name conflicts
- `Color` represents color values at [[RGB color model]]
	- recolor defined by `int` values from `0-255` representing intensity of red green and blue
	- other colors obtained by mixing these 3 colors
	- data type value of `Color` represented by 3 8-bit integers
- `Color` constructor takes 3 integer arguments
```Java
Color red = new Color(255, 0, 0);
Color bookBlue = new Color(9, 90, 166);
```
- Here color is used to demonstrate object-oriented programs, as well as being a useful tool for program development
	- mainly exploring one property [[monochrome luminance]] to show that using oop for abstract concepts like color is convenient approach

##### Luminance (343)
- luminance is the effective brightness of a color and is critical to the function of modern LCD displays
- it is a [[linear combination]] of the 3 RGB intensities
$$Y = 0.299r + 0.587g + 0.114b$$
- coefficients are positive and sum to 1, meaning luminance is a real number from 0 - 255
##### Grayscale (344)
- when all 3 RGB intensities are equal, produces a color in the [[grayscale]]
	- ranges from black (all 0's) to white (all 255)
- to print in black and white need a function to convert color to grayscale
- this can be accomplished by *replace color with new one where rgb values equal monochrome luminance*

##### Color compatibility (344)
- **monochrome luminance** also helps determine whether colors are compatible if printed together
- *rule of thumb* difference between two color's luminance should be >= 128
- Using Color objects as arguments and return values simplifies libraries developed to process color
	- alternative would be functions passing around 3 rgb intensities
		- passing values is cumbersome
		- no way to return multiple values without objects
	- object allow maintenance of state

#### Digital image processing (346)

##### Digital images (346)

##### Grayscale (347)

##### Scaling (349)

##### Fade effect (351)

- abstraction for color can also be built upon to build [[higher-level data types]] that have color values (344)
- Can be used to create data types that can be utilized in programs for image processing (344)
- [[digital images]] are now computationally dependent and easily allow users to perform operations on image attributes
	- [[crop]]
	- [[scale]]
	- [[fade]]
	- [[contrast]]
	- [[brightness]]
##### Digital images (346)
- digital images are a rectangular grid of [[pixels]]
	- each color of a pixel is individually defined making up the atomic elements of digital images
	- pixels are the values that are processed when rendering digital images and operated on when modifying
- [[Picture object]] is an implementation of this abstraction
	- it is a two dimensional matrix, where each element is a separate [[Color object]]
	- Instance methods defining operations include
		- creating blank image with given width and height
		- load image from file
		- set a pixel value to a color
		- return color of a pixel value
		- return the width/height of an image
```Java
//Picture API
	Picture(String filename) //creat picture from file
	Picture(int w, int h)    // create blank wxh image
int width()                  // return picture width
int height()                 // return picture height
Color get(int col, int row)  // return color of pixel at (c,r)
void set(int col, int row, Color c) // set color of pixel at (col,row) to c
void show()                         // display image
void save(String filename)          // save image to file
```
- (0,0) customarily the top -left pixel, meaning images are ordered like 2D arrays
	- contrast to `StdDraw` functions that have (0,0) as bottom left-most location
	- oriented like [[Cartesian coordinates]]
- These methods along with `Color` data type provide ability for image processing
##### Grayscale (347)
- converting to grayscale is greatly simplified with pixel based abstraction implemented as an object
- Need to calculate luminance for color pixels, then convert to a grayscale color with the same intensity by setting all 3 RGB values to the *monochrome luminance* returned
- A target is created where each pixel corresponding to the original image is set to its monochrome luminance value
	- Creates new `Picture` object, which is initialized to the color original, then converts each pixel by applying `Luminance.togray()` to the color in value in the pixel  

##### Scaling (349)
- [[scale]] common task in image processing is making image bigger or smaller
- If target image needs to be scaled to half size can simply delete half the pixels
	- technique known as [[sampling]]
- For doubling need to take a different approach
	- can replace the pixel with 4 pixels of the same color
- halving a doubling an image will not give back the same image as information is lost in the scale down
- Can adapt a general strategy for [[upscaling]] and [[downscaling]]
	- go through pixel by pixel in target
	- scale each pixel's coordinates to identify pixel color in the source
	- source:
		- width $w_s$
		- height $h_s$
	- target 
		- width $w_t$
		- height $h_t$
	- scale column index by $w_s/w_t$
	- scale row index by $h_s/h_t$
	- this means we get the color for pixel in col c and row r of the target for
		-  column $c*w_s/w_t$
		- row $r*h_s/h_t$ 
	- other approaches can be taken for low resolution photos
		- might downscale to half size by taking average of four pixels in source to make one pixel in target
```Java
public class Scale{
	public static void main(String[] args){
		int w = Integer.parseInt(args[1]);
		int h = Integer.parseInt(args[2]);
		
		Picture source = new Picture(args[0]);
		Picture target = new Picture(w, h);
		for(int colT = 0; colT < w; colT++){
			for(int rowT = 0; rowT < h; rowT++)
			{
				int colS = colT*source.width()/w;
				int rowS = rowT*source.height()/h;
				target.set(colT, rowT, source.get(colS, rowS));
			}
		}
		source.show();
		target.show();
	}
}
```

##### Fade effect (351)
- [[fade effect]] transform one image into another
- uses [[linear interpolation]] to create transition effect
	- $n-1$ intermediate pictures calculated
	- each pixel in picture $i$ weighted average of corresponding pixels in source and target images 
- static method `blend()` implements interpolation
	- source pixel weighted by factor of $1- i/n$
	- target pixel weighted by factor of $i/n$
```Java
import java.awt.Color;

public class Fade{
	public static Color blend(Color c1, Color c2, double alpha)
	{
		double r = (1-alpha)*c1.getRed + alpha*c2.getRed();
		double g = (1-alpha)*c1.getGreen + alpha*c2.getGreen();
		double b = (1-alpha)*c1.getBlue + alpha*c2.getBlue();
		return new Color((int)r, (int)g, (int)b));
	}

	public static void main(String[] args){
		Picture source = new Picture(args[0]);
		Picture target = new Picture(args[1]);
		int n = Integer.parseInter(args[2]);
		int w = source.width();
		int h = source.height();
		Picture picture = new Picture(w, h);
		for(int i = 0; i <=n; i++){
			for( int c = 0; c < w; c++){
				for(int r = 0; r < h; r++)
				{
					Color c1 = source.get(c,r);
					Col0r c2 = target.get(c, r);
					double alpha = (double)i/n;
					Color color = blend(c1, c2, alpha);
					picture.set(c, r, color);
				}
			}
			picture.show();
		}
	}
}
```

#### Input and output revisited (353)
- standard input is convenient as it is accessible from anywhere in the program, 
- unfortunately dependent on the the OS's piping and redirection utilities to access files
- also restricts I/O to one file input, one output file, and one drawing
- can use OOP to define I/O mechanisms that allow multiple [[input streams]], [[output streams]], and drawings in a single program
- can now define multiple objects of each I/O data-type which allows us to connect multiple I/O streams to different sources and destinations
- can also assign these objects to variables and manipulate like any other object

##### Input stream data type (354)
- [[input stream data-type]] 
	- no longer restricted to one abstract input stream
	- can now specify the source including input streams from
		- *file*
		- *website*
- specified file/website becomes source for the assigned object
	- now possible to process multiple files in same program as multiple objects can be created with different sources
- ability to access web for input streams greatly expands access to data to the entire world wide web
	- can access files maintained online by other like:
		- scientific data files
		- satellite photos
		- astronomical observations
		- stocks performance
		- government agency data
			- federal reserve
			- census
- can now write programs that directly read these files

##### Output stream data type (355)
- [[output data-type]] serves as a similar analog allowing text to be printed to a large variety of [[output streams]]
- can now specify a location to send output to, as well as standard output


##### File concatenation and filtering (356)
- [[file concatenation]] programs can be composed with input and output objects to allow us to combine files into a single output file, while specifying filter conditions
- the ability to control implementation details rather than the OS `cat` utility is useful in many applications including [[web scraping]]
##### Screen scraping (357)
-  many websites defined with text files
- using input and output data-stream objects, can set website as source destination and extract text
	- stored in highly structured format like `HTML`
	- Java sees text as just another string
	- filters can be set in program to ignore irrelevant elements in web text
- process known as [[web scraping]]
	- allows us to extract info without having to browse site
- `String.indexOf()` and `String.substring()` methods can be used to take advantage of `HTML` structure find and extract patterns for data you are interested in
	- HTML highly structured and uses tagging to identify content types
	- can find tag patterns and extract the substring between them
- website formats may change, potentially requiring changes in program implementation if the program needs to be used continuously


##### Extracting data (358)
- spreadsheets can be saved into some organized text format like [[comma separated value files]] (**CSV**)
	- data delimited by commas, where each comma indicates new column
	- each line is a separate row
- This data can be read into java into java as input streams
	- `String.split()` can be used to read file line by line, splitting by the delimiter (",")
	- this allows us to isolate and extracts specific columns
	- Can then go on to define multiple output streams, dedicating a different file to every column

##### Drawing data type (361)
- can create multiple objects containing drawing type
- can have multiple output windows
#### Properties of reference types (362)
- [[reference data-type]]s capture the distinction between a thing and its name
	- [[Rene Magritte]] [[This is not a pipe]]
	- once an object is created multiple names can be assigned all referencing the same object
	- similar to [[array assignment]]
	- 
##### Aliasing (363)
- [[aliasing]]-  assignment  with reference type creates a copy of the reference
	- does **not** create a new object
	- both variables will refer to same object
	- [[aliasing bugs]] this can be a source of bugs
- following this logic changing the state of an object changes the state for all references to that object
##### Immutable types (364)
- [[immutable]] types are objects where data-type values cannot be changed once created
- may be used to prevent [[aliasing bugs]]
- `Strings` are *immutable*, there are no operations available to clients that can change the string's characters
	- conversely `arrays` and `Picture`objects are  [[mutable]] data-types
##### Comparing objects (364)
- for reference data-types `==` compares whether references are equal, not whether they contain the same values
- instance methods to check equality need to be explicitly defined for new data-types
##### Pass by value (364)
- when arguments are passed to methods, Java passes copy of the argument value from the caller to the method
	- [[pass by value]]  primitive types arguments Java passes  a copy of that value
	- [[pass by reference]] for arguments of object references, Java passes a copy of the object reference
- this is because individual primitive type values will be small, but abstract data-types can be arbitrarily large and needing to copy all elements could potentially be resource instensive
- this also means methods can't change the value of a caller's variable, each time a reference type is used a new *alias* is created for it
	- method cannot change the caller's object reference (make it refer to a different `Picture`  for object)
	- it can change the value of the object (`Picture.set()` to change a picture's color)
##### Arrays are objects (365)
- [[array]]s are [[mutable]] objects
	- appropriate for typical function where we want to be able to modify the elements within
		- `shuffle()`
		- `exchange()`
- built in language support for arrays like `Strings` for certain operations
	- declaration
	- initialization
	- indexing

##### Arrays of objects (365)
- arrays can contain any type of data-type including objects
- arrays of objects are actually [[array of references]] to objects
	- gain efficiency if objects are large as we don't have to shuffle values around
	- if objects are small we lose efficiency following references every time information about object is needed
- create an [[array of objects]] in 2 steps
	1. create array with `new` and square bracket syntax
	2. create each object using `new` to call constructor method for object of interest
```Java
Color[] a = new Color[2];
a[0] = new Color(255, 255, 0);
a[1] = new Color(160, 82, 45);
```
##### Safe pointers (366)
- many languages provide [[pointer]]s to locate and manipulate memory addresses 
- similar to Java references
	- common in C and C++
- pointers can be dangerous and error prone
	- languages often provide special methods for working with pointers to avoid these errors
- Java implements concept of [[safe pointer]]s where Java guarantees each reference points to an object of that data-type not an empty memory address
	- only one way to create a reference (with `new`)
	- only one way to manipulate that reference (with the [[assignment statement]])
- this means programmers can only create and copy references
##### Orphaned objects (366)
- ability to assign different objects to a reference variable can lead to [[orphaned]] objects
	- an object in a program that can no longer be referenced, if originally assigned a reference which now references a different object
- objects out of scope are also considered to be orphaned
##### Memory management (367)
- Programs will typically create many objects, but only need a small number at any time
- Need mechanisms to [[allocate memory]] when storage need for data-type variables then [[free memory]] when no longer needed
- memory easier to manage for primitive types, because storage needs are know at compile time
- object memory management more complicated
	- knows when to *allocate* with `new` keyword
	- less straightforward to know when to *free* the memory because when an object is orphaned depends on the execution dynamic of a program at run-time 

##### Memory leaks (367)
- languages like C and C++ require programmer to **manually** *allocate and free memory*
- Can be tedious and error prone
- If a program deallocates memory then continues to refer to the object later in the program program may have reallocated the memory for other purposes in between leading to chaos and error
- If programmer forgets to deallocate memory for *orphaned objects* can result in a [[memory leak]] where memory dedicated to orphaned objects accumulates
	- causes performance degradation as if memory leaking out of computer
	- one of reasons rebooting solves many issues
##### Garbage collection (367)
- Java automatically manages and clear unused memory including orphaned objects through [[garbage collection]]
- *safe pointer* allows this to be done automatically
- programmer no longer needs to keep track of orphaned objects and returning memory
	- debated whether additional overhead worth the gain
#### Q&A
- [[pass by object reference]] Java is purely a *pass by value language* with objects you are passing the value of the reference to the object
	- value is either a primitive data type or a reference to an object
	- method cannot modify the data type and it cannot modify the reference name, but can modify the value of the object at the reference address 
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
- while many convenient abstractions defined for data types beyond primitive data-types, built in libraries could not possibly capture all potential needs for every user
- [[data abstraction]]: need to be able to define custom data-types in Java
- creating data types is similar to writing libraries of static methods
- key differences 
	- data is associated with the method implementation 
- API specifies constructor and and instance methods needed to be implemented but are free to define any appropriate representation
- ability to define abstractions helps address arbitrarily complex programming challenges
#### Basic elements of a data type (383)
- demonstrate process of implementing data type with `Charge` data-type
- 
##### API (383)
- API is contract with all clients and should be the starting point for defining the `Charge` data-type
- To implement data-type
	- define data-type values
	- implement constructor that creates charged particle
	- method `potentialAt()` returns potential at $(x, y)$ point due to charge
	- `toString()` return String representation of charge

##### Class (383)

- data-types are implemented as classes
- key features of a data-type
	- [[instance variable]]s
	- [[contractor]]s
	- [[instance method]]s
- each element of data-type qualified by [[access modifier]]
##### Access modifiers (384)

- [[access modifier]]s sometimes precede class names, *instance variable* names and method names, control access of these items from the client code  
	- `public` accessible by clients
	- `private` not accessible by clients
	- `final` value of variable does not change once initialized
- **convention:**
	- `public` used for constructors and methods defined in API
	- `private` used for everything else (usually helper functions to simplify code in the class)
- 
##### Instance variables (384)

- need to declare [[instance variable]]s before [[instance method]]s can be defined to operate on data-type values stored in variables
- can be of any data-type
- declared same way as local variables
- declared as first statements in class
- [[difference between instance and local variables]]
	- only one value for each local variable in a block or method
	- will be as values for  instance variables as there are objects of the data type
	- each time instance method is invoked it is done with an object reference to the object whose value is actually being manipulated. *separation of concerns*
```Java 
public class Charge{
	private final double rx, ry;
	private final double q;
}
```
##### Constructors (384)

- [[constructor]]s are special methods that create and provide references to an object
- automatically invoked with `new` keyword
- Code needs to initialize constructor with meaningful values for instance variables
- Share same name as the class 
- can be [[overloaded]] with multiple constructors with different signatures 
- `new` with constructor name equivalent as a function that returns an object reference of specified type
- no return type as they *always return reference to object of the data type*
- each time constructor is invoked
	- memory allocated for object
	- constructor code invoked to initialize instance variables
	- reference to new object returned
- **typical  constructor** *initializes instance variables with values provided by client as arguments*

##### Instance Methods (385)

- implementation of [[instance method]]s similar to [[static method]]s 
- [[instance vs static methods]]
	- each method has 
		- signature specifying return type and parameter variables
		- body consisting of sequence of statements and return statement 
	- when instance method invoked by client
		- parameter variables initialized with client values
		- statements executed until return reached
		- value returned to client
	- only difference is that **instance methods** *perform operations on **instance variables***
##### Variables within methods (386)

- *instance methods* use three types of variables
	1. [[parameter variable]]s (same as static method)
	2. [[local variable]]s (same as static methods)
	3. [[instance variable]]s
- instance variables are completely different from other two
	- hold data-type values for objects in class
	- scope is the *entire class*
- each object of class has a value
- code in instance method refers to *value for object used to invoke method*
- distinction between [[instance vs. parameter vs. local variables]] used to implement instance methods key to understanding *OOP*
| variable  | purpose                          | example  | scope  |
| --------- | -------------------------------- | -------- | ------ |
| parameter | pass value from client to method | `x, y`   | method |
| local     | temporary use within method      | `dx, dy` | block  |
| instance  | specify data-type vale           | `rx, ry` | class       |
##### Test client (388)

- `main()` can be used for testing methods in each class
##### Summary of basic data type elements
- every data type has same basic elements
	- instance variables
	- constructors
	- instance method
	- test clients
- Each data-type implemented with same steps
	1. specify API to *separate clients from implementation* and enable [[modular programming]]
		- should think about needs of client  then accomodate in data-type
		- [[two goals for API]]
			1. enable clear and correct client code
			2. Want to be able to implement needed operations
		- no point specifying operations that we can't realistically implement
	2. second step is *implement class meeting API specifications*
		1. choose instance variables
		2. write code to manipulate instance variables to implement contructors and instance methods specified
	3.  this write test clients to validate design decision made in previous steps
#### Stopwatch (390)
- [[object-oriented programming useful for modeling real world objects]] like a stopwatch
#### Histogram (392)
- [[whenever you can clearly separate data and associated operations within a program you should do so]]
#### Turtle Graphics (394)
- small amount of [[state]] can greatly simplify computations allowing data-types to maintain values for manipulation
- should clearly separate state/data like other tasks when possible within a program
- [[turtle graphics]] originally developed in 1960s at MIT to demonstrate LOGO programming language
##### Recursive graphics (397)
- [[koch curve]] 
	- order 0 straight line
	- order $n$ 
		- draw curve of $n-1$ 
		- turn left 60 degrees
		- draw second curve $n-1$ 
		- turn right 120 degrees (left -120 degrees)
		- draw third curve
		- turn left 60 degrees
		- draw fourth curve
- recursive implementation made simpler with objects
- useful modeling self-similar structures found in natures like snowflakes
- **proof by induction** width of curve order $n$ is $3^n * \text{step size}$  

##### Spira mirabilis (398)
- [[logarithmic spiral]] results if step size decreases each step
##### Brownian motion (400)
- [[brownian motion]] 
#### Complex Numbers (402)
- [[complex number]] is number of form $x + iy$
	- $x \text{ and }  y$  real numbers
	- $i$ is $\sqrt{-1}$ 
	- $x$ is *real part*
	- $i$ is *imaginary part*
- complex numbers quintessential mathematical abstraction
- used in applied mathematics
- model many types of physical systems
	- circuits
	- soundwaves
	- electromagnetic fields
- developing data type for complex numbers perfect use of abstract data types
	- provides freedom to think in new abstractions
- can develop methods once to deal with a data type operation then not have to worry about how to implement again, it is *reusable* (404)
	- save debugging
	- allows changing implementation if needed since separate from clients
- *whenever you can clearly separate data and associated tasks within a computation you should do so* (404)
##### Accessing instance variables of other objects of the same type (403)
- if private cannot access instance variables from another class
- within a class can access instance variables of any object from same class directly
	- not just limited to instance variables of invoking objects
```Java
public Complex plus(Complex b)
{
	double real = re + b.re;
	double imag = im + b.im;
	return new Complex(real, imag);  
}
```
##### Creating and returning new objects (404)
- clients can manipulate data types like complex numbers naturally by being able to manipulate local variables in the type `Complex`
```Java
public Complex times(Complex b)
{
	double real = re * b.re - im * b.im;
	double imag = re * b.im + im * b.re;
	return new Complex(real, imag);  
}
```
##### Chaining method calls (404)
- can chain method call into single statement eliminating need for intermediary variables
- can use any object reference to invoke methods even without a name
	- like one that results from evaluating subexpression
- moving left to right instance will be invoked that is then passed to next instance method in chain
```Java
public static void main(String[] args)
{
	Complex z0 = new Complex(1.0, 1.0);
	Complex z = z0;
	z = z.times(z).plus(z0);
	z = z.times(z).plus(z0);
	StdOut.println(z);
}
```
##### Final instance variables (404)
- [[final instance variable]] values don't change during lifetime of objetc
```Java
public class Complex{
	private final double re;
	private final double im;
	public Complex(double real; double imag)
	{ re = real; im = imag}
}
```
#### Mandelbrot Set (406)
- [[mandlebrot set]] is set of self similar recursive pattern that cannot be described by an equation, instead is defined by an algorithm
#### Commercial Data Processing (410)
- need for reliable [[commercial data processing]] software has been driving force for OOP
- can maintain different states of data for different objects of same type
	- like balances within an account object
- ro enable processing we need
	- [[file format]]
	- [[data structure]] or internal representation
##### File format (411)
- most modern systems use text files for data to minimize dependencies on formats defined for specific prorgams
- can incorporate [[tags]] to introduce additional structure and label data reducing dependencies
##### Data Structure (411)
- use [[instance variable]]s to represent information for processing
- specifies type of information and provide structure needed to refer to it in code`
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

# Chapter 4: Algorithms and Data Structures

### 4.1 Performance
#### Intro (495)
- important to *pay attention to the cost* of a program
- cost dictates
	- focus of implementation designed by engineers
	- performance of software designed by developers
	- which scientific problems can be addressed by physicists and biologists
	- key to the jobs of businessmen and economists
- Study cost with the [[scientific method]]
- derive cost models with [[mathematical analysis]]
- with programs the features of cost we study is *time*
	- since complex operations are composed of relatively simple tasks, modeling time is relatively straightforward
##### Scientific method
1. *observe* feature of the world
2. *hypothesize* a model consistent with observations
3. *predict* events using hypothesis
4. *verify* predictions with additional observations
5. *validate* by repeating until hypothesis agrees with observations
- experiments must be [[reproducible]] 
- hypotheses must be [[falsifiable]]
#### Observations (495)
- programs have a *problem size* characterizing difficulty of computational tasks
- typically the size of the input
- running time should increase with problem size
- question is by *how much?*
- other problems may not change with input size
- need a way to quantify sensitivity to input
- need to quantify correspondence between problem size and running time
- *what is the relation between problem size $n$ and running time?*
#### Hypotheses (496)
- Despite all potential confounding factors, possible *in principle* to create an accurate model to predict running time ([[Donald Knuth]])
- Analysis requires
	- Detailed understanding of the program
	- Detailed understanding of the system and computer
	- Advanced mathematical analysis tools
- Simpler to create *back-of-the-envelope* calculations that capture essence of run-time growth using empirical observations and simpler mathematical analysis
##### Doubling hypotheses (496)
- Simple hypotheses can be formulate for many programs *what happens to running time of a program if the input size doubles*
- known as the [[doubling hypothesis]]
##### Empirical analysis (496)
- might start by observing how runtime increases by tracking with a stopwatch and changing the input
- can use a graph to add further clarity and help determine possible mathematical function of growth
##### Mathematical analysis (498)
- [[total runtime depends on two factors that are properties of the system and the algorithm]]
	- Cost of executing each statement (property of system)
	- frequency of executing each statement (property of algorithm)
- can be difficult to identify frequency of execution, leading to complicated mathematical expressions
- can practically simplify by using [[approximate expressions]]
	- work only with the [[leading term]] 
	- focus on instructions that occur most frequently, the [[inner loop]] of the program
- instructions outside the inner loop and smaller than the leading term become practically insignificant as input grows large
- **key point** For many programs running time satisfies relationship $T(n) \sim cf(n)$
	- $c$ is a constant
	- $f(n)$ is the [[order of growth]] function for the run time
- do not need complex mathematical analysis for the most part
	- safe to ignore costs outside *inner loop* because it is negligible in comparison
	- don't need to know constant, because it cancels out as input grows
- *approximate analysis* separates the algorithm from the system, allowing us to ignore the specifics of a machine or language
- *algorithm determines the **order of growth***
- separation allows us to develop knowledge of algorithm performance and apply the knowledge to any system 
#### Order-of-growth classifications (503)
- order of growth often falls into one of a few common types
| description  | function              | factor for doubling hypothesis |
| ------------ | --------------------- | ------------------------------ |
| constant     | $\mathcal{O}(1)$      | $1$                            |
| logarithmic  | $\mathcal{O}(log n)$  | $1$                              |
| linear       | $\mathcal{O}(n)$      | $2$                              |
| linearithmic | $\mathcal{O}(nlog n)$ | $2$                              |
| quadratic    | $\mathcal{O}(n^2)$    | $4$                              |
| cubic        | $\mathcal{O}(n^3)$    | $8$                           |
| exponential  | $\mathcal{O}(2^n)$    |$2^n$                                |

##### Constant (503)
- [[constant time complexity]] executes a fixed number of statements meaning run time unaffected by problem size
##### Logarithmic (503)
- [[logarithmic time complexity]] almost as fast as *constant time*
- common example [[binary search]]
- program size grows slowly in proportion to growth of input size
##### Linear (504)
- [[linear time complexity]] require a constant amount of time for each input
- execution time increases at a constant rate as program size increases
##### Linearithmic (504)
- [[linearithmic time complexity]] solutions can often be implemented for prorgams that are naturally quadratic
- typically approach improvement with [[divide-and-conquer]] strategy
##### Quadratic (504)
- [[quadratic time complexity]] typically crops up with nested loops
- [[insertion sort]]
##### Cubic (506)

##### Exponential (506)
- [[exponential time complexity]] execution time grows at a faster rate with each additonal increase of input size
- extremely slow, cannot be used for large problems
- important role in [[theory of algorithms]] as many types of problems for which exponential time is best that can be don3e
- [[towers of hanoi]]
#### Predictions (507)
- knowing [[order of growth]] allows us allows us to predict running time and make decisions about addressing problems that can be met with resources at hand without needing to actually run the program beforehand

##### Estimating the feasibility of solving large problems (507)
- *will this program be able to process input in a reasonable amount of time?*
- If input size it too large for problem's time complexity need to find another approach
- knowing *order of growth* allows you to predict accurately the limitations of the size of problems that can be solved
##### Estimating the value of a faster computer (507)
- *how much faster can I solve the problem with a faster computer?*
- [[Moore's law]] can expect a computer with about twice the speed and double the memory in 18 months from now
- cannot necessarily solve a program of double the input size in same time or the same input in half the time, because it depends on how fast the time grows, as increased speed and memory only decreases execution time at a constant rate
- [[value of linear and logrithmic algorithms with increased computing resources]] is that they allow your performance to keep pace with Moore's law, as computer that is 10x faster with 10x memory will be able to solve programs 10x as large, unlike quadratic time complexities and slower
##### Comparing Programs (508)
- give two algorithms for same problem,, want to know which will solve w/ fewer computational resources
- With ability to predict performance during development, can guide towards more efficient code
- *order of growth allows us to compare an algorithm against entire classes of algorithms*
	- once we have a *linearithmic solution* we're not interested in *quadratic* even if they are optimized
- can use time complexity to estimate and compare run times of solutions

#### Caveats (509)
- Can get inconsistent/misleading results when analyzing program performance
- error can will be due to underlying assumptions of hypothesis being incorrect
- Can develop new hypothesis based on new assumptions but more care is required in analysis when more details are needed to be accounted for
##### Instruction time (509)
- incorrect to assume each instruction takes same amount of time due to [[caching]]
	- *caching* is a way of organizing memory, and accessing elements in large arrays can take longer if they are not close
##### Nondominant inner loop (510)
- problem sioze $n$ might not be large enough to make leading term outsized compared to rest of program
- programs with significant code in [[outer loop]] need to be taken into consideration

##### System considerations (510)
- many things going on in computer both within Java and in the rest of the computing environment consuming resources
- makes it difficult for *reproducible research* as computing environment won't be the same at all times
- whatever else is going on in system should be negligible *in principle*

##### Too close to call (510)
- one program may be faster than another in certain situations, depending on additional considerations mentioned

##### Strong dependence on input values
- assumption is that running time depends on problem size and relatively insensitive to input values, but not always the case sometimes leading to inconsistent results
- prime design goal is to limit dependence on input values
- if can't be done need to model carefully input to be processed which can be a difficult task

##### Multiple problem parameters (511)
- if multiple parameter input sizes, each will need to be analyzed independently 

#### Performance guarantees (512)
- [[performance guarantees]] provide *worse case scenario* boundary where programs need to be below a certain execution time bound
- particularly important for applications with catastrophic results if performance cannot be guaranteed to certain level (brakes, nuclear reactors, air traffic control)
- performance guarantee hypotheses would be difficult to verify experimentally, need to take  mathematical approach [[big O notation]]
- *task of* *algorithm analyst* to discover as much relevant inof about algorithm as possible
- *task of programmer* to apply info to develop programs to solve problem at hand
- **ideally** want algorithms leading to concise clear code with good worst-case guarentee and good performance on the types and size of input we're interested in
#### Memory (513)
- need to be aware of [[memory usage]] to assess cost as well
- takes up limited number of free circuits 
- Java's memory allocation system automatically manages memory, but shoulds still be aware of memory impact *approximately* so you can assess whether amount of memory can realistically address problem
##### Primitive types (513)
- measy to estimate memory for simple programs of mostly primitive types, as memory for each dat-type is fixed
count number of variables weighted by bytes associated with data-type
| type      | bytes |
| --------- | ----- |
| `boolean` | 1     |
| `byte`    | 1     |
| `char`    | 2     |
| `int`     | 4     |
| `float`   | 4     |
| `long`    | 8     |
| `double`          |  8     |

##### Objects (514)
- for objects add the amount of memory used by each *instance variable* to [[object overhead]] 
	- typically 16 bytes
	- memory is [[padded]] to be a multiple of 8 bytes
- *object reference* typically uses 8 bytes of memory
- when class include *object reference* as *instance variable* need to separately account for object reference and memory needed for object itself
##### Arrays (515)
- implemented as objects
- for [[primitive data-type arrays]] 
	- 24 bytes [[array overhead]]
		- 16 bytes *object overhead*
		- 4 bytes for *length*
		- 4 bytes *padding*
	- n time bytes needed to store each element
- [[object arrays]] are arrays of references to objects,
	- need to account for memory needed for references and memory needed for objects themselves
##### String objects (515)
- memory for `String` accounted for like any other object
- typically $2n + 56$ bytes
	- 16 bytes *object overhead*
	- 8 bytes reference to `char` array
	- $2n + 24$ bytes memory for `char` array
	- 4 bytes one `int value`
	- 4 bytes padding
##### Two-dimensional arrays (516)
- array of arrays

#### Perspective (518)
- *intractably slow program almost as useless as an incorrect one*
- need to *pay attention to the cost* at outset to understand what times of problems can be potentially solved with a practical program
- don't make mistake of paying too much attention to performance characteristics first priority is *clear and correct code*
	- "premature optimization is the root of all evil, or at least most of it" [[C.A.R. Hoare]], [[Donald Knuth]]
	- only useful to improve performance if performance improvement is significant
- second common mistake is to ignore performance characteristics entirely
- pay attention to cost and developing clean and clear programs, and will reap the benefit every time you use it
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
- [[sorting]] problem is to arrange an array of items into ascending order
- keeping things in order makes it much easier to [[search]] and is critical to the performance of many applications
- Sorting and searching important for
	- commercial applications
	- scientific applications
	- data compression
	- computer graphics
	- computational biology
	- numerical computing
	- combinatorial optimization
	- computational biology
	- cryptography
- *efficient algorithms* are key to effective solutions to computational problems
- Many searching and sorting algorithms available, which should we use?
- 
#### Binary Search (533)
- twenty questions with a number and asking whether higher or lower demonstrates principle
[[binary search]]
- **base case:** if *hi-lo* equals 1 then secret number is *lo*
- *reduction step:* ask if secret number is greater than or equal to *mid*,
	- *mid = lo + (hi-lo)/2*
	- If so repeat in range $[mid,hi)$
	- If not repeat in range $[lo, hi)$
##### Correctness proof (535)
- Need to be convinced the algorithm correct and always leads to the secret number
- Establish following facts
	- Interval always contains secret number
		- enforced by code
	- Interval sizes are the powers of 2, decreasing from $n$
		- follows from noting that if $(hi-lo)$ is a power of 2 then $(hi-lo)/2$ is the next smaller power of 2
- Basis of induction proof that algorithm works as intended
- Eventually interval size becomes 1, leaving only answer
##### Analysis of running time (535)
- Let $n$ be number of possible values
- $n=2^k$ where $k = lg(n)$
- Let $T(n)$ be the number of questions
- Recursive strategy implies $T(N)$ should satisfy recurrence relation
$$T(n) = T(n/2)+1$$
-  with $T(1) = 0$ 
- can [[telescope]] the recurrence
$$T(2^k) = T(2^{k-1}) +1 = T(2^{k-2}) +2 =...= T(1)+k = k$$
- substitute $n$ for $2^k$ and $lg(n)$ for $k$
$$T(n) = lg(n)$$
##### Linear-logarithmic chasm (535)
- alternative would be a [[brute force search]]
- *enormity of difference between n and lg(n) is key to understanding importance of algorithm design and analysis*

##### Binary Representation (536)
- nearly same computation as converting a  number to binary (`program 1.3.7`)
- in example know number is between 1 and 127 means number of bits in binary representation is 7 
- If special number is 77 sequence of answers is `no yes yes no no yes yes no` yields `1001101` the binary representation of 77
- thinking in terms of binary is another way of undertsanding the [[linear-logarithmic chasm]]
	- when running time is *linear* in a parameter $n$ run time is proportional to the *value* of $n$
	- when run time is *logarithmic* it is proportional to the *number of digits* in $n$
##### Inverting a function (536)
- binary search useful for computing the [[inverse of a function ]] (increasing function) $f(x)$
	- given a value $y$ find a value $x$ such that $f(x)=y$
- in this context *binary search* often referred to as [[bisection search]] since interval is bisected at each stage
##### Binary search in a sorted array (538)
- one of the most important uses of [[binary search]] is finding information using a key to guide the search
	- similar to using alphabetical order to find info in a phone book or dictionary
	- 

##### Exception filter (540)
- [[existence problem]] does a key exist in a sorted array of keys
- need to adjust binary search to return a value indicating if key is not located int the array
- [[exception filter]] reads in a sorted list (known as a [[whitelist]]) of strings and prints those that do not appear
##### Weighing an object (540)
- can determine the weight of an object using only weights that are powers of 2 with binary search

#### Insertion sort (543)
- *insertion sort* requires [[quadratic time complexity]] for many situations, meaning we should consider faster potential algorithms to sort large arrasy
- [[binary search]] requires that the data is sorted
- [[sorting]] also has many other applications
- [[insertion sort]] naïve brute force sorting algorithm
	- similar to how people arrange a shuffled deck of playing card
		- consider each card one at a time
		- insert each into proper place with cards that have already been sorted
```java
public static void sort(String[] a){
	int n = a.length;
	for(int i = 1; i < n; i++)
	{
		for(int j = i; j > 0; j--){
			if (a[j-1].compareTo(a[j]) > 0) 
				exchange(a, j-1; j);
			else break;
			
		}
	}
}
```
- at the beginning of an iteration all elements up to `i` will have been previously sorted
- the inner loop then sorts `i` into the proper place checking if it should be placed before the previous element and `exchange`s it if so. 
- This continues until a value is reached that should rpeced the lement, or the beginning of the list is reached
- the outer loop then iterates to the elemnet that was after `i` at the start and repreats the process of sorting this
- this continues until the end of the list is reached and all elements have been sorted

>At the beginning of each iteration of the outer for loop, the first i elements in the array are in sorted order; the inner for loop moves a[i] into its proper position in the array by exchanging it with each large value to its left, moving from right to left, until it reaches its proper position. Here is an example when i is 6:
>
> ![Insertion sort iteration](https://introcs.cs.princeton.edu/java/42sort/images/insertion-iteration.png)
>
This process es executed first with i equal to 1, then 2, then 3, and so forth, as illustrated in the following trace.
>
> ![Insertion sort trace](https://introcs.cs.princeton.edu/java/42sort/images/insertion.png)

##### Analysis of running time (544)
- Inner loop is a double nested for loop suggesting [[quadratic time complexity]], but cannot be sure yet as there is a `break` statement, 
- this means the run time can vary based on how the input arrives
	- *best case* if array is already in sorted order the `break` is reached immediately and inner loop is only iterated once for each outer loop index, meaning it will run with [[linear time complexity]] 
	- *worst case* if array is in descending order meaning the inner loop will run completely through with no `break` and frequency of execution $1 + 2 +...+n-1 \approx \frac{1}{2} n^2$ meaning [[quadratic time complexity]]
	- *average case* expect array to be randomly sorted where each element equally likely to fall into any position, and on average expect any element to only need to move halfway to the left and the program will execute $n^2/4$ cycles meaning the average case has [[quadratic time complexity]]
##### Sorting other types of data (545)
- want to be able to sort many types of items, and need a general *functional abstraction* to work with
- we can sort an array of any object as long as we can assume that elements can be compared as larger or smaller
- Jav provides the `java.util.Comparable` interface for this
```java
public interface Comparable<Key>
int compareTo(Key b) //compare object with b for order
```
- compares objects so that `a.compareTo(b)` 
	- negative `int` if `a` is less than `b`
	- positive if `a` is greater
	- `0` if they're equal
- `compareTo()` must define a [[total order]] requiring 3 properties to hold
	1. [[Antisymmetric]] if both $x \le y$ and $y \le x$ then $x=y$
	2. [[Transitive]] if both $x \le y$ and $y \le z$ then $x \le z$
	3. [[Total]] either $x \le y$ or $y \le x$ or both
- this type ordering applies to many types of ordering
- data types that follow this ordering are [[comparable]] with their associated total order is known as [[natural order]]
- can create data types that follow this type of order using [[implements keyword]] and adding a [[compareTo() method]] 
```Java
public class Counter implements Comparable<Counter{
	private int count
	public int compareTo(b)
	{
		if      (count < b.count) return -1;
		else if (count > b.count) return +1;
		else                      return  0;
	}
}
```
##### Empirical analysis (548)

##### Sensitivity to input
- when algorithm performance is sensitive to the input values may not be able to make accurate predictions without accounting for that

#### Mergesort (550)
- originally created by [[John von Neumann]], he recognized (554)
	- sorting is essential to many applications
	- [[quadratic time complexity]] is often too slow for practical purposes
	- [[divide-and-conquer]] strategy is effective
	- proving programs correct and knowing cost is important
- [[mergesort]] utilizes the [[divide-and-conquer]] strategy of algorithm design to implement a faster seach method
	- can often solve a problem by *dividing* into independent parts and *conquer* each independently then compose those smaller solutions into a complete solution for the whole
- To sort an array with this strategy with [[mergesort]] 
	- divide it into two halves
	- sort the halves indpendently
	- *merge* results to sort full array
- [[mergesort]]
	- *base case*: if sunarray is length 0 or 1 it is already sorted
	- *reduction step*: compute `mid = lo + (hi - lo)/2`, recursively sort the two subarrays `a[lo, mid)` and `a[mid, hi)` and merge
##### Analysis of runtime (553)
- frequency of execution is proportional to the sum of subarray lengths
- quantity emerges when calls arranged on levels by size
- $k = lg(n)$ levels and each call has $n$ operations
- leaves us with a [[linearithmic time complexity]] $\mathcal{O}(n*lgn)$
##### Quadratic-linearithmic chasm (553)
- difference between $n^2$ and $n \log(n)$ makes a practically signifcant difference in sorting, more so as input size grows large
	- closer to [[linear time]] than [[quadratic time]]

##### Divide-and-conquer algorithms (554)
- [[divide-and-conquer]] useful paradigm for solving many algorithmic problems

##### Reduction to sorting (554)
- A problem [[reduces]] to another problem if we can use the solution from the reduction to solve the original
- with [[divide-and-conquer]] simpler approach is often better
	- given a new problem how would you solve if the data were sorted
	- simple linear pass through data can often accomplish task
- [[element distinctness]] trying to find if values in an arrray are all distinct
	- sort the array
	- pass through arrays to check whether any element is equivalent to the next
	- if end is reached and this never returns true then all values are distinct
- can also be used for the [[median]] 

#### Application: frequency counts (555)

##### Computing frequencies (555)

##### Sorting frequencies (556)

##### Zipf's law (556)
- [[Zipf's law]] frequency of the $i$th most frequent word in a text of $m$ distinnct words is proportional tto $1/i$ 
- with [[constant of proportionality]] the inverse of the harmonic number $H_M$
	- second most common word should appear half as often as the first

#### Lessons (558)
- majority of programs inolve *managing the complexity of addressing new pracical problems by*
	- developing *clear and correct* solution
	- breaking problem into manageable modules
	- testing and debugging solutions
- The *clear and correct solution* is not always sufficient due to computational cost

##### Respect the cost of computation (558)

##### Reduce to a known problem (558)

##### Divide-and-conquer
#### Terms
#### Propositions
#### Questions
#### to-do
- [x] **3.1.1** `reverse()` **pg 373**
	- [ ] properties of `substring`
	- [ ] attempt with character array
- [ ] **2** *problem*  **pg**
- [ ] **3.** *problem*  **pg**
- [x] **3.1.4.** `GrayScale` histogram  **pg 373**
	- [ ] pictures and standard input
	- [ ] pictures and standard output
	- [ ] piping pictures 
- [x] **3.1.5.** *flip picture horizontally*  **pg 373**
	- [ ] **remember** can swap pixels as the new picture so only have to traverse half the width
- [ ] **6.** *problem*  **pg**
- [ ] **7** *problem*  **pg**
- [ ] **8.** *problem*  **pg**
- [ ] **9.** *problem*  **pg**
- [ ] **10.** *problem*  **pg**
- [ ] **11.** *problem*  **pg**
- [ ]  **12.** *problem*  **pg**
- [ ] **13.** *problem*  **pg**
- [ ] **4.2.14.** modify `Counter` to implement `Comparable` *problem*  **pg 561** 
- [ ] **4.2.15.** modify `Merge` to support sorting subarrays  **pg 561**
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