# Regular Expression - Matching an Email

Regular expressions, often referred to as regex, refers to a distinct string usually made up of various sets of characters that can be used as both a query tool and a validator in code bases, as well as traditional documents. They were dervied in the early 1950s out of the concept of regular language coined by the mathemitician Stephen Cole Kleene. They became widely used in 1968 within the theoretical computer science field as a way to match patterns within text files and support lexical analysis. Although regular expressions are known for being extremely cryptic looking, when broken down piece by piece, one can see they are not quite as complex as they look to the untrained eye, and one could start writing their own regex expressions fairly easily.

## Summary

This tutorial will be covering the regex expression used for both matching and validating an email:

`^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$`

Imagine your a software developer tasked with finding all emails within a code base that were being utilized in a non-secure way. Searching through the code base and other documents using the regular expression shown above would help find all emails extremely quickly. The regular expression shown above can also be implemented as a string within a code base as a way of matching and validating an email. Making sure that when users fill out certain forms requiring a valid email address, the regex string can be implemented in a way that will not allow the user to continue until they have entered an unspecified number of characters, followed by an @ symbol, followed by a domain name an unspecified number of characters long, followed by the domain name system (in this example the domain name system needs to be between 2 and 6 characters long i.e. .com, .net, .dev, etc.).
