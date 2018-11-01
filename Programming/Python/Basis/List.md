 List
 ===
 
 Index
 ---
 <!-- TOC -->
 
 * [列表的定义](#列表的定义)
 * [列表的基本操作](#列表的基本操作)
   * [访问列表中的值](#访问列表中的值)
   * [列表脚本操作符](#列表脚本操作符)
   * [列表函数](#列表函数)
   * [列表方法](#列表方法)
 * [列表的高级操作]()
 
 <!-- TOC -->
 
 ## 列表的定义
 Python中最基本的数据结构。序列中的每个元素都分配一个数字 - 它的位置，或索引，第一个索引是0，第二个索引是1，依此类推</br>
 Python有6个序列的内置类型，但最常见的是列表和元组</br>
 序列都可以进行的操作包括索引，切片，加，乘，检查成员</br>
 此外，Python已经内置确定序列的长度以及确定最大和最小的元素的方法</br>
 列表是最常用的Python数据类型，它可以作为一个方括号内的逗号分隔值出现</br>
 列表的数据项不需要具有相同的类型</br>
 创建一个列表，只要把逗号分隔的不同的数据项使用方括号括起来即可
 
 ## 列表的基本操作
 ### 访问列表中的值
 * **list[index]** 按照索引取值</br>
 列表从左边第一个元素的索引是`0`，从右边第一个元素的索引是`-1`
 ```python
list_ = [1,2,3,4]
print list_[0]
print list_[-1]
 
 1
 4
 ```
 * **list[start,end,step]**</br>
 `start`--起始索引</br>
 `end`--终止索引</br>
 `step`--索引步长</br>
 切片切出来的是子列表,输出的子列表中的最后一个元素的索引是`end-1`
 ```python
 list_ = [1,2,3,4,5]
 list[0:3:1]
 
 [1,2,3]
 ``` 
 ### 列表脚本操作符
   |Python 表达式  |结果    |描述    |
   |-----         | -----: |----     |
   |[1,2,3]+[4,5,6]|[1,2,3,4,5,6]|列表组合|
   |['abc'] * 4|['abc','abc','abc','abc']|列表重复|
   |'a' in ['abc']|False|元素是否存在与列表中|
   |for i in [1,2,3]|1,2,3|列表元素迭代|

 ### 列表函数
 * **len(list)** 计算列表长度
 ```python
 list_ = [1,2,3,4]
 print len(list_)
 
 4
 ```
 * **max(list)** 返回列表中最大的值
 ```python
 list_ = [1,2,3,4,5]
 print max(list_)
 
 5
 ```
 * **min(list)** 返回列表中最小的值
 ```python
 list_ = [1,2,3,4,5]
 print min(list_)
 
 1
 ```
 * **list(seq)** 将元组转化为列表
 **注:** 元组和列表非常类似，但是元组不能修改并且是用圆括号
 ```python
 seq = (1,2,3,4)
 print (list(seq))
 
 [1,2,3,4]
 ```
 
 ### 列表方法
 * **list.append(obj)** 列表末尾追加元素
 ```python
 list_ = [1,2,3,4]
 list_.append()
 print list_
 
 [1,2,3,4,5]
 ```
 * **list.extend(obj)** 将一个列表中的全部元素添加到另一个列表中
 ```python
 list_1 = [1,2,3,4]
 list_2 = [5,6,7]
 list_1.extend(list_2)
 list_1
 
 [1,2,3,4,5,6,7]
 ```
 * **list.insert(index,obj)** 指定索引位置添加元素
 ```python
 list_ = [2,3,4,5]
 list_.insert(0,1)
 print list_
 
 [1,2,3,4,5]
 ```
 * **list.pop([index=-1])** 默认删除列表末尾的元素,并且返回该元素的值
 ```python
 list_ = [1,2,3,4,5]
 print(list_.pop())
 
 5
 list_
 
 [1,2,3,4]
 ```
 * **list.remove(obj)** 删除列表中指定的元素
 ```python
 list_ = [1,2,3,4,5]
 list_.remove(3)
 list_
 
 [1,2,4,5]
 ```
 * **list.count(obj)** 统计列表中某个元素出现的次数
 ```python
 list_ = [1,1,1,2,3]
 print list_.count(1)
 
 3
 ```
 * **list.index(obj)** 用于从列表中找出指定值第一个匹配项的索引位置,如果没有找到就会抛出异常
 ```python
 list_ = [1,1,2,3,4,5]
 print (list_.index(1))
 print (list_.index(1,2))
 
 0
 1
 ```
 * **list.reverse()** 没有返回值，直接将列表反转排序
 ```python
 list_ = [1,2,3,4,5]
 print list_.reverse()
 
 [5,4,3,2,1]
 ```
 * **list.sort(cmp=None, key=None, reverse=False)** 用于对原列表进行排序, 列表中的元素必须是相同数据类型</br>
 `cmp`--可选参数，如果指定了该参数会使用该参数的方法进行排序</br>
 `key`-主要用来进行比较的元素，只有一个参数，具体的函数的参数取自可迭代对象中，指定可迭代对象中的一个元素进行排序</br>
 `reverse`-- `reverse=True`降序，`reverse=Flase`升序</br>
 ```python
 list_ = ['Google','Facebook','Tencent']
 print list_.sort(reverse=True)
 
 ['Tencent','Google', 'Facebook']
 
 list_ = [(4,2),(3,3),(1,1),(6,4)]
 def cmp_second(element):
     return element[1]
 print list_.sort(key=cmp_second)
 
 [(1,1),(4,2),(3,3),(6,4)]
 ```
 * **list.clear()** 清空一个列表
 ```python
 list_ = [1,2,3,4]
 print list_.clear()
 
 []
 ```
 * **list.copy()** 深度拷贝一个列表到另一个地址中
 ```python
 list_1 = [1,2,3,4]
 list_2 = list_1.copy()
 list_2
 
 [1,2,3,4]
 ```
 ## 列表的高级操作
