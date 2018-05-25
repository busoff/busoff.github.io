---
layout: post
title: Magic Number
date: 2017-07-16 12:28
categories: programming
---

>Any number other than 0 or 1 is likely to be magic and should have a name of its own

- Give a name to magic number
- Define number as constants instead of macro: macro is too powerful to use it for this. constants are born to this purpose.
- Use character constants instead of integer

```cpp
// prefer to
if( c>='A' &&  c <= 'Z')
// instead of
if( c >= 65 && c <= 90)
```
  - number 0

```cpp
// for pointer
char* str = nullptr;

char text[1024] = {'\0'};

```

- use language to calculate the size of object

```cpp
// recommended
fget(buffer, sizeof(buffer), stdin)

// not recommended
fget(buffer, 1024, stdin)

```
