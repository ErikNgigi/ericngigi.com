---
title:       "How to Create a Hugo-Based Blog Hosted on GitHub Pages and Netlify: A Technical Guide"
summary:    "A Step-by-Step Tutorial for Setting up a Blog with Hugo, GitHub, and Netlify."
date:        2023-04-26 09:00:00
author:      "Eric Ngigi"
image:       "images/post/hugo/header-banner-image-02.jpg"
tags:        ["Hugo", "Github Pages", "Netlify"]
---

# How to Create a Hugo-Based Blog Hosted on GitHub Pages and Netlify: A Technical Guide

This post marks the beginning of a series where I will be sharing my experience and expertise on how to initiate a blogging journey from a technical perspective. The primary objective of this tutorial is to provide step-by-step guidance on how to create a blog from scratch, using Hugo, GitHub, and Netlify.

If you have decided to start blogging, but you are unsure of where to begin, it all depends on your technical abilities. If you are not technically inclined, it may be more feasible to opt for blogging platforms such as WordPress.com or Wix.com. On the other hand, if you possess software development skills or expertise in a related field, creating a blog using Hugo, GitHub, and Netlify is the ideal way to go. Why should you use the Hugo-GitHub-Netlify combination?

To begin with, creating content using Markdown, a lightweight markup language, offers a simple formatting syntax and cross-platform portability. Furthermore, you can embed pure HTML in your Markdown content.

Secondly, Hugo, an open-source static site generator, provides excellent performance, various out-of-the-box features, quick built-in server reloads, and a plethora of themes to choose from to construct all your website content.

Lastly, deploying and hosting your website using Netlify is uncomplicated and effortless. Netlify offers a free tier plan that is sufficient for any static website built with GitHub and Hugo. Netlifys Continuous Deployment feature, in conjunction with GitHub, significantly automates the content publishing workflow.

Now lets get started. The tutorial outlined below contains the following steps:

+ Install Hugo
+ Create New Site
+ Customize Example Site
+ Create About Page
+ Push Git Repository to GitHub
+ Deploy on Netlify

Basic knowledge of Git with its command-line interface and GitHub/Netlify accounts are the prerequisites for this tutorial. As a host operating system, I will be using Archlinux.

## Install Hugo

According to the official Hugo documentation, it is not recommended to install Hugo using the pacman manager using the code below to the latest version of Hugo. 

```
pacman -S hugo
```
![installing-hugo](/images/post/hugo/installing-hugo.png)

## Creating a new site

To create a new site, execute the hugo new site command in the site’s root directory, for example:

```
hugo new site 'examplesite'
```

I'm using erikngigi.github.io as a site name because I currently own the domain name and intend to utilize it as a custom domain for my website. The freshly generated site has the proper framework, but no content or theme.

![hugo-new-site](/images/post/hugo/creating-hugo-new-site.png)

You must first select a Hugo theme before continue. [Hugo](https://themes.gohugo.io/) has a profusion of themes to meet a variety of interests and needs. I choose the Clean White Hugo theme because it is blog-friendly, responsive, and multilingual. It also supports Disqus comments, Algolia search, and Google Analytics.

Move to the site’s root directory and initialize a Git repository:

```
cd erikngigi.github.io
git init
```

Then move to themes directory and add the theme in question as a Git submodule:

```
cd themes
git submodule add https://github.com/
```

The git submodule add allows cloning of the theme repository to your project and keeping it as a subdirectory of the site repository. Also, it permits Netlify to recursively clone the site repository along with the theme repository when building and deploying the site.

Copy the content of the themes/clean-white-theme/exampleSite/ folder to the site’s root directory, remove the default archetype and move back to the site’s root directory:
