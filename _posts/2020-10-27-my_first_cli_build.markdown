---
layout: post
title:      "My First CLI build"
date:       2020-10-28 00:38:34 +0000
permalink:  my_first_cli_build
---


As a complete newbie to the world of programming, not to mention Ruby, I was pretty intimidated by this first project build. What is a CLI? What is an API? How are they related and how do I use what I've learned so far to make them work together? These are the questions I was asking myself as I tried not to panic. Turns out, like a lot of things in life, it was a bit simpler than I'd imagined. 

## API & CLI

I learned that API stands for Application Programming Interface, which is just a collection of data that I could interact with and build functionality around. The challenge: finding the right API for my skill level... newbie. 

I also learned that CLI stands for Command Line Interface. Okay, so a user can type in the command line to interact with my code. I got it! 

Thankfully, after some digging through the suggested APIs provided by my awesome cohort lead, I was able to find a couple of APIs that seemed interesting to me. To be honest, the first API I chose seemed a little beyond my skills as a Rubyist. I first tried to build around the Pokemon API, which was very cool, but VERY dense and difficult to understand. So, I returned to the 'suggested' list and found the Studio Ghibli Films API (*angels singing*)! Because of the wonderful JSON browser add-on that I installed, I was able to easily recognize the data within the API. There were several hashes storing various types of legitimately interesting information that I could access. Yes!  

## The Project

I was able to build an API class responsible for pulling down the information I wanted to access, a Film class that is responsible for holding onto that information and a CLI class that is responsible for interaction with the user. All of these, combined with an environment file allowing these classes to interact and an executable file allowing the user to startup the program, resulted in an a little program that I'm legitimately proud of. 

A user (maybe you!?) can startup the program, and when prompted, reply "y" (for yes) to see a list of all 20 films produced by Studio Ghibli, select a film title from an indexed list, and see a brief, albeit detailed summary of the film, learn the year it was released, by whom it was directed and produced, and even the average Rotten Tomatoes score. Cool, right? 

## The Journey

No endeavor that's worthwhile ever comes entirely absent of struggle, and this particular endeavor is no exception. There were some snags along the way.  First, as I mentioned before, was just finding the right API. I discovered that not all APIs are created equally and finding one that looked like something I was familiar enough with to use was a brief challenge. Then there was getting started with my environment. I was having a very hard time using the downloadable IDE-- operator error, I'm sure, but either way, the silver lining was that it lead me to finally set up my local environment. It took a bit of time getting everything installed, but once I had it, I was immediately experiencing the benefits of working in a local environment. Then, in the process of building the app there were definitely some stoppages here and there, but thankfully, using pry, I was able to test and problem solve as I went. I definitely want to add some additional functionality to my app at some point, but I'm able to be proud of, and recognize the achievement of what I've made. In particular, I noticed that in my API, there are keys pointing to urls that hold information relating to particular characters, locations, vehicles and other things that are part of the films. I'd like to access those urls and give the user the ability to learn about that information, too. I'd also like to give the user the ability to search for a director and see a list of all the films by that director.  I'm sure I'll think of other ways I could improve the program as the journey continues...
