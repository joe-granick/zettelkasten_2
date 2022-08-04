
---
aliases: ['2a6b']
---
Added: 202208041207
Status: #permanent-note 
Tags:
Links: [[markdown]]


```Java
public class NewtonsMethodSqrt{
	public static void main(String[] args){
		double c = Double.parseDouble(args[0]);
		double EPSILON = 1e-15;
		double t = c;
		while (Math.abs((t*t)-c) > EPSILON){
			t =  ((c/t) +t)/2.0;
		}
		System.out.println(t);
	}
}


```
