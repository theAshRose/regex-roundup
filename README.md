# regex-roundup

# Regex-Roundup

I wrote this to practice syntax which is otherwise readily available in multiple places.

## Summary

Here we will being going all displayed in the table of contents below. Regular expressions may be seen as "cheating" in some coding interviews.

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

Special characters which match up substrings. They include:

-  ^ matches at start of desired string
-  $ matches at end of desired string
-  \b matches a word boundary - for example, when a previous character isnt a word character.

### Quantifiers

You may follow an "atom"(or a regular expression) with these. The quantifiers. They generate undounded matching possibilities including amount.

-  * for 0 or more instances of specified atom
-  + for 1 or more instances of specified atom
-  ? for 1 or 0 instances of specified atom   
-  {number here} for exactly that number of atom instances
-  {numeber 1, number 2} exactly 1-2# instances of specified atom

One may also follow quanified with '?', signifying the match be MINIMUL as opposted to the default MAXIMAL.

### Grouping Constructs

Contructs(usually multiple characters) used for grouping! 

Such as matching a subexpression repeated on input string, applying quantifier, include subexpression which is returned by .replace or match.result methods, or retrieving individual subexpressions from match.groups property to access them seperately from matched text in totality. 

They can be either capturing or noncapturing. Differences between the two are rather self-evident as one finds matched substrings and keeps them while the other does not. 

Captured(matched subexpressions):

(subexpression)

-  \number, so it would look like this: "(\4)".
-  `\k<name> or \k<number>`, a named backreference contruct. we call on the expression by name or number
-  $number replacement with regex.replace or match.result
-  (\w+) matches one or more characters(initial capturing group)
-  \s matching white spaces
-  (\1) matching a string in first group.
-  \W non-word character pairing, which includes punction and white space preventing regex pattern from pairing a word starting with initial captured group word.

If you'd like to learn about Noncaptured, check out the documentation where i got my info here https://learn.microsoft.com/en-us/dotnet/standard/base-types/grouping-constructs-in-regular-expressions#noncapturing_group. 
### Bracket Expressions

Brackets hold characters usually to be matched: `[characters here]`. 

-  ^ is for literals except the start of our expression. If at the beginning it matches NOT from the list.
-  - defines ranges: `[a-e-i-o-u]`. one cannot end the range with the same character which was started. its literal at the beginning or end of an expression

### Character Classes

-  `[xyz]` or `[a-c]` are for character classes, matching any included characters. normal letters here. this may be prefixed with a ^ to look for all characters NOT included.

(these find matches for... ):
-  \d digits
-  \D NOT a digit
-  \w alphanumeric characters including underscore(A-Z, a-z, 0-9, _)
-  \W anything NOT a word character
-  \s white space characters
-  \S single character NOT a white space character
-  \t horizontal tab
-  \r carriage return

for more details visit here https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Regular_Expressions/Character_Classes

### The OR Operator

Normally in javascript we use "||" as an OR operator, but with regex its half the work by using "|".
such as:

`String regex = "(q|Q)"`

### Flags



### Character Escapes

These are the same syntax as character classes but they are placed after the expression instead of within.

## Author


