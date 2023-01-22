# Question
What is the out put of the following string comparison
![[Pasted image 20221209153012.png]]
## Answer
![[Pasted image 20221209153027.png]]
even though `==` only compares object addresses, it does work a like a primitive equality comparison for `String` literals, as the compiler only keeps one copy of a string constant in memory and uses it everywhere that constant is used
![[Pasted image 20221209153637.png]]

### Further review
