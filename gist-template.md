# Alphanumeric regex w/ spaces

This article is a walkthrough tutorial on how the alphanumeric regular expression works. It will go into detail on each part of the expression and describe how they
work seperately. Each section can be accessed throught the table of contents below.
An additional resource that may help during the tutorial process is https://regexone.com/.

## Summary

The regular expression that this tutorial will go over tests if the provided string or number only contains alphanumeric values. It looks like this:
```
/^[a-zA-Z0-9 ]*$/
```
Any special characters provided will including periods, explanations points or commas, will invalidate the expression. The provided string can include all capital and lowercase letters without causing errors. All numbers are also allowed as well.
Examples of this expression are:
```
/^[a-zA-Z0-9 ]*$/.test("Hi"); // true
/^[a-zA-Z0-9 ]*$/.test("user345"); // true
/^[a-zA-Z0-9 ]*$/.test("My name is Jenny"); // true
/^[a-zA-Z0-9 ]*$/.test(334); // true
/^[a-zA-Z0-9 ]*$/.test("!..."); // false
```

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Bracket Expressions](#bracket-expressions)

## Regex Components

### Anchors
The anchors present in this regex are these:
```
^
```
```
$
```
The caret checks to see if there is a match at beginning of the string. The dollar sign checks if there is a match at the end of the string. Together, they check if 
the expression is a full match, meaning the expression matches as the beginning middle
and end. An example of an anchor that uses a full match is...
```
 /^It's snowing$/.test("It's snowing"); // true
 /^It's snowing$/.test("There is snow"); // false
```
### Quantifiers
The Quantifier present in this regex is:
```
*
```
The star in the regex means that the characters may appear zero or more times as long as they are characters allows within the bracket expression (square brackets). This means that the characters provided in the expression can appear either not at all or as many times as it needs to.
An example of the "zero or more" quantifier is
```
console.log("200 10 3".match(/\d0*/g)); // ['200', '10', '3']
```


### Bracket Expressions
The Bracket Expressions/ranges present in this regex are these:
```
a-z
```
```
A-Z
```
```
0-9
```
```
(empty space)
```
The first expression means that all lowercase letters from a to z are permitted in the expression. The second expression means All uppercase letter from A to Z are also
allowed. The last two expressions mean that all numbers are allows and so are empty spaces.
An example of range bracket expressions is
```
/[a-zA-Z0-9 ]/.test("aA1"); // true
/[a-zA-Z0-9 ]/.test("!.%"); // false
```

## Author

If you have any questions about the repo, open
an issue or contact me directly at simone.anthony1@yahoo.com. You
can find more of me at [simone188535](https://github.com/simone188535)
