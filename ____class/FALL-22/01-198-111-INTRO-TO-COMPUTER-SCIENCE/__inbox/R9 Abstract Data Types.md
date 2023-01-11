### Problem 1: Palindrome
A Palindrome is defined as a string that is the same both forwards and backwards. For example, "bob" and "otto" are both palindromes, while “hello” is not.
1. Write a method that takes in a string and returns true if the string is a palindrome, false otherwise.
2. Modify this method so that the detection is not case sensitive. For example, "Bob" and "OtTo" should now return true.
3. Modify this method so that the detection ignores spaces. For example "nolemon,no melon" should now return true.

You may create three different methods like palindrome, palindrome2, and palindrome3.

Hint: Use `s.length()` & `s.charAt(i)`

```Java
public class class Palindrome
{
	public static boolean palindrome1(String word)
	{
	boolean isPalindrome = true;
	for(int i = 0; i < word.length()/2; i++)
		if(word.charAt(i) != word.charAt(word.length()-i))
		{
			isPalindrome = false;
			break
		}
	return isPalindrome;
			
	}
}

public class class Palindrome
{
	public static boolean palindrome2(String word)
	{
	boolean isPalindrome = true;
	int len = word.length();
	for(int i = 0; i < len()/2; i++)
	if(word.charAt(i).equalsIgnoreCase() != word.charAt(len-i).toLower())
		{
			isPalindrome = false;
			break
		}
	return isPalindrome;
			
	}
}
```

```java
string a
```


### Problem 2: Recursive Palindromes
Write a recursive method, `isPalindrome`, which takes a String as a parameter, and returns true if the String is a palindrome.

Note: For the purposes of this method, you may assume Strings with a length of 0 or 1 are palindromes.

Hint: Use `s.charAt` & `s.length()` & `s.substring(b, e)`




Problem 3: Anagrams
An anagram is a rearrangement of the letters of a word to form a new word. For example, an anagram of "listen" is "silent".

Write a method, anagram, that takes a String as input, and returns true if it is an anagram.

