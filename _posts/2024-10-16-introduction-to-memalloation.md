---
title : "Introduction to static memory allocation"
date : 2024-10-16 00:00:00 +0000
categories: [memory, computers, technology]
tags: [memory, optimization, computers]
---

**In this blog we will be learning about how the memory can be allocated staticly!**


**it is recommended to have a decent grasp on some concepts like `pointers`, `stack|heap memory`, I'm going to assume that you are already familiar with these topics so lets dive in!


## what is static memory allocation?

**Static memory allocation means that the memory for variables is allocated at compile time. This memory is fixed and cannot be changed while the program is running**

```c++
void memoryallocation()
{
int x = 10; // static memory allocation
int arr[] = {1 , 2};// static memory allocation of an array
// when function ends , The memory is automatically deallocated
}
```

**One major difference in `static` and `dynamic` memory allocation is the amount of control we have on the allocation process of our code that takes place inside the memory**


### How much control do we have?

1. you might have heard that we have no control at all in `static memory allocation` but it is only partially correct because we are still in control of the memory allocation process `partially` , because we can specify the `data type` and also the `scope` of a variable 


### allocation and deallocation
1. In static memory allocation, the size and memory address of variables are determined when you compile the program .

2. when we  `staticly allocate memory` most of the work is done by the computer itself , look at the code above to better understand this 

3. When the function `memoryallocation()` is finished , the computer itself automatically deallocates all the memory that was taken up by the variables we made inside that function


## Relation btw Static Mem allocation and Stack
let us talk about the relation between stack and static memory allocation , I'll be demonstrating all this using code and pictures .

![alt](https://raw.githubusercontent.com/NeoSoul01/NeoSoul01/refs/heads/main/relation.png)

1. Static allocation and stack work very closely because the allocation takes place inside the stack which is a part of memory 
	1. **whenever static allocation is mentioned first thing that should come to you're mind is `stack`**

2. Stack follows the `lIFO` method , so the function that are called first are placed in a way which is very clear by the picture , and that process keeps on happening 

**Example :**
1. `Main()` is the first one to be called that is why its the first one inside stack
2. `memoryallocation()` is the second one to be called that is why it is present at the second place inside the stack and so on...

    ![alt](https://raw.githubusercontent.com/NeoSoul01/NeoSoul01/refs/heads/main/example.png)

**you will be wondering , where did the `add()` go from the stack**

1. That is called popping , when a function is called and after performing its duty code is coming to an end , more specifically when it reaches `return` , that function automatically gets popped from the memory

2. This process of `popping` keeps taking place till there are no more functions left even the `main()` functions `stack` is popped when it has performed its duties . 


### Summary

1. **Popping Stack Frames:**
    
    - Each time a function (including `main()`) completes its execution, its stack frame is popped from the call stack. This process continues until there are no more functions left to return to.

2. **Main Function’s Role:**
    
    - The `main()` function is special as it serves as the entry point of the program. Once it finishes executing its code, its stack frame is also removed from the call stack, just like any other function.

3. **Final State:**
    
    - After the `main()` function reaches the return point , the program terminates, and the operating system cleans up any remaining resources allocated for the program.