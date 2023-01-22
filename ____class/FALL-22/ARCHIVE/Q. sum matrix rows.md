# Question
For a matrix `int[][] arr` of arbitrary row and column size calculate each row sum printing each sum on a new line
## Answer
```java
//traverse in row major order and retrun row sums
for(int i = 0; i < arr.length; i++){
	int sum = 0; //for each new row reset sum to 0
	for(int j = 0; j < arr[i].length; j++)
		sum + = arr[i][j]; //sum all elements in row
	//when all c's in row are in sum, print and move to next line 
	System.out.prinln(sum);  
}
```


### Further review
- [[row-major order]]