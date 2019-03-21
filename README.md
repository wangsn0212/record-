# record-
## 输入一个链表，按链表值从尾到头的顺序返回一个ArrayList ##


链表的定义：是一组数据项的集合，其中每个数据项都是一个节点的一部分，每个节点还包含指向下一个节点的链接
链表的结构：data为自定义的数据，next为下一个节点的地址。

- 在C/C++中，通常采用**“指针+结构体”**来实现链表；
- 而在Python中，则可以采用**“引用+类”**来实现链表。


基本元素：

`节点：每个节点有两个部分，左边部分称为值域，用来存放用户数据；右边部分称为指针域，用来存放指向下一个元素的指针。`
`head:head节点永远指向第一个节点`
`tail: tail永远指向最后一个节点`
`None:链表中最后一个节点的指针域为None值`
`链表种类：单向链表、单向循环链表、双向链表、双向循环链表`

 # -*- coding:utf-8 -*-

     class ListNode:

          def __init__(self, x):
              self.val = x
              self.next = None
 
     class Solution:
         # 返回从尾部到头部的列表值序列，例如[1,2,3]
         def printListFromTailToHead(self, listNode):
        # write code here
             l = []
             head = listNode
             while head:
                 l.insert(0, head.val)
                 head = head.next
             return l

备注：



- next() 返回迭代器的下一个项目。

next(iterator[, default])


iterator -- 可迭代对象；default -- 可选，用于设置在没有下一个元素时返回该默认值，如果不设置，又没有下一个元素则会触发 StopIteration 异常。
返回值：返回对象帮助信息。
实例

    #!/usr/bin/python
    # -*- coding: UTF-8 -*-
 
    # 首先获得Iterator对象:
    it = iter([1, 2, 3, 4, 5])
    # 循环:
    while True:
    try:
    # 获得下一个值:
    x = next(it)
    print(x)
    except StopIteration:
    # 遇到StopIteration就退出循环
    break
 输出结果为：

    1
    2
    3
    4
    5 

- iter() 函数用来生成迭代器。

   iter(object[, sentinel])

实例

    lst = [1, 2, 3]
    for i in iter(lst):
        print(i)
    ... 
    1
    2
    3

- insert() 函数用于将指定对象插入列表的指定位置。

list.insert(index, obj)
   
     #!/usr/bin/python

     aList = [123, 'xyz', 'zara', 'abc']

     aList.insert( 3, 2009)

     print "Final List : ", aList
以上实例输出结果如下：

     Final List : [123, 'xyz', 'zara', 2009, 'abc']
