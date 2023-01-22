# Question
- Use arrays to create a a deck of cards. The following arrays are reuired
	- `String[] rank`: containing card ranks from 2 - Ace
	- `String[] suit:` containing four card suits (clubs, diamonds, hearts spades)
	- `String[] deck` containing all 52 combinations of suit and rank
## Answer
![[Pasted image 20221109181749.png]]

### Follow up question
What happens if the order of the for loops is switched?
![[Pasted image 20221112143320.png]]
#### Answer
![[Pasted image 20221112143353.png]]

### Further review
- remember loop structure
- `suit[4]`: clubs, diamons, hearts, spade
- `rank [12`]: 2-10
- deck needs to range from elements 0 - 51
- `deck[i+13*j] = rank[i] = suit[j]
- [[array representation of a deck of cards]]
