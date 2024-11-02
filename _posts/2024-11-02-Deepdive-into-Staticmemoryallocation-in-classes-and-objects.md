---
title: "Static memory allocation in object|classes in c++"
date: 2024-11-02 00:00:00 +0000
categories: [memory, computers, technology]
tags: [memory, optimization, C++, static allocation, classes]
---

**I would first suggest that go and read the `introduction-to-static-memoryallocation` blog it has all the details about what static memory allocation is**

**we would be discussing about how static variables act in the context of classes and object today!**

## Regular | non-static variable

**Before we hope on to learning how static variables work inside the classes , it is better to first understand how non-static variable work in classes so that we can differentiate between them**

```c++
#include <iostream>
using namespace std;

class Increment {
public:
    int x;

    void inc() {
        x = x + 1;
        cout << "Value of x is now: " << x << endl;
    }
};

int main() {
    Increment inc1; // Creating an object called "inc1" of class "Increment"
    inc1.x = 100;   // Initializing x of inc1 to 100
    inc1.inc();     // Calling the increment function
    inc1.inc();

    cout << "--------" << endl;

    Increment inc2; // Creating an object called "inc2" of class "Increment"
    inc2.x = 200;   // Initializing x of inc2 to 200
    inc2.inc();     // Calling the increment function
    inc2.inc();

    return 0;
}
```
**Output**
```bash
value of x is now :101
value of x is now :102
--------
value of x is now :201
value of x is now :202
```
1. We simply created 2 different objects of the same class and we set `x=100` for `inc1` while we initialized the `x=200` for `inc2` 
2. The thing to note from the output is both of them have their own copy of `x` that is why they were able to print out separate values

**non-static variables inside classes each get their own copy inside memory when a new object is made in short each object | instance has its own copy of the variables of the class**

![Visual representation](https://raw.githubusercontent.com/NeoSoul01/NeoSoul01/refs/heads/main/v1.png)

**This is the visual concept of what is happening**

## static variable in classes objects

**The way static variable work in classes is that one copy of the static variable is made inside the memory and that same variable is shared across all the object | instances**

```c++
#include <iostream>
using namespace std;

class Increment {
public:
    static int x; // Static allocation of a variable

    void inc() { // Function that increments x
        x = x + 1;
        cout << "Value of x is now: " << x << endl;
    }
};

// Telling the compiler to allocate the memory for x
int Increment::x = 0;

int main() {
    Increment inc1; // Creating an object called "inc1" of class "Increment"
    inc1.inc();
    inc1.inc();

    cout << "--------" << endl;

    Increment inc2; // Creating an object called "inc2" of class "Increment"
    inc2.inc();
    inc2.inc();

    return 0;
}
```

**Output**
```bash
value of x is now :1
value of x is now :2
--------
value of x is now :3
value of x is now :4
```
1. I previously said that the static variable is shared across all the objects | instances , what does it mean? it means that inside memory there will only one variable (static) and all the objects created for that class->`(inside which static var exist)` all those objects will use that same `variable`

    ![Image Description](https://raw.githubusercontent.com/NeoSoul01/NeoSoul01/refs/heads/main/v2.png)

2. When we understand all this and then focus on the output , the dots start to connect why the value of `x` kept going from `1 -- 4`
	1. When we call the function 2 times `inc()` using `inc1` (object) our value goes from   `0-> 1 -> 2` 
	2. But normally you would be thinking it should reset after that right? because memory is deallocated after a function call ends? **That is the point where I would suggest do not confuse a normal variable with static variable** their lifetime is till the end of the `program` not just the end of `function`

    **The value keeps getting incremented where it left off `2->3->4` Due to the following reasons :**
- **Since there is a common variable which is being used by objects and due to its lifetime so `inshort` because of `static variables` all of this is happening**

## dive into the code

**The rest of the code , i have already explained but there was a bit out of the norm thing that we encountered here , let us discuss about that :**

```C++
static int x ; // declaration of the static varianle
int increment::x=0; // definition and initiliazation of the static variable
```

**You saw these in the code above right? some questions do arise that why are we doing this? lets discuss about these in detail**

Declaring and defining a `static` variable in a class actually requires two separate steps:

**Declaring**
1. In the first line of code we are declaring the static variable , we are telling the compiler that "Mr.Compiler we have a static variable `x` that now exist in the class `increment`"
	1. However, at this point, no memory is allocated, and no initial value is assigned to `x`.

**Definition**
1. In the second piece of code we are basically telling the compiler that " inside the `increment` class there is a variable called `x` allocate memory to that variable and also initialize it to `0`"
	1.  It **allocates memory** for `x` in a single place in memory (not per instance of the class).
	2. It **initializes** `x` to `0`.


```c++
#include <iostream>
using namespace std;

class TestClass {
public:
    TestClass() { // Constructor
        cout << "This is constructor" << endl;
    }

    ~TestClass() { // Destructor
        cout << "This is destructor" << endl;
    }
};

int main() {
    if (true) {
        TestClass t1; // Creating an object of TestClass
    } // t1 goes out of scope here, destructor is called

    cout << "End of main function" << endl;

    return 0;
}
```
**Pretty simple right? constructor gets called , when we exit `if` statement destructor will be called , after that it will just print the following statement in the code**

**output**
```bash
this is constructor
This is destructor
End of main function
```

**lets actually introduce the `static` object now we will simply just put a keyword `static` before the class name and boom now we have a `static` object**

```c++
int main() {
    if (true) {
        static TestClass t1; // Declaring a static object of TestClass
    }

    cout << "End of main function" << endl;

    return 0;
}
```
**let us take a look at output now**

```bash
this is constructor
End of main function
This is destructor
```
**Did u notice the order? the destructor gets called at the end now , but why? because of the `lifetime of static variables`**
