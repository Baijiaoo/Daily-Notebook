Regular Expression
===

Index
===

## Defination of Regular Expression


### Defination of Regular Expression
A regular expression is a special sequence of characters that helps you easily check if a string matches a pattern.</br>
Python has added the re module since version 1.5, which provides a Perl-style regular expression pattern.</br>
The `re` module gives the Python language full of regular expression functionality.</br>
The `compile` function generates a regular expression object based on a pattern string and optional flag parameters. This object has a set of methods for regular expression matching and replacement.</br>
The re module also provides functions that are fully functional with these methods, using a pattern string as their first argument.

### `re.match` function
`re.match` attempts to match a pattern from the beginning of the string. If it is not the matching of the starting position, match() returns none</br>

`re.match(pattern, string, flags=0)`

|Parameter      |Description      |
|========       |==========       |
|`pattern`        |matched regular expression   |
|`string`         |the string to match          |
|`flag`           |flag bit, used to control how regular expression to match    |




