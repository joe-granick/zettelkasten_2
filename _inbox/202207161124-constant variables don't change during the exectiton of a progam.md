---
aliases: ['202207161124']
---
Status: #idea
Tags: [[variables]], [[naming conventions]], [[constant variable]]

While variables can change over the course of program execution sometimes you will want variables that are meant to have a static value over the entire execution.

These are referred to as **constant variables**.^[[[Computer Science an Interdisciplinary Approach]]**pg 16**]

From the computers perspective they are no different than normal variables, and would change value if used in an operation like a normal variable ^[[[202207150840-variables store data-type values that can be changed referred by name|202207150840]]] 

Rather it is a useful design construct to refer to these static stores of value separately to identify them as serving a different purpose for the program. 

This separation is often indicated by using as separate naming convention, using all caps for the identifier^[[[Computer Science an Interdisciplinary Approach]]**pg 16**]