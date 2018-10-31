 List
 ===
 
 Index
 ---
 <!-- TOC -->
 
 * [列表的定义]()
 * [列表的属性]()
 * [列表的基本操作](#列表的基本操作)
 * [列表的高级操作]()
 
 <!-- TOC -->
 
 ## 列表的定义
 ## 列表的属性
 ## 列表的基本操作
 * 按照索引取值</br>
 列表第一个元素的索引是0，最后一个元素的索引可以用-1表示
 ```python
list_ = [1,2,3,4]
print list_[0]
print list_[-1]
 
 1
 4
 ```
 * 切片[start,end,step]</br>
 切片切出来的是子列表,输出的子列表中的最后一个元素的索引是**end-1**
 ```python
list_ = [1,2,3,4,5]
list[0:3:1]
 
 [1,2,3]
 ```
 * len() 计算列表长度
 ```python
 list_ = [1,2,3,4,5]
 print len(list_)
 
 5
 ```
 * append() 列表末尾追加元素
 ```python
 list_ = [1,2,3,4]
 list_.append(5)
 print list_
 
 [1,2,3,4,5]
 ```
 * insert() 指定索引位置添加元素
 ```python
 list_ = [2,3,4,5]
 list_.insert(0,1)
 print list_
 
 [1,2,3,4,5]
 ```
 
 
 
 
 
 
 
 ## 列表的高级操作
