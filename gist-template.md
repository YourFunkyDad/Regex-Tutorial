# Regex Tutorial - HTML Tags

Regex, short for Regular Expressions, is the specification of certain special characters when defining a search pattern. The search pattern can have small to large amounts of requirements for whatever the use may be. This tutorial will cover the usage of a HTML-Tag Regex Search. 

## Summary

HTML tags contain < > as "open"  and "closed" tags. Examples include <main> , <body> , <footer> and so on. 

When a tag is opened, it must contain a closed tag as well to contain any code within the parameter. If it does not have a proper closed tag, the code will not run/function. This included multiple tags being opened within one another as well. 

HTML tags can include alpha-numeric and special characters, so a regex string-search must include a wide range of available characters. 

Example:

/^<([a-z]+)([^<]+)*(?:>(.*)<\/\1>|\s+\/>)$/

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
Patters must be wrapped in slash characters (/).

### Anchors
The character ^ indicates the beginning of a string, with any characters that follow it. The character $ indicates the end of the string, with all characters that precede it. 

Regex is CASE SENSITIVE!!

### Quantifiers
Quantifiers will set the limit on your string that the regex will match. This also applies to individual sections in the string too. Examples include:

* - Matches the pattern zero or more times. 

+ - Matches the pattern one or more times. Characters placed directly to the left of the + will only be matched. 

Example: 'Allred+' (The quantifier is only applied to the lowercase "d". Remember Regex is case-sensitive!).

? - Matches the pattern zero or one times. 

{ } - Sets Limits for a match:
    { 5 } - Matches the pattern EXACTLY 5 times.
    { 3, } - Matches the pattern AT LEAST 3 times. 
    { 3, 9 } - Matches the pattern for a minimum of 3 times to a maximum of 9 times.

    /^[a-z0-9_-$%@]{2,10}$/ - This example means the pattern will match any lowercase letters between 'a' and 'z', as well as matching patterns with numbers 0-9, the special characters of a underscore, hyphen, a dollar sign, and percentage sign, and the 'at symbol'. The quantifier also limits pattern to a minimum of 2 characters and a maximum of 10 characters. 

### OR Operator
The OR Operator is identified using the | symbol. The search pattern will match anything that precedes or follows |

### Character Classes
In regex, character classes defines a set of characters that can be used in an input string. There is also character escape, which when using the backslash '\', helps a character not be interpreted literally. 

. - matches any character except the newline character.

\d - matches any numerical digit. The same as using [0-9]

\D - matches any non-numerical digits.

\w - matches any alphanumerical character including the underscore. The same as using [A-Za-z0-9_]

\s - matches a single whitespace character including lines and breaks. 

' - accepts any input


### Flags

i - ignores the case when searching in the string.

g - global search meaning all possible matches will be searched. 

m - multi-line input string

s - global search for whitespace characters


### Grouping and Capturing
When grouping a section of regex, you use parenthesis. () The sections within the parenthesis is called a subexpression. You can also include a numerical counter to a subexpression. 

'(Jacob){5}' searches for 'JacobJacobJacobJacobJacob'

### Bracket Expressions
Also known as positive character group, anything put inside of square brackets [] will represent a wide range of characters we want to match. 

Hyphens are used to represent a range of characters. 

[a-g] = [abcdefg] 
[abc] = will match anything that contains any of those characters, regardless of the length. 

### Greedy and Lazy Match
Lazy and Greedy matches are added to quantifiers to either lengthen or shorten the search results. 

Lazy - Adding a ? to a quantifier will make it match as few occurrences as possible. 

Greedy matches are any of the above quantifiers to match as many possible occurrences. 

### Boundaries


### Back-references


### Look-ahead and Look-behind


## Author

You can call me YourFunkyDad. I am a full time father, a full-time serving, and most recently I have taken up coding as a means to challenge myself to learn a new skill. I hope one day I will be able to transition into a coding profession. But for now, I will continue to study and practice. 

https://github.com/YourFunkyDad
