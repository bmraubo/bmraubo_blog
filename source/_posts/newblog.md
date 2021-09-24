---
title: Building a Netlify Blog
date: 2021-09-22 12:07:07
tags:
---

I have been asked to make a Netlify blog, partially as training and partially as a means of recording the progress and experiences of the apprenticeship here at [8thLight](https://8thlight.com/). Since we are still in the midst of Welcome Week, I've mainly been given simple tasks that keep me busy before the more serious project work begins. 

The previous task (using TDD principles to solve a kata, with a focus on GitHub Actions/Merge Protection) was meant to familiarise me with Continuous Intergration principles. The blog is meant to build on that by seeing how Continuous Delivery works in practice.

The requirements are that the site uses a Static Site Generator to deploy from Github, takes a directory of markdown files as the input source, and then applies a template to them. I've been asked to purchase a cheap domain name for the site so that I can explore how DNS works in a little more detail. 

A big challenge for me is my very limited knowledge of HTML, CSS and frontend work in general.

I decided to use Hexo because it was based on Node.Js and focused on blogging - I do not need extra functionality, and would prefer to keep it simple so that I am not overwhelmed. Initially, I used the JamStack button to circumvent the whole `hexo init` process, but that left me in a pretty poor position where I had a template blog set up and linked to a GitHub repo, but had no idea how any of it worked. 

I deleted the repo and the site and started again using the helpful [Netlify step-by-step guide](https://www.netlify.com/blog/2015/10/26/a-step-by-step-guide-hexo-on-netlify/). After some permissions errors that were resolved by getting a bit more familiar with nvm (on Linux I would have sudo’d my way around this, but this was not advised), I managed to get a boilerplate blog and repo set up manually.

I created a test post using `hexo new post` in Terminal, and pushed it to the repo. All works fine! - the build process is automatic so I am taking some time reading through the deployment logs trying to understand what is going on behind the scenes.

Next step: mess around with themes - initially went for [Frame](https://frame.zhangyongqi.com/) because of its simplicity. However, I found this design a little too complex to modify myself, so I went for [Hexo Minima](https://adisaktijrs.github.io/minima/), which was a) simple (using only CSS and JS), and b) had clear comments within the code, allowing easy editing by a person who has limited knowledge of frontend work (i.e. me). It also looks cool and has a very groovy button that switches between light and dark mode.

Well done Adi Sakti Jrs. I have taken the liberty of modifying the theme footer to include a link to your GitHub.