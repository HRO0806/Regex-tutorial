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

    Looks for an email: /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

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

    Looks for an email: /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

### OR Operator
    a(b|c) Matches a string where a is followed by eather b or c (and captures b and c).

    a[bc] Matches string where a is followed by eather b or c (and does not capture b or c).

    (When something is captured it means it is being seen as a whole unit vs separate characters.)

    example: In this Regex which is looks for a hex-value we see the (|) and the [] oporators being used to search for combinations of six letters and numbers.

    Looks for a hex value: /^#?([a-f0-9]{6}|[a-f0-9]{3})$/

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

    Looks for an email address: /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

### Flags
    /Regex/ Every Regex starts and ends with / oporator.
        note: a flag goes after the closing / marker.

    g(global) Won't return the first match, this then restarts the pervious search.

    m(multi-line) ^ and $ oporators will match the start and end of a line instead of the start and end of a string.

    i(insensitive) This make the whole Regex no longer case sensitive.

    example: In the following Regex which checks for a Hex-Value we can see that the i flag makes the search no longer case sensitive.

    Looks for a Hex-Value: /^#?([a-f0-9]{6}|[a-f0-9]{3})$/i    

### Grouping and Capturing
    a(bc) The parentheses make a capturing group with the value bc.

    a(?:bc)* ?: disables the capturing group.

    a(?<foo>bc) ?<foo> puts a name to the group.

    example: In the following Regex which for an HTML tag we can see that it uses the ?:. It does this to tell the Regex to disable the capturing group for the HTML tag. We also see it capturing several groups.

    Looks for an HTML tag: /^<([a-z]+)([^<]+)*(?:>(.*)<\/\1>|\s+\/>)$/

### Bracket Expressions
    [abc] Matches a string where eather an a, b, c is included.

    [a-z] Matches a string that contains any lowercase letter.

    [a-zA-Z0-9] Matches a string that contains a lower-case letter, upper-case letter, or any digit 1-9.

    [0-9]% Matches a string where any character 0-9 is followed directly by a %.

    [^a-zA-Z] A string with no lower or uppercase letters.

    example: In the following Regex which looks for a Hex-Value we see that it searches for a string with lowercase letters ranging from a to f or a (numerical) digit in both search expressions. It does this by using the expression [a-f0-9].

    Looks for a Hex-Value: /^#?([a-f0-9]{6}|[a-f0-9]{3})$/

### Greedy and Lazy Match
    <.+>(Greedy) Expands the match as far as it can. For example in our case anything between and including two HTML tags.

    <.+?>(Lazy) Does the same as the last one but it only searches for HTML tags themselves.

    <[^<>]+> This would be a better way of writing the previous expresion as it is more strict.

    example: In the following Regex which looks for an HTML tag we see that it uses the solution to finding just the HTML tags. It this by using [^<]+ to tell it to only look for the tag itselfe and not what is in between the opening and closing tags.

    Looks for an HTML tag: /^<([a-z]+)([^<]+)*(?:>(.*)<\/\1>|\s+\/>)$/

### Boundaries
    \b Is an anchor similar to ^ and $. It matches a position where one side is \w character and the other is not (a (numerical) digit or whitespace).

    \B Matches anything \b does not match.

    example: In the following Regex which looks for a single word we see that the \b anchoris used to tell us that there is a space at the end of the word.

    Looks for a single word: /\w.*\b/

### Back-references
    
### Look-ahead and Look-behind

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
