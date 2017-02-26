---
title: The Technology of this Blog
subtitle: The Tools Behind the Useless Content
description: A quick look at the tools I use to put this site together
date: 2017-02-26 11:57:58
tags:
- hexo
- markdown
---

This post aims to shed some light on how a blog is put together.  If you're already an experienced software developer, this will probably be very easy for you to find out for yourself (in fact you'll find many hundreds of alternatives too), but for everyone, here's a quick run-down of the technologies involved.

Starting from the beginning, the process looks something like this:

* I write the article in Markdown format
* I use a tool called Hexo to turn this into an HTML blog
* Then I deploy these pages to my personal GitHub account
* Finally, I use DNS to set up my own personal domain to point at the GitHub pages

# Writing the Content

This blog, like many content websites out there, is primarily text - with some markup (meaning headings, bullet points, links etc.) to make it look more interesting and feel more interactive.  There are many ways to write content, from crafting the HTML yourself^[Right-click anywhere on this page and choose 'view page source' to see what that would look like - not pretty!] to using a much simpler text format which is then generated into a web-friendly format.

I prefer to write my content using [Markdown](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet), which takes away a great deal of the hassle, and allows me to focus on the text.  If you're interested, you can see this blog post in its original Markdown form [here](https://raw.githubusercontent.com/CJTozer/CJTozer.github.io/blog/source/_posts/The-Technology-of-this-Blog.md).

I strongly recommend getting to know Markdown - I use it wherever I can.  Above and beyond ease of use, there are two other reasons I love it:

* Almost all modern text editors give you syntax highlighting support for Markdown.  At the moment I'm using the [Atom](https://atom.io/) editor, mainly because I'm also tweaking various JavaScript and CSS etc. files for the blog too.  I've also really enjoyed using [MarkdownPad](http://markdownpad.com/) when dealing with pure Markdown.
* Markdown is extremely well-suited to maintaining your content under version control^[A later post will cover version control] - because it's just text, you can really easily track changes over time.  I have a habit of committing my work frequently, as I'm a little paranoid in that way!

# Blog Generation

Once I've got the content in Markdown format, I do need it to be converted into an HTML website, and this is where you'll find no end of options.  For no reason in particular, I decided to have a go with the [Hexo](https://hexo.io/) tool, which can manage a blog for you - converting your content into a website.

This tool makes it pretty simple to manage the process.  For example, to get this post written, I used these commands:

* `hexo new draft "The Technology of this Blog"` - this creates the `The-Technology-of-this-Blog.md` file where I should put my content for this post.
* `hexo server --draft` - this lets me see my blog as it would look if I published this draft (so I can check how it looks without publishing yet).
* `hexo publish "The Technology of this Blog"` - when complete, this then moves the post from the drafts to the set of published posts.
* `hexo deploy -g` - this is used (in conjunction with a little config) to generate my blog website, and publish it to my personal [GitHub pages](https://pages.github.com/).

A couple of notes about Hexo:

* One of the reasons I chose it was that it seemed to have some pretty good themes available - see the [gallery](https://hexo.io/themes/).  I use my own fixed/modified version of the Anisina theme.
  * The great thing about using a pre-packaged theme is that someone else has already done a lot of the hard work to make sure your blog will be well laid-out and readable on all manner of devices - from widescreen monitors to smartphones.
* Hexo (as is the case for most blogging tools) generates _static_ webpages - this means that the content is generated up-front and can be handled easily.  If you need features like back-end authentication, or database access etc. (or if you want different pages to be available based on some external conditions), then this won't give you all that.  But for a blog, it's usually what you want - write some content, then publish it, end of story.

# Personal Domain

So at this point, I've got a blog published, and it's available on my [personal GitHub page](https://CJTozer.github.io).  All that remains to get to where we are now is to host the blog on a different domain (in this case [zerotdev.com](https://zerotdev.com)).

To do this, you first need to decide on, and then purchase the domain you want.  I used [Google domains](https://domains.google/) to both search for available domains, and to purchase (on an annual subscription) the domain I wanted.

## Linking it all Together

Finally, to link it all together, I needed to have requests for [zerotdev.com](https://zerotdev.com) be pointed at the [GitHub pages site](https://CJTozer.github.io), and also for the GitHub website to know that it was serving up the data on behalf of another domain.

This actually turned out to be slightly trickier than I'd hoped - and in the middle of it all I had some fun redirect loops where the two domains were infinitely redirecting the requests to each other!

As part of this, I decided to use [Cloudflare](https://www.cloudflare.com/) for my DNS ^[Domain Name Services - the part responsible for telling your browser where to look for e.g. [zerotdev.com](https://zerotdev.com)], as it also adds some extra security to help prevent my site being exploited.  If you're interested in the full process for setting this up, I won't repeat here, but I will point you at [the blog post that really helped me out](https://sheharyar.me/blog/free-ssl-for-github-pages-with-custom-domains/).

# Final Thoughts

* There are some great tools out there for making the process as easy as possible
* Do you have a blog/website?  What tools do you use?  What do you think of them?
