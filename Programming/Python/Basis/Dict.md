Dict
===

Index
---
* [Defination of Dict](#defination-of-dict)
* [Basic Operation of Dict]
  * [Visiting values in Dict]
  * [Updating Dict]
  * [Deleting element in Dict]
  * [Built-in functions of Dict]
  * [Methods of Dict]
  
## Defination of Dict
Dictionary is one of variable container, which can store any types of objectives</br>
Dictionary's each `key=>value` is splitted by `,`, the whole dictionary is enclosed by `{}`</br>
`key` must be unique and can not change its datatype, `value` can be any data types
```python
dict = {key1:value1, key2:value2}
````

## Basic Operation of Dict
### Visiting values in Dict
Using `key` to visit the corresponding value in Dict
```python
dict_ = {name:'Peter', age:18, gender:'male'}
print dict['name']

Peter
```
If the `key` is not existing in dict, it will cause error
### Updating Dict
We can use `dict[new_key]=new_value` to add new key/value pair in the dict, and we can also update the existing `key=>value`
```python
dict_ = {name:'Peter',age:18, gender:'male'}
dict_['national'] = 'USA'
print dict_

{name:'Peter',age:18, gender:'male',national:'USA'}

dict[age] = 25
print dict_

{name:'Peter',age:25, gender:'male',national:'USA'}
```
### Deleting element in Dict
We can delete elements in the dict or we can delete the whole dict
```python
dict_ = {name:'Peter',age:18, gender:'male',national:'USA'}
del dict_['national']
print dict_

{name:'Peter',age:18, gender:'male'}

dict_.clear() #clear all of elements in dict
print dict_
{}

del dcit_ #delete `dict_`
```
### Built-in functions of Dict
**len(dict)** getting the length of dict(number of keys)
```python
dict_ = {name:'Peter',age:18, gender:'male',national:'USA'}
print ("Length of Dict: %d" % len(dict_))

4
```
**str(dict)** transferring datatype to `str`, this way mostly used in `.json`
```python
dict_ = {name:'Peter',age:18, gender:'male',national:'USA'}
print type(str(dict_))

<type:str>
```
### Methods of Dict
**dict.copy()**  Copying of dict
**dict.fromkeys(seq[,val])** Creating a new dictionary, use the elements in the sequence `seq` as the key, and `val` is the initial value of all the keys in the dictionary
```python
seq = ('Google', 'Facebook', 'Twitter')
 
dict_ = dict.fromkeys(seq)
print "new_dict : %s" %  str(dict_)
{'Google':None,'Facebook':None,'Twitter':None}

dict_ = dict.fromkeys(seq, 10)
print "new_dict : %s" %  str(dict_)
{'Google':10,'Facebook':10,'Twitter':10}
```
**dict.get(key,default=None)** `get()` function returns the value of corresponded key, if key is not in the dictionary it will return the `default` value
```python
dict_ = {name:'Peter',age:18, gender:'male',national:'USA'}
print dict_.get(name)
Peter
print dict_.get(height)
None
print dict_.get(height,100)
100
```
**dict.setdefault(key,default=None)** `setdefault` returns `value` if `key` exists in dict, if not existing return `default` value
```python
dict_ = {name:'Peter',age:18, gender:'male'}
print dict_.setdefault(name, None)
Peter
print dict_.setdefault(national, 'USA')
USA
```
**dict.has_key(key)** If `key` in dict return `True`, if not return `False`
```python
dict_ = {name:'Peter',age:18, gender:'male',national:'USA'}
dict_.has_key(name)
True
```
**dict.items()** `items()` return traversable (key, value) tuple array in a list
```python
dict_ = {name:'Peter',age:18, gender:'male',national:'USA'}
print dict_.item()

[(name,Peter),(age,18),(gender,male),(national,USA)]
```
**dict.keys()** return all `keys` in dict by a list
```python
dict_ = {name:'Peter',age:18, gender:'male',national:'USA'}
print dict_.keys()

[name, age, gender, national]
```
**dict.values()** return all `values` in dict by a list
```python
dict_ = {name:'Peter',age:18, gender:'male',national:'USA'}
print dict_.values()

['Peter', 18, 'male', 'USA']
```
**dict1.update(dict2)** adding dict2's `key=>value` into dict1
```python
dict_1 = {name:'Peter',age:18, gender:'male'}
dict_2 = {'national': 'USA'}
print dict_1.update(dict_2)

{age:18, gender:male, name:'Peter', national:'USA'}
```
**dict.popitem()** random return one pair of `(key,value)` and delete it from dict
```python
dict_ = {name:'Peter',age:18, gender:'male'}
pop_item = dict.popitem()
print pop_item
print dict_

(age, 18)
{name:'Peter', gender:'male'}
```
