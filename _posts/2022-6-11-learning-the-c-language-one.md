---
title: Learning the C language (Part 1)
tags: [C, Linux, Datastructures]
style: border
color: light
description: In this short blog post I describe my learning of the C programming language as a consequence of me starting a new study at the Amsterdam Codam Coding College. This from the perspective of a C# developer.
---

As a C# programmer you are not always aware of how much the language does for you. Starting with C has made me realize how much tedious tasks there actually are during development if not handled for you.

In this blog post I want to talk about concepts/tools that I think C# makes easier when compared to C.
- Null Termination
- Malloc vs the new keyword

Disclaimer:
> At this point I have been programming in C for about 2 to 3 months so some of the information I am giving might not be complete or misses some nuance. If this might be the case, please send me a message on [LinkedIn](https://www.linkedin.com/in/benjamin-van-der-wolf-742305160) or [email me](mailto:benjaminvanderwolf@gmail.com). I am always willing to learn more.

## Null Termination

One of the first things you will encounter when programming in C are Segmentation Fault Errors. One defintion for Segmentation Faults reads: 

*Core Dump/Segmentation fault is a specific kind of error caused by accessing memory that “does not belong to you.”* 

So, why do we not get this error in C#? In my opinion, this is because of the 'Length' property and Count for ICollection implementations. (Also, thank you  [IndexOutOfRangeException](https://learn.microsoft.com/en-us/dotnet/api/system.indexoutofrangeexception?view=net-6.0))

I got so used to being able to use Length and Count for all my iterations that I didn't even think about what problem they actually solve.

Every enumerable collection of memory needs some sort of way to indicate an end. Otherwise, memory not used for it can be accessed. When you use the **new** keyword in C# to create an Array, the Length is stored for you as a class member. C doesn't do this. This means, a different concept has to be used to provide safe iteration. Lets take a look at this code snippet:

{%- gist 20969364d1aea7b5ded3a112825a41ff %}

We create a new string of characters and use a "for" loop toghether with the "write" function to print each character to the standard output. Instead of checking our variable 'i' with a property 'length' we check if the current character is a '\0' character. The question is ofcourse: Why?

This string that we created might look like it has six characters in it but it actually has 7. When creating a string literal in C, it automatically appends a '\0' character to the end which, if we look at the [ascii table](https://man.archlinux.org/man/ascii.7.en) we will find that it refers to the number 0. This convention spreads to pointers as well where the address 0x0 is used as null terminator, which is hexadecimal for the number 0 as well.

Luckily for me I used only string literals at the start of programming in C and the only Errors I had where Bus errors (If you already worked with C you can probably understand why). This did change though when I learned about the "Malloc" function.

## Malloc vs the new keyword

During my working time as C# developer I only heard the terms "Heap" and "Stack" a few times. They where pretty far away concepts as their functionality's where never really explicitly explained in my C# work and so I assumed I didn't need to know about them.

In C, you start learning about the heap and malloc, the moment you need to start allocating memory dynamically. For me, this was when I needed to move away from string literals ("this is a string") and create functions that would create a new string based on some input parameters (e.g. substring).

Very early on I found out, after multiple Segmentation Faults, that the "malloc" function does **not** allocate the null terminating '\0' I was so used to from the string literals. I had to understand that every string (especially the ones used by libc functions) **need** to be null terminated. Otherwise iteration is not possible. The same I would later find out for any array or enumerable datastructe for that matter needed some type of null termination.

I assume null termination is not a thing in C#, but wrapping this kind of memory safety feature inside a "new" keyword (I now realize) makes things a lot easier on the brain. This as you can focus on writing your high level functionality instead of painstakingly writing the same memory code every time and maybe having it fail sometimes having written it after a long working day.

<p class="text-center">
{% include elements/button.html link="learning-the-c-language-two" text="Part 2" %}
</p>