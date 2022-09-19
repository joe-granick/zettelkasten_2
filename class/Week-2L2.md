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

# Wednesday 2022-09-14
- **Count Operations**
	- careful with branching operations
- **Error condition vs. pre-condition**
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