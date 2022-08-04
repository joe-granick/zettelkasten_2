---
aliases: ['2a7']
---
Status: #permanent-note 
Tags: [[LaTeX]], [[TeX]]

- 1977 Donald Knuth received proofs for second edition of "The Art of Computer Programming" and dissatisfied with style
- 1st edition published in 1968 was made using "hot metal printing"
- 2nd edition industry had changed to photo type setting
- Knuth created typesetting system $\TeX$ in order to produce that classic look with the goals of
	- **Accessible** high quality publications
	- Guarantee **reproducible** result on all computers
- Developed **METAFONT** as programming language to produce fonts, mathematical underpinnings allowed precise font definitions
	- meant to be used in tandem with $\TeX$ to  create reproducible documents
	- **METAFONT** creates letters $\TeX$ puts them on the page
- 80s Leslie Lamport extended $\TeX$ by compiling functions into a high level language $\LaTeX$ 
	- Now standard for scientific and mathematical publication
- Much like markdown **WYSISWYM**


#### inline
```md
$P(A \mid B) = \frac{P(A \cap B)}{P(B)}$
```

This is a formula $P(A \mid B) = \frac{P(A \cap B)}{P(B)}$ written **inline**


#### block
this is a formula written in a separate block
```md
$$\mu_x = \frac{1}{n} \sum_{i=1}^nx_i$$
```

$$\mu_x = \frac{1}{n} \sum_{i=1}^nx_i$$

---
https://www.youtube.com/watch?v=9eLjt5Lrocw