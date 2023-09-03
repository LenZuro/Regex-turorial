# Regular Expression - Matching an Email

Regular expressions, often referred to as regex, refers to a distinct string usually made up of various sets of characters that can be used as both a query tool and a validator in code bases, as well as traditional documents. They were dervied in the early 1950s out of the concept of regular language coined by the mathemitician Stephen Cole Kleene. They became widely used in 1968 within the theoretical computer science field as a way to match patterns within text files and support lexical analysis. Although regular expressions are known for being extremely cryptic looking, when broken down piece by piece, one can see they are not quite as complex as they look to the untrained eye, and one could start writing their own regex expressions fairly easily.

## Summary

This tutorial will be covering the regex expression used for both matching and validating an email:

`^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$`

Imagine your a software developer tasked with finding all emails within a code base that were being utilized in a non-secure way. Searching through the code base and other documents using the regular expression shown above would help find all emails extremely quickly. The regular expression shown above can also be implemented as a string within a code base as a way of matching and validating an email. Making sure that when users fill out certain forms requiring a valid email address, the regex string can be implemented in a way that will not allow the user to continue until they have entered an unspecified number of characters, followed by an @ symbol, followed by a domain name an unspecified number of characters long, followed by the domain name system (in this example the domain name system needs to be between 2 and 6 characters long i.e. .com, .net, .dev, etc.).

## Table of Contents 




## Regex Componets 

The regex components that define this particular expression are anchors, quantifiers, meta escape characters, character classes, single character matches, grouping and capturing, and bracket expression. Regarding the example used in this tutorial: `^` and `$` are the anchors used, `+` and `{2, 6}` are the two quantifiers, `\d` represents the meta escape character utilized, `[a-z0-9_\.-]`, `[\da-z\.-]`, and `[a-z\.]` represent the character classes, `_`, `\.`, `-` represent the single character matches used, `()` represents the way this regex expression utilizes grouping and capturing, and `[]` delinates the bracket expression used.


### Anchors 

Anchors within regex mark the start and end points of the expression. In regards to this expression, the `^` marks the start of the expression and the `$` marks the end of the expression. 

### OR Operator 

There are no OR operators within this particular regex expression but in general OR operators are represented with the pipe `|` and specified under the regex type of alternation.


### Flags

Regex flags are used to modify an expressions behavior -> case sensitivity, etc. There are only 6 of them in JavaScript -> i: case-sensitivity, g: looks for all matches, m: multiline mode, s: enables "dotall" mode that allows a dot `.` to match a newline character `\n`, u: enables full Unicode support, and y: "sticky" mode. 

The regex expression covered in this tutorial does not utilize flags.

### Quantifiers

Quantifiers are meta characters that modify the previous character in the regex and say, how many of those do I want to match in a row.

Quantifiers allow the specification of how many character or character classes should be matched.

### Bracket Expressions

`[]` create a character or group range and represent a single character. In regards to the regex expression this tutorial is covering, the brackets are used to separate each character class. The character can be anything specified within the brackets.

### Boundaries

`\b` is an example of a word boundary. It usually represents matching positions on either side; where once side is a word character and the other is something other than a word character.

Word boundaries are particularlly useful when you want to match a sequence of letters or digits on their own, to ensure they occur at the beginnning or end of a specific sequence of characters.

### Look-ahead and Look-behind

Usually represented with `?=foo`, look-ahead represents what immediately follows the string "foo", while look-behind, the inverse, is notated as `?<=foo` and represents what immediately precedes the string "foo".

### Back-references

Back-references are commands which refer to a previous part of the matched regualr expression. They are generally specified with a backslash and a single digit `\2`

### Greedy and Lazy Match

Greedy matching is a default behavior of regex where the regex engine will try to match a much of the string as possible, while lazy matching is the inverse and will try to match as little of the string as possible. 

- Greedy will keep searching until the condition is satisfied
- Lazy will stop searching once the condition is satisfied

### Grouping and Capturing

`()` creates a sequence or sub expression and is a way to treat multiple characters as a single unit. You will notice the regex expression being covered in this tutorial uses `()` to distinct groups of characters. The first set covers all characters before the `@` symbol. The second group coveres all characters before the `.`, and the last group covers all characters from the `.` to the end.

### Character Classes

Character classes are the attribute in a regex expression that allow us to define specific sets of characters that can be used in a search pattern.

The character classes utilized in this regex expression are `[a-z0-9_\.-]`, `[\da-z\.-]`, and `[a-z\.]`.

`[a-z0-9_\.-]`: `a-z` matches a single character in the range between a (index 97) and z (index 122) (case sensitive), `0-9` matches a single character in the range between 0 (index 48) and 9 (index 57) (case sensitive), `_` matches the character _ with index 9510 (5F16 or 1378) literally (case sensitive), `\.` matches the character . with index 4610 (2E16 or 568) literally (case sensitive), and `-` matches the character - with index 4510 (2D16 or 558) literally (case sensitive).

`[\da-z\.-]`: `\d` can be used to match any digit (0-9), `a-z` matches a single character in the range between a (index 97) and z (index 122) (case sensitive), `\.` matches the character . with index 4610 (2E16 or 568) literally (case sensitive), and `-` matches the character - with index 4510 (2D16 or 558) literally (case sensitive).

`[a-z\.]`: `a-z` matches a single character in the range between a (index 97) and z (index 122) (case sensitive), and `\.` matches the character . with index 4610 (2E16 or 568) literally (case sensitive)

Other examples of single characters:

`\d` can be used to match any digit (0-9), `\w` to match any alphanumeric character (a-zA-Z0-9), and `\s` any white space such as a space or a tab


### About the Author 

Len Zuro is a Front-End Dev who wants to be able to help create pretty and useful sites for all people to use and share. Len is a San Diego native and is looking for work as a remote frnt end dev !

[Link to Github](https://github.com/LenZuro)

[Link to Linkedin](https://www.linkedin.com/in/leonard-zuro-481175214/)

<a href="mailto:leoanrdzuro@gmail.com">leoanrdzuro@gmail.com</a>