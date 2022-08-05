
---
aliases: ['2a6b']
---
Added: 202208041207
Status: #permanent-note 
Tags:
Links: [[markdown]]

# code blocks
- obsidian can indicate code wither inline or in a separate block
- using a separate block specific language can be used, and plug-ins provide syntax highlighting


# inline

This code is represented inline with other text `int i = 1`

## code
```md
This code is represented inline with other text `int i = 1`
```


# code block
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
}```

## code
```md
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
}```
```