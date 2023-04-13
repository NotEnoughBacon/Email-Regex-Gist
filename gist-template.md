# Email Regex

Regex is a common word meaning "regular expression". A regex is a string of characters that defines a search pattern that are made up of a combination of letters, numbers, and special characters that use regex syntax. Here is an example of an email's regex.
```
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
```

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Character Escapes](#character-escapes)

### Anchors
There are two types of anchors in email regex: 
1. The caret: `^`<br/>
The caret anchor matches the start of the input. For example the regex `^hello` matches the work `hello`, only if its at the beginning of the input string. This would be the users email.

2. The dollar sign: `$`<br/>
The dollar sign does the same as the caret, but for the end of the input string. So `world$` would match `world` only if it appears at the end of the input string. This would be the users email controller.


### Quantifiers
The two used quantifiers in email regex are:
1. The plus sign: `+`<br>
The plus sign matches ONE or more occurrences of that portion of the string. So the regex `[a-z0-9_\.-]+` Shows you must have atleast one character before the `@` symbol of the email.
2. The curly braces: `{}`<br>
The curly braces specify how many characters are allowed to be in that group of characters. So `{2,6}` specifies the email controller must be between 2-6 characters.
### Grouping Constructs
As well as the curly braces above, there are two more groupings in our email regex:
1. Square brackets: `[]`<br>
The square brackets define a "class" which matches any one of the characters listed in the brackets. So `[a-z0-9_\.-]` defines that the beginning of the email address can be any letter a-z, number 0-9, have an underscore, dash, or a period.
2. Parentheses: `()`<br>
Parentheses are used to separate strings before special characters in the regex. So we separate the two groups of string inside of parentheses `([a-z0-9_\.-]+)@([\da-z\.-]+)` so we can allow the `@` inbetween

### Character Escapes
Character escapes are used to define a specific character that already has a meaning in regex. So in our email regex `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/` we often use `\.` to allow the use of `.` as a character vs using it in the regex expression.
## Author

This was made by Julian. Here is my [github](https://github.com/NotEnoughBacon).
