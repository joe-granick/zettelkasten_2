# Question
**Declare, create and initialize** an `int` array `a` of length `n` with values equal to the array index
## Answer
> **Array Creation**
> Making an array in a Java program involves three distinct steps:
	-   Declare the array name.
	-   Create the array.
	-   Initialize the array values.
```Java
int[] a;                    // declare the array
a = new int[n];             // create the array
for (int i = 0; i < n; i++)    // elements indexed from 0 to n-1
   a[i] = i;                 // initialize all elements to 0.0
```
### Further review
- [[array creation]]
- [[array declaration]]
- [[array intialization]]
