---
 title: How I Created My Portfolio & Blogging Website 
 tags: [portfolio, website]
 style: fill
 color: primary
 description: Hello everyone, I welcome you all to my first ever blog post. I am super excited to write this blog in which I will be focussing on how I purchased my domain and what else I did before thinking of creating my portfolio website.
---

## Introduction
 
Hello everyone, I welcome you all to my first ever blog post. I am super excited to write this blog in which I will be focussing on how I purchased my domain and what else I did before thinking of creating my portfolio website.

## Motivation 

Before even thinking of motivation I already have a few awesome friends who always motivate me to push into my boundaries and make me realize what is best for me and what I am good at. The reason for you people reading this blog is also a result of the huge guidance and support provided to me by them. Secondly, I found this topic really interesting and worth learning so started working on it. You shall see my various pieces of work in future as well.

## Why I Decided to Create My Own Website

A website is an important tool, one of the best ways to develop an online reputation, whether you are an entrepreneur, job seeker, artist, or a writer. It is not difficult to make your own website, there are templates and tools available to create a website. At first I thought about writing my content on any of the websites that are available on the internet, but then I decided to create my own because there are multiple benefits that I could get by doing that like:

- If I had my own website it would be a good learning path for me on how to create and host it over the internet.
- If I am writing a blog and want people to read it, I need a lot of research and hands-on experience  to get good and correct knowledge about the topic I am writing on which will eventually expand my knowledge.
- My creativity level can get a lot better as I will try my level best to create content that people will find interesting.
- I can even promote myself because a website  can showcase a lot about me, including my resume. 
- Website connects you to the whole world  as it is a global platform where anyone can read your content from  anywhere in this world.


## Options Available For Blog Post Website
 
So when I decided to create a website for posting my blogs, I found that there are many options available for it like Wordpress.com, Medium, Tumblr and many more. I explored  almost all of them. These all are managed blog post websites but I wanted to learn how to create a portfolio website and hosting it over the internet


## Getting my own Domain

I spent a lot of time searching for a domain suitable for me and then I got my domain shivam-sharma.tech. I had options to purchase it for a year or two but being a beginner I chose to buy it for one year. It cost me 799/year which is a good price compared to many other options that were available on [BigRock](https://www.bigrock.in/). There are many other options available with even lesser price depending on your choice of domain.


## Creating Website Using Open Source Available Themes 

After researching how to create a website, I found some useful tutorials which helped me to create a website from scratch. But writing code to create a website was taking a lot of time and effort. So, I started searching for alternate ways to create websites and found that there are multiple open source themes available to use such as  [jamstackthemes.dev](https://jamstackthemes.dev/) where collections of open source themes are available. After trying out a few themes, I selected [YoussefRaafatNasry/portfolYOU](https://github.com/YoussefRaafatNasry/portfolYOU) theme (as shown in below screenshot) which is available on Github and is absolutely free. 



<img src="/assets/images/github1.png">


I was able to modify websites after looking into their instructions in documentation. I just had to edit the configuration and markdown (md) files that automatically generates static websites. portfolYOU theme is using jekyll which is a static site generator tool.

<img src="/assets/images/github2.png">
<img src="/assets/images/github3.png">


## Hosting My Website 


Now my website was ready to be hosted over the internet. I found a lot of information on vendors who could give support and servers to host my website. After some more research I found that we could utilize [Github to host static code](https://www.geeksforgeeks.org/using-github-to-host-a-free-static-website/). This was pretty cool for me to explore more about github functionality. You can generate a github page by following their [tutorial](https://pages.github.com/). Now it was the time  to add a custom domain which we could be set up by following github’s [tutorial](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site) but after setting up the domain, I was getting multiple issues like SSL error and not properly updating with my domain.



## Switching on Netlify

After doing some more research on the issues,  I found one good article on [How to host a website on Netlify with a custom domain for FREE — Step by Step Guide](https://levelup.gitconnected.com/how-to-host-domain-to-netlify-site-for-free-step-by-step-guide-45d0c2102db3) which was super helpful for me. 
 

Netlify helps you to automate your process to deploy websites on your custom domain. You can follow the below steps:

First we need to setup our custom domain in the Domains module

<img src="/assets/images/netlify1.png">

Added my custom domain shivam-sharma.tech which was purchased on Bigrock.

<img src="/assets/images/netlify2.png">

Netlify will ask you to update the domain's name server on domain manager. It will allow netlify to manage our custom domain.

<img src="/assets/images/netlify3.png"> 
<img src="/assets/images/netlify4.png">
<img src="/assets/images/netlify5.png">

Now we have to import our website theme from github into Netlify by clicking on “New Site from Git”

<img src="/assets/images/netlify6.png">

Selected Github and given authorization permission to Netlify.

<img src="/assets/images/netlify7.png">
<img src="/assets/images/netlify8.png">

Once we have selected a project and branch of the project we need to provide commands that run to build the website.


Build Command:

```bash
bundle exec jekyll build
```


<img src="/assets/images/netlify10.png">

Once the application deployed successfully we get the netlify.app link where our website is hosted. 

<img src="/assets/images/netliy11.png">

Now we need to enable HTTPS and wait for DNS verification. Once DNS verification is successfully verified our custom domain will not go through SSL error.

<img src="/assets/images/netlify12.png">

We need to select our custom domain as the primary domain.

<img src="/assets/images/netlify14.png">

You can visit my website at [https://www.shivam-sharma.tech/](https://www.shivam-sharma.tech/) and see my blog posts and activities.

<img src="/assets/images/netlify13.png">

