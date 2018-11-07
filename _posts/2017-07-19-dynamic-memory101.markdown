---
layout: post
title: Dynamic Memory 101
date: 2017-07-19T13:30:00.000Z
author: James Huxtable
categories:
  - Blog
  - Low-Level Programming
  - Development
  - Nothing Interesting
img: post01.jpg
thumb: c_thumb.jpg
published: false
---

<b>Dynamic Memory</b> is the use of memory during runtime. It is dynamic in that the compiler is unable to ascertain the exact amount of memory its allocation will require. This differs from static allocation where its size is determined at compile time and its location in memory is the stack. When objects are dynamically allocated they use a special region of memory called the heap. Let's look at those differences. <!--more-->

When using static allocation, the memory we use is stored in a very fast contigous block known as the stack. Each function contributes to the stack placing any static data on to it. When the function is unwound or exited, the memory is freed. The stack has limits in that it is restricted in size and data can not exist outside of it's original scope. Dynamic memory instead uses the region known as the heap. The heap is a large region of memory where allocations and deallocations can happen during runtime and do not obey scope. For example, If you were to allocate memory inside the function, when the function exits the memory remains allocated, it is not freed. This can lead to memory leaks, so care needs to be taken. 


#### Why do we use it?
Because the stack is restrictive


#### How do we use it?
```C++
int  static_int  = 2;
int* dynamic_int = new int(2);
```

#### How do we free it?
```C++
if ( dynamic_int )
{ 
  delete dynamic_int;
  dynamic_int = nullptr;
}
```

Dynamic memory is a complex and detailed area of C++ programming. There is still much to learn, but understanding why it exists and how it compares to static allocation can aid you in it's usage and understanding. Till next time.
