---
title: "Online Presence"
date: 2023-01-29T23:30:01+05:30
description: The story behind setting up this website!
---

I've tried multiple times to setup up a website. It has been a PITA for me every single time. There are multiple reasons for this. 

The very first language I programmed was the BASIC programming language. 
I remember me cycling with two other friends to a quite far place *3 Kilo meters approx, it was far for a 5th or 6th grade 'me'* to meet a guy, maybe a college graduate who had a computer at home with a color monitor *yes, we had only monochrome monitors at school*. That is the very first time I'm seeing a color monitor. I was awe-struck when I saw BASIC's graphics drawing colored circles and squares. The picture of a **pink circle** is etched in my brain and I'll take it to the grave with pleasure.
We got some tips from him to create a graphics demo for our science fair.
I vaguely remember creating multiple silly demos for a science fair in our [school](https://maryannschool.in/). Among the 5 or 6 demos we made, the two demos I remember are a Pac-man like character chasing a dot and a program that shows a billboard when there is lightning etc... 😆 ya *lighting*... why not? 

The only thing I remember is, **it was hard**. I've no idea why the computer is doing what it is doing. The billboard was planned to be something else, but due to some reason, I had some flashing like effect that I couldn't get rid of. Due to time constraints and everything, I settled for a billboard and built a story around it with lighting and stuff... LOL. That Pac Man like thing was the satisfying one 😊

Fast forward a few years, I was learning [VB6](https://en.wikipedia.org/wiki/Visual_Basic_(classic)) in a computer center next to my home. Then out of interest I went ahead and learned [C](https://en.wikipedia.org/wiki/C_(programming_language)) using [Turbo C++ IDE](https://en.wikipedia.org/wiki/Turbo_C%2B%2B). The point here is, I got used to the color coding and basic functionalities provided by these [IDE](https://en.wikipedia.org/wiki/Integrated_development_environment)s.

Later in college, I was introduced to [java](https://en.wikipedia.org/wiki/Java_(programming_language)) and [html](https://en.wikipedia.org/wiki/HTML)](https://en.wikipedia.org/wiki/HTML). I hated them right there just because there was no IDE. I hated writing programs in notepad for java, then compiling them in the command prompt and mapping the error to my code *(no double click or keystrokes to do it!!!)*. To top all these inconveniences, there was no line number in notepad then, and I dint bother to check if it can be enabled or not. The whole working style bothered me and I just hated it. 
I couldn't overcome my hatred for java and html for a very long period and I just didn't learn anything related to web development then. Even simple web programs look very complex to me.

With this background, I tried to set up a website for myself and had a horrible experience. By that time, the only thing I could do with ease was to buy a domain name. I kept it in my possession for several years without ever trying to set it up. If at all I tried, I never succeeded. Eventually, I will give up in a week or so. Html, PHP, CSS, js etc... I fiddle with everything without knowing their purpose. Altogether, I think I would've lost around 50$ to [AWS](https://aws.amazon.com/), [DigitalOcean](https://www.digitalocean.com/) and [Vultr](https://www.vultr.com/) trying to host my website. I even had my domain up on GitHub[ Pages](https://pages.github.com/). I needed some control over my website and the name; GitHub Pages dint serve my purpose and hence I wasn't impressed. 

The next important thing I expected was to have a custom theme as I wished. I should be able to write my content in [markdown](https://en.wikipedia.org/wiki/Markdown) only. Even before stumbling into the blog that made me set up the website, I fell in love with this [Vulkan tutorial](https://vulkan-tutorial.com/) which uses markdown for content. 
I fiddled around with [daux.io](https://github.com/dauxio/daux.io), which the Vulkan tutorial is using to generate the website from and failed at it.
In a nutshell, these are the basic requirements I was looking for:
* markdown content
* the theme that I can customize

How did I succeed after all these failed endeavors? 

A couple of weeks back, I was reading a blog post on some graphics stuff. I checked the about section only to find that he has hosted it in [NFSN](https://www.nearlyfreespeech.net/). The name **nearlyfreespeech** caught my attention. Did some quick research on the hosting service and was happy with the info I could gather from different blog posts and some hacker news threads. 
From the short description, I understood that these are something that I was looking for. He was using [Jekyll](https://jekyllrb.com/) to generate the website from markdown. There was a link to a [post](https://ericbernier.com/jekyll) on the steps involved. It looked super easy. So I jumped right into it, searched for a Jekyll theme, added content, generated a website, created an account in NFSN and pushed stuff. 

Damn! I hit a wall. The ruby version in NFSN was a bit older and one of the gems failed to install. I tried to install a previous version and likewise, I kept modifying versions of many gems. About 6 to 8 hrs after I came to my senses 😓 told myself it is never gonna work 😖

Out of curiosity, I started searching about *static website generators* a keyword I just learned and landed on [Hugo](https://gohugo.io/). It was looking neat, all steps are almost similar to Jekyll. So once again I repeated all steps. Find a Hugo theme, this time I dint add content. The first thing I wanted to do was to make sure **I can**** generate a website and host it in NFSN. 

Finally, I succeeded! I hosted a website using a minimal theme. I've made it. I'm got my space online ... hurray!!!

It was difficult at first, but then I managed to understand Hugo's templates and its theme structure. I had heavily [modified a theme](https://github.com/madptr/cleanslate) and hosted my website. My past two weeks have been busy modifying the theme, writing a couple of articles and seeing how it is rendering on PC and mobile. Asked a friend to read it, making sure it is all working as expected. 