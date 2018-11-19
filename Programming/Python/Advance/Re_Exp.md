Regular Expression
===

Index
====

* Defination of Regular Expression
* Basic Operation and Function
  * [`re.match()` function](#rematch-function)
  * [`re.search()` function](#research-function)
  * [`re.sub()` function](#resub-function)
  * [`re.compile()` function](#recompile-function)
  * [`re.split()` function](#resplit-function)
  * [`findall()`](#findall)
  * [Diff between `re.match` and `re.search`](#diff-between-rematch-and-research)
* [Regular Expression Objects](#regular-expression-objects)
* [Regular Expression Option Marker](#regular-expression-option-marker)
* [Regular Expression Method](#regular-expression-method)
  * [Basic Operations](#basic-operations)
  * [Reapting](#repeating)
  * [Exact match and minimum match](#exact-match-and-minimum-match)

### Defination of Regular Expression
A regular expression is a special sequence of characters that helps you easily check if a string matches a pattern.</br>
Python has added the re module since version 1.5, which provides a Perl-style regular expression pattern.</br>
The `re` module gives the Python language full of regular expression functionality.</br>
The `compile` function generates a regular expression object based on a pattern string and optional flag parameters. This object has a set of methods for regular expression matching and replacement.</br>
The re module also provides functions that are fully functional with these methods, using a pattern string as their first argument.

### Basic Operation and Function
#### `re.match()` function
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
#### `re.search()` function
`re.search` scanning the whole string and return the first matched pattern
`re.search(pattern, string, flags=0)`

```python
import re
print (re.search('www', 'www.google.com').span())
print (re.search('google','www.google.com').span())

(0,3)
(4,10)
```

#### `re.sub()` function
`re.sub` retreiving and repalcing sunstrings in strings</br>
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
#### `re.compile()` function
`re.compile` creating pattern and used on `re.match` and `re.search`</br>
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
#### `re.split()` function
`re.split()` Dividing the string into a list according to the substring that can be matched</br>
`re.split(pattern, string[, maxsplit=0, flags=0])`
#### `findall()`
`findall()` Finding all matched regular expression and returning a list, if no match returning a empty list
```python
import re
pattern = re.compile(r'\d+')
m = pattern.findall('1234 google 456 facebook')
print m
['1234','456']
```
#### Diff between `re.match()` and `re.search()`
`re.match` only matches the beginning of the string. If the string does not match the regular expression, the match fails, the function returns `None`; and `re.search` matches the entire string until a match is found.

### Regular Expression Objects
* re.RegexObject
  * `re.compile()` returns `egexObject()` Object
* re.MatchObject
  * `group()` returns the matched string
  * `start()` returns the start position of matched string
  * `end()`   returns the end position of matched string
  * `span()`  returns a tuple (strat, end) of matched string

### Regular Expression Option Marker
Regular expressions can contain optional flag modifiers to control the pattern of matches. The modifier is specified as an optional flag. Multiple flags can be specified by bitwise OR`(|)`. For example, `re.I | re.M ` is set to the I and M flags

|<center>Modifer</center>     |Description          |
|-----------------------      |-----------          |
|`re.I`                       |Not sensitive to capitalization|
|`re.L`                       |Do (locale-aware) matching|
|`re.M`                       |Multiple lines matching, has influence on `^` and `$`|
|`re.S`                       |     |
|`re.U`                       |Parsing characters based on Unicode character set, has influence on `\w`,`\W`,`\b`,`\B`|
|`re.X`                       |This logo gives you a more flexible format so that you can write regular expressions more easily|

### Regular Expression Method
#### Functional Character: 
`.`,`*`,`+`,`|`,`!`,`^`,`$`,`?`,`/`,etc, they have special function. Especially the `/` character, which is an escaped guide symbol, and the characters following it generally have a special meaning.
#### Rule delimiter: 
`[' ']`,`( ' ' )`,`{' '}`, etc., that is, several brackets.
#### Predefined escape character sets: 
`/d`,`/w`,`/s` and so on, they begin with the character `/` followed by a specific character to indicate a predefined meaning.
#### Other special function characters: 
`#`,`!`,`:`,`-`, etc. They only indicate special meanings in specific situations. For example, `(?# ...)` means a comment, and the contents are ignored.

Let's explain the meaning of these rules one by one, but the order of explanation is not in the above order, but I think it is arranged from shallow to deep, from basic to complex. At the same time, for the sake of intuition, try to give more examples in the process of explanation to facilitate understanding.

#### Basic Operations
`'['']'`
First, explain how to set the character set. A character enclosed in a square bracket indicates a set of characters that match any of the characters contained in it. For example, `[abc123]` indicates that the characters 'a' ‘b’ ‘c’ ‘1’ ‘2’ ‘3’ meet their requirements. Can be matched.</br>
In `[' ']` you can also specify the range of a character set by the `-` minus sign. For example, you can use `[a-zA-Z]` to specify the case of the English letter, because the English letters are from small to small The big order is to order. You can't reverse the order of the size, for example, writing `[z-a]` is not right.</br>
If you write a `^` at the beginning of `[' ']`, it means no, that is, the characters in parentheses do not match. For example,`[^a-zA-Z]` indicates that all English letters are not matched. But if ‘^’ is not at the beginning, it is no longer a fetch, but a self, such as `[a-z^A-Z]`, which matches all English letters and characters `^`.</br>

`'|'`
The two rules are juxtaposed and joined by `|`, indicating that they can be matched as long as one of them is met. such as
`[a-zA-Z]|[0-9]` means that the number or letter can be matched. This rule is equivalent to `[a-zA-Z0-9]`</br>
**Note:** There are two things to note about ‘|’:</br>
First, it no longer represents or in the `[' ']`, but represents his own character. If you want to represent a `|` character outside of `[' ']`, you must use a backslash, ie `/|`;</br>
Second, its effective range is the entire rule on both sides. For example, `dog|cat` matches 'dog' and 'cat' instead of 'g' and 'c'. If you want to limit its effective range, you must use a non-capturing group ‘(?: )’ to wrap it up. For example, to match ‘I have a dog’ or 'I have a cat', you need to write `r'I have a (?:dog|cat)'` instead of `r'I have a dog|cat'`</br>
```python
import re
s = 'I have a dog , I have a cat'
re.findall(r'I have a (?:a dog|a cat)',s)
['I have a dog','I have a cat']
```

`'.'` matching all characters
Matching all characters except the newline `'/n'`. If the `re.S` option is used, all characters including `'/n'` are matched.
```python
import re
s = '123/n456/n789'
re.findall(r'.',s)
['123','456','789']
re.findall(r'.',s,re.S)
['123/n456/n789']
```

`'^'` and `'$'` match the beginning and end of the string</br>
**Note**: that `'^'` cannot be in `'[ ]'`, otherwise the meaning will change. See the description of `'['']'` above. In multi-line mode, they match the beginning and end of each line. See the section on the `re.M` option in the compile function description below.</br>

|<center>Predefined escape character sets</center>       |<center>Description</center>      |
|------------------------------------------------        |-----------      |
|`'/d'`|Matching a number, which is equivalent to `[0-9]`|
|`'/D'`|Matching a non-numeric character, equivalent to `[^0-9]`|
|`'/w'`|Matching all English letters and numbers, which is equivalent to `[a-zA-Z0-9]`|
|`'/W'`|Matching non-English letters and numbers,which is equivalant to `[^a-zA-Z0-9]`|
|`'/s'`|Matching characters such as spaces, tabs, carriage returns, etc., which are equivalent to `[ /t/r/n/f/v]`.(note that there is a space in front of it)|
|`'/S'`|Matching non-spacer, which is equivalant to `[^ /t/r/n/f/v]`|
|`'/A'`|Matching the beginning of a string.The difference between it and `'^'` is that `'/A'` only matches the beginning of the entire string, even in the `re.M` mode, it does not match the other lines|
|`'/Z'`|Matching the end of a string.The difference between it and `'$'` is that `'/Z'` only matches the end of the entire string, even in the `re.M` mode, it does not match the other lines|
|`'/b'`|Matching the boundary of a word, such as a space, etc., but it is a '0' long character, and the matched string does not include the delimited character. And if you match with `'/s'`, the matching string will contain that delimiter.|
|`'/B'`|Matching non-boundary characters. It is also a 0 length character|

```python
import re
s= '12 34/n56 78/n90'
re.findall( r'^/d+', s, re.M )
[12, 56, 90]
re.findall(r'/A/d+', s, re.M)
[12]
```

```python
import re
s =  'abc abcde bc bcd'
re.findall(r'/bbc/b', s)
[bc]
re.findall(r'/sbc/s', s)
[ bc ]
re.findall(r'/Bbc/w+', s)
[bcde]
```

`(?:' ')` No capture group means that when you want to perform some operations on a part of the rule as a whole, such as specifying the number of repetitions, you need to enclose the part of the rule with `(?:' ')`, not just a pair. Parentheses, which will give absolutely unexpected results
```python
import re
s = 'ababab abbabb aabaab'
re.findall(r'/b(?:ab)+/b', s)
['ababab']

re.findall(r'/b(ab)/b', s)
['ab']
```

`(?#' ')` Python allow you to write comments in regular expression, and the content in `(?#' ')` will be ignored

#### Repeating
Regular expressions need to match strings of variable length, so it is necessary to indicate a repeating indicator. Python's regular expressions' repeating rule is flexible. The general form of a repeating rule is followed by a character rule followed by a rule indicating the number of repetitions. It has been shown that the previous rule needs to be repeated a certain number of times.</br>

`'*'` zero or multiple times matching</br>
`'+'` one or multiple times matching
```python
import re
s = ' aaa bbb111 cc22cc 33dd '
re.findall(r'/b[a-z]+/d*/b',s)
['aaa','bbb111']
```
`'?'` one or zero times matching
```python
import re
s = ' 123 10e3 20e4e4 30ee5 '
re.findall(r'/b/d+[eE]?/d*/b', s)
['123','10e3']
```

#### Exact match and minimum match
Python's regular expression can set the exact matching times:</br>
`'{m}'` exact matching m times</br>
`'{m,n}'`minimum matching m times, maximum matching n times</br>
If you only want to specify a minimum number of times or just specify a maximum number of times, you can empty another parameter. For example, if you want to specify at least 3 times, you can write `{3,}` (note the comma), and if you only want to specify a maximum of 5 times, you can write `{, 5}` , or you can write `{0,5}`
```python
import re
s= ' 1 22 333 4444 55555 666666 '
re.findall(r'/b/d{3}/b', s)
['333']
re.findall(r'/b/d{3,5}/b',s)
['333','4444','55555']
re.findall(r'/b//d{,5}b')
['55555','666666']
```

**Minimum match**</br>
`'*'` `'+'` `'?'` are usually as many matching characters as possible. Sometimes we want it to match as little as possible. For example, a c language comment `'/* part 1 */code /* part 2 */'` if the maximum rule is used
```python
import re
s =r '/* part 1 */ code /* part 2 */'
re.findall(r'//*.*/*/',s)
['/* part 1 */ code /* part 2 */']
re.findall(r'//*.*?/*/',s)
['/* part 1 */' ,'/* part 2 */']
```













