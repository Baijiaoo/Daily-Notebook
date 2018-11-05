Tuple
===

Index
---

## Tuple
* Defination and characteristic of Tuple
* Basic Operation of Tuple
    * Visiting values in Tuple
    * Updating Tuple
    * Deleting elements in Tuple
    * Tuple Operator
    * Built-in function in Tuple

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
