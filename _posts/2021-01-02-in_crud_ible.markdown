---
layout: post
title:      "In CRUD ible!"
date:       2021-01-02 21:46:26 +0000
permalink:  in_crud_ible
---


Pun intended. Having just built my first full-fledged Sinatra application, I'm feeling pretty great. Entering into the world of Ruby development has been a grind for me, but I finally feel like the big picture is coming into focus. 

For this project, I decided to build a simple web application for a user to create and keep track of a roster of basketball players. This program could potentially be the first step for a larger application that would handle a fantasy sports league, or something similar, so I wanted a user to only be able to interact with their own data, but view data from all other users. 

One of the most interesting parts of the project build for me was seeing nested params in action. For example, having nested params for all of the different attributes of my team object meant that when I was writing out the patch request in my controller, I didn't need to reference each of those attributes individually, just the params. I found this to be a very useful and powerful tool. 

Another tool I found particularly handy was ActiveRecord validations. The simplicity of including a "validates" line in you object model can open up so many possibilities. This project validates that a username is present and unique, and that all fields are complete on a new team form. That's not a whole lot of validation, but I can imagine the ways in which I'll use ActiveRecord validations in the future. 

What I found most satisfying, however, was being able to really control the user-side experience using shotgun. I loved being able to write a few lines of code, pop into my browser and test it out, then determine what changes needed to be implemented, and make them. One particular example came when I was showing off my project to my wife. I was demonstrating how only the user who owns a particular team can make changes to that team, and when I went to update a team I had created, I realized that one of my fields was not updating! I quickly realized that I had not nested the params for that particular field, fixed the error, and immediately could see that the issue was fixed user-side. I also enjoyed deciding which pages needed links to which other pages to dictate the flow of the user's interaction with the application. I am really looking forward to building more applications and implementing more complex functionality. 



