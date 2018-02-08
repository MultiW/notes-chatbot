[I] Regex examples
[Q] Show me regex examples.
[Q] What are some examples for regex?   

Here's an example on how to use regex:   
[M:] Regex example 1   
[M:] Regex example 2   
[M:] Regex example 3   


[I] Regex example 1
[Q] Show me how to write the regex for phone number.
[Q] Show me an example on how to write a phone number regex.
[Q] How do I write the regex for a phone number?
[Q] Show me regex example 1.

**Problem**   
Suppose we want to write a regex for a phone number format like the following: `(###)###-####`. Assume that this format is rigit, meaning we don't have to account for spaces between numbers or symbols.   

**Solution**   
Let us first represent each symbol in the telephone format.   
* The numbers, 0-9, is represented as `\d` in regex.
* The symbols `(`, `)`, and `-` have special meaning in regex, as in they do not match `(`, `)`, and `-`, but perform some function for regex. Since these symbols perform functions in regex, we can add a `\` before each symbol, like `\(`, to show that what we want is the actual symbols themselves.   

Now that we know how to represent each symbol in regex, we can place them in order according to the telephone format. 
We can simply replace the telephone format symbols with the regex symbols, resulting in `\( \d \d \d \) \d \d \d \- \d \d \d \d`.   
Note that the spaces added in the regex representation do not mean anything in regex, it is simply used to make the regex look nicer.   

Our current regex will match with any string that contains a telephone number, meaning strings like `bla bla (998)887-7665 bla bla` also matches our regex. This is useful in certain cases, but if we want to make our regex match only strings that are completely telephones, we can add anchors to our regex like this: `^\(\d\d\d\)\d\d\d-\d\d\d\d$`.   

[M: Anchoring patterns in regex] Learn more about anchors   


[I] Regex example 2   
**Problem**
Suppose we have this regular expression `(.*)(a|b|c|abc)`. If we match this regex to the string `something---abc`, what do each groups in this regex match to?

**Solution**
We must first note that the first group `(.*)` is greedy. If we match this expression to a string, say `something---abc`, the first group can match to `something---` if the second group matches to `abc`, or the first group can match to `something---ab` and the second group matches to `c`, and so on until there are no more possibilities. However, only one matching must be made. Since the first group is greedy, as we mentioned above, then it will make sure to maximize the character count of the first group, thus it will match the first group as `something---ab`.   

[M: Regex capturing groups] What are groups?   
[M: Regex greedy expression] What is a greedy expression?   


[I] Regex example 3   
**Problem**
Suppose we have this expression `(.*?)(a|b|c|abc)`. If we match this regex to the string `something---abc`, what do each groups in this regex match to?

**Solution**
We must first note that the first group `(.*?)` is lazy. If we match this expression to a string, say `something---abc`, the first group can match to `something---` if the second group matches to `abc`, or the first group can match to `something---ab` and the second group matches to `c`, and so on until there are no more possibilities. However, only one matching must be made. Since the first group is lazy, as we mentioned above, then it will make sure to minimize the character count of the first group, thus it will match the first group as `something---`.   

[M: Regex capturing groups] What are groups?   
[M: Regex lazy expression] What are lazy expressions?   