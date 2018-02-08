# Regex notation notes

## Character sets
### Character sets
_How do I represent a set of characters?_   
_What are square brackets used for?_   

`[]` (square bracket) represents any single character identified inside the brackets. For example, `[abc]` is equal to `a`, `b`, or `c`.   
Special symbols can be used to further define the set of possible characters   
* `-` (dashes) represents a range of characters. `[a-zA-Z0-9]` will represent any single uppercase letter, lowercase letter, or digit.   
* `^` (carrots) exclude any characters in the brackets. `[^a-c]` represents any single character that is not `a`,`b`, or `c`.   

### Negative character sets
_How do I represent negative character sets?_
_How do I represent a set of non-characters?_

To define a character set that contains anything but some specified characters, use `^`.

Consider this regex `[^aeiouAEIOU]`.   
This regex matches any letters of the alphabet that isn't a vowel.

### Quantifiers
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

You can use the above symbols to repeat expressions as well as single letters. For example, `[abc]*` can be `a`, `aaa`, or `aaabbbccc`.   
---

## Anchors
_How do I match regex at the beginning of a string?_   
_How do I match regex at the end of a string?_   
_How do I write a regex pattern that matches an entire string?_   
_What are anchors?_

By default, a regex pattern matches any string that _contains_ the expressed pattern. So the regex `[abc]` can match the string `apple` because the `a` at the beginning matches the regex pattern.   
To define a regex pattern that matches strings entirely following the pattern, you can place anchors `^` (caret) and `$` (dollar sign) around the expression. For example, `^[abc]$`.  

`^`
- Used at the beginning of a regex to state that a string must begin with the regex pattern. An example is the regex `[abc]` and the string `apple`.   

`$`
- Used at the end of a regex to state that a string must end with the regex pattern. An example is the regex `[abcd]` and the string `Hello World`.   

## Escaped characters
_What are escaped characters?_   
_How do I escape a character?_   

When you have characters like `()` that has special meaning in regex, but you want to represent the parentheses symbol, you can escape the parenthesis symbols so that they represent the symbols themselves. `\(\)` matches to the string `()`.

## Character representations
_What does dot represent?_   
_How do I represent numbers in regex?_   
_How do I represent letters in regex?_   
_How do I represent spaces in regex?_   
_What do escaped letters mean in regex?_   

. represents any character
\d represents a digit [0-9]   
\s represents a whitespace char. Tab, space, newline etc.   
\w represents a word char [a-zA-Z_0-9]

Note, the uppercase version of the above symbols represent the negation of their character representations. So `\D` represents any char other than digits, or `[^0-9]`.

Here are representations for space characters:   
\s represents single space   
\t represents tab character   
\n represents new line character

<!--
*****If chat channel supports md tables, use this.
Symbol|Meaning
-|-
.|any character
\d|a digit [0-9]
\s|a whitespace char. Tab, space, newline etc.
\w|a word char [a-zA-Z_0-9]

Note, the uppercase version of the above symbols represent the negation of their character representations. So `\D` represents any char other than digits, or `[^0-9]`.

Here are representations for space characters:   
Symbol|Meaning
-|-
\s| single space
\t| tab character
\n| new line character
-->
