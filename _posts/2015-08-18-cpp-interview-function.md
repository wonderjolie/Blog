---
layout: post_layout
title: C/C++技术类面试题集合08
year: 2015
month: Aug
day: 18
subtitle: 函数
series: cpp_interview
excerpt: 本文摘选自《C/C++程序员面试宝典》的技术类面试题，包含C/C++的语言基础、数据结构、算法、软件工程、数据库、操作系统、计算机网络以及部分思维拓展题。
---

**C/C++技术类面试题集合08（函数）**
=====

本文摘选自《C/C++程序员面试宝典》的技术类面试题，包含C/C++的语言基础、数据结构、算法、软件工程、数据库、操作系统、计算机网络以及部分思维拓展题。

----------

##  什么是函数？ ##

> 函数由函数名、参数、返回值类型以及一组包含操作语句的语句块组成。函数可以支持重载，程序就是由函数组成的。

----------

## 形参与实参有什么区别？ ##

> 形参是函数定义或声明时的函数形式参数，形参表制定了函数参数的个数和数据类型，实参是函数调用时传递给函数的参数，传递时要与形参一一对应。

----------

## C++支持参数个数不确定的函数吗？ ##

> C++可以通过隐藏参数机制来支持参数个数不确定的函数。

----------

## 什么是内联函数？ ##

> 在类声明的内部声明或定义的成员函数叫做内联（inline）函数。

----------

##  引用形参和非引用形参有什么区别？ ##

> 引用形参是将参数用参数变量的地址来进行传递，可以通过函数对形参的调用来修改实参的值。

----------

## 使用引用形参有什么问题？ ##

> 调用非const类型的引用形参，实参必须不是const类型的，而且实参的类型和形参的类型应当一致。调用一个有const引用的形参的函时，如果实参不是一个变量或者类型不匹配时，函数会创建一个无名的临时变量用来存储实参的值，并把这个形参作为该临时变量的引用。

----------

## 指针形参与引用形参有什么区别？##

> 指针形参是指函数的参数是指针，它不会像引用形参那样通过函数调用影响实参的值，但是调用后它会修改实参的对象。程序中尽量少使用指针形参，这样会使程序的可读性下降。

----------

## 什么是类成员函数？有哪些特别的类成员函数？ ##

> 类成员中的函数就是类的成员函数，特别的类成员函数有构造函数和析构函数。

----------

## 什么是静态函数？如何使用静态函数？ ##

> 静态函数是使用static修饰符修饰的函数，静态函数没有this指针，只能访问静态变量。在类中如果函数调用的结果不会访问或者修改任何对象数据成员，这样的成员声明为静态成员函数比较好。

----------

## 静态函数能访问类的私有成员？ ##

> 静态函数只能访问类的静态私有成员，静态函数不可以直接访问类的非静态私有成员，但是可以通过自定义的一些特殊方法比如宏替换访问类的非静态私有成员。


----------

## 一个类可以访问另一个类的私有成员吗？ ##

> 外部类可以使用宏定义等特殊方法来实现访问类的私有成员。

----------

## 函数重载与作用域 ##

> 函数重载是指在相同的作用域中，具有相同的名称而形参列表不同的多个函数。

----------

## 如何进行函数重载的匹配？ ##

> 编译器遇到对重载函数的调用时，必须确定调用哪个函数。如果没有能找到参数完全匹配的函数，则找一个替代函数。此时编译器将实在参数与所有重载函数的参数做比较，这一过程称为参数匹配。

----------

## 函数重载时如何实现实参的类型转换？ ##

> 在函数重载匹配时，先通过标准转换类实现匹配，如果不行，再通过类类型转换来实现匹配。


