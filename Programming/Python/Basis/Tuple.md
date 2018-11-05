Tuple
===

Index
---

## Tuple
* [Defination and characteristic of Tuple](#defination-and-characteristic-of-tuple)
* [Basic Operation of Tuple](#basic-operation-of-tuple)
    * [Visiting values in Tuple](#visiting-values-in-tuple)
    * [Updating Tuple](#updating-tuple)
    * [Deleting elements in Tuple](#deleting-elements-in-tuple)
    * [Tuple Operators](#tuple-operators)
    * [Built-in functions of Tuple](#built-in-functions-of-tuple)

### Defination and characteristic of Tuple
Python tuples are similar to lists, except that the elements of the tuple cannot be modified</br>
Tuples use parentheses and lists use square brackets</br>
Tuple creation is simple, just add elements to the parentheses and separate them with commas</br>
Creating empty tuple
```python
tuple_ = ()
```
Only one element in tuple, we need to add comma behind the element
```python
tuple_ = (50,)
```
Tuple is similar to the string, and the subscript index starts from 0, and can be intercepted, combined, and so on
### Basic Operation of Tuple
#### Visiting values in Tuple
We can use the subscript index to visit elements in Tuple
```python
tuple_ = (1,2,'James','Chole',[1])
print tuple_[2]

James
```
#### Updating Tuple
We can not modify any elements in the Tuple, but we can combine two Tupels to create a new Tuplele
```python
tuple_1 = (1,2,3)
tuple_2 = ('age','name','date')
tuple_3 = tuple_1 + tuple_2
print  tuple_3

(1,2,3,'age','name','date')
```
#### Deleting elements in Tuple
We can not delet any elements in the Tuple, but we can use `del` to delete the whole Tuple
```python
tuple_1 = (1,2,3)
del tuple_1
print  tupel_1

NameError: name 'tup' is not defined
```

#### Tuple Operators
|Operator   |Result     |Description      |
|----       |----       |----             |
|(1,2,3)+(4,5,6)          |(1,2,3,4,5,6)      |Combining two Tuples |
|("Hi!") * 2              |("Hi!","Hi!","Hi!")|Copy elements|
|3 in (1,2,3)             |True               |Determining if an element existing|
|for i in (1,2,3); print i|1 2 3              |Iteration|

#### Tuple Index
Tuple is also a sequence, we can access the element at the specified position in the tuple, or we can intercept an element in the index, as shown below
```python
L = ('spam', 'Spam', 'SPAM!')
print L[2]
print L[-2]
print L[1:]

'SPAM!'
'Spam'
('Spam','SPAM!')
```

#### Built-in functions of Tuple
**len(tuple)** return the length of tuple
```python
tuple_ = (1,2,3,4)
print len(tuple_)

4
```
**max(tuple)** return the max value in the tuple
```python
tuple_ = (1,2,3,4,5)
print max(tuple)

5
```
**min(tuple)** return the minimum value in the tuple
```python
tuple_ = (1,2,3,4)
print min(tuple_)

1
```
**tuple(seq)** transfer list to tuple
```python
list_ = [1,2,3,4]
print tuple(list_)

(1,2,3,4)
```
