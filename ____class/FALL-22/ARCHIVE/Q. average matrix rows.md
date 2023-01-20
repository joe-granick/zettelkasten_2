# Question
For a matrix `double[][] arr` of row length `m` and column length `n` calculate each row average and store in a new array
## Answer
```java
//traverse in row major order and retrun row sums
double[] rowAvg = new double[m];
for(int i = 0; i < m; i++){
	double sum = 0.0; //for each new row reset sum to 0
	for(int j = 0; j < n; j++)
		sum + = arr[i][j]; //sum all elements in row
	rowAvg[i] = sum/n; 
}
```
### Further review
