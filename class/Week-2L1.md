---
aliases: []
---
Added: 202209121415
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

# Monday 2022-09-12
- **Annotated notes posted online**
- **Count Operations**
- Nested Statement
- **trace** nested for loops
- Nest **for** and **if** statements
## Comparison Operators 
- fundamental operation defined for *primitive data-types* allows comparison of values
- **Operand** - two expressions of the same type
- **Result** Boolean value
- **Operators**
	- `AND` returns `True` IFF all Operands True returns `False` otherwise
	- `OR` returns `True` if at least one operand true, returns `False` if all operands are false
	- `NOT` returns `True` if expression evaluates to False and `False` if expression evaluates True
## HALT Psuedocode
- Skips remaining operations when executed
## LO 1.1-1.3 Input output and error conditions
- **LO 1.1 Program 1**
	- **input:** Ana's cats, Ellen's cats
	- **output:** sum of Ellen and Ana cats
	- **errors:** cat input cannot be negative
- **LO 1.2 **
	- specify code to solve problem
	- use **if-then** to check that both inputs >=0
- **LO1.3 Program 1 (error handling)**
	- Need to design test cases for programs to determine validity of behavior
		- test cases need to cover **boundary conditions**
- **LO 1.3 Program 2**
	- **Input**
	- **Output**
	- **Error** 
```
READ number
IF number%2 is 0 THEN
	DISPLAY even
ELSE
	DISPLAY odd
ENDIF
```
## Analyzing code
- many potential ways to solve problem
- need to analyze for efficiency to decide what is best approach
- If not efficient, can it be improved?
- How to analyze code?
	- If we know code
		1. identify set of instructions
		2. count possible execution under different conditions
**Precondition:** certain constraints need to be met before using code (e.g. input needs to be of *integer data-type*)
	- can be used instead of error code
	- places responsibility on user for using appropriate input
**Boundary conditions**

**Program 4**
![[2022-09-12 (2).png]]
- can remove second check for `cakeSize >=6` because previous conditional check for `cakeSize<6` would have executed separate branch any was
- **test cases** designed to check boundary conditions
**Program 5**

![[class/chrome_RBbBWvCnl3.png]]
### Test cases
- may not be able to cover all test cases
- loop w/ +1,00,000 iterations, may not be able to write a test case for each potential execution

# Review
## Telling a computer what to do
- **Machine Language**
- **Natural Language**
- **High-level language**
## Algorithmic thinking
## Algorithm development
1. **Analyze**
2. **Solve**
3. **Evaluate**