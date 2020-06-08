---
layout: post
title:      "Mom, I'm Bored!!!!.... Javascript Project!"
date:       2020-06-08 16:39:36 +0000
permalink:  mom_im_bored_javascript_project
---


Since the recent "Stay at Home" orders that many of us have been under, I am sure that I am not the only one who has experienced their child saying, "Mom, I'm bored".  Hearing this phrase consistently gave me the idea to build a single page app, full of activity ideas for kids to do.  

So started the planning...

Since I am a planner, I decided to map out everything from models, controller actions, to fetches and stretch goals.  I decided to start with a simple has_many belongs_to relationship, where a category has_many activities and an activity belongs_to a category.  I made some stretch goals of eventually adding a user model, making the categories dynamic, and a destroy controller action.  

The BEST planning that I did was deciding to build vertically. 
I built out each controller action individually on a separate branch.  This saved me an enormous amount of time and allowed me not to destroy any code that I had previously working. 

Once I had my "plan of attack" as I like to call it, it was time to start building.  I started building out the backend first by creating a new rails api.  Once I had the rails skeleton, it was time to branch off from the master and build vertically.  I used generators to create the model and controller.  After migrations took place, it was time to build out the routes, serializers and controller actions.  Oh, and of course I cannot forget to mention that I needed to add the gem rack-cors so the front and back can communicate!!

Then came the frontend build...

Once the main directories and files were set up and linked, I started out by adding an event listener to load the DOM and console logging as the event handler to confirm that I had properly set up the event listener.  I also checked that the rails api route was working as expected in the rails server.  

Time to make some functions!
My favorite part came in when I got to play "Go Fetch"!  FINALLY, it was time to get the JSON data from the backend.  For this part, I used debugger and determined how the attributes were being brought in by JSON.  Once I was able to console log the data being brought in, it was time to render the data for the user to see.  

On to creating a new activity... First I needed to create a form with an id,  that the user can fill out to add a new activity.  The id will allow me to use a query selector and add an event listener to it.  The createFormHandler function takes in the values and passes them to the postFetchActivity function which will then send the values via JSON to the backend and add the new activity to the activities container.  

From here I went on to create a patch function to edit an activity.

Lastly, added a bit of styling!  

I really enjoyed this project and realized how much faster it is to build vertically then horizontally!  

Happy coding to all and to all a great day!!!


