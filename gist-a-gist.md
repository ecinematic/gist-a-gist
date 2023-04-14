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
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Grouping and Capturing](#grouping-and-capturing)
- [Author](#author)

## Regex Components

Regex can seem complex to the untrained eye. However, in order to better read and understand what the regular expression is trying to accomplish, it is better to look at each component separately.

All regex will need to be wrapped with forward slashes in order to identify them as such.

Backslashes in regex are called an escape character and it indicates that the character preceding it should be taken into literal context. 

For the purpose of understanding of how regex is used to match for a URL, let's look at the following components.

### Anchors

The anchor is a special character, often referred as token, that does not match any other character. 

In the case of our regex, the caret is used to define the beginning of the string or line and the dollar sign to indicaate the end of the line. 

> Caret - **^**

> Dollar Sign - **$**

> ` /^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/ `

### Quantifiers

The Quantifiers "quantify" or specify the number of instances that the character(s) show up within the text. 

In the case of URL matching, the following quantifiers are used:

The following ? is used to indicate that the s is not required and thus https or http are both possible matches.

> `https?`

The following ? is used after https:// to indicate that this prefix may not be necessary in the URL.

> `(https?:\/\/)?`

This third ? is used at the end to indicate the forward slash may or may not be present, however, both are acceptable. Note the foward slash is used to indicate that the back slash should be referenced in its literal sense. 

> `\/?`

The curly braces are also quantifiers that can be used to determine the {2,6} indicates that the web extention or top-level domain following the dot (.) may contain from 2 up to 6 characters (ex. .ca or .com, etc).

> `[a-z\.]{2,6}`

The plus sign is used to match one or more of the preceding characters.

> `([\da-z\.-]+)`

The asterisk is used to match zero or more of the preceding characters. 

> `([\/\w \.-]*)*`


> ` /^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/ `

### Character Classes

The character class matches any of the characters enclosed within the brackets. 

The following includes digit, characters a through z plus it includes the period and hypen character.

> `[\da-z\.-]`

The following includes the characters a through z plus the period character.

> `[a-z\.]`

The following includes the back slash, *any word character (\w)*, period, plus the hyphen character.

> `[\/\w \.-]`


> ` /^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/ `

### Flags

The URL Matching Regex does not have any flags. 

For referenct, flags are used to designate how matches are performed.

For example, the "g" flage looks for a global match, rather than just the first match. The "i" flag matches for both the uppercase and lowercase character.

### Grouping and Capturing

Grouping and Capturing is a way for regex to treat a set of characters as one unit. It is denoted by a pair of parentheses. 

The following grouping is to categorize the protocol portion of the URL. 

> `(https?:\/\/)`

The following grouping categorizes the digits, letters, dots, and hyphens that could follow the http(s) protocol.

> `([\da-z\.-]+)`

The following categorized the extension that will contain letters and dots.

> `([a-z\.]{2,6})`

And finally, the last grouping categorizes the optional files and directories that the URL may contain. 

> `([\/\w \.-]*)`


> ` /^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/ `


## Author

- Manuel Corral
- GitHub: https://github.com/ecinematic
- Email: ecinematic@yahoo.com
- LinkedIn: https://www.linkedin.com/in/josemcorral/
