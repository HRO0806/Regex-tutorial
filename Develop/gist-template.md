# Title (replace with your title)

Introductory paragraph (replace this with your text)

## Summary

Briefly summarize the regex you will be describing and what you will explain. Include a code snippet of the regex. Replace this text with your summary.

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
    ^ Mathches the string that follows it.

    $ Match the string that precedes it.

    ^$ Matches the string in between the ^ and $.

    example: In this Regex which looks for an email the ^ and $ characters signify the start and end of the string the Regex is looking for.

    Looks for an email: ^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$

### Quantifiers
    abc* Matches a string where ab is followed by 0 or more c.

    abc+  Matches a string where ab is followed by 1 or more c.

    abc? Matches a string where ab is followed eather 0 or 1 c.

    abc{3} Matches a string where ab is followed by 3 c.

    abc{3,} Matches a string where ab is followed by 3 or more c.

    abc{3,6} Matches a string where ab is followed greater than or equal to 3 and less than or equal to 6 c.

    a(bc)* Matches a string where a is followed by 0 or more sequences of bc.

    a(bc) {3,6} Match a string where a is followed by the sequence ab greater than or equal to 3 and less than or equal to 6 times.

    example: In this Regex which looks for an email we see the {2,6} oporator. This searches for a domain between 2 and 6 characters.

    Looks for an email: ^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$

### OR Operator
    a(b|c) Matches a string where a is followed by eather b or c (and captures b and c).

    a[bc] Matches string where a is followed by eather b or c (and does not capture b or c).

    (When something is captured it means it is being seen as a whole unit vs separate characters.)

    example: In this Regex which is looks for a hex-value we see the (|) and the [] oporators being used to search for combinations of six letters and numbers.

    Looks for a hex value: ^#?([a-f0-9]{6}|[a-f0-9]{3})$

### Character Classes
    \d Matches a single (numarical) digit character.

    \w Matches a word character.

    \s Matches whitespace.

    \t Matches a tab.
    
    \n Matches a new line.

    \r Matches a return.

    . Matches any character.

    \D Matches a single non-(numerical)digit.

    \W Matches a non-word character.

    \S matches a lack of whitespace.

    \$\d Matches matches a string where $ oporator exists behind one digit.

    example: In the following Regex which checks for an email, we can see in the second set of parenthesis that it is search for a single numerical digit followed by any chararcater between a-z one or more times. It this by using the \d, and . oporators as well as the + oporator mentioned previously.

    Looks for an email address: ^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$

### Flags

### Grouping and Capturing

### Bracket Expressions

### Greedy and Lazy Match

### Boundaries

### Back-references

### Look-ahead and Look-behind

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
