---
marp: true
theme: presentation-theme
backgroundColor: #fff
html: true
---

# The Web Dev's Guide to Automated Testing

---

# About Me
<!--
Fam: Married 16 years, 4 kids, 15, 14, 12, 10
Community is important.  JS Meet-up has been wonderful, community of people at church.  
    - The title of this talk as actually inspired by something my Pastor said during a sermon.  Please don't tell him I day dream during his sermons.
Hobbies: Archery, Blood Bowl.
 -->
 
Personal Stuff:
- Meet the Fam!
- Community & Church
- Hobbies

![bg right](IMG_3296.JPG)

---

# About Me: Professional Stuff

<!--
Education: I fully recognize that most of you care where I graduated from 20 years ago.  But I'm a proud Iowan! segways to experience
Experience: I've been a full stack developer for 20 years
Current Role: with Freewheel for almost 14 years. 

Today I'm here to talk about testing.  Why talk about testing?
-->

- **Education:** 2004 Iowa State University Grad. w/ B.A. Info. Systems 
- **Experience:** Nearly 20 Years as “Full-Stack” Developer
- **Current Role:** Lead Software Engineer @ FreeWheel

---
<!--
I often feel like the direction set for automated testing feels like this.

Tell brief narative about this

This is an over characterization, and maybe its not fair.  But it seems to be what happens.

It leads us to a place where we experience...
-->

![h:575 center](code-cov-meme-1.png)

---

<!--
Where we "game-ify" or work the system me meet a measurable Goal.  

Charles Goodhart was a british economist credited with this adage as it relates to monetary policy.  We may not be talking about money, but the sentimet applies to many areas of life and I think often times to automated testing as well.

You see, when the metric becomes the expressed goal, it can lead to... undesireable results.

As an example a, focus on test coverage can lead to some thing like this
-->

# Goodhart's Law
> When a measure becomes a target, it ceases to be a good measure

---

<!--
Have a careful look at this.  Who knows what this does?

Yes, that's exactly right!  It tells the tooling... hey don't check for coverage in these places.  It excludes all of the key modules from our fictional business application!  

Now.  Does this really help us?

Before anyone asks.... yes I have seen this happen in real life.  I have simplified the code block for clairity, and I did rename the packages to protect the identity of violators!

-->

```js
/* jest.config.js */
{
    collectCoverageFrom: [
        'packages/**/*.{js,jsx,ts,tsx}',
        '!**/packages/auth-module/**,'
        '!**/packages/billing-module/**',
        '!**/packages/core-business-logic/**',
        '!**/packages/data-repository/**',
        '!**/packages/insert-all-directories-here/**'
    ]
}
```

---
<!--
So my hope today, stop chasing vanity metrics.  
we can move away from this as a definition.  With a mentatility similar to, "It works on my machine!"

So we can get away from chasing vanity metrics. Move to a place where we take a purposeful and principled approach to automated testing.  

And as a first step I want to clear state what I think the intended purpose of testing is.

-->

![h:100% center](unit-test-def.jpg)

---

<!--
It may seem obvious but the reason we writes tests is to ensure we have a high level of confidence that our software is working.  

In the beginning our software may be very simple, and it may not need tests.  Some software never needs tests.
    - A hobby project
    - A very simple CLI tool that just one thing
    - A small web form that isn't business critical

But as our software becomes becomes more complicated, more valuable, more critical.
Testing becomes more important.  
    - medical software that deals with life and well being
    - handling of peoples money and their livelihoods
    - Delivering critical communications (mail, email, phones, etc)

Most often in our day jobs we are building complicated, critical software.  So, when we talk to our teams about testing related topics, this is the filter through which we should be having those conversations. 

In hopes of meeting this purpose I've got 4 principles to share with you today

-->

# Purpose of Testing

_To have a high level of confidence that our software is working as expected._

---

<!--
The principles are as follows. 

We'll break these down as we move forward and include some common helpful practices

-->
# Principles for Creating an Effective Test Suite

1. Write tests that resemble how your software is used
2. Well written tests are essential documentation
3. Value Test Case Coverage over Code Coverage
4. Optimize for fastest possible developer feedback loop.

---

# Principle 1:
## Write tests that resemble how your software is used

---

# Principle 2:
## Well written tests are essential documentation

---

# 5 Questions Every Test Should Answer

  1. What were you testing?
  2. What should it do?
  3. What was the output (actual behavior)?
  4. What was the expected output (expected behavior)?
  5. How can the test be reproduced?

---

# Principle 2:
## Naming Conventions


---

# Principle 2:
## Arrange Act Assert pattern

---

# Principle 3: 
## Value Test Case Coverage over Code Coverage



---

# Principle 4
## Optimize for fastest possible developer feedback loop
- Automation!  
- Processing on CI
- Fast runs locally
- Necessary refactoring/changes to keep them as fast as possible
- Sword fighting example.

---

<!--
Remember this old xkcd comic about compiling?  

Yea it applied to testing too!
-->
![h:575 center](xkcd-compiling.png)

---

<!--  
- Each of these in very important
- Help us ensure quality
- Should be automated
  - Locally
  - CI jobs
  
later we'll get into some specific practices and patterns to help with Unit and Integration testing.

-->
# Types of Testing
_Testing Trophy, courtesy Kent C. Dodds_

![bg right h:600](testing-trophy.webp)

---



---
