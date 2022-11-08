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

Quantifiers are used to quantify how many times a part of the regular expression should be repeated. Depending on what the quantifier is in your regular expression will determine if it is a greedy match or a lazy match. 'Greedy' refers to the longest possible string and 'lazy' refers to the shortest. Since our first two quantifiers are '+', we know the regex will be attempting a greedy match. The '+' quantifier tells the expression to match the pattern one or more times. Our third quantifier is '{2,6}', meaning the regex will try to match with a character as many times as possibly within the rang of 2 and 6.

### OR Operator

We do not use the OR Operator '|' in this regular expression.

### Character Classes

Character Classes are some of the most commonly used features of regular expressions. They are used to match a specific character in the string to a specific set. The character classes used in the regex for validating an email are '.' and '\d'. The one that shows up  the most frequently being '.', is used for matching any character except the newline character. The '\d' character class matchers any arabic numeral digit, and is the equivelant to the bracket expression '[0-9].

### Flags

Flags define additional functionality or limits for the expression and are placed at the end of the regex. Flags are optional, and none are used in this specific expression.

### Grouping and Capturing

The main way to group a section of a regular expression is by using parentheses. Within the grouping constructs are two main categories: Capturing and Non-Capturing. Capturing groups capture the matched character sequences for re-use, whereas non-capturing groups do not.

### Bracket Expressions

Bracket Expressions are anything inside of a set of square brackets, '[a-z0-9_\.-]','[\da-z\.-]', and '[a-z\.]' in our case, represents the range of characters that we want to match. Bracket expressions can also be refered to as a 'Positive Character Group', because they outline all characters we want to include. Breaking down the expressions in this specific regex tells us the following: The '[a-z]' shown above is telling us that the string can contain any lowercase letter between a-z. The '[0-9]' in the first bracket expression is saying that the string can include any number between 0-9, '_' and '-', which can be seen in the first two expressions above are telling us we only want a string that includes '_' or '-'. It is important to remember that a bracket expression does not require the string to meet every requirement in the pattern.

### Greedy and Lazy Match

As I mentioned previously when describing quantifiers, we know this regular expression is a greedy match, meaning it will search for the longest string possible instead of the shortest, which would be a lazy match.

### Boundaries

There are multiple types of boundries in regular expressions such as word boundries, and non-word boundries. A word boundry can be recognized as '\b' and a non-word boundry as '\B'. This expression contains neither.

## Author

I, Josh Murray, am currently finishing up the Full Stack Coding Bootcamp through UCLA extenstion while living in Los Angeles. My github can be found at:

www.github.com/joshgmurray
