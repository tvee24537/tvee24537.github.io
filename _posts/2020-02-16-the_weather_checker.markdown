---
layout: post
title:      "The Weather Checker"
date:       2020-02-17 02:34:25 +0000
permalink:  the_weather_checker
---


This project, the **Weather Checker**, started out well, the walkthrough video did a great job setting me up to a good start. The approach I went with is to make a simple list, much like what is detailed in the video. Which is to list what the gem needs to do, how the user will interact with the data, where to get the data, and building a simple working structure before starting the more complex scraping parts. Starting out this project, I begin by making a gem through bundler. The bundler set almost everything up to work. It was not totally the same as what was in the video, but very similar. I’m glad I could work with the learn built-in IDE, which saved me the trouble of looking for another console.

The first problem I got was not about how to scrape, it was about the gemspec file very early on. I spent over 2 hours trying to fix it only to see that it only requires me to put in my GitHub repo in as a spec and to add the spec.add_dependency for all the gems required. The second problem was that the video didn’t prepare me well enough for scraping. The example of scraping shown had a website with very nice and orderly Html codes, the website I chose had a big group of string in the same box, I had to use doc.search(“something-here”)[23].text to get what I wanted. At first, I was being too specific with it and the search returned blanks “ “ from the website. Then I was being too vague, so it gave me a wall of text instead of just that one bit of string I needed. That’s when I reach out to my cohort mates and got the square bracket method after the search parentheses and before .text. That selects only one Nokogiri object from that wall of text based on its position in that wall. It was interesting to see how it worked, on some it worked on others that I was being too specific, it resulted in an undefined text method instead. The third problem I faced was trying it all together, getting all the methods in each class to play nice together was very tedious. In the end, there’s only one thing that didn’t work as intended which is the user error text. The exit command works to have the user exit the program is somehow being treated as user error, therefore prompting the “not sure what you mean, type list or exit…” to be returned before exiting the program. 

To improve this gem I can make it scrape more detail about each day under the detailed forecast and change the detail right now to return with the days selection. I’ll make a new file for scraping, and optimize the way to scrape using each method. I should have done it, but due to time constraints, I wasn’t able to get it working in time. 

This is the link to CLI Gem walkthrough: [https://www.youtube.com/watch?v=_lDExWIhYKI](http://)

This is the link to the website that was scraped:  [https://f1.weather.gov/MapClick.php?lat=38.8988&lon=-77.0365#.Xkny1WhKiUl](http://)


