---
title: Much Ado About Me
date: 2021-09-22 14:25:40
tags:
---
I wanted to add an about me page, leaving the main page for blog content only. Hexo makes it pretty easy to add new pages using `hexo new page [name]`, but that simply gives me a blank page - I had to create a template myself, largely using the css already within the theme code.

I basically want to create two columns: one with a picture of me, with some space below for info, such as tech stack and projects that I am working on (links to Github repos - as time goes on I could expand this into a distinct projects page). The approach is basically to read through the .css files within the Minima theme and experiment with different options. 

Even though this blog will be deployed through Netlify, the inbuilt `hexo server` feature is pretty useful - I can deploy a local version of the site for preview purposes. This has made the trail&error approach to html/css much more viable.

### Images => Cannot GET

So this problem was pretty annoying and I never found a proper *solution* to it, merely a work-around. Basically, I got a 'cannot GET image' problem when trying to load the photo in the about page. The StackOverflow solution was to use the express.static function to serve the images, however my knowledge of EJS is practically non-existent, and I could not figure out how/where to implement this. 

Instead, I looked at the implementation of the thumbnail images within _config.yml and copied the approach by adding an about_photo option that linked to the picture within /images/. I hoped that whatever code dealt with allowing the serving of images would be able to pick up on it - and I was right, although this is obviously an area that I will have to revisit.

### Writing about myself is the thing I enjoy the least...

...so it is best to get the pain out of the way quickly in one monologue.

I was born in Poland in the turbulent year of our Lord 1989. In 1998 (kind of...) we moved to the United Kingdom. After a pretty unremarkable childhood I studied Archaeology and was involved in several excavations in the Middle East, including the site of Miletus. Academia was never for me - the very first archaeology professor that taught me referred to it as 'intellectual masturbation'; lots of fun, but of no benefit to anyone. I think he was broadly correct. I say this not to disparage the field of study (which is quite interesting), but I could not have made a career out of it. However, it did instill in me a love for understanding systems - abstract things of human construction that end up controlling more of our lives than we let ourselves admit. 

After some abortive attempts to do other things, I ended up studying law. Mixed feelings about that - hard to understate its importance (it is after all the source code of human civilisation), but the every day practice of it was far from what I had hoped. I could not escape the feeling that the organisation of legal field left much to be desired. I learned to code (in Python) partly as an attempt to address those deficiencies - I wanted to streamline the legal administrative process to be able to deliver greater value to clients, but I did not have a receptive audience. I did, however, found that I really enjoyed writing code. 

I ended up applying for the 8thLight Apprenticeship, and after a pretty intense (but genuinely engaging process) I started as a Trainee Software Crafter in September 2021. This blog will serve as some kind of record of this apprenticeship, and after that... who knows?

This will need trimming down for brevity. Okay, enough. 8th Light have organised this a number of events to introduce the new Apprentices to the company (including a Zoom-based coding retreat), and one of these events starts shortly.