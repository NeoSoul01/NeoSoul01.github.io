---
title : "Introduction to static memory allocation"
date : 2024-10-18 00:00:00 +0000
categories: [memory, computers, technology]
tags: [memory, optimization, computers]
---

**In this blog we will be learning about how the memory can be allocated staticly!**


**it is recommended to have a decent grasp on some concepts like `pointers`, `stack|heap memory`, I'm going to assume that you are already familiar with these topics so lets dive in!**


```c++

int z = 10; // global variable which is also allocated staticly

void memoryallocation()
{

static int x = 10; // memory allocated staticly using keyword "static"
int y = 10; // automatic (stack) allocated memory

x++;
cout<<"value for x is : "<<x<<endl;
//incrementing y  
y++;
cout<<"value for y is : "<<y<<endl
//incremented z  
z++;
cout<<"value for z is :"<<z<<endl;

}

int main()
{
for(int i = 0 ; i<3 ; i++)
{
memoryallocation();
}
}
```

**One major difference in `static` and `dynamic` memory allocation is the amount of control we have on the allocation process of our code that takes place inside the memory**

### dive into the code

`memoryallocation()`

1. In this function we create 2 variables , one of them `x` is `staicly allocated` inside `memory` and it is also a `static variable` 

2. Then we have the variable  `y` , which is `allocated automatically (stack)`

3. We also have a global variable `z` which is created outside the function `memoryallocation()` and it's `memory` is also  `allocated staticly`

4. This function is also responsible for `incrementing` and `displaying` the values of the variables.


`int main()`

1. we simply use a `for` loop to call the function `3` times , now what is going to be interesting is the output

`output`

```bash
value for x is : 11
value for y is : 11
value for z is : 11
value for x is : 12
value for y is : 11
value for z is : 12
value for x is : 13
value for y is : 11
value for z is : 13
```

1. The values of `x` and `z` are the only values which are being incremented every time and being updated , Both of the values started from `10` and finished at `13` because we called the function `memoryallocation()` 3 times , They are `staticly allocated` that is why they retain their values till the very end of the `program itself`  not just the `function` and when program finishes  , that is when they are finally `deallocated` from the memory 

2. The value for `y` did not change , ehh why? because it is not allocated statically due to which every time the function `memoryallocation()` exits , `y` is destroyed and then again when the function `memoryallocation()` is called  , the value for `y` is `reinitialized` and this keeps happening that is why value for `y` never changes

## How much control do we have?

1. you might have heard that we have no control at all in `static memory allocation` but it is only partially correct because we are still in control of the memory allocation process `partially` , because we can specify the `data type` and also the `scope` of a variable 


### Allocation of Static Memory

1. The  memory for `staticly allocated variables` is allocated at compile time and it retain it's value throughout the program , not just till the end of the function


### Deallocation of Static Memory

1.  Unlike dynamic memory (allocated with `new`), which must be manually deallocated with `delete`, both global and static variables are automatically deallocated by the operating system when the program terminates. This means that while they exist in memory for the program's duration, they don't require explicit cleanup.



## Relationship with the Stack

1. These are stored in the data segment and have a lifetime equal to the program’s duration. They are not affected by function calls and do not follow the stack’s LIFO principle.

2. While in the case of `automatically allocated variables` they do follow the stack's LIFO principle and  stored on the stack and their lifetime is limited to the function call which means they are `reinitialized` every time the function they are declared inside is called
