Regular Expression
===

Index
===

* Defination of Regular Expression
* Basic Operation and Function
  * [`re.match` function](#rematch-function)
  * [`re.search` function](#research-function)
  * [Diff between `re.match` and `re.search`](#diff-between-rematch-and-research)


### Defination of Regular Expression
A regular expression is a special sequence of characters that helps you easily check if a string matches a pattern.</br>
Python has added the re module since version 1.5, which provides a Perl-style regular expression pattern.</br>
The `re` module gives the Python language full of regular expression functionality.</br>
The `compile` function generates a regular expression object based on a pattern string and optional flag parameters. This object has a set of methods for regular expression matching and replacement.</br>
The re module also provides functions that are fully functional with these methods, using a pattern string as their first argument.

### `re.match` function
`re.match` attempts to match a pattern from the beginning of the string. If it is not the matching of the starting position, match() returns none</br>

`re.match(pattern, string, flags=0)`

|<center>Parameter</center>|<center>Description</center>|
|----------        |------------         |
| `pattern`        |matched regular expression|
| `string`         |the string to match|
| `flag`           |flag bit, used to control how regular expression to match|

Matches the successful `re.match` method to return a matching object, otherwise returns `None`.</br>
We can use the `group(num)` or `groups()` matching object functions to get the matching expression.
</br>

|<center>function of matching object</center>|<center>Description</center>|
|----------        |--------------        |
|`group(num)`      |`group()` can enter multiple group numbers it returns a tuple containing the values for those groups.|
|`groups()`        |returning a tuple containing all the group strings, from 1 to the included team number|

```python
import re
print (re.match('www','www.google.com').span())
print (re.match('google','www.google.com'))

(0,3)
None
```
### `re.search` function
`re.search` scanning the whole string and return the first matched pattern
`re.search(pattern, string, flags=0)`

```python
import re
print (re.search('www', 'www.google.com').span())
print (re.search('google','www.google.com').span())

(0,3)
(4,10)
```
### Diff between `re.match` and `re.search`
`re.match` only matches the beginning of the string. If the string does not match the regular expression, the match fails, the function returns `None`; and `re.search` matches the entire string until a match is found.







