---
aliases: ['202207171358']
---
Status: #idea
Tags: [[operator precedence]], [[Java]]


Java uses expressions to represent sequences of operations ^[[[202207150901- expressions compute new values by combining entities like formulas in math|202207150901]]] and consistent execution of the sequence requires a formalized rule set for the order of operation exaction or an **Operator Precedence**

Arithmetic operations follow the PEMDAS conventions of mathematics^[[[Computer Science an Interdisciplinary Approach]]**pg 17**]


| Precedence | Operators        | Description                       |
| ---------- | ---------------- | --------------------------------- |
| 1.         | $()$             | Parenthesis                       |
| 2.         | $x^n$            | Exponentiation                    |
| 3.         | $\star , / , \%$ | mutliplication, division, modulus |
| 4.         | $+, -$           | addition, subtraction             |

For operations with the same, sequences are exectuted in order of **left associativity**^[[[202207171413-operators of the same precedence are executed in order of left associativity|202207171413]]]

$$
p(a \mid b) = \frac{a \cap b}{p(b)}
$$

