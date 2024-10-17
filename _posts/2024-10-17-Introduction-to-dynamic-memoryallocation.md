---
title : "Introduction to dynamic memory allocation"
date : 2024-10-17 00:00:00 +0000
categories: [memory, computers, technology]
tags: [memory, optimization, computers]
---

**In this blog we will be learning about how the memory can be allocated dynamically!**

**This blog is kind of a sequel to our previous blog `introduction to static memory allocation`,
because our concepts do get more clear when we compare both of these side by side, anyways lets get into it**


## what is dynamic memory allocation

1. **We simply make a pointer on the stack and that pointer just points towards the memory address of the memory that we allocate `dynamically`** 
2. **The only way we can modify the content of what is on the `heap` is through this `pointer`**

```c++
//Dynamic memory allocation for a simple int
int* ptr1 = new int;
*ptr1 = 14;   
cout<<"the value in heap is:"<<*ptr1<<endl;

//Dynamic memory allocation for an array of type int
int* ptr2 = new int[10];
for(int i=0 ; i < 10 ; i++)
{
ptr2[i] = 10;
cout<<"the value of pointer at index "<<i<<" is :"<<ptr2[i]<<endl;
}
```
**syntax**
- `int *(pointername) = new (datatype)`

- In order to allocate memory inside the `heap` we need to use the `keyword` which is `new` and along with that we need to do all this using a `pointer` because there is no way to access the data that we will be allocating dynamically without `pointers!`


## dive into the code

1. We simply allocate  memory of type `int` using a pointer called `ptr1`  in the starting of code and of course in order to modify the value inside that memory address , we use the `dereference operator` combined with a `pointer` 

2. In the second part of code , we make an `array` that can take in `10 int digits` and then put values inside each element of array through the `for loop` and the loop also just prints out the 

**One of the most important thing to note is :
unlike `static memory allocation`  or how the `stack` does it , our memory that is allocated is not going magically `deallocate` on its own , when we are dealing with `heap/dynamic memory allocation` we have to `deallocate` the memory ourselves**

## delete keyword

we just talked about that we must deallocate the memory ourselves , otherwise it can cause a big issue in the memory  and how do we do that? lets dive into the `how`

```c++
int main()

{
int* ptr1 = new int;
*ptr1 = 14;
cout<<"the value in heap is:"<<*ptr1<<endl;
delete ptr1;
cout<<*ptr1<<endl;
ptr1 = NULL


int* ptr2 = new int[1]; // allocate memory 
*ptr2 = {1};  // put value 
cout<<"the value in heap is:"<<*ptr2<<endl; // print its value
delete[] ptr2; // delete the value stored where the pointer is pointing
cout<<*ptr2<<endl;// print the value to check if it's deleted
ptr2 = NULL // makes sure it aint pointing towards anything
}
```
- So through the keyword called `delete` , we can deallocate the memory that we set inside the `heap`

## dive inside the code

1. In the code , we allocate the memory of type `int` and then we set its value and output its value 
2. Then we use the keyword `delete` but the important thing to note is , we are not deleting the pointer itself with this keyword rather the `address` it is pointing toward is getting deleted

3. just to make sure we deleted what was present at that address , we displayed the value using `*ptr1` and we did get a garbage value on displaying that means we were successful

4. Last thing we do is set the pointer to `null` which is done to make sure the pointer is not pointing to anything anymore .
