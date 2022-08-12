---
aliases: ['202207251929']
---
Status: #idea
Tags: [[String]], [[data-type]], [[Java]]

`Strings` are built-in to Java, but aren't primitives like their underlying characters. ^[[[Computer Science an Interdisciplinary Approach]]**pg 19**]

`Strings` are classes, with methods used to manipulate them and are composed of the atomic `char` data type.^[[me]] Even though they are built in^[[[Computer Science an Interdisciplinary Approach]]**pg 19**] `Strings` aren't consider primitive since primitive data types are not classes and do not have methods, rather operators are solely responsible for their manipulation, and primitive data-types must be atomic, not an abstraction composed of lower level components.^[[[me]]]

Strings are so critical to creating complex programs operations for input and output that Java often treats `Strings` like they are primitive data-types. They have a built in concatenation operator `+` much like a primitive, that is used to compose new strings from multiple `String` literals and or variables. They are also declarable and assignable like primitive data-types ^[[[202207251946-string primitive-like treatment critical for complex computing programs|202207251946]]]