---
title: "My Week 9 Journey"
date: 2025-09-11 00:00:00 +0000
categories: [ computers, technology, Programming]
tags: [CS50, Flask, Web-programming, Jinja]
---

# Week 9 - Week 9: Flask, the Final Boss of CS50

Hey there, welcome back to another yap session - where I talk endlessly about my progress related to CS50.

For those of you who don’t know what CS50 is - it’s a course any noob can take and learn the basics of computer science. But let me be clear: **this isn’t just another tutorial-hell YouTube series**. This course teaches you how to solve problems, how to think, how to **break** problems down and crush them. it completely re-shapes how your brain approaches tech.

I have to say - this week was the toughest of all the weeks - not because I couldn't grasp the concepts in the lecture series but because of 1 particular problem set which took me a long time to solve.

I will be talking about both the problem sets that I needed to complete at the end but before that I will be sharing my experiences throughout the week because... let's be real - You are here to learn from my experience.

Anyway, let's dig right into the details because that's where the good parts are.

## Experience with Lecture Series

This week introduced some new things with which I didn't have any experience at all.

I am talking about: 

- Flask
- Jinja
- Implementation of sessions

And so much more...

This week was directly related to the previous one where we learned about fundamentals of web-programming. This week was about stacking things on top of those foundations.

When I realized that you don't need to write the boring `html boiler plate` code again and again when making a new `html` file - that stood out to me. We could literally use `jinja` which is a python-based template engine to do all that manual work for us.

Over all, David did a great job at holding our hands throughout the entire lecture series. And the one thing I love about `CS50` is that - whenever they introduce a new concept, they teach you how it is implemented and then they also show how hackers can abuse a feature if you don't take the right steps.

You must be wondering... well, what's so special about it soul, right?

**Here's a bit of background:**
I am a big privacy advocate and a security conscious person.
I look for flaws inside systems and outside systems.. because it's rooted in my nature

And when I see people not taking security seriously, it angers me.
It bugs me when they don't realize the consequences of not securing things.

So yeah... when David was actively making sure students are aware of what hackers can do to your website if you don't implement server-side validation and all that - it really stuck with me due to my personality.

---

### What I Experienced Throughout The Week

As we progressed through the week - I was learning more and more about things related to backend and everything was finally clicking about how real world websites function.

Honestly, I think there is a threshold in the world of web development.
Students stay stuck learning the same basics, forever.
(Yes, I am referring to `html, css, javascript`)

And I was one of them as well, but the things I was learning with each passing minute in the lecture was proof that I had shattered that threshold and risen above it.

In flask, there are different routes - when you visit a website you can switch routes manually using the `/(route)` 

Mostly, you do that by clicking buttons and those buttons can be controlled with Javascript and you can redirect users to those paths.

And guess what we were doing throughout the week?
Handling those routes.
And yes, it was mind boggling.

I was slowly realizing how much work developers need to do in order to do the smallest things everyone takes for granted - So yeah, if any developer is reading this - hats off to you, sire.

**Back to the main topic**

Of course I faced problems this time as well.
There were times when i couldn't grasp different concepts related to how sessions work.
And that's when I realized

- Theory is one thing.
- Implementation is another.

Here's an analogy:

- You can read about how to run a business all you want.
- But if you never get your hands dirty, you are not going to know how to do shit.

So, I had a lot of these moments.

Moments where I knew what the theory behind a certain topic was but when it came to actually implementing it - it challenged me... but still **just like every time, I came on top.**

And yes - I used my good old strategy:

> Breaking down the logic.  
> Practicing the syntax.  
> Using AI to help me understand certain topics.

I just kept repeating all this - **day in, day out.**
And just like that... the **week was over.**

---

### Another Interesting Story

I forgot to tell this earlier but then I thought... since it's that important - I can just add a separate section for you guys.

I mentioned session tokens earlier as well.
Well for those of you who don't know what they are - here is a quick explanation:

When you visit a website, you don't log in every single time - That is because that website stores your session token and identifies you because of it every time you visit that website.

It knows - Oh! It's `bigdick69` Let him in.

**And here's where it gets interesting:**
If someone can hijack your session token, then he can literally login the website without needing your password and yes! He also ends up bypassing any kind of `2FA` you had for that site.

**How do I know that?**
Because at the same time I was taking this course - i was actually practicing phishing as well.

Don't worry, I wasn't trying to hijack your `mom's bank credentials` to steal the 10$ she has - I was just doing it for "educational purposes"

And while doing that - Apart from learning a whole buncha other shit, I also learned to hijack session tokens for the first time and man, it was fucking awesome.

**What does this have to do anything with CS50?**
Well... when David was teaching us about sessions - that other part of me clicked
I was like... man this is so cool - I just learned how to hijack them and now I am learning how to use them in real world websites to track users.

**What's my point?**
I told you all of this for a reason - It's because knowing the both sides of the coin can really take you far in the world of computers. 

Think about it:

- If you know how to break a thing
- And you also know how to make that thing.

Then you are already ahead of majority of developers or hackers.
There is a reason why the top hackers have a background as developers or experience in some other domain which allows them to understand computers in and out.

So, if any of you is trying to make a career in cybersecurity - don't just spend time on 1 side of the coin - make sure you spend time on the other side as well.

![alt text](fightclub.png)

*Who am I even talking with? There is no body on the other side of the screen, sometimes... I feel just like him.*



## Experience with problem sets

This week’s problem sets were very different - not going to lie, but they were very difficult as compared to the rest of the problem sets.

**Problem Set 1** was not that hard - they gave us some starter code which was helpful. But it felt like the great calm before the storm - we had to implement small snippets of code and there wasn't much work to do but it did give us an idea of how things worked with Flask.

**Problem Set 2** was the final boss and no, I am not exaggerating. It was so long and we had to implement so many paths. I had to spend time understanding what to do in each path each day and then work on implementing it... 

Let me walk you through it.

---

### Problem set 1

I talked about it earlier.

There wasn't much to do in it, we simply had to implement 1 route in it and write the flask and html code related to it.

Our goal was to make a form that allowed user to enter his birthday details and we just had to loop the content the user provided and display it. **That's it.**

----
### Problem set 2

This is where things got super interesting.

We had a total of `6` paths and we had to write the related flask and html code related to it. There was a lot of similar things we had to do each time but nevertheless everything was different at the same time.

**A paradox - it was.**

**Here was my approach throughout the problem set:**

1. For each path - I had to understand what to do in depth.
2. Then I wrote pseudo code for it.
3. Then for each part that I needed to implement, I had to break it down further in my mind and work on implementing it.

We were given a lot of pre-written code but while it did help us it was nothing but a bit of support for us - To be honest, that code was a blessing - students were able to focus on solving the real problem because of it.

We were also given a database which had some tables in it already.
But we did have to implement tons of important tables and details in that database as well.

So, it was like - they were testing us with everything they had taught us so far:

- Python
- Html
- Javascript
- CSS
- Flask

And of course - our ability to solve the problems.

Our goal was to implement a working website that allowed users to lookup details of the stock, buy them, sell them, look at their portfolio, look at the history of transactions... and so much more.

And this is just the details from a very high point of view.
We also had to make sure everything was secure.

Whether it was making sure the passwords were hashed properly before being stored in the database, the strength of the password or the server side validation for each thing the user did.

Server side validation was a very important thing - that I learnt this week.
It's important because hackers can manipulate client side code in real time and do bad things but that's where server side validation steps in.

And of course - **knowing the theory behind this and knowing how to implement all this are 2 very different things.**

I also got an understanding about how every website works underneath the hood - because the things that we had to implement this week are very general things - Every website out there follows this pattern.

Also - another key realization I had was - how to use AI the correct way.

There was a point in my life, when I wasn't even able to read the code nor understand it and I wasn't even able to write the code - which made me feel very dumb and I used to use AI to write the code for me and then I would spend time understanding it with it's help.

That felt productive but it's wrong.
And although it's wrong it still taught me many things.

It gave me the ability to understand code as well as build logic for the code.

Now - although my approach was wrong - I am still glad that I used AI in some good ways which led me to where I am right now... and just so you know I still struggle with writing the actual code.

And tons of new programmers have this problem, it's not unique - but I believe there are stages to becoming a programmer - the following stages:

- Being able to understand the code
- Being able to build the logic for the code
- Converting the logic to code.

The 3rd step is where I struggle. To solve this, I used to utilize AI but then I talked with my friend from discord about this and that's when I realized that I am basically fucking myself by doing this.

I realized this and the very next day, I started changing this. 

I simple took the problem that I was facing and broke it into multiple sub-steps and started to tackle it 1 by 1  and that's how I started writing my own code.

Now - there are a lot of discussions going on about this very topic - About whether any beginner should even use AI in the first place when learning anything and after making a lot of mistakes - Here is my take on this:

- Completely not using AI is stupid
- Use AI but be very careful about how you use it
- Use it so you can understand the problem itself
- But build the logic yourself and most importantly **write the code your fucking self

And you can apply this rule almost everywhere - 

There has been a rise of vibe coding, recently.
And know this - vibe coding or using AI to generate code for you - isn't a thing for beginners, especially when you are building your foundations - It's for seniors who already know what they are doing.

For example - I am a technical content writer and It's been a while since I have been writing.
I am pretty open about - that I do utilize AI in my writing but you know what the interesting thing is? **I never used it when I was learning how to be good at my craft.**

You need a level of expertise in your domain to be able to use AI.
Because - you always have to be the one to guide AI to do the work for you and in result you are going to get different outputs, it's going to be your job to identify the good from the bad and you don't get that ability without knowing your shit.

I can talk about this all day.
But if I had to summarize this topic, then here's what I would say:

**Be vary of when you are using AI, if you are in the early stages of mastering your craft - don't let AI do the manual work for.**

**Back to the main topic:**

Solving the problem set itself didn't require a new approach, it was the same. 

- Break down problems.
- Take proper notes.
- Try understanding the problem, first.
- Build the logic and then code.

But you hear that everywhere, right?
That's why I wanted to give you a very useful insight to my journey of solving this problem, I feel like I learned a lot because of this problem set.

Yes - I got to know the in and outs of a website.

Yes - I got comfortable writing code in these specific frameworks and languages.

**But more importantly - I learned so much more about problem solving and the utilization of AI.**


## That’s a Wrap (For Now)

Now, I am done with CS50 - The only thing left is the final year project and of course I will be working on it but I haven't decided on what to work on yet...

Sometimes, I think of some low level program in C.

Other times, I want to make a web-based application.

I do have a lot of resources pinned down, I will have to research on what to make.
I want to make something that will push me to use everything that I have learnt so far while making sure I end up learning new things as well.

I will keep you updated on that.

And also - The next time you read my blog - it might just be on my new website that I am planning to build using Wordpress - Because I need some hands on practice with a popular CMS like Wordpress for some important reasons.

Anyway, If any of you is on the same journey - Whether it's CS50 or just trying to get skilled at some craft, I wish you good luck, if any of you want to reach out to me - you can just message me on my Linkedin or Discord.

And while this course can be completed in a short amount of period - It took me a lot of extra time because this was kind of my first computer science course and before this I didn't have any habit of consistency or stuff like that.

So - that's another thing, this course has taught me - **being consistent.**

Alright - fuck off now.
No thanks for reading.
