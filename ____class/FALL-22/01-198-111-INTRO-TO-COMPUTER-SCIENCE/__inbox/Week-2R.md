---
aliases: []
---
Added: 202209150840
Professor:
TA:
Tags: #class #recitation
Topics: 
Textbooks:
Resources:
Assignments:
Dates:
Exams:
Pre-Requistes:
Pre-Requisites to:
Grades:
URL

# Notes
TA: Tiffany Lee 
Head TA: 
Code: **adddropweek**
- Extra recitation quizzes can be used to cover lost points
- Only get points for quizzes where lecture attended

# Structure
- 55 min once a week
- practice problems
- start with previous week lecture

# Resources
- study groups rlc.rutgers.edu
- Rutgers **Cave**:
	- Hill Center 252 to discuss CS
	- Check time?
- Piazza
	- can ask questions
# Psuedocode
- What is an algorithm 
- What is pseudocde
- What is role as coder
# Questions
## Create algorithm to determine if someone can vote, determine **inputs**, **outputs**

**INPUT**: age
**OUTPUT:** whether someone is eligible to vote

**READ** age
**SET** minVotingAge **AS** 18
**IF** age < 0
	**DISPLAY** please enter positive number
	**HALT**
**ENDIF**
**IF** age >= minVotingAge
	**DISPLAY** Can Vote
**ELSE** 
	**DISPLAY** Cannot Vote
**ENDIF**

## average of 5

**INPUT:** 5 numbers
**Output:** average of those 5 numbers
**Errors:** Non-numeric input

**READ** num1
**READ** num2
**READ** num3
**READ** num4
**READ** num5
**COMPUTE** sum **AS** num1 + num2 + num3 + num4 + num5
**COMPUTE** average **AS** sum/5
**DISPLAY** average

## ==Is it time to wake up?== Review on Website
- On vacation always wake up at 12
- Not on vacation wake up at
	- 9 on weekdays
	- 10 on weekends

**READ** vacation
**READ** day
**IF** Vacation 
	**SET** alarm **TO** 12:00
**ELSE** 
	**IF** day = M, T, W, T, F
		**SET** alarm **TO** 09:00
	**ELSE**
		**SET** alarm **TO** 10:00
	**ENDIF**
**ENDIF**

**TEST CASES**
- (Vacation = T, Weekday = T )
- (Vacation = F, Weekday = T)
- (Vacation = F, Weekday = T)

# to do
- [ ] Post recitation quiz
- [ ] review last pseudocode
- [ ] scarlet questions
# resources
- coding Bat
- java visualizer
- CS Discord
- Aresty
- 
 



