---
layout: post
title:      "The Guild Idea Single Page App!"
date:       2021-01-15 21:46:27 +0000
permalink:  the_guild_idea_single_page_app
---

When it comes to the single-page application (SPA), I had no clue when I started. I figured everything was going to be like what the rails project is, a multi-page dynamic website. I was unprepared for javascript that will be used for the majority of this project. We didn’t do a whole lot of JS in FlatIron, only about 3 weeks of it. I was struggling to piece together rails and JS when I’m not the best at both, a little more uncomfortable with JS. 
For those who do not know a SPA is a web application or website that interacts with the user by dynamically rewriting the current web page, instead of loading a new page, refreshing the page that the user currently sees. Since the majority of what the user sees will remain the same throughout, it was a bit difficult to get a good problem for this project. The example FlatIron provides are mostly music applications like this one is a remixer using simple notes, check them out: https://remixer-v2.firebaseapp.com/ 
I didn’t have problems related to music, I’m just not musically inclined. I figured that I might as well do something that will help me in my hobby instead. I hold an officer rank in my online gaming guild and one of my duty is to record what goes on in the meeting, so an idea pops out. I’ll make an idea page to keep a tracker of the discussions and new ideas that were brought forth. 
Starting this project was quite tedious, I separated the files between frontend and backend. The frontend folder holds the JS, CSS, and Html, while the backend folder holds all the ruby on rails.
It looks something like this (sorry for the bad diagram, I still haven’t figured out how to post a picture on here):
GuildIdea
--Backend
----App
----DB
----Gems
--Frontend
----index.html
----index.js
----CSS
I followed along with a live lecture video from FlatIron, I’ll put the video link at the end. After setting everything up I was hit with my first problem, the PostgreSQL. I’m using Ubuntu with Virtual Studio Code and it just won’t let me do the rails db:migrate. I had to uninstall it after I could not restart it’s server and reinstall it then restart the server, It worked for a bit then some other problems too complex for me to solve happened so since it’s not a requirement for this current project to use PostgreSQL, I opped out to use SQLite instead, that was what I used in the rails project as well.

After setting up the rails part, I draw out a simple diagram on how the JS should flow and also how the page will look like. I’m not the best in Html or CSS so I kept it simple. After that is complex work on how to link up JS with Html and rails. The application is very simple, you can signup and login at the start, post ideas/questions, and then comment on existing idea/questions.
There are many improvements to be done like adding in user authentication, sign out buttons (right now refreshing the page with F5 will do), making it more stylish, or adding a link button, but that’s all the time I have right now before the due date.
https://www.youtube.com/watch?v=CxZ-fG2KGsY&ab_channel=AysanIsayo

