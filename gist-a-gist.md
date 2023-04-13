# Just a Gist: URL edition

Regular Expression or Regex are a sequence of symbols, letters, numbers, and other characters that need to be searched and identified from within a bigger set of text, document, or documents.

## Summary

The regex that we will be covering in this document will  allow you to **Match for a URL**. URL matching is a very important part of the web developers toolkit when creating scripts that require validation.

The following is the regex for URL Matching:

> ` /^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/ `

Please feel free to use the link in the table of contents to skip ahead.

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

Regex can seem complex to the untrained eye. However, in order to better read and understand what the regular expression is trying to accomplish, it is better to look at each component separately.

All regex will need to be wrapped with forward slashes in order to identify them as such.

For the purpose of understanding of how regex is used to match for a URL, let's look at the following components.

### Anchors

The anchor is a special character, often referred as token, that does not match any other character. 

In the case of our regex, the caret is used to define the beginning of the string or line and the dollar sign to indicaate the end of the line. 

> Caret - **^**

> Dollar Sign - **?**

> ` /^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/ `

### Quantifiers

The Quantifiers "quantify" or specify the number of instances that the character(s) show up within the text. 

In the case of URL matching, the following quantifiers are used:

> **? is used after https to indicate that the s is not required and thus https or http is a possible match**

>**A second ? is used at the end to indicate a forward slash may or may not be present but both are acceptable.**

> **{2,6} indicates that the web extention or top-level domain following the dot (.) may contain from 2 up to 6 characters (ex. .ca or .com, etc).

> ` /^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/ `

### OR Operator

### Character Classes

### Flags

### Grouping and Capturing

### Bracket Expressions

### Greedy and Lazy Match

### Boundaries

### Back-references

### Look-ahead and Look-behind

## Author

Manuel Corral
GitHub: https://github.com/ecinematic
Email: ecinematic@yahoo.com
LinkedIn: https://www.linkedin.com/in/josemcorral/
