# Regex Tutorial

Regular Expressions or, Regex's are encoded text strings that are used to match patterns in other strings. One of the most common uses for regex is confirming that the information a user enters into a form is correct.

## Summary

For this tutorial, I will be breaking down how the regular expression for validating an email address functions. 

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

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

### Anchors

Anchors are used to assert that the current position in the string matches a determined location. The anchors for this specific regular expression consist of <^> at the beginning of the expression and <$> at the end. These force the regex to find its specific match at the start and end of the subject text. By placing the regular expression inside of these anchors it is requiring the regex to match the entire subject.

### Quantifiers

Quantifiers are used to quantify how many times a part of the regular expression should be repeated. Depending on what the quantifier is in your regular expression will determine if it is a greedy match or a lazy match. 'Greedy' refers to the longest possible string and 'lazy' refers to the shortest. Since our first two quantifiers are '+', we know the regex will be attempting a greedy match. Our third quantifier is '{2,6}', meaning the regex will try to match with a character as many times as possibly within the rang of 2 and 6.

### Character Classes

Character Classes are one of the most commonly used features of regular expressions. They are used to match a specific character in the string to a specific set.

### Flags

### Grouping and Capturing

### Bracket Expressions

### Greedy and Lazy Match

As I mentioned previously when describing quantifiers, we know this regular expression is a greedy match, meaning it will search for the longest string possible instead of the shortest, which would be a lazy match.

### Boundaries

### Back-references

### Look-ahead and Look-behind

## Author

A short section about the author with a link to the author's 
GitHub profile (replace with your information and a link to your 
profile)
