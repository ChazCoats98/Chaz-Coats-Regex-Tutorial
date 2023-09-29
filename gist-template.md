# Breaking down a regex 

A regex is a universally usable expression, meaning it can be used across all programming languages. Regexes are used to match specified patterns within a string. This is a very useful "search" or "filter" expression that can be used to pull specific information out of a string. In order to better understand how regex expressions work, the following tutorial was made to break down each element of a specific regex.

## Summary

In this tutorial I will be explaining how the regex /^<([a-z]+)([^<]+)*(?:>(.*)<\/\1>|\s+\/>)$/ is used for matching HTML tags.

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
In this expression, the anchors are ^ to mark the beginning of the string and $ to mark the end. 
### Quantifiers
The + quantifier is used to mach an instance one or more times. The * qualifier matches an instance 0 or more times rather than 1 or more, and the ? quantifier matches an instance 0 or 1 times. 
### OR Operator
The OR operator in this equation is used to match the closing tag of the HTML element. Matching either closing tag or self closing tag.
### Character Classes
The character class in this expression (\s) is used to match white space characters. 
### Flags
This expression doesn't contain any flags. As an example, the i flag would be used to ignore case when looking at letters. This regex is lower-case sensitive so we wouldn't want to use that here. 
### Grouping and Capturing
This expression starts off with the grouping ([a-z]+). This grouping is used to match, then capture, one or more lower-case characters in the opening HTML tag. The next group ([^<]+) is used to match one or more characters that do NOT match the opening HTML tag. This group doesn't capture any characters. The next group (?:>(.*)<\/\1>|\s+\/>) is denoted as a non-capturing group, designated by the ? symbol. The (.*) group within this overarching group matches anything within the html tags.
### Bracket Expressions
There are 2 bracket expressions in this regex. The first [a-z] matches any lowercase letters (a to z). The second [^<] matches any characters excluding the < character, being the opening HTML tag.
### Greedy and Lazy Match
This expression uses greedy matching. Quantifiers like + and * start at a minimum match and find a match as many times as possible. 
### Boundaries
In this expression, boundaries are not used.
### Back-references
In this expression <\/\1> is used to back-reference to the string that was captured in the first grouping. 
### Look-ahead and Look-behind
In this expression, look-ahead and look-behind references aren't used.
## Author

This tutorial was written by Chaz Coats: [GitHub](https://github.com/ChazCoats98)
