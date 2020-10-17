---
layout: post
title: Group Jekyll Posts into Collections
date: 2020-10-17 15:09 +0200
image: /uploads/jj-ying-8bghKxNU1j0-unsplash.jpg
tags:
  - Jekyll
---

Jekyll offers tools to publish blog posts to your website but misses an important thing: separate posts into categories. You can add tags to your posts, but in the end, they will still end up in a single long list.

I write the majority of my blog posts in English but wanted to start a new series written in Dutch. After a quick search on the Internet, I found a way to separate this new series and my default post library. The nice thing is that the solution is already implemented: [Jekyll Collections](https://jekyllrb.com/docs/collections/)! Collections allow you to group related content. Think about people on a team page, your talks at a conference or - in my case - a series of posts in a different language.

The end result is [a new page on my website](https://yordi.me/ask/) that holds all articles related to my series. Here's how I did it:

# A new collection

The first step is to create a new collection in your Jekyll site. You can do this by adding a new collection to the root of your `_config.yml`. My new collection's name is "ask".

```yaml
collections:
  ask:
    output: true
```

I've added `output: true` as option for my new collection, to ensure posts in this collection render on my website. 

The next step is to create a new directory that holds all content for this series. This works the same as for the built-in Posts.

In the root of your website, create a new directory with the same name as your collection and prefix it with an underscore. In my case, the name of this directory is `_ask`.

# The collection's layout

Now that the basics are in place, you need a new page to show the content of your new collection. You can design the new page from scratch, or use a similar layout as your normal page for Posts. I've done the latter and copy-and-pasted my Posts archive into the new page. Check out the [Jekyll Docs](https://jekyllrb.com/docs/) for all information on how to build pages, layouts and posts.

# Set the permalink (optional)

You can do one more thing for the content in your new series: set the permalink. The permalink is the generated URL for each piece of content in your new series. By default, Jekyll adds the name of the directory as prefix to a piece of content. In my case, posts are accessible via `/ask/<post title>`. Because I will transfer posts to my new series and want to keep the same link, I need to overwrite the permalink. The Jekyll website has good [documentation on how to create your own permalinks](https://jekyllrb.com/docs/permalinks/#collections). You can add the permalink option to the collection settings in your `_config.yml`:

```yaml
collections:
  ask:
    output: true
    permalink: /:title
```

This syntax for permalinks makes each piece of content accessible from the root of my website. That results in links like `https://<your website>/<new series content>`.

![](/uploads/jj-ying-8bghKxNU1j0-unsplash.jpg)
*Photo by [JJ Ying](https://unsplash.com/@jjying?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText) on [Unsplash](https://unsplash.com/s/photos/network?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText)*

And that's it! A simple and effective way to separate a series of posts from your default Posts archive. I hope it helps you too!