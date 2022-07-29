---
aliases: ['202207181300']
---
Status: #idea
Tags: [[Java]], [[strongly typed]], [[declaration statement]], [[type safety]]

Java and other strongly typed languages require the variable's data type declared^[[[202207150859-declaration statements are how variables are allocated space in Java|202207150859]]] before initializing a value to ensure **type safety** at compile time.^[[[Computer Science an Interdisciplinary Approach]]**pg 18**]

Declaring a variable reserved the memory space for only values within that data-types set of possible values, this explicit safety mechanism prevents invalid values from being assigned to variables of incompatible data types, and prevents variables of different data types (or uninitialized variables) from being operated on in the same expression. ^[[[Computer Science an Interdisciplinary Approach]] **pg 18**]