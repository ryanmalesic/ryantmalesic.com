---
title: "Hugo"
date: 2020-08-26T23:11:27-04:00
slug: "hugo"
description: "A brief guide to hugo"
keywords: ["gohugo", "hugo", "go", "blog"]
draft: true
tags: ["hugo", "guide"]
math: false
toc: true
---

<sub>Use the table of contents on the side of the page to skip to the guide if you
don't want to read all of the fluff that comes before.<sub>

## A nagging question

Recently, I found myself wondering how I could share my thought, ideas,
and projects with the world.

I learn best from example. Without the hundreds, or even thousands, of articles
that I've read over the years, I wouldn't know a quarter of the things I do now.
Why not contribute what I have picked up so that more people can learn?

So I started thinking about the best way to accomplish this goal.

## Where to begin?

First I thought about existing soccial media and blog spaces.

I frequent [reddit](https://reddit.com) and various computer-related subs, but
these platforms are great for sharing content, not so much for posting
**original** content.

You see so many people now-a-days, especially in the field of software
devlopment, writing [Medium](https://medium.com) articles. Nothing against
Medium, but just isn't for me, so i kept searching.

After exhausting the options of pre-existing content platforms, I turned to more
original thought.

I've been exposed to a decent amount of web development over the years from
university, personal projects, and internships, so eventually the thought
arrived: _"Why not make my own?"_

My experience with web development is well-rounded. I can create full-stack
applications from start to finish with any frameworks given the time to learn.
However, why reinvent the wheel?

There are millions of people out there who have done the TODO or Blog
cookie-cutter application. Even the _tutorial_ for [NextJS](https://nextjs.org)
(my favorite React framework) is creating a blog. At this point, it's simply
not impressive unless you have something new to introduce, which I don't.

Thats when I started to look at companies like
[WordPress](https://wordpress.com). Wordpress looked like a good platform, but
I wanted more control over the blog.

Then, I stumbled upon Hugo.

## Hugo

[Hugo](https://gohugo.io) is an open-source static site generator written
in [GoLang](https://golang.org).

It seemed to me like a solid choice for two big reasons:

1. All pages are rendered from markdown source
2. Themes are very customizable and there is a library of shared themes
   (who doesn't love that?)

In fact, I liked what I saw so much that this blog you are currently reading is
thanks to Hugo!

## The Guide

**Finally**. The guide.

Let's dive in and see how you can make a simple blog of your own using hugo.

### Pre-requisites

- Knowledge of basic command line usage
- Git installed on your development machine

### Installation

Installing Hugo isn't too hard, especially if you know how to use a package
manager of your choice. Hugo has a detailed page about installation
[here](https://gohugo.io/getting-started/quick-start/).

Since I develop on a Macbook, the following is the installation process for
MacOS.

```bash
brew install hugo
```

That's it.

Verify the installation with `hugo version`.

### Generate a site

Hugo comes with command line tools to help generate a new site

Open a terminal in the directory you want to create your new site folder in and
execute `hugo new site <site_name>` (replacing <site_name> with the name of
the site).

Boom! A new folder with the foundation of a site is now in your current working
directory.

### Themes

Time to pick a theme.

Head over to [here](https://themes.gohugo.io) and browse around until you find
one you like.

This blog at the time of writing this article is useing the
[Codex](https://github.com/jakewies/hugo-theme-codex) theme. Installation
instructions can typicallly be found in the README of the Github repo for the
theme.

Each theme also has different configuration settings that you can customize in the
`config.toml` file. Make sure to read the documentation for the theme you decide
to use.

### Posts

For Codex, after customization, blog posts can be made by executing
`hugo new blog/<title>.md` in the root of your project's directory, where
`<title>` is the name of your file / post. This command generates the
markdown file for the new post in the `content` directory of the project.

From here, you can create the contentof the post using markdown syntax.

### Development

While making your post, it may be helpful to view the rendered content of the
markdown.

In the root directory of your project, execute `hugo server -D` in a terminal.

The `hugo server` portion will start the server that will re-build the pages on
source file changes. The `-D` will also build any posts that are marked as drafts.

### Building

After you are satisfied with the content of the post, it is time to build the static
files for production.

Execute `hugo` in ther terminal in the root directory of your project. This command
will compile and build the static html, css, and js files and output them in
a directory named `public`.

### Hosting

Hosting the site is beyond the scope of this post. There are many
options that you can choose from to host your newly created site. Pick whichever
one is best suited for your indivdual needs.

## Final Notes

Hopefully you found this article helpful! There is a lot to hugo that wasn't
covered. Definately checkout the documentation for hugo and dive in to all of the
features that are available.
