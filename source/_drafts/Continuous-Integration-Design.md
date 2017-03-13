---
title: Continuous Integration Design
subtitle: How not to do it Wrong
description:
tags:
  - continuous integration
---

For my day job, we're currently building a high-performance system, pretty much from scratch.  One of the challenges facing us lately has been considering how to test this new system - and during the initial thinking we struck on something I thought I'd share.

*Some context here - the various products I've worked on over the years have ~~almost~~ exclusively been harder to test than they are to write.  Sometimes this is the nature of the beast, but often it comes down to bad design.  This blog post isn't trying to tell you the right way to do CI design - but it is a few things to think about that are often overlooked, and in my experience can contribute to the 'badness' of many test frameworks.*

# Use Cases

This is a common thing to do in many walks of software development, but one I've never seen applied to test or CI frameworks - and now it's been planted in my brain I can't stop thinking how important this is to ensuring success.

It's easy to assume that your CI pipeline is something like:

> Developer checks in a fix, build passes or fails

...but is that really all there is to the story?  When I started thinking about it, there were very many more potential users/use cases for our CI system.  To get you thinking, here's some ideas broken down into users...

## Developer

* makes functional bug fix, adds new test for it
* makes performance improvement, measures improvement
* adds feature, adds performance test for it and checks other performance tests for regressions

## Maintainer

* checks performance improvement/degradation over time - can pinpoint bad commits
* checks quality of product before releasing

## Tester

* has confidence in product being delivered for testing
* knows what's already been tested, so doesn't need to cover the same ground
* adds test for new functional/performance area that devs didn't think of

## Product Manager (/Sales?)

* presents detailed performance data to customer prospect
* spins up a demo of the system performing superbly under high load

---

So, that's just the things off the top of my head.  From thinking like this, it was immediately clear to me how the previous frameworks I'd worked with just didn't fit the bill.  I'm really hoping we're able to make all of these use cases a success!

# Final Thoughts

I've found thinking about use cases really helpful.  Have you tried it?  What interesting use cases have I missed?
