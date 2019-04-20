---
layout: post
title:      "Fake It Til You Make It"
date:       2019-04-20 14:57:33 -0400
permalink:  fake_it_til_you_make_it
---


As I started out coding my first project, the CLI Gem Scraper, there were many thoughts running through my head….

              1. How will my CLI class work…. Will the user have to type yes or no, or will I simply bring in the movie list for them with my first method?
              
              2. What will my Movie class store? Will I initialize with just a movie title and movie url, or should I include the movie rating also?  Will the user even need to use the url, or can I scrape all of the data that they will need? 
              
             3. Will I need a scraper class?  What will I name my methods in my scraper class?
             
             4. What data will I scrape?  The movie title, rating, genre, and description?  Is that enough data for my users, or am I missing a very important detail that they will want?.......
						 
						 
And the lists kept running through my head as fast as lightning bolts! As one thought would leave, another would enter.  In order to slow these thoughts down, I decided to start out by coding fake data.  
	
I wrote down some thoughts of how I would like my user to interact with the CLI and what I wanted to scrape.  After that, I started out in my CLI class with making fake data.  

For starters, I made a simple call method and used the old, “Hello World”!  This was just to test, that everything I had done up to this point, was working correctly.  Once the method was returning “Hello World", I was off to the races!  

Initially, I made a case statement in the CLI class that was lengthy, but it entertained all of my thoughts of how the users would interact with the gem.  From there, I created a movie class and a method within, to store the fake data.   As I was inputting the fake data, I realized that I needed to refactor my CLI class with a simpler if/else statement.  Once I had the fake data in and the CLI refactored, I started running tests to ensure that the code I had written was working. 

Time for real data!
Now that I had the gem working with fake data, I decided it was time to scrape for real data.  As I would find  the css selectors, I would replace the fake data with the css selectors which contained the real data.  All along, I was testing that my code was still working.  Then I created a  Scraper class and moved the scrape methods from the Movie class and into the Scraper class.  Again, I kept checking my code to see that it was still working.

By using fake data in the beginning, it allowed my to build the structure of my code in the correct order.  Once the structure was standing tall, I was able to convert the fake data to real data.  

For me, coding is fun!  It lets my imagination run wild with ideas of ways to better the web.  I may not always know how to get the code that I want in the beginning, but I can fake the data until I make it real!

