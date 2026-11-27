---
layout: page
title: 从0开始写的C++教程
permalink: /code/cpp/
---

> 这个教程希望在我去世之前能写完QvQ

本人是比较喜欢 C++ 的，C++ 相比于其他语言，学习难度不能说是很大，只能说巨大了。

因此这个教程相比于是给别人看的，更像是一个个人的笔记，用于记录我学习 C++ 曾经或者是现在遇到的问题。

## 目录

- [1. 什么是 C++](#what-is-cpp)
- [2. 打印 Hello World](#hello-world)

## 前置知识

- 会基本的电脑操作
- （可选）有 C 语言基础，学习初期会更轻松

---

###### 1.什么是c++ {#what-is-cpp}

我在初次看到c++时，给我一种这个玩意跟c语言有什么区别，当上手写了一段时间后感觉

> 这个玩意跟c直接除了加入了面向对象的部分之外真的有区别吗?

你说的对，但是

> c++它是由 Bjarne Stroustrup 于 1979 年在贝尔实验室开始设计开发的

它最初的目的就是想在c语言的基础上，扩充和完善了一些内容。

重点在于加入了面向对象的部分，因此如果你学过c语言，那么在学习c++的初期阶段会十分简单(当然只是初期)

###### 2.打印Hello World {#hello-world}

在学习编程的时候总会提到一个经典的第一步，打印Hello World。具体的代码在c++中如下

```cpp
#include <iostream>

int main() {
    std::cout << "Hello, World!" << std::endl;
    return 0;
}
```

```cpp
#include <iostream>
//尽管现在不会报错，但在编写大型项目的时候可能会出现命名冲突
using namespace std;
int main() {
    cout << "Hello, World!" << endl;
    return 0;
}
```

```cpp
#include <iostream>
//这样写可以使程序变得简洁些（但是当内部有重名的时候就不要这么写了）
using std::cout;
int main() {
    cout << "Hello, World!" << std::endl;
    return 0;
}
```

这里需要知道上述的代码每行的含义

1.  #include \<iostream> 代表引用了头文件 iostream 这个头文件的具体作用会在后面讲解

2. int main() 程序的主函数 程序在运行时大多数情况下会先运行这个函数(具体的特例类似于全局对象调用构造函数)

3. std::cout 这里需要注意，我在初学(你可能也一样)的时候看的教程给出的cout前并没

   有std，而是在main函数前写一个 using namespace std; 

   他的作用是告诉程序在这里使用命名空间std，但这会引发严重的命名冲突，如果感觉std::cout写起来很麻烦 可以写一个类似的 using std::cout; 具体如上

4. std::cout的作用类似于其他语言的print函数 其可以将 << 右侧的字符 变量进行打印，顺序为从左往右

5. return 0 这个是函数的终点 表示这个函数返回一个0 在主函数里可以省略这个，在编译时，会默认加上这个return 0

下个文档会讲解环境的构建^^