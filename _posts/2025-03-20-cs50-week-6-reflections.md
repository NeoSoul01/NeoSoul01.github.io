---
title: "Week 6: Exploring Python in CS50"
date: 2025-03-20 00:00:00 +0000
categories: [computers, technology, programming]
tags: [CS50, Python, Functions, Loops]
---

# Week 6: Another Step Forward

## Introduction:

Hello folks! Welcome back to Soul's yap session about what he learned in the gut-wrenching Harvard course known as CS50. Once again, I will be talking about my experiences and the challenges I faced and mainly about my journey of this week of CS50. 

For those of you who are unfamiliar with what I am talking about, Harvard offers a course called `Cs50` which any noob like me can take and learn about computer sciences from scratch. I have been taking this course for some time and so far I have reached week 6 in which we are introduced to the famous programming language known as Python.

To be honest, this week of CS50 as compared to the last one was really easy. I am the type of guy who has been programming in the lower level languages `C|C++` for some time, I am still a noob at it, I admit it and recently even started learning `assembly` (I can't stay consistent with it, I need beating) But due to all this experience, the shift to python didn't seem that hard.

Well, of course - It's not like I didn't face any hardship at all, whatever challenged me, every little detail about it, and most importantly how I tackled it. I will go through it all, so this blog can be helpful for anyone who reads it.

## Experience with Lecture Series

So, when I started this week, I was pretty excited for the shift from lower-level languages to python. I always wanted to learn python and did have some experience in it but it wasn't enough. I started learning python a year ago but I left it in between and forgot about it. Later I jumped to another programming language `C++`.

And now...because of CS50 I was back to learning python after a long time but this time, I was a different person, so I knew I wouldn't quit it like last time even if bored me to death. (Yeah...not really a big Python fan.)

### Starting of Week 6

So, when I started week 6, our teacher David threw the translation of the previous week's code in Python right in our faces and just like always I didn't understand the code, I got overwhelmed by it thoughts like: **"am I that bad in programming?"** started occurring to me but I quickly snapped out of it and took a unique approach to tackle this. What approach?

I made a new note section in Obsidian and wrote the following:

**"So the week started and David translated the problem set of weeks 4 and 5 into Python, by the end of the lecture Goal is to translate my version of these problem sets to Python"**

It might seem like a small thing but it gave me hope and courage to continue my journey of week 6. Another important thing to note is that, unlike previous week, where I only took notes for the concepts which troubled me. I changed that approach completely this time.

You might be wondering: **"What approach I took, right?"** Well, I basically started noting everything down, things that seemed easy and especially the things that were hard. **"Why I did do that?** I did it because it seemed right, I was learning a new language, and I simply wanted to note everything down in my own wording.
### How I Utilized C to Help Me in Python

You thought this was it? Nah! One of the most important things that I did was I didn't just leave the previous languages in which I had some experience. Yes, I am referring to `C` and `C++`.

The way I used both of these languages to help me learn Python is pretty interesting. The concepts to which we were introduced in `python` were similar to `C`. Well, because the basics of programming are always the same, it's just the syntax, that you need to get used to.

I simply referred back to C, each time I was introduced to a different topic in python. I practiced that concept in C and then I just applied all that knowledge to python and boom!

Here is a simple example of C code that just prints Hello World:

```c
include headers-
include more headers-
int main()
{

printf("Hello World\n"); // cout<<"Hello World"<<endl; ( in c++)

}
```

Similarly, we can do the same in Python with only one line of code

```python
print("Hello world")
```

I kept repeating this method over and over again. The example above is really simple, but you can take the same approach when programming something complex - at least that is what I did. I always referred back to the programming language in which I had faith over, I solved the problem in that language, and then boom! I made the switch to Python and translated it.

I simply used this approach throughout the lecture series. Sure, there were times when things were getting a bit hard. Topics such as truncation always got to my head. But guess what? C always had my back, so I used it whenever I could to help me understand whatever was challenging me.

Basically, this is how I completed the lecture but completing the lecture is the easy part, now we had to deal with the ending boss. Yes, I am talking about the problem sets.

## Experience with Problem-sets

This week's problem sets were different. Different in what sense? Well, we had to translate some of the most important problem sets from the previous week into Python. Sounds easy, right? Well, not for me.

Turns out, I had accidentally missed some of the problem sets from the previous week and I hadn't realized that until some time ago. Week 6 problem sets included translating those same problem sets that I had missed earlier. Can you actually believe this? True definition of being cursed.

I did plan to implement the problem sets I had missed earlier in the near future..But nature wanted me to do them right now, I guess. So, how exactly did I translate those problem sets? When they didn't exist in the first place, let's get to that.

### Problem Set 1

So, the first problem set we are supposed to translate is `Mario`, we do have 2 versions of it.

The first version of that problem set is known as `Mario-less` which is for people who are less comfortable solving problems and the next is called `Mario-more` which is for people who are just stronger, smarter, and better (jk). Luckily I did complete both of them in the past

But here is the twist, unfortunately, I didn't save the code for both of them. I thought I had it but when I checked it, it wasn't there `-_-` So, I had to rewrite it as well. I wrote both of them in `C` first which did challenge me a bit because I don't have 1 TB of memory rather my brain is like a register.

Anyway, after completing both versions' code in `C`, I had to translate it into Python. Although It is not really necessary to solve both of them, you can just complete 1 of them and you are good to go. But.. I am Soul, I had to do both of them to satisfy my inner self. Damn, I should become a philosopher at this point, I yap too much.

So, when I started translating it into Python, I faced one problem. Any guesses on what that might be? The problem I encountered was inside Python's loop. Let me show you some of my code to explain things in a better way.

```python
number = int(input("Enter the number : "))
while number < 1 or number > 8:
number = int(input("Please Enter the number : "))

for i in range(1, number+1): # equivalent to i=1 , i <= number
    for j in range(number - i):
        print(" ", end ='')

# more of the code, which I can't show for academic reasons...
```

The outer loop, in front of which there is a comment, do u see that? To make it similar to how the code was in `C`. I needed to do `1, number+ 1` meaning that the loop gets initialized at `1` and will continue till it is `equal to the number` not `less than that number` 

Now, I know this is a very simple thing, but I had to use 1-2 extra brain cells to figure it out. Other than that, It was simple and this is the `Mario-less` code. The difficult version of it which is `Mario-more` is very similar just more extra stuff. My fundamentals were cleared because of this problem which is why It didn't take me much time to solve the `Mario-more` version.

### Problem Set 2

Time passes fast... we are now onto the second problem set, so what was this about? It's called cash and yeah you have to deal with currency in this problem set. You can visit the website called [edx.com](https://edx.org), search for cs50, find this problem set, and understand it yourself because if I start explaining the problem set itself, I would turn old.

So, the main key in this problem set was actually understanding the problem set, although this is the key to solving 90% of programming problems, the rest is just being familiar with the syntax. So, how did I go about implementing the solution to solve this problem set? You are probably curious about it, right? If you aren't then I will cry.

Anyway, let's dive into the code so I can make you understand things in a better way.

```python
def main():
    cents = int(input("Change owed : "))
    while (cents <= 0):
    cents = int(input("Invalid value , re-enter: "))

quarters , cents = calculate_quarters(cents)

# code I can't show...
  
def calculate_quarters(cents):
    quarters = 0
    while(cents >= 25):
        quarters = quarters + 1
        cents = cents - 25
    return quarters, cents

# code I can't show...
```

Are your eyeballs looking at this function? Yes, this very exact function is the problem, If you end up figuring out the logic of just this one function, you can solve the rest of the program easily. I originally implemented this program in `C` So, over there I used a different approach. I used a concept called `pass by reference`, which involves pointers and stuff. I did that, to reduce my lines of code, and because I just wanted to and also there is a quote.

**"If you can, just do it" -soul**

Don't go and murder your friend because of this quote, I just said it in the context of this particular problem. Well, the only thing I didn't know was how the hell pass-by reference works in python. because to my current knowledge, I don't think there are pointers or any of that stuff in Python.

Well turns out you don't need to, you can simple return the values, make new variables and just store those return values into those variables by calling the function. I figured all this out by googling, and asking AI how stuff works in python. Using AI isn't a bad thing in my opinion, just use it wisely and don't tell it to give you the solution.
### Problem Set 3

The last problem set is called `readability`, I was also supposed to implement it a while ago but I didn't because I am blind. That is why I had to implement this as well in `C` first, after that I translated the code into `Python` which was fairly simple. But, since this is Python week I won't show my `C` code, I will just show my Python code and talk about the portions where I was challenged and how I tackled it.

```python
def main():
    sentence = input("Text: ")
    
    letters = count_letters(sentence)
    grade = calculate_index(letters, words , sentences)

   

def count_letters(text):
    count = 0
    i = 0
    while i < len(text) :
        if text[i].isalpha():
            count = count + 1
        i = i + 1

    #print(f"the number of letters are: {count}")
    return count


def calculate_index(letters, words , sentences):
    L = (letters / words) * 100
    S = (sentences / words) * 100
    value = 0.0588 * L - 0.296 * S - 15.8
    index = round(value)

    return index

main()
```

Look at the `count_Letter` function, that is the key to figuring out this whole damn problem set, they told us to count letters but didn't give us any clue as to that how to identify letters. Maybe they did it purposely, so we can figure it out. I had a friend who banged his head in the wall for days to figure it out. He did give me some clues such as that use `Asci` table somehow, and that is how I thought I was going to do it as well. 

But.. I found a more simpler approach, just use the `.alpha()` function. Well, this is fairly simple in Python but in `C`, things were different. Python abstracts tons of lower-level detail but `C` doesn't do that, you have much more control and that is the thing I like about `C`. Anyway, I am drifting away from the topic again. Let me show you a tiny piece of code of this problem set that I wrote in `C`


```c
int count = 0;
int i = 0;
while (text[i] != '\0')
{
if(isalpha(text[i]))
{
 count++;
}
i++;
}
```

Can you notice the difference? Strings don't have a definite size like `int..etc` So the only way a computer can tell if a string is finished is by the literal character `\0`. so what I meant in the loop was as long as they don't encounter that symbol, just keep incrementing count and that solved my problem for `counting letters`.

Translating this to python was a piece of cake, you just had to use the `len` function and python would handles thing for you itself.

There are two other functions as well, in which we are supposed to count words and the sentences and that was fairly simple, you just had to edit this same logic and change conditions and everything was good to go.

The next challenge I faced in implementing this problem was the Coleleuma.. formula, whatever the hell it is called, I don't care. So, I didn't know that you had to implement it in code. I had no clue what to do with it, but after some time and help, I figured out that you are just supposed to apply the formula in code and that's it. 

And with that, I ended up solving this problem set as well. Freedom finally!

There is another problem set called `DNA` after `readability` but, I didn't solve it. It had too much biology in it. I am not doing that shit again. I already solved another version of `DNA` in week 5 but this time? Hell nah! I ain't doing that. Perhaps in the future...maybe.


## Personal Advice

So, I don't have much to say, but still I would like to again emphasize on the point that some of you reading this might think that I am some genius who solved this very quickly. No! Everyone has their own way of doing things, don't compare yourself with other's on the internet or even your friend group in a way that you get demotivated.

And if you do end up solving some problems quicker than others, no need to get cocky as well. Just stay humble, and consistent and keep going. I am rooting for all of you out there.

**And as always Stay safe, stay secure.**
