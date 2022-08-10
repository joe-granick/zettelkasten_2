#flashcards/intro-to-cs/exam-1 
Q. (10 points) Write a program in pseudocode that reads a 3-digit number and determines if the number is a palindrome or not. A number is a palindrome if it reads the same from left to right and right to left. For example, 121, 212 are palindromes, but 122 is not. You may use the operators / and % to complete this assignment. You are not allowed to use loops. The program must display the messages “Palindrome” or “not Palindrome”.
*Note: Given a problem write an algorithm using Pseudocode (no loops)*
?
A.
``` md
READ number
COMPUTE firstDigit as number / 100
COMPUTE thirdDigit as number % 10
IF (firstDigit == thirdDigit)
	DISPLAY “Palindrome”
ELSE
	DISPLAY “not Palindrome”
ENDIF
```