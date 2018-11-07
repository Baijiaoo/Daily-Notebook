String
===

Index
---

* Defination of String
* Basic Operation of String
  * [Visiting values in String](#visiting-values-in-string)
  * [Updating String](#updating-string)
  * [Repeating String](#repeating-string)
  * [Escape String](#escape-string)
  * [Formatting String](#formatting-string)
  * [Unicode String](#unicode-string)
  * [Common Build-in Functions](#common-build-in-functions)

## Defination of String
Strings are the most commonly used data types in Python. We can use quotation marks `""` to create a string</br>
Creating a string is as simple as assigning a value to a variable

## Basic Operation of String
### Visiting values in String
Python accesses substrings, you can use square brackets `[]` to intercept strings
```python
str_ = "Hello World"
print  str[0]

H
```
### Updating String
We can use `+` to update existed string
```python
str_ = 'Hello'
print str_ + ' James'

Hello James
```
### Repeating String
We can use `*` to repeat string
```python
str_ = 'H'
print str_ * 4

HHHH
 ```
### Determining whether substring exists in String
We can use `in` and `not in`, it will return 'True' or `False`
```python
str_ = 'Hello World'
print 'H' in str_
True

print 'Q' in str_
False
```
### Escape String
Python uses a backslash `\` escape character when you need to use special characters in characters</br>

|<center>Escape String</center>      |<center>Description</center>      |
|------------------          |------------------          |
|`\`(end of the line) |Continuation     |
|`\\`                 |BackSlash Symbol |
|`\'`                 |Apostrophe       |
|`\''`                |Double apstrophe |
|`\a`                 |Ringing bell     |
|`\b`                 |Back Space       |
|`\e`                 |Escaping         |
|`\000`               |Blank            |
|`\n`                 |Changing Line    |
|`\v`                 |Designing Table Vertically|
|`\t`                 |Designing Table Horizontally|
|`\r`                 |Returning        |
|`\f`                 |Changing Page    |
|`\oxx`               |Octal Number, `\o12` means Returning|
|`\yxx`               |Hexadecimal Number. `\y12` means Returning|

### Formatting String

|<center>Format String</center>|<center>Description</center>|
|------------------------------|----------------------------|
|`%c`|Formatting character and its ASCII code|
|`%d`|Formatting int|
|`%e`|Formatting float by scientific notation|
|`%E`|Same as `%e`|
|`%f`|Formatting float, and decimal numbers `.2f%`|
|`%o`|Formatting no symbol ocatal number|
|`%x`|Formatting no symbol hexadecimal number|
|`%u`|Formatting no symbol int|
|`%p`|Formatting varirables hexadecimal address|

### Unicode String
The lowercase `"u"` in quotation marks indicates that a Unicode string is created here. If you want to add a special character, you can use Python's Unicode-Escape encoding.
```python
# '\u0020' means space
print u'Hello\u0020World !'

u'Hello World'
```
### Common Build-in Functions
* `string.capitalize()` Capitalizaing this first character in string</br>
* `string.center(width)` Centering the string and using space to fill the new string to width</br>
* `string.count(str, beg=0, end=len(string))` Returning the number of `str` in `string`, start is `beg` and end is `end`</br>
* `string.decode(encoding='UTF-8',errors='strict')` Using `encoding` to decode `string`</br>
* `string.encode(encoding='UTF-8',errors='strict')` Using `encoding` to encode `string`</br>
* `string.endwith(str, beg=0, end=len(string))` Checking `string` is end with `str`, range from `beg` to `end`</br>
* `string.expandtabs(tabsize=8)` Changing tabs in `string` to space and default `tabsize` is 8</br>
* `string.find(str, beg=0, end=len(string))` Checking whether `str` existing in `string`, ranging from `beg` to `end` and returning the start index, if not existing will return `-1`</br>
* `string.format()` Formatting `string`</br>
* `string.index(str, beg=0, end=len(string))` Checking whether `str` existing in `string`, ranging from `beg` to `end` and returning the start index, if not existing will post `error`</br>
* `string.isalnum()` If at least one character exists in `string` and all of characters are `alpha` or `number`, will return `True` otherwise will return `False`</br>
* `string.isalpha()` If at least one character exists in `string` and all of characters are `alpha`, will return `True`otherwise will return `False`</br>
* `string.isdecimal()` If at least one character exists in `string` and all of characters are `decimal`, will return `True`otherwise will return `False`</br>
* `string.isdigit()` If at least one character exists in `string` and all of characters are `digit`, will return `True`otherwise will return `False`</br>
* `string.isspace()` If at least one character exists in `string` and all of characters are `space`, will return `True`otherwise will return `False`</br>
* `string.join(seq)` Using `string` as seperation sympol and connecting all elements in seq to create a new string</br>
* `string.lower()` Transferring all upper elements to lower in `string`</br>
* `string.lstrip(obj)` Removing all `obj` from left side of `string`</br>
* `string.rstrip(obj)` Removing all `obj` from right side of `string`</br>
* `string.split(obj, num)` Splitting `string` according to `obj` for `num` times, and return a list</br>
* `string.strip(obj)` Removing all `obj` from both right & left sides of `string`</br>
* `string.swapcase()` Reverting all capitalization in `string`</br>
* `string.title()` Transforming `string` to be title, means all words in `string` to start with upper</br>
