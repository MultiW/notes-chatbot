# Regex notation examples
## Example 1
Let's look at this regular expression (regex) `^[a-z][a-zA-Z0-9]*$`.   

This regex matches the following strings: `x`, `numStudents`, `obj1`.   
Here's why   
`x`
- The regex describes that the beginning of the string must follow the expressed pattern (because of the anchor `^`). So the string must begin with a letter from a to z (because of `[]`). `x` matches this condition.   
[M:] Anchors   
[M: Character sets] Square brackets   
- The matched string must then be followed by 0 or more of the characters `[a-zA-Z0-9]` (because of `*`). Since the string ends after `x`, it matches the pattern.   
[M: Repeating patterns] Kleen Star `*`

`numStudents`   
- The first letter of    the string, `n`, is a character from `a-z`. The rest of the characters include uppercase and lowercase letters. These are all in the character set `[a-zA-Z0-9]`.   

`obj1`
- This is similar to `numStudents`.   


This regex doesn't match the following strings: `Alphabet`, `2ab`, `next_value`.   
Here's why   
`Alphabet`
- The letter begins with a capital A, but the regex pattern enforces (with anchor) that the string must begin with lowercase letters `[a-z]`.   
`next_value`
- The first letter `n` is a lowercase letter.
- However, the rest of the letters include a `_`, which is not in the set `[a-zA-Z0-9]`.

## Example 2: Quantifiers
_What regex notation repeats characters or patterns?_   
_How do I repeat something zero or more times?_   
_How do I repeat something one or more times?_   
_How do I repeat a character a specific number of times?_   

`*` (star)
-  Repeats the regex representation that precedes it zero or more times. For example, `a*` can represent anything from a blank string to `aaa`.   

`+` (plus)
- Similar to `*` but repeats one or more times.   

`{}` (curly brackets)
- Repeats the preceeding regex a specific number of times, specificed by the number inside the brackets. `a{3}` represents `aaa`.   

`?` (question mark)
- An expression or character before it can appear zero or one times. For example, `a?bc` can match `bc` and `abc`.

You can use the above symbols to repeat expressions as well as single letters. For example, `[abc]*` can be `a`, `aaa`, or `aaabbbccc`.   



## Example 3: Repeating a pattern vs repeating a choice of character
Consider the following regular expression: `\( \d{3} \) \d{3} - \d{4}`   

Let's look at what these patterns represent   
The braces `{}` repeats the previous pattern, in this case `\d`. This means that the regex is equivalent to `\( \d\d\d \) \d\d\d - \d\d\d\d`.   
A string that matches this regex is any phone number in the proper format: (987)654-3333.   

Suppose then we have the regex `(\d\d\d) \1`. Note the parentheses have not been escaped.    
[M:] Escaped characters   
The escaped 1 repeats the contents in the first capturing group `()` before it. However, `\1` doesn't simply repeat the pattern of the capturing group, it also repeats the choice of character in the pattern.   
[M:] Capturing groups   
So a string that matches this regex would be 123123, and a string that doesn't match this pattern is 123456.

## Example 4: