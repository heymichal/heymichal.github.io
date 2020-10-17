---
layout: post
title: Publish your Obsidian Vault to your Digital Garden
date: 2020-10-10 20:00:00 +0000
image: /uploads/pexels-david-cassolato-818563.jpg
tags:
- Obsidian
- Second Brain
- Digital Garden
- Personal Knowledge Management

---
The brain is for having ideas, we need something else to store them. We need a [Second Brain](https://fortelabs.co/blog/basboverview/).

![](/uploads/pexels-david-cassolato-818563.jpg)  
_Photo by_ [**_David Cassolato_**](https://www.pexels.com/@davidcassolato?utm_content=attributionCopyText&utm_medium=referral&utm_source=pexels) _from_ [**_Pexels_**](https://www.pexels.com/photo/person-holding-string-lights-photo-818563/?utm_content=attributionCopyText&utm_medium=referral&utm_source=pexels)

I'm inspired by [building a second brain](https://www.buildingasecondbrain.com/). A place where you can offload your ideas into notes for future use. This relates to the concept of a [Digital Garden](https://maggieappleton.com/garden/). A digital garden is a public place on the internet where you publish these notes for others to see and enjoy.

I use [Obsidian](https://obsidian.md/) to manage my second brain. Obsidian recently launched their [Publish](https://publish.obsidian.md/help/Plugins/Publish) plugin. This publishes your notes to the internet. The result is a [visual representation of your second brain](https://publish.obsidian.md/lyt-kit/_START%20HERE).

But I missed something. I have [my own place on the internet](https://yordi.me/) and would like to have my second brain, my digital garden, in the same place. While Obsidian Publish is cool, it is different from my website's style. What I'm looking for is a garden of my notes that I can integrate with my existing website. I've looked around quite a bit to find the tools that can help me achieve this wish, and I found them. Meet the combination of [Obsidian](https://obsidian.md/), [Jekyll](https://jekyllrb.com/) and the [Obsidian to HTML converter](https://github.com/kmaasrud/obsidian-html): [my digital garden](https://yordi.me/garden/).

# A look at the internals

Jekyll is one of the tools available to create your website based on plain text- and markdown files. A couple of alternatives are [Gatsby](https://www.gatsbyjs.com/), [Hugo](https://gohugo.io/) and [Hexo](https://hexo.io/) To use a setup that is like to mine, any static site generator will do.

The real magic is in the [Obsidian to HTML converter](https://github.com/kmaasrud/obsidian-html). This is a Python script that takes (part of) an Obsidian Vault with notes and converts it into HTML files.

## Download and installation

You can install the converter using `pip`:

```bash
sudo pip install git+https://github.com/kmaasrud/obsidian-html.git
```

or you can clone the repository to your local computer and install it:

```bash
git clone https://github.com/kmaasrud/obsidian-html.git
cd obsidian-html
pip install .
```

I chose the latter option since I made a small edit of the script to let it fit my needs (more on that later).

## Run the converter

Once installed, run the converter using the command `obsidian-html`, combined with some arguments. I use the following one-liner to convert my Obsidian Vault into my website:

```bash
obsidian-html <path to my Obsidian Vault> -t template.hml -d "writings" "notes" -o <path to my website>/garden
```

The first part of the command points to the location of the Obsidian Vault on my computer. The argument  `-t` defines a template and puts the resulting HTML files into your own format. My template looks as follows:

    ---
    title: {title}
    layout: page
    comments: false
    ---
    
    {content}

The top part (between dashes) is [Jekyll Front Matter](https://jekyllrb.com/docs/front-matter/): meta-data that describes a page. The template uses `{title}` and `{content}` to put the note's title and content in the HTML file.

By default, the converter only converts the files that are in the root of the directory you give as input. To include nested directories, you can specify them using the argument `-d`. In my case, I also want to include the directories `writings` and `notes` in the converting process. Finally, the argument `-o` specifies the output path where the HTML files will end up. I let it point to the `/garden` directory of my website, which is all I need to include the HTML files when I publish my site.

## A small converter update

Obsidian uses double square brackets (`[[like so]]`) to link from one page to another. By default, the converter creates relative links for this. For example, the link `[[Luke Skywalker]]` will end up as `<a href="luke-skywalker">Luke Skywalker</a>`. This messes up my website since I host all my notes under the directory `/garden`.

To solve this challenge, I made a small update to the converter tool. The file `utils.py` ([find it here](https://github.com/kmaasrud/obsidian-html/blob/master/obsidian_html/utils.py)) performs the link generation, in the function `md_link()` . I updated this function to always include my `/garden` directory as a prefix:

```python
def md_link(text, link):
  return "\[" + text + "\](/garden/" + link + ")"
```

![](/uploads/pexels-sevenstorm-juhaszimrus-704767.jpg)  
_Photo by_ [**_SevenStorm JUHASZIMRUS_**](https://www.pexels.com/@sevenstormphotography?utm_content=attributionCopyText&utm_medium=referral&utm_source=pexels) _from_ [**_Pexels_**](https://www.pexels.com/photo/123-let-s-go-imaginary-text-704767/?utm_content=attributionCopyText&utm_medium=referral&utm_source=pexels)

And that's that! A nice and fairly simple way to publish my Obsidian Vault to my website.