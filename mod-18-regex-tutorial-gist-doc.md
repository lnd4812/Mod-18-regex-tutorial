# Title

Module 18 Regular Expressions Tutorial Challenge - Matching a Hex Value

## Summary

A regular expression, or regex, may be used to search for specific patterns of different characters to either find, find and replace or validate those specific characters.

Each symbol in the regex represents a specific criteria of the search pattern.  The purpose of this tutorial is to describe the particular components that comprise the regex for matching a Hex value used to designate colours, i.e. /^#?([a-f0-9]{6}|[a-f0-9]{3})$/  

## Table of Contents

- [Title](#title)
  - [Summary](#summary)
  - [Table of Contents](#table-of-contents)
  - [Regex Components](#regex-components)
    - [Anchors](#anchors)
    - [Quantifiers](#quantifiers)
    - [OR Operator](#or-operator)
    - [Grouping and Capturing](#grouping-and-capturing)
    - [Bracket Expressions](#bracket-expressions)
    - [Greedy and Lazy Match](#greedy-and-lazy-match)
  - [Author](#author)

## Regex Components

Matching a Hex Value - /^#?([a-f0-9]{6}|[a-f0-9]{3})$/
The two forward slash symbols enclosing the regex are delimiters which mark the main regex components specifying the search or validation criteria.

### Anchors

The caret symbol, ^, is an anchor that specifies the beginning of a string.  Example: ^It would search for a string that began with "It".  It may also designate the start of a line in a pattern of lines, like a paragraph.  

In the case of the Hex value, the ^ in front of the # matches a string beginning with the hashtag symbol, as all Hex values do.

### Quantifiers

The question mark, ?, is a quantifier; on a stand-alone basis, it matches the character in front of it 0 or 1 time, meaning that symbol doesn't necessarily appear in the search value.

When used in combination with other regex characters, it acts as what is termed a lazy quantifier in that it reduces number of matches that might otherwise be returned, i.e. match "this" but as few times as possible.  

Used in a Hex value regex, it matches a string that is followed by either 1 or no #.

The curly brackets, {}, are quantifiers and, in this instance, the {6} indicates a group of exactly 6 letters and/or numbers within the designated ranges following the # symbol.

### OR Operator

The vertical line symbol, |, represents a concept of "or", meaning the search patter on either side of it is valid.  For instance, (cat | bat) would match a string with either "cat" or "bat" in it.

In a Hex value search, the regex combination on either side of the | would return the specific search criteria.

### Grouping and Capturing

Round brackets, ( ), capture the components within them, signifying that they represent a defined group.  For instance, the regex (cat) would match strings containing the combination of c+a+t, such as "cat", "catch" or "scatter".

In the case of the Hex value regex, the regex combinations within the ( ), i.e. the ranges & quantifiers on either side of the | symbol are the captured group.

### Bracket Expressions

Square brackets, [], signify a range of the characters within the square brackets.  For instance, [a-zA-Z] represents a range of lowercase and uppercase letters ranging over the entire alphabet.

In the case of the Hex value regex, the range is a string of lower case letters from a-f and/or string of numbers from 0-9.

### Greedy and Lazy Match

Greedy operators (* + {} ) {purpose is to expand match as far as possible within provided text. Adding ? makes it lazy

## Author

The author, Laurel David, is a reinsurance underwriter for an international MGA and enrolled in the February 2022 session of the Full Stack Bootcamp course being offered through the U of T School of Continuing Studies.  

The GitHub repository link [github.com/lnd4812](https://github.com/lnd4812).
