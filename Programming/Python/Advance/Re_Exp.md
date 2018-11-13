Regular Expression
===

Index
===

* Defination of Regular Expression
* Basic Operation and Function
  * [`re.match` function](#rematch-function)
  * [`re.search` function](#research-function)
  * [`re.sub` function](#resub-function)
  * [`re.compile` function](#recompile-function)
  * [Diff between `re.match` and `re.search`](#diff-between-rematch-and-research)


### Defination of Regular Expression
A regular expression is a special sequence of characters that helps you easily check if a string matches a pattern.</br>
Python has added the re module since version 1.5, which provides a Perl-style regular expression pattern.</br>
The `re` module gives the Python language full of regular expression functionality.</br>
The `compile` function generates a regular expression object based on a pattern string and optional flag parameters. This object has a set of methods for regular expression matching and replacement.</br>
The re module also provides functions that are fully functional with these methods, using a pattern string as their first argument.

### Basic Operation and Function
#### `re.match` function
`re.match` attempts to match a pattern from the beginning of the string. If it is not the matching of the starting position, `match()` returns `none`</br>

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
#### `re.search` function
`re.search` scanning the whole string and return the first matched pattern
`re.search(pattern, string, flags=0)`

```python
import re
print (re.search('www', 'www.google.com').span())
print (re.search('google','www.google.com').span())

(0,3)
(4,10)
```

#### `re.sub` function
`re.sub` retreiving and repalcing sunstrings in strings
`re.sub(pattern, repl, string, count=0, flags=0)`

|<center>Parameter</center>|<center>Description</center>|
|-------------             |---------                   |
|`pattenr`                 |Matched regular expression  |
|`repl`                    |Replacing string or function|
|`string`                  |The string to match         |
|`count`                   |After matching the max number to replace, default 0 represents all replacement|

```python
import re
phone = '123-456-7890 # This is a foreign number'
print re.sub(r'#.*$', '', phone)
print re.sub(r'\D', '', phone)

123-456-7890
1234567890
```
#### `re.compile` function
`re.compile` creating pattern and used on `re.match` and `re.search`
`re.compile(pattern[, flags])`
```python
import re
pattern = re.compile(r'\d+')
m = pattern.match('one12twothree34four')
print m
None

m = pattern.match('one12twothree34four',2,10)
print m
None

m = pattern.match('one12twothree34four',3,10)
print m
<_sre.SRE_Match object at 0x10a42aac0>

m.group()
'12'
m.start()
3
m.end()
5
m.span()
(3,5)
```
```python
import re
pattern = re.compile(r'([a-z]+) ([a-z]+)', re.I)
m = pattern.match('Hello World')
print m
<_sre.SRE_Match object at 0x10bea83e8>

m.group(0)
'Hello World'
m.group(1)
'Hello'
m.group(2)
'World'
m.span(2)
(6,11)
m.groups()
'Hello World'
```


#### Diff between `re.match` and `re.search`
`re.match` only matches the beginning of the string. If the string does not match the regular expression, the match fails, the function returns `None`; and `re.search` matches the entire string until a match is found.









