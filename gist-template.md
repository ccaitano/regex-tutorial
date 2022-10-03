# Regex Tutorial: Matching an Hex Value

A simple tutorial on a regular expression (regex) for matching a hex value.


## Summary

Given a series of characters this tutorial will aid in identifying a search pattern for hex values.

Example of Regex for a Hex Value:

```/^#?([a-f0-9]{6}|[a-f0-9]{3})$/```


## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Boundaries](#boundaries)
- [Back-references](#back-references)
- [Look-ahead and Look-behind](#look-ahead-and-look-behind)


## Regex Components


### Anchors

Anchors in regex match a position either before of after characters.

- `^` - Indicates the beginning of the text. For our Hex example, `/^#` indicates that our string must begin with a `#`
- `$` - Indicates the end of the text. For our Hex example, `$/` indicates that our string must either have 3 or 6 alphanumeric characters before the end of the string.


### Quantifiers

Quantifiers help match a number of instances of a particular character, group, or character class in a given string.

Exact Count - `{n}` - A number in curly brackets appended to a particular character or character class will specify how many characters or character classes you would like to match.

Example: `/\d{6}/` is equivalent to `/\d\d\d\d\d\d/` and will match a six-digit number. 

For our Hex example, `[a-f0-9]{6}` indicates that our string must match the preceding pattern of six caharcters of a, b, c, d, e, f, 0 , 1, 2, 3, 4, 5, 6, 7, 8,  or 9.

Zero or One - `?` - This is shorthand for either a boolean value or, 0 or 1. Usually this implies the preceding character is optional. For our Hex example, `/^#?` indicates that it is optional for '#' to appear at the beginning of our string.


### OR Operator

The `OR` operator or `|` signifies 'or' logic outside of brackets.

Example: `(a|b|c)` will return anything with an `a`, `b`, or `c`.

For our Hex example, `[a-f0-9]{6}|[a-f0-9]{3}` indicates that we can have either a string of six characters containing lowercase values of 'a' through 'f' and/or integers between 0 and 9 `OR` a string of three characters containing lowercase values of 'a' through 'f' and/or integers between 0 and 9.


### Character Classes

Character classes define which range of characters the regex is looking to match. Hyphens (`-`) are used to indicate the range of characters and more than one range can be specified. 

For our Hex example, `[a-f0-9]` indicates a lowercase value of a, b, c, d, e, or f `OR` an integer between 0 and 9.


### Flags

Flags are used at the end of a regex to define additional functionality or limits for the given regex.

- `g` - Global Search indicates the regex should be tested against all possible matches in a string.
- `i` - Case-Insensitive Search indicates case should be ignored while attempting a match in a string.
- `m` - Multi-Line Search indicates a multi-line input string should be treated as multiple lines.

However, for our Hex example, no flags are required.


### Grouping and Capturing

`()` are used to group the regex and treats the contents as a single unit. For our Hex example, `([a-f0-9]{6}|[a-f0-9]{3})` denotes that the pattern must match the contents prior to our end string anchor of `$/`.


### Bracket Expressions

A set of square brackets `[]` represents a range of characters that the user wants to include in their search. Again, for our Hex example, `[a-f0-9]` indicates a lowercase value of a, b, c, d, e, or f `OR` an integer between 0 and 9.


### Greedy and Lazy Match

In terms of regex, greedy indicates that a string should match the longest possible string, while lazy indicates that the string should match the shortest possible string. 


### Boundaries

Word boundaries are indicated by `\b` in terms of regex. This allows the user to perform a search for the entirety of the contents within the boundary specified. Our Hex example does not include any boundaries.


### Back-references

Back-references refer to the ability to match the same text as previously matched in regex. Commonly used to match pairs of opening and closing HTML tags. Our Hex example does not include any back-references.


### Look-ahead and Look-behind

Look-aheads and look behinds (commonly referred to as lookarounds), helps search for and identify other patterns without returning matches as a result. Again, our Hex xample does not include any lookarounds.


## Author

- [Github Profile](https://www.github.com/ccaitano)  
- [LinkedIn Profile](https://www.linkedin.com/in/cheryl-caitano-0a8a8250/)
- [Email Me](mailto:cheryl.caitano@gmail.com)

Cheryl Caitano &copy; September 2022