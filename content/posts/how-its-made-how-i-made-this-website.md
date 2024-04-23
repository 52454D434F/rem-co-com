---
title: How It's Made - how I made this website
image: /images/uploads/hugologo.avif
date: 2024-04-23T13:11:00.000Z
categories:
  - Development
tags:
  - Netlify
  - Hugo
  - DecapCMS
layout: post
---
# How I made this website

This article describes how I made this website and the systems, applications, and configuration I used.

My monthly costs are $0, which is pretty chill, of course.

## The front end is HUGO, gohugo.io

[Hugo](https://gohugo.io/documentation/) is a static site generator written in Go. Steve Francia originally created Hugo as an open-source project in 2013. Since v0.14 in 2015, Hugo has continued development under the lead of Bjørn Erik Pedersen with other contributors.

## I'm using DecapCMS to manage my content and media for the back end.

[Decap CMS](https://decapcms.org/docs/intro/) (formerly Netlify CMS) is an open-source content management system for your Git workflow that enables you to provide editors with a friendly UI and intuitive workflows. You can use it with any static site generator to create faster, more flexible web projects. Content is stored in your Git repository alongside your code for easier versioning, multi-channel publishing, and the option to handle content updates directly in Git.

## To store my data, I use GitHub

[GitHub](https://docs.github.com/) is a developer platform that allows developers to create, store, manage and share their code. It uses Git software, providing the distributed version control of Git plus access control, bug tracking, software feature requests, task management, continuous integration, and wikis for every project.

## All is hosted on Netlify

[Netlify](https://docs.netlify.com/) is a remote-first cloud computing company that offers a development platform that includes build, deploy, and serverless backend services for web applications and dynamic websites.

---

# Let's start

I use VSCode, Homebrew, and a macOS terminal for all my command line codes.  

1. Create a Netlify account and start from a Hugo starter template. Then, deploy to GitHub.
2. Get your repository URL. As an example, here is mine: <https://github.com/52454D434F/rem-co-com.git>
3. In the terminal, go to your working folder and run:

```
git clone https://github.com/52454D434F/rem-co-com.git
cd rem-co-com
git submodule add https://github.com/onweru/newsroom themes/newsroom
echo "theme = 'newsroom'" >> hugo.toml
hugo
hugo server
```

Open the browser and go to <http://localhost:1313/>

```
touch .gitignore
echo .DS_Store >> .gitignore
echo /public/ >> .gitignore
git add .
git commit -m "My first commit back to Github"
git push origin main
```

In Netlify, add Environment variable HUGO_VERSION with value 0.124.1 (your Hugo version)

Update the Hugo version in file netlify.toml to your Hugo version and push to GitHub

The new template should work.

Installing DecapCMS: follow the instructions on <https://decapcms.org/docs/basic-steps/>
