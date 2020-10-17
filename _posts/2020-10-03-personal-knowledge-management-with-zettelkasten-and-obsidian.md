---
title: Personal Knowledge Management with Zettelkasten and Obsidian
layout: post
date: 2020-10-03T10:00:00.000+02:00
image: /uploads/stanislav-kondratiev-6po3qfkk7hq-unsplash.jpg
tags:
- Personal Knowledge Management
- Second Brain
- Obsidian

---
![A physical second brain](/uploads/stanislav-kondratiev-6po3qfkk7hq-unsplash.jpg "A physical second brain")  
_Photo by_ [_Stanislav Kondratiev_](https://unsplash.com/@technobulka?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText) _on_ [_Unsplash_](https://unsplash.com/s/photos/books?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText)

Did you ever have a brilliant thought while walking through nature? Or while showering? Or while riding your bike to work? Chances are you did. And chances are you totally forgot you had the thought a day or even an hour later.

The mind gives you wonderful, creative insights in moments you least expect it. That's no surprise: your mind exists to _have_ ideas. At the same time, it is horrible at storing them. Tools like [Evernote](https://evernote.com/) or a more traditional, physical notebook can help, acting as our personal, external storage. The downside is that they lack capabilities to link individual ideas and notes together, creating knowledge silos instead.

Over the last few years, the notion of a [Second Brain](https://fortelabs.co/blog/basboverview/) has gained popularity. In addition to offloading ideas to individual notes, this concept introduces links between those notes, mimicking the structure of a real brain. This is where knowledge management- and note-taking methods like [Zettelkasten](https://zettelkasten.de/) are entering the picture. In short, a Zettelkasten (German for "slip box") is a collection of many individual notes with meta-data (like tags or links) that connect them together.

I took a dive into the wondrous world of Personal Knowledge Management (PKM) systems. I read about and experimented with various strategies to figure out which one works best for me (although that will be a continuous and never-ending process). What I do want my system to be is [Stupid Simple](https://en.wikipedia.org/wiki/KISS_principle). Starting from this principle, I ended up using a combination of Zettelkasten, [LYT](https://forum.obsidian.md/t/lyt-kit-live-on-obsidian-publish-downloadable-on-oct-13th/390) (notes organized with an index) and [Obsidian](https://obsidian.md/). Let me take you on a trip through my second brain.

## The method: Zettelkasten with LYT

My second brain is built on two pillars: Zettelkasten and Linking Your Thinking (LYT).

A Zettelkasten is a collection of notes linked together. You can think about it as a graph with nodes (holding the knowledge) and connections between them. This is similar to how your brain works: a large set of neurons linked together, forming a network or circuit. Notes can be put into one of two categories: literature notes or permanent notes. Literature notes are written as you consume content, such as books, articles or videos. They contain anything that sticks with you, written down in your own words. Think of these notes as your short-term memory. These literature notes can be summarized and organized in permanent notes that end up in your personal knowledge system (your long-term memory).

The LYT system was designed by [Nick Milo](https://twitter.com/nickmilo?lang=en) and is a framework to work with notes. It consists of one _Home_ note (the main index for all your notes, like the index of a book), multiple Maps of Content (collections of similarly themed notes) and other fluid frameworks (any additional way you organize your notes).

The LYT system is one of many ways you can use to organize a Zettelkasten system. Is it the best one? It depends. It is the best one for me at the moment, although future insights could move me to use something else instead. The only way to figure this out for yourself is to try it, review it and make your own decision.

## The software: Obsidian

The first question I had when thinking about the software I could use was: "do I need to use any software at all?" And of course, you could do without. You could choose to keep notecards in physical boxes and link them together using a relational system. Author [Ryan Holiday](https://ryanholiday.net/) does this, as he explained in his [article on the notecard system](https://ryanholiday.net/the-notecard-system-the-key-for-remembering-organizing-and-using-everything-you-read/). While this is a perfectly valid way of maintaining a second brain, it is too much hassle for me.

So, on to software. As far as software goes, it should check two boxes: it should be stupidly simple to use (without offering all kinds of features you're not using) and it should be future-proof (a layer over plain and simple data that can be imported into another system if needed).

I chose [Obsidian](https://obsidian.md/). It's a knowledge base on top of plain text Markdown files kept locally on your computer (which I also store in the cloud with [Dropbox](https://www.dropbox.com/h)). Its main features are linking files together and visualize them in a graph view. Of course, there are a lot of alternatives which I'm leaving out of scope here. To just name a few: [Notion](https://www.notion.so/Clips-783299e2c1c0450a81f3e2173fcda0c6), [Roam Research](https://roamresearch.com/), [RemNote](https://www.remnote.io/) and [Evernote](https://evernote.com/).

![](/uploads/josh-riemer-oh5brdggi2w-unsplash.jpg)  
_Photo by_ [_Josh Riemer_](https://unsplash.com/@joshriemer?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText) _on_ [_Unsplash_](https://unsplash.com/s/photos/brain?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText)

## Example workflow

Let's take a look at how I go about making notes on some content and how I put this into my second brain in Obsidian, using the article [Building a Second Brain: An Overview](https://fortelabs.co/blog/basboverview/) as an example.

The first thing I did was reading the article and write notes on it. This resulted in the following literature note:

    Type: #article 
    Author: [[Tiago Forte]]
    Links: https://fortelabs.co/blog/basboverview/
    
    # Building a Second Brain: An Overview
    We consume a lot, but we fail to use it. The brain is for *having* ideas, we need something else to store them. We need a [[Second Brain]], so that our actual brain can keep its focus on creativity.
    
    This extra brain should be linking things together instead of consisting of silos.
    
    Steps to build a second brain:
    1. **Remember**
    	1. Think about what you want to remember. Make curated choices. The outcome of this could be your main index.
    	2. The [[PARA]] system organizes information by "when" you would like to see it next, instead of organization by category.
    2. **Connect*
    	1. Reading about topic A could lead to insights in topic B. Without having that goal before reading.
    	2. Summarizing and organizing happen in small steps over time. Progressively summarize notes (summary of summary). Organize and add value to a note every time you touch it.
    3. **Create**
    	1. Use your second brain as basis for creation. For example, to write an article. Stand on the shoulders of giants.
    	2. Information only becomes knowlege when you use it.
    	3. It's never a good time to start, so just start. Work incrementally and improve.
    
    Anything you consume can be put to use anywhere, sometimes in unexpected places.

The top of the note contains meta-data. As _Type_ I use an [object tag](https://zettelkasten.de/posts/object-tags-vs-topic-tags/), showing the kind of content. The _Author_ is an internal link to another note in my system. The _Link_ is the URL to the article.

At this stage, the literature note is just a mostly isolated node in the system (possibly connected to some other notes). The next step is to transfer it into a permanent note, promoting it to the long-term memory of the second brain. In my case, I have a _Home_ (or _Index_) note that contains a couple of Maps of Contents (MOCs), "Productivity" being one of them. A MOC is a way to group similar notes together. The numbers I use as prefix are there for organization purpose only (based on the [Dewey Decimal System](https://en.wikipedia.org/wiki/Dewey_Decimal_Classification):

    # 000 Home
    
    ## Areas
    - [[010 Mind MOC]]
    - [[020 Body MOC]]
    - [[030 People MOC]]
    - [[040 Interests MOC]]
    - [[050 Quotes MOC]]
    - [[060 Writings MOC]]
    - [[070 Productivity MOC]]

Within the "Productivity" MOC, I have a list of permanent notes and I can add one or more new ones related to the notion of a "second brain". How you map a literature note into a permanent note is up to you. You could summarize the literature note and use that as one new permanent note, or you could create multiple permanent notes, like one for every step (_Remember_, _Connect_, _Create_). There is no ideal way; it depends on the literature note and what you think is the best in each specific scenario.

This process builds up an interesting knowledge graph over time, towards a second brain you can always rely on. It can provide a starting point for articles you write, or for noticing relations between books you read, and so on.

## Conclusion

Zettelkasten, in combination with Linking Your Thinking (LYT) and supported by Obsidian, is an interesting and promising way to organize your second brain. Especially when kept simple, it will probably be my go-to solution for the foreseeable future.

What are your takes on the second brain? What method and software do you use? Let me know in the comments.