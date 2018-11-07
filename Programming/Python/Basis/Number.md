Number
===

Index
---

* Defination of Number
* Basic Operation of Number
  * [Number type tansformation](#number-type-transformation)

## Defination of Number
The Python Number data type is used to store numeric values</br>
The data type is not allowed to change, which means that if you change the value of the Number data type, the memory space will be reassigned.</br>
</br>
Python supports four different numeric types:
* **Int** - Usually referred to as an integer or integer, is a positive or negative integer without a decimal point.
* **Long integers** - Infinite integers, the integer is an uppercase or lowercase L.
* **Float** - The floating point type consists of an integer part and a fractional part. The floating point type can also be expressed in scientific notation (2.5e2 = 2.5 x 102 = 250)
* **Complex** - Complex numbers consist of real and imaginary parts, which can be represented by `a + bj`, or `complex(a,b)`. The real part `a` and the imaginary part `b` of the complex number are both **float**.

## Basic Operation of Number
### Number type transforamtion

|Function         |Description        |
|========         |===========        |
|`int(x,[,base])`   |Transfer x to integer|
|`long(x,[,base])`  |Transfer x to long integer|
|`float(x,[,base])` |Transfer x to float|
|`complex(real[,imag])`|Creating a complex number|
|`str(x)`           |Transfer x to string|
|`eval(str)`        |`str` is a expression and return the result of expression|
|`hex(x)`           |Transfer an integer to hex|

### math model and cmath model
The functions commonly used in mathematical operations in Python are basically in the math module and the cmath module.</br>
The Python math module provides a number of mathematical operations on floating point numbers.</br>
The Python cmath module contains some functions for complex operations.</br>
The functions of the cmath module are basically the same as the math module functions. The difference is that the cmath module operates on complex numbers, and the math module operates on mathematical operations.

```python
import math
dic(math)

['__doc__', '__name__', '__package__', 'acos', 'acosh', 'asin', 'asinh', 'atan', 'atan2', 'atanh', 'ceil', 'copysign', 'cos', 'cosh', 'degrees', 'e', 'erf', 'erfc', 'exp', 'expm1', 'fabs', 'factorial', 'floor', 'fmod', 'frexp', 'fsum', 'gamma', 'hypot', 'isinf', 'isnan', 'ldexp', 'lgamma', 'log', 'log10', 'log1p', 'modf', 'pi', 'pow', 'radians', 'sin', 'sinh', 'sqrt', 'tan', 'tanh', 'trunc']

import cmath
dic(cmath)

['__doc__', '__name__', '__package__', 'acos', 'acosh', 'asin', 'asinh', 'atan', 'atanh', 'cos', 'cosh', 'e', 'exp', 'isinf', 'isnan', 'log', 'log10', 'phase', 'pi', 'polar', 'rect', 'sin', 'sinh', 'sqrt', 'tan', 'tanh']
```

### Math Function

|<center>Function</center>       |<center>Description</center>      |
|========================        |=================                 |
|`abs(x)`              |Returning the absolute value of `x`         |
|`math.ceil(x)`        |Returning the up integer, `math.ceil(4.1)`=>`5`|
|`math.exp(x)`         |Returning the power of x of e|
|`math.fabs(x)`        |Returning the float type absolute value of `x`|
|`math.floor(x)`       |Returning the down integer, `math.floor(4.1)`=>`5`|
|`modf(x)`             |Returning the part of integer and float, both are float type|
|`log(x)`              |Like math.log(x), `math.log(100,10)`=> `2.0`|
|`pow(x,y)`            |Returing the power of x of y|
|`sqrt(x)`             |Returning the square root of x|

### Random Function
* `choice(seq)` Randomly select a element from seq
```python
import random
list_ = [1,2,3,4,5]
print random.choice(list_)

3
```
* `randrange(start, end, step)` Randomly select a number from the range(`start`,`end`)
```python
import random
print random.randrange(100, 1000, 2)

888
```
* `random()` Creating a random number in range of `[0,1)`
```python
import random
print random.random()

0.201755309108
```
* `seed()` Changing the seed of the random number generator, which can be called before calling other `random` module functions
* `shuffle(lst)` Randomly sorting elements in `lst`
```python
import random
lst = [1,2,3,4,5]
random.shuffle(lst)
print lst

[1, 5, 2, 3, 4]
```
* `uniform(x,y)` Randomly creating a number in range of (x,y)
```python
import random
print random.uniform(8,9)

8.01955790002
```















