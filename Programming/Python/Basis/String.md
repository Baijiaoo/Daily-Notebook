String
===

Index
---

* Defination of String
* Basic Operation of String
  * Visiting values in String
  * Updating String
  * Repeating String
  * Escape String

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
### Upadting String
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

'HHHH'
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
Python uses a backslash `\` escape character when you need to use special characters in characters
|Escape String      |Description      |
|====               |====             |
|\(end of the line) |Continuation     |
|\\                 |BackSlash Symbol |
|\'                 |Apostrophe       |
|\''                |Double apstrophe |
|\a                 |Ringing bell     |
|\b                 |Back Space       |
|\e                 |Escaping         |
|\000               |Blank            |
|\n                 |Changing Line    |
|\v                 |Designing Table Vertically|
|\t                 |Designing Table Horizontally|
|\r                 |Returning        |
|\f                 |Changing Page    |
|\oxx               |Octal Number, \o12 means Returning|
|\yxx               |Hexadecimal Number. \y12 means Returning|

### 






