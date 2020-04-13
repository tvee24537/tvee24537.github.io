---
layout: post
title:      "Simple Tracker"
date:       2020-04-13 03:24:19 +0000
permalink:  simple_tracker
---


It all started when someone close to me starts to become a little forgetful. It’s easy to write something down on a small notepad, sticky note, etc., but then losing that as well gets annoying. To help them out, I created this simple application called Simple Tracker. My plan looks something like this:

* User can Login >> sees instruction, create/ delete list
* User create/pick existing list database
* User can add/delete data in the list, list updates after clicking submit
* User can back out of list currently viewing to the main page
* User can Logout and also delete their account if needed

It’s as simple a list as it gets, but it gets the job done. After the base is made, it’s easier to build up upon it. I started with the Corneal gem that is used to being the foundation of a Sinatra application that uses shotgun gem. From there I with the simple stuff like making the controller, models, and views folders and files that will be in it. While I was thinking about how the application should function, I came across Expensy, which seems very similar to what I had in mind. I had a hard time figuring it out as I was not skilled in CSS, java, or HTML so I left what aesthetic Corneal gave me in the layout alone and focus more on the relationship between the user, list, and item being created. Using belongs_to and Has_many relationships, I linked them together and build outward from there.

The tougher parts are in the views folder, the show pages that display the data to the user is complex. I didn’t have a lot of experience with HTML, but I managed to build a table following some references. The table is the most vital part of the application, it needs to be clearcut and easy to use. I was able to get the application to work as I wanted it to, making it simple so that an elderly can use it. Simple installing by cloning the file, run bundle install, rake db:migrate, and then finally shotgun to launch the application. The front page doesn’t look amazing in any way but I think simplicity is best when dealing with the elderly.


