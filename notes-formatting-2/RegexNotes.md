[I] All regex knowledge
[Q] Show me all knowledge on regex.
[Q] What are all the things you can tell me about regex?   

Here's a list of everything I know about regex:   
[M: Representing a set of characters in regex] Representing a set of characters in regex   
[M: Repeating regex patterns] Repeating regex patterns   
[M: Representing exact strings in regex] Representing exact strings   
[M: Anchoring patterns in regex] Matching patterns at the beginning or end of strings   
[M: Regex capturing groups] Regex capturing groups   
[M: Regex greedy expression] Regex greedy expression   
[M: Regex lazy expression] Regex lazy expression   
[M: Using regex in coding] Using regex in coding   
[M: Built-in character representation] Built-in character representations in regex

Here are all the examples on regex:   
[M: Regex examples] Regex examples   


[I] Regex summary
[Q] What is regex?
[Q] What is regex used for?   
[Q] Give me a summary of regex.

Regex, short for regular expression, is a notation that represents patterns in a string.   
You can use regex to you search for or match patterns in a string. It can be used to extract information from a string or validate a string's format.   

For a more detailed explanation, refer here:   
[M: Regex long explanation] Regex long explanation   

The following list contains some basic regex notations.   
If you are new to regex, I recommend going through all of them.   
Or you can learn from examples.   
[M: Representing a set of characters in regex] Representing a set of characters
[M: Repeating regex patterns] Repeating patterns   
[M: Representing exact strings in regex] Representing exact strings   
[M: Anchoring patterns in regex] Matching patterns at the beginning or end of strings   
[M: Regex capturing groups] Regex capturing groups
[M: Built-in character representation] Built-in character representations in regex

Here are some examples:   
[M: Regex examples] Regex examples   

Here's how to use regex in coding:   
[M: Using regex in coding] Using regex in coding   


[I] Regex long explanation
[Q] Give me a long explanation of regex.
[Q] Explain to me in depth what regex is.
Regex, short for regular expression, is a way of representing patterns in text.   
For example, the regex `^\(\d\d\d\)\d\d\d\-\d\d\d\d$` represents the format for a phone number with a three digit area code and a seven digit number.   
Every regex equals to a set of texts. The phone number regex we mentioned represents the set of all phone numbers in the defined format.
Thus, any string that is an element of that regex set is formatted as a phone number.   
Regular expressions can be used in computer programs to verify that a given string follows a regex pattern or to search for a certain pattern in a body of text.   

For a simplified explanation, see here:   
[M: Regex summary] Regex summary   

For examples, see here:   
[M: Regex examples] Regex examples   


[I] Representing a set of characters in regex
[Q] How do I represent a set of characters in regex?
[Q] What regex notation represents a set of characters?
[Q] How do I define a regex pattern that contains a set of possible characters?
[Q] What are square brackets used for in regex?
[Q] How do I define a range of numbers or letters in regex?
[Q] How do I search for a set of possible characters using regex?   

`[]` (square bracket) represents any single character identified inside the brackets. For example, `[abc]` is equal to `a`, `b`, or `c`.   
Special symbols can be used to further define the set of possible characters   
* `-` (dashes) represents a range of characters. `[a-zA-Z0-9]` will represent any single uppercase letter, lowercase letter, or digit.   
* `^` (carrots) exclude any characters in the brackets. `[^a-c]` represents any single character that is not `a`,`b`, or `c`.   
* `.` (dot) represents any single character. `a`, `1`, `+`, `[`, etc. all are all valid representations.   

Note:
* You can also represent symbols. However, note that some symbols like `-` and `[]` must be escaped using a backslash `\`.   
* You can place these single character notations next to each to represent multiple single character notations. For example, `[ab][cd]` can represent `ac`.   


[I] Representing a set of words in regex
[Q] How do I represent a set of words in regex?
[Q] How do I represent a set of character combinations in regex?
[Q] What regex notation represents a set of characters?
[Q] How do I search for a set of words?
[Q] How do I search for a set of character combinations?

You can use a vertical bar, `|`, to represent a set of character combinations. To use this, you can write the regex `hello|bonjour|hola` to match the words `hello`, `bonjour`, or `hola`.   

If you want to represent a set of characters (only), you can use square brackets instead.   
[M: Representing a set of characters in regex] Representing a set of characters in regex   

If you want to exclude a set of words, you can use negative lookaheads:   
[M: Negative lookahead] Negative lookahead


[I] Negative lookahead
[Q] How do I exclude words in regex?
[Q] What regex symbol allows me to exclude words?
[Q] How do I match a string in regex that excludes words?

To write regex that excludes words, you can use a negative lookahead `?!`.   
Suppose you want to exclude the words `hello`, `hi`, you can write `(?!hello|hi)`.   

[M: What does the vertical bar represent?] Representing a set of words in regex


[I] Repeating regex patterns
[Q] What regex notation repeats characters or patterns?
[Q] How do I repeat some part of an expression in regex?
[Q] How do I repeat a character a specific number of times?   

* `*` (star) repeats the regex representation that precedes it zero or more times. For example, `a*` can represent anything from a blank string to `aaa`.   
* `+` (plus) is similar to `*` but repeats one or more times.   
* `{}` (curly brackets) repeats the preceeding regex a specific number of times, specificed by the number inside the brackets. `a{3}` represents `aaa`.   
You can use the above symbols to repeat expressions. For example, `[abc]*` can be `a`, `aaa`, or `aaabbbccc`.   


[I] Representing exact strings in regex
[Q] How do I search for an exact string in regex?
[Q] How do I represent strings exactly in regex?
[Q] Do I need special notations to compare word for word using regex?
[Q] How to compare word for word using regex?   
To represent an exact string in regex, simply write the exact strings without any special symbols. `Hello` in regex represents the string `Hello`.


[I] Anchoring patterns in regex
[Q] How do I search for patterns at the [location on string] of a string?
[Q] How do I check if the [location on string] string matches a regex pattern?
[Q] How do I write a regex pattern that matches [location on string] string?
[Q] What is an anchor in regex?   

You can anchor in regex by using the following terms:
[M:] How do I search for patterns at the beginning of a string?   
[M:] How do I search for patterns at the end of a string?   


[E] Exact
[E] Exactly
[E] Entire
[E] Whole

Regular expressions by default equal a set of texts that _contain_ the expressed pattern. So the regex `[abc]` expresses the string `apple` because the `a` at the beginning matches the regex pattern.   
To define a set of text that entirely follows a regex pattern, you can place anchors, `^` (caret) and `$` (dollar sign), around the expression. For example, `^[abc]$`.  

Here's what they mean.
[M:] How do I search for patterns at the beginning of a string?   
[M:] How do I search for patterns at the end of a string?   

Here's an example:   
[M:] Regex example 1   


[E] Beginning
[E] Start
`^` can be used at the beginning of a regex to state that a string must begin with the regex pattern. An example is the regex `[abc]` and the string `apple`.   


[E] End
`$` can be used at the end of a regex to state that a string must end with the regex pattern. An example is the regex `[abcd]` and the string `Hello World`.   


[I] Regex capturing groups
[Q] What is grouping in regex?
[Q] What does it mean when my regex matches multiple groups?
[Q] Tell me what grouping means in regex.
In regex, grouping is a way of specifying and enclosing sub-expressions of a regex. This way, it is easy to refer to those sub-expressions when, suppose, matching a string to a regex.
Grouping is done using parenthesess, `()`, to enclose the sub-expression.   

When used in coding, you can refer to each group in a regex by an index value. The first group is the one with its parenthesis `(` the furthest left, and the rest of the group ordering follows.   
For example, regex `((a|b|c)abc)(123)` has group #1 as `((a|b|c)abc)`, group #2 as `(a|b|c)`, and group #3 as `(123)`.   


[I] Regex greedy expression
[Q] What are greedy expressions in regex?
[Q] Why does my regex match the longer pattern first?
[Q] What does it mean for an expression to be greedy?

Greedy expressions describe the behavior of a regex sub-pattern when it matches to strings. They come into effect when they are in capturing groups.   
When a regex with capturing groups matches a string, there may be multiple valid matches such that each capturing group can capture multiple substrings.   
This occurs when there are repeats (like `*` and `+`) in capturing groups.   
[M: Repeating regex patterns] What are repeats?   
[M: Regex capturing groups] What are capturing groups?   

To decide on one valid match, regex by default maximizes the capturing groups with repeats. This is called a greedy behavior.   

You can also set an expression to be lazy:   
[M: Regex lazy expression] Regex lazy expression   

Here's an example:   
[M: Regex example 2] Regex example   


[I] Regex lazy expression
[Q] What are lazy expressions in regex?
[Q] Why does my regex match the shorter pattern first?
[Q] What does it mean for an expression to be lazy?

Refer here if you are unfamilliar to expression behaviors. 
[M: Regex greedy expression] What are greedy expressions?

To make a repeat expression lazy, you can add a question mark `?`. For example, these expressions `.*?`, `.+?` are lazy.    

Here's an example:   
[M: Regex example 3] Regex example   


[I] Built-in character representations in regex
[Q] Does regex have built-in character representations?
[Q] Show me regex's built-in character representations.
[Q] How do I represent [character type] in regex?
[Q] What's the symbol for [character type] in regex?

Regex provides some built in representations of some characters.
Here's a list of some common ones:   
[M: How do I represent digits in regex?] Digits   
[M: How do I represent whitespaces in regex?] Whitespaces   
[M: How do I represent word characters in regex?Letters and numbers] Letters and numbers    


[E] numbers
[E] digits
[E] 0-9

You can represent numbers 0-9 in regex as the symbol `\d`.   


[E] whitespaces
[E] blank spaces
[E] all blank spaces

You can represent whitespace characters in regex as `\s`. This includes all types of whitespace like the single space, tab, newline, etc.   


[E] word characters
[E] letters
[E] letters and numbers
[E] numbers and letters

You can use the regex symbol `\w` to represent all letters (lowercase and uppercase), underscore `_`, and numbers 0-9.   


[I] Regex notations reference
[Q] Show me a list of regex notations.
[Q] Show me the regex cheat sheet.   

[Regex Reference](http://www.rexegg.com/regex-quickstart.html)


[I] Using regex in coding
[Q] How do I use regex in [programming language]
[Q] How do I represent a regex pattern in [programming language]

I can teach you about using regex in the following programming languages:   
[M: How do I use regex in C#?] C#
[M: How do I use regex in Java?] Java


[E] programming
[E] programming language
[E] programming languages
[E] coding   
Most programming languages provide libraries that can match regex to text.   
Below are some guides to use regex in various programming languages.    
[M: Regex in C#] Regex in C#
[M: Regex in Java] Regex in Java   

[E] C#   
C# has the classes `Regex` and `Match` to compare strings and regex. You can import these packages from this namespace `System.Text.RegularExpressions`.   

Suppose you have strings `text` and `regex`, where `text` represents the string in which you want to search for a pattern, and `regex` is the pattern you are searching for.
You can perform a regex match like this:   
``` c#
Match match = Regex.Match(text, regex);
```
`match.Success` is a boolean that will tell you whether the regex pattern matches the text.   
If the matching is a success, you can retrieve the matching result from `match.Groups[index].Value`, just specify the integer `index`. By default, all successful regex matches will have `match.Groups[0]`, which is the part of `text` that matches the entire pattern in `regex`. The rest of the slots in `match.Groups` contains the matched string for each group in `regex`.   

For information on regex capturing groups and their ordering, refer here:   
[M:] Regex capturing groups   

Matching regex patterns and strings is pretty flexible in C#. You can play around with the `Match` and `Regex` classes to find new tools and different ways of matching.   

Depending on your requirements, you may want to create a `Regex` object using your regex string.
Here's an example.
``` c#
Regex r = new Regex(regex);
Match m = r.Match(text);
```

You can also customize some aspects of regex matching. The class `RegexOptions` helps you set options to ignore case, match regex for every line of a text, etc.   
To use this, you can do `Regex.Match(text, regex, RegexOptions.IgnoreCase)` for example, or `new Regex(regex, RegexOptions.IgnoreCase)` if you want to initialize a `Regex` variable.

Here's a reference to notations in regex that are compatible with .NET.   
[.NET Regex Reference](https://docs.microsoft.com/en-us/dotnet/standard/base-types/regular-expression-language-quick-reference)


[E] Java   
[Java Regex Reference](http://www.tutorialspoint.com/java/java_regular_expressions.htm)