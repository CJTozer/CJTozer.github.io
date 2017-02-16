---
title: Code Comprehension
tags:
  - pro tips
date: 2017-02-16 23:13:49
subtitle:
description:
---


Reading code is such a fundamental part of being a developer, but often we take it completely for granted.  The ability to take unfamiliar source code, and turn it into a mental picture of what's going on is an absolutely fundamental skill for any serious software developer.  It's always getting exercise:

* Learning a new area of code (a new component or brand-new project)
* It's essential for being able to do good code review
* Without it, efficient debugging is impossible
* Even writing designs, you'll often have to resort to reading code to working out the details the API docs don't tell you

So, given that, what should you do if you find this is a hard skill to master?  What if you've not been able to just pick up the ability by osmosis?

# Deliberate Practice

I propose one possible route to improvement: [Deliberate Practice](https://en.wikipedia.org/wiki/Practice_(learning_method)#Deliberate_practice).  Deliberate practice is more commonly associated with skills like playing a musical instrument, but I've found success when using it to train people in very specific areas of software development.

By practicing on a very frequent basis, discussing progress, and getting input from a mentor, it's possible to take real strides.  The method I have used is:

* Find 15 minutes _every_ day to practice.  Ideally practice is done with a mentor/expert to provide input and advice.
* Randomly choose a recently-changed file from the codebase (this way it's more likely that the code will have potential relevance).
    * Using Git to give a selection of 3 possibilities: `git diff --stat --name-only @{2.weeks.ago} | shuf | head -3`.
* Pick a sensible amount of code to focus on.
    * Depending on the level of the training, and the complexity of the code, this could mean going into all the details for a single function, or skimming a whole file at a higher level (both are valuable skills, so both should be practiced).
* Talk through the code as you think through it.
    * Don't sit there to try and work it out first - make it a conversation.
* Make sure you're thinking about the pointers below - and are getting education if the high-level picture isn't there.

## Pointers

To give you some idea what I think you want to be aiming for here, when you're really good at code comprehension, you should - when looking at a new area of code - be able to:

* Build up a high-level picture of the context for the code
* Be explicit about any assumptions you're making about the code (and you will likely want to follow up on these later!)
* Avoid getting stuck in a quagmire of detail - instead filtering so that you only dig into areas that are likely to be relevant to you

# Punch Line

I believe practice can help.  What do you think?  What other skills do you think this kind of technique might help with?
