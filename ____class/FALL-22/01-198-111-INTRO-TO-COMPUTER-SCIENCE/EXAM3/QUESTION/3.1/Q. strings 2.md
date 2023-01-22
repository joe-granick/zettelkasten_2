# Question
What are the values of the strings after the following statements are executed?
![[Pasted image 20221209131453.png]]
## Answer
- `stringA`: "cat"
- `stringB`:  "house"
- `stringC`: "dog"
### follow up
If strings are immutable how is the value of `stringA` now "cat"
#### Answer
a new object with the identifier `stringA` is created and initialized with "cat" is created. "cat" is an entirely new object and `stringA` points to it, `stringC` points to the object that the previous `stringA` identifier points to
![[Pasted image 20221209131914.png]]
### Further review
