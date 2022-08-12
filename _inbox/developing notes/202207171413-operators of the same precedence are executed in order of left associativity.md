---
aliases: ['202207171413']
---
Status: #idea
Tags: [[operator precedence]], [[left associativity]], [[Java]]

For operators of the same precedence, execution is ordered from left to right. ^[[[Computer Science an Interdisciplinary Approach]] **pg 17**]

For: 
- `a-b-c` 
- `a-b = x` 
- `a-b-c = x-c`

The result of the left most operation is evaluated, then the next leftmost operation is applied to the result. This continues until all operators of the precedence level are complete, which repeats at the next precedence level until expression evaluation is complete.

Operator precedence can be overridden by use of parenthesis.^[[[Computer Science an Interdisciplinary Approach]] **pg 17**]


For
- `a-(b-c)`
- `b-c =x`
- `a-(b-c) = a -x`

Even if precedence is correct, it is often good stylistic practice to make precedence specifci with parenthesis for verbose and complex expressions. ^[[[202207151835-style and naming conventions are crucial for understanding complex codebases and reducing tech debt|202207151835]]]
