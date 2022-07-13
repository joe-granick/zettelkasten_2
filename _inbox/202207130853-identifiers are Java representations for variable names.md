---
aliases: ['202207130853']
---
Status: #idea/
Tags: [[identifier]]

Variables need names to identify them, Java represents these names a **identifiers**.^[[[Computer Science an Interdisciplinary Approach]] **pg 15**]

Identifiers can be made up of a sequence of letters, numbers and currency symbols.^[[[Computer Science an Interdisciplinary Approach]] **pg 15**]

However they must start with a letter, other symbols are restricted, as are **reserved words**^[[[Computer Science an Interdisciplinary Approach]] **pg 15**]

Identifiers are case sensitive meanin `A` and `a` are assigned to different memory addresses ^[[[Computer Science an Interdisciplinary Approach]] **pg 16**]

Just because an identifier is valid doesn't mean it is good. For more readable and understandable programs it is important to follow stylistic conventions and use meaningful names.^[[202207130903-meaningful varable names following stylistic conventions important to managing complexity and writing undertsandble programs|202207130903]]

### Valid Identifiers
- `abc`
- `abc123`
- `Ab$`
- `a_b`
### Invalid Identifiers
- `Ab*`: invalid symbol 
- `1abc`: starts with number
- `a+b`: operator cannot be used in variable name
- `public`,`static`, `int`, `double`, `true`, `false`, `null`, `String`: **reserved words**