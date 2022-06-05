# Matching Hexadecimal Values

In this Gist, I'll be summarizing the purpose and usage of regular expressions, also known as 'Regex', more specifically, how to match hex values with Regex.

## Summary

Before we start a discussion over the process of matching hex values with regular expressions, do you know what hex values are? Hexadecimal value notation is a system to represent specific color with the highest precision available for computation, it provides accuracy and consistency. Below is a code snippet of the regex we use for Hexadecimal matching...

```
/^#?([a-f0-9]{6}|[a-f0-9]{3})$/
```

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operators and Grouping](#or-operators-and-grouping)
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Bracket Expressions](#bracket-expressions)

## Regex Components

### Anchors

```
^
```
The preceding character signifies the beginning of a string, for example: `^example` signifies that the string will begin at `example`. In the scope of hexadecimal notation however, values must always begin with `#` so to initialize that, we have the following `^#`.
```
$
```
Just as we use special characters to initiate the string, we must also end with one so that the processing machine knows when to stop. We use the following `$` to signify when the string is completed, for example: `example$` signifies that the string will end at `example`. In this scope of hexadecimal notation, we only use 3, or 6 number values, so the string will end on the third or sixth character.

### Quantifiers

```
?
```
The first quantifier we have is a `?`, this is comparable to a conditional statement looking for the following `{3}` or `{6}`. Contingent on the hexadecimal values, depends on how many characters are containted in the string for a specific color.
```
{3} or {6}
```
The preciding provides us with length values for the hexadecimal notation. Some hex codes are just 3 characters, those being generalized colors when precision is not as necessary, while most other hex codes being 6 characters. Hex code length notation comes after the `#` designation.

### OR Operators and Grouping

```
([a-f0-9]{6}|[a-f0-9]{3})
```
Within the grouping above, we have an OR operator which states whether the length is 3 or 6 characters using the following grouping structure: `[a-f0-9]`

```
|
```
Since hex codes can have a length of either 3 characters or 6 charcters but no both, it needs to be seperated by an OR operator. It states that after the `#`, the following code to provide the hex value, it will be either 3 or 6 characters long.

### Character Classes

```
[a-f0-9]
```
In our specific class, we have 2 seperate criteria for characters that will be used for our hex values. The first of which being `a-f`, when using the alphabet for hex values, the code will never exceed `f`. The following letters will be used for hex values: `a`, `b`, `c`, `d`, `e`, and `f`, as well as the following numbers being used for hex values: `1`, `2`, `3`, `4`, `5`, `6`, `7`, `8`, and `9`.

### Flags

This regular expression does not contain any flags!

### Bracket Expressions

```
[]
```
Criteria for the given expression goes within square bracketing. The contents in these brackets are to be characters which are used to make up the hexadecimal notation expression, in our case: `[a-f0-9]`

## Author

Hello! I'm Travis, current student at the University of Oregons full stack software development bootcamp with the hopes of embarking on a new journey into the vast world of opportunity that is computer science. below is a link to my github, thanks for checking out my Gist on matching hexadecimal values for the purpose of precision color coding.

Check it out!
[GitHub](https://github.com/ValiantThor92)
