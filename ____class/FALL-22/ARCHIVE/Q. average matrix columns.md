# Question
For a matrix `double[][] arr` of row length `m` and column length `n` calculate each column average and store in a new array
## Answer
```java
double colAvg[] = new double[m];
for (int col = 0; col < n; col++){
	double sum = 0.0;
	for (int row = 0; row < m; row++)
		sum+= arr[row][col];
	colAvg[i] = sum/m;
}
```
### Further review
