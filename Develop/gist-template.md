# Introduction to Regex
 Regex stands for "regular expression" and is used as a tool to set search paramaters. For example you can tell it search for certain types of characters, specific charaters, a range of characters, or a grouping of specific characters.

## Summary
    The Regex we are using as an example in this tutorial looks for a hex-value. If you are not sure what a hex-value is, follow this link: https://marketing.istockphoto.com/blog/hex-colors-guide/.

    The Regex I am using: /^#?([a-f0-9]{6}|[a-f0-9]{3})$/

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)

## Regex Components

### Anchors
    ^ Matches the string that follows it. Think of it as marking the start of the string.

    $ Match the string that precedes it. Think of it as marking the end of the string.

    ^$ Matches the string in between the ^ and $. Think of them sort of like quotation marks. They tell the Regex to search for what is inside of them.

    example: In the Regex that I chose which searches for a hex-value, the ^ and $ oporators are used to to mark the begining and end of the hex-value.

    My Regex example: /^#?([a-f0-9]{6}|[a-f0-9]{3})$/

### Quantifiers
    abc? Matches a string where ab is followed eather 0 or 1 c. In our case it is telling the Regex to match a hex value with eather 3 characters or 6 characters. This way it knows that #000 is still a hex value even though the full hex-value is #000000.

    abc{3} Matches a string where ab is followed by 3 c. In our case it is being used to tell the Regex how many characters it should include in the captured group. It is being told that the hex-value will be eather 3 characters or 6 characters long.

    (When something is captured it means it is being seen as a whole unit vs separate characters.)

    example: In the Regex that I chose which searches for a hex-value the ? oporator is being used to tell it to search for a string that is eather 3 characters long or 6 characters long. The {} are being used to specify how many characters long the string is.

    My Regex example: /^#?([a-f0-9]{6}|[a-f0-9]{3})$/

### OR Operator
    a(b|c) Matches a string where a is followed by eather b or c (and captures b and c). In our case it is being used to tell the Regex to look for eather the first set ([a-f0-9]{6}) or 
    the second set ([a-f0-9]{3}).

    a[bc] Matches string where a is followed by eather b or c (and does not capture b or c). In our case this is being used to tell the Regex to search for any lowercase characters from a to f or any number from 0 to 9.

    example: In the Regex I chose which searches for a hex-value we see both the (|) and [] oporators which tell it to looks for one or the other. The (|) oporater is used to tell the the Regex to look for a string of eather 3 characters or 6 characters. The [] oporator is being used to tell the Regex to look for eather any lowercase letter from a to f or any number from 0 to 9. Both a lowercase letter from a to f and a number from 0 to 9 are seen as valid characters for the string.

    My Regex example: /^#?([a-f0-9]{6}|[a-f0-9]{3})$/

### Grouping and Capturing
    a(bc) The parentheses make a capturing group with the value bc. In our case it is capturing the the hex-value. In other words it is seeing the hex value as a single unit rather than individual characters.

    example: In the Regex I chose which searches for a hex-value we can see that it is using parentheses to capture the hex-value. This makes the Regex see it as a single unit rather than individual characters.

    My Regex example: /^#?([a-f0-9]{6}|[a-f0-9]{3})$/

### Bracket Expressions
    [abc] Matches a string where eather an a, b, or c is included. In our case it matches a string where any lowercase letter from a to f or any number from 0 to 9 is included.

    [a-z] Matches a string that contains any lowercase letter. In our case it only searches from a to f (a-f).

    [a-zA-Z0-9] Matches a string that contains a lower-case letter, upper-case letter, or any digit 0-9. In our case it only matches a string with lowercase letters from a to f or numbers from 0 to 9.

    example: In the Regex I chose which searches for a hex-value we can see that it uses [a-f0-9] to tell the Regex that it matches any string with these paramaters.

    Regex example for finding a hex-value: /^#?([a-f0-9]{6}|[a-f0-9]{3})$/

## Author

Henry Olson is a young and new developer who is passionate about coding and web-development and wants to share his passion with the world. Henry has deep love of learning and loves sharing the things he is learning with others.

Henry's GitHub profile: https://github.com/


