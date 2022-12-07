# Question
For a matrix `int[][] arr` of arbitrary row and column size calculate each column sum printing each sum with a space in between
## Answer
```java
//traverse in row major order and retrun row sums
```java
//traverse matrix in column-major order
for (int j = 0; j < arr[0].length; j++){
	int sum = 0; // reset sum for reach new col
	for(int i = 0; arr.length; i++)//loop over r's arr[i:n][j] 
		sum += arr[i][j]; // add element [r=i][c=j] to sum
	// when all rows in sum, print and move to next line
	System.out.print(sum + " ");
}
```


### Further review
- [[column-major order]]