---
title: Write your own tools
subtitle: ...and learn new skills doing it...
description: A look at how fixing your day-to-day problems can help you get started coding.
tags:
  - pro tips
  - learn to code
---

# Getting Started

Learning to write code can be daunting.  I know some people who claim they would love to be able to write code (and I certainly believe they're telling the truth), but have never quite found it possible to get started.

Normally I've found that this comes down to two things:

* Not knowing where to start
* Not having a _need_ that forces them into it

The second of these is simpler on the face of it - if there's no _need_ to learn, chances are the motivation is harder to get.

Not knowing where to start is probably getting harder not easier these days - there's no shortage of really excellent tutorials, guides and books out there.  But which one do you pick?  And what if you choose the wrong one?

# See a Need, Fill a Need

{% asset_img bigweld.jpg Bigweld %}

If you can think up a tool that you actually think you'd use, that's the perfect opportunity to force yourself to learn.  Depending on what you use your computer for, this tool might be:

* A script to rearrange documents, ensuring they are all consistently named
* A script to copy updated files around to back them up
* A tool to scrape the latest headline from a news site - or score for your favourite team, and display it
* A countdown clock

If you can't think of anything you'd actually use, then this is a harder problem.  You can try to pick an example similar to the above, or ask someone else for ideas for a tool that they might like.

## Clear Vision

The next step is to make sure you actually have a really clear idea of what you're going to build.  You wouldn't start learning to cook by saying "I'm going to learn how to make dinner" - you'd pick a specific dish, make sure you knew what you were aiming for, and as a result you'd have a much higher chance of success.

Some examples of things you should consider before you start (and writing down the answers might be a good plan):

* What are the ways the tool is going to be used?  Pick the most important one, and you'll focus solely on that for the moment.
* What are the inputs/information that your program will need?
* Where is the tool going to run?  Do you need it to be a website?  Or is a simple command-line a better option?^[This makes me think I ought to write a quick intro to the command line.  I'll do that and link it when complete!]

# What Language to Choose?

Once you've got the picture of what you're going to build, it's time to decide how.  This in fact can be one of the most daunting parts of the whole process.

The good news is that **there's no wrong answer**.  Remember that the aim is to learn.  If you try using C to write a website, or Prolog to write a text-based adventure game, the chances are you'll find the going quite rough - but that you'll learn an awful lot along the way.

That said, given this is your first project, there's some advice I'd give here - all of which you're welcome to ignore if it doesn't fit with your vision.

* Start with a simple command-line tool, not a complex UI.  There are various good frameworks for making web pages or native applications, but my advice while you're learning to code is to stay slightly lower-level than that, so you can clearly see the effects of each line of code you write.
* Pick a scripting language.  Depending on what skills you're actually trying to build, there are lots of options here, but I'm going to pick out three that tend to be quite easy to pick up.
    * In general, Python is a great choice - it's simple and versatile.  If there's no good reason to use the next two, Python is a great place to start.
    * If you know you want to be writing websites, then JavaScript is an essential tool, so you could get started with that.  There's a little more infrastructure to get started with JavaScript running from the command line (you'll need Node - [here's](https://developer.atlassian.com/blog/2015/11/scripting-with-node/) a good tutorial on the subject)

# Punch Line

* Pick a problem to solve or tool to build (ideally one you'd actually use)
* Build a clear view of what your tool will be - and keep it simple to begin with!
* Start with a simple scripting language
