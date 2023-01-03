# Regex Expression - Matching an Email:

The following tutorial will explain the use of the regex to match emails, specifically useful in authentication purposes.

## Summary

The expresion, `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`, is used to find a specific pattern in a given string and validate it with a given form of the desired string.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [The OR Operator](#the-or-operator)
- [Flags](#flags)
- [Character Escapes](#character-escapes)

## Regex Components

### Anchors

This expression uses 2 anchors, `/^/`, and `/$/`, which are used to indicate the beginning and end of a string, respectively.

### Quantifiers

The most obvious quantifier in this expression at first glance is `/{2,6}/`, which indicates a range of 2-6 characters, in this case being used to verify the string having ".com" or another ending. The other quantifier that is used is the `/+/`, which in this case, is used to connect the user + service + .com

### Grouping Constructs

The main grouping construct used in this expression is `/()/`, which is used to indicate the specific portion of the string the expression is looking for. In this case, it surrounds the user, the service, and the .com sections.

### Bracket Expressions

There are 3 bracketed expressions in this larger expression. The first is `/[a-z0-9_\.-]/`, which matches a-z characters and is case sensitive, and also searches for characters 0-9, and "_","-", and ".". The second is `/[\da-z\.-]/`, which looks for any character a-z, case sensitive, as well as "-" and ".". The final one is `/[a-z\.]/`, which is a-z, again case sensitive, a single character thats 0-9, and ".".

### Character Classes

The only character class in this expression is `/\d/`, in the bracket expression `/[\da-z\.-]\`, which searches for a single character 0-9.


### Character Escapes

Character escapes are used to match with characters that have special meaning, so in this case our examples are `/\/` in `/[a-z0-9_\.-]/` which is used to switch from a-z, 0-9 to looking for the special characters, "." and "-", and in `/[\da-z\.-]/`, and `/[a-z\.]/` for the same use.

## Author

View my projects at https://github.com/awgore99