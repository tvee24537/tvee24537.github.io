---
layout: post
title:      "The Wishlist"
date:       2021-03-20 22:53:24 +0000
permalink:  the_wishlist
---


There are just too many things to do in a day, I can’t keep track of them all. I love to build up trackers, they make my day a little more manageable. The idea came from my last visit to my old home in Thailand, most of my relatives came over to visit. You know for sure that you need souvenirs for them, especially for the elders that looked after you. There are also too many relatives at a get-together this size, I can’t keep track of all the stuff they look forward to when I visit. I need another tracker! This latest project is the Wishlist.

This project is made to keep track of gift ideas for friends and family. This tracker will let you add and delete the destination where the gift will go, the image on the destination is optional. Under the existing destination, you can add and delete gift ideas. You can sort each destination in the granted or waitlist page with buttons below the destination card when you go into the destination. Within the API folder is the Ruby on Rails part which manages the database. Within the client folder is the JavaScript with React-Redux part that manages the frontend of the project.

This project is done under these requirements set by FlatIron:

* The code should be written in ES6 as much as possible
* Use the create-react-app generator to start your project.
* Your app should have one HTML page to render your react-redux application
* There should be 5 stateless components
* There should be 3 routes
* The Application must make use of react-router and proper RESTful routing
* Use Redux middleware to respond to and modify state change
* Make use of async actions and redux-thunk middleware to send data to and receive data from a server
* Your Rails API should handle the data persistence with a database. You should be using fetch() within your actions to GET and POST data from your API - do not use jQuery methods.
* Your client-side application should handle the display of data with minimal data manipulation
* Your application should have some minimal styling: feel free to stick to a framework (like react-bootstrap), but if you want to write (additional) CSS yourself, go for it!

Let’s start with Rails API:

I made a root folder to house both the frontend JavaScript and the backend API folders first, then created the API with “Rails new <name> --api” command to not have unnecessary files. Then I used Rails g scaffold to make the models and associations which will be destination has_many gifts and gift belongs_to destination. I’m keeping it simple, I don’t need users right now since no one else should see what’s on my tracker for gifts. Set up the Rack CORS gem with bundler to allow restricted resources on a web page to be requested from another domain outside the server’s domain; to allow get, post, patch, and delete requests from our Rails API. Then set up the serializer to build JSON objects for selective information display. Set up and update the database and you’re pretty much done with the API backend part.

Making a React App:

As per the requirement and also a way to make an app fast, I use the “npx create-react-app” command to set up the react app with all the basic components. Before doing anything else, you want to delete unnecessary files before installing Redux and Redux-Thunk. React-Redux allows React components to interact with the Redux store, it provides the Provider that enables interaction of Redux store with the rest of the app and the Connect function which enables the connection of component to the store. Redux-Thunk middleware will handle asynchronous actions within the app which avoids problems like having an action creator returns an action before data is fetched from the API. Then the React Router enables the app to have different views without reloading the entire page. The app will have at least 3 views, so at least 3 routes will be used.

Improvements and concerns:

This project has a long way to go, but right now it passes the requirements and some more. The term used is destination instead of person because it is just a draft to work around, I would like to add on categories like country, friends, family, etc. to it so to not get confused later on. 

