---
title: Evolving my testing workflow
tags: [C, Testing]
style: fill
color: warning
description: In this short blog post I describe a new improvement in my testing workflow, displaying a simple flow diagram and a reference to source code in C.
---

During my development time at DTT in Amsterdam I came into contact with testing en TDD (Test Driven Development). I got to understand unit testing and its importance during development. I learned about testing frameworks and testing in the Unity Game Engine.

While getting to know testing in general, you start to look differently at writing code. You start to write your functions with testing in mind which (in my opinion) increases their quality. I also started to develop a testing workflow for myself. 

It has been at least one year now that I have applied testing practises to my code. In this blog post I will lay out the steps that form my current testing workflow. Starting from "Beginning an implementation" to "Completing an implementation".

An example where this workflow is used is in a "strings between" function which I wrote, being inspired by its example usage in the [Effective Software Testing book](https://g.co/kgs/psoqAb) I am currently reading. You can find a link to the source code for it at end of this blog. 

### The workflow

![Testing Workflow](../assets/img/blog/testing-workflow/Testing%20Workflow.png)

**1. Writing the prototype**

I always start of by creating the prototype for my implementation. In the case of a single function this will be the prototype of this function. This gives my the first insights I need for my test cases: input and output. 

**2. Writing out test case(s)**

This step consists of writing out test cases based on my current knowledge. This is initialy based on knowledge gained from writing the prototype, but additional test cases can be added while writing the implementation. 

**3. Writing the implementation**

This step consists of writing out the implementation. Knowledge from writing out the test cases can be used to increase quality. At any point during this step, a switch to step two can be made after an insight of a different test case has been gained.

**4. Find edge case(s)**

An edge case can be found while writing the implemenation or while manually testing it. If this happens, we go back to step 2. 

**5. Write tests**

After going through all the steps (and maybe 2-4 multiple times) we have the implemenation and a set of test cases to test it. We can now write unit tests and possibly integration tests.

> During the writing of tests, additional test cases may be also be found. In this case, we'd go to step two again to write out the test case to update our implementation after.

### Summary

In my development work, I try to write code with testing in mind to increase quality. I add test cases in the form of comments while creating the prototype. When writing the implementation, I might find edge cases to translate to test cases. After I have completed the implementation based on my test cases I can start writing my actual test functions.

<p class="text-center">
{% include elements/button.html link="https://github.com/Bvanderwolf/libft/blob/main/ft_strsbtwn.c" text="Source" %}
</p>