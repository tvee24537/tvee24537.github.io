---
layout: post
title:      "Game Tracker"
date:       2020-11-17 00:46:54 +0000
permalink:  game_tracker
---

I started this application because I was having a problem keeping track of the games I owned. I want a tracker that will keep my progress and the review of the games I played. I did a tracker for my last project with Sinatra as well so I will use what I learned then on this app as well.

I started this with a skeleton app that will have most, if not all, of this current Rails project requirements by following the example video on the building of MyBlog. I did not use the methods I used in Sinatra because Rails many shortcuts and magics. 

What this app will do in summary: 
* Create user, lets a user log in with google authenticator 
* Create, list, rate, place price, and categorize games
* Create reviews for games under user
* To do all that was quite challenging, a different challenge from the Sinatra project. 

While the model relationships got easier, it also got more complex, like having a has_many :reviewed_games, through: :reviews, source: :game. Making the skeleton app itself also got way easier and faster with rails generators, but there are some downsides to the generators as well, like how rails new “project” command added some gems that I did not need into the gemfile. The gem ‘webpacker’ had me losing a few hairs, because I could not figure out why the rails server was not working until my cohort lead had me comment out that gem since it’s not needed for this project.
While working on it, I got my server stuck in an infinite loop:

![https://imgur.com/a/NzpG4J8](http://)
 
This is what I was seeing on my webpage:

![https://imgur.com/a/2IvmQWW](http://)
 
It was happening because I have ‘before_action :redirect_if_not_logged_in’ method in most of my controller. I fixed this by adding in 'skip_before_action :redirect_if_not_logged_in' where it needed, which was in the session and user controller. 

Another error was from the webpacker gem, rails came with it so I didn’t check if it was working or not but it gave me this error which had me thinking something was wrong with the code and not the gem itself.

![https://imgur.com/a/F6TLTxs](http://)
 
The solution to this one was easier, I just need to remove that highlighted line from this application since I was not using webpack gem. That was the only line that uses webpack.

After debugging a little more, I found this after I log in using google omniauth:

![https://imgur.com/a/0Tvte8c](http://)
 
I had no idea what that is, so I googled that title and found out that I need to put in ‘skip_jwt: true’ after the omniauth builder code to stop JWT from checking something that I didn’t need it to.

Again, I’m leaving the aesthetic as the basic form of what is given due to the time constraint and lack of experience, but I now have a navigation bar on top that persists throughout the views.


