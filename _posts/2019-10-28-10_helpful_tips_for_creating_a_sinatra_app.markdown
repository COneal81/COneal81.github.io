---
layout: post
title:      "10 Helpful Tips for Creating a Sinatra App"
date:       2019-10-28 15:22:23 -0400
permalink:  10_helpful_tips_for_creating_a_sinatra_app
---


As I was creating my Sinatra project, I came up with some helpful tips for others creating a Sinatra app.  

**1. Ruby gem Corneal**
       a. Use the Ruby gem Corneal to start your Sinatra app.  Corneal is a Sinatra app generator that will load all of your routes, models, and views for you.  
       b. In your terminal, run gem install corneal
       c. To generate your app, run corneal new APP-NAME
       d. Run bundle
       e. Run shotgun to confirm  that everything is working
       f. Corneal has other commands as well to generate MVC’s.  For more info: https://thebrianemory.github.io/corneal/
When I used the corneal app, I realized how much time I just saved.  It generated all of the main file structures and the MVC’s for me!  What more can you ask for!   


**2. Params**
       a. Imagine that params is an airline called Params Air.  Params Air transports the attributes from one side of the country to another.  The attributes board the plane when the user has typed in the information and clicked submit.  The airplane then flies the attributes to the controller, where it lands at the route destination, post. Once the attributes get off the plane at your post route, you see them displayed on the show page, their final destination.
       b. While using Pry, you call params in your terminal.  This will help you find what attributes are on the airplane!
       c. The params attribute comes from the “name” in the input form.  It also needs to match the attributes on your schema.


**3. Schema and Forms**
       a. When creating your forms in the views directories, I recommend that you go into your schema.rb file and copy the attributes from the table you created.  Paste those attributes in the views file that you are building the form in.  This helps you to remember what you called your attributes in your database and also prevents errors.  I found this to be a time saver.


**4. Navigation Bar**
       a. As I was building my project, I quickly realized that I needed a navigation bar.  Technically I could put a link on each page, but this would be cumbersome and I would be breaking the rule of DRY (Don’t Repeat Yourself).  Instead, I placed a navigation bar in the views/ layout file, above the yield, in a div class.  
This will help when testing your app in shotgun.


**5. Tux**
Use Tux to help with relating your objects and checking attributes.
To exit tux, type exit.  


**6. Binding.Pry**
       a. Use with Shotgun.  
       b. While in Shotgun, put binding.pry in your code.  
			 c. Go back to your app, and use your app as a user would.  Type the information into the form.  Once you hit the submit button, you should hit your pry.  If for some reason you do not hit your pry, try placing your pry one line above or below in the route. 
        d. Place your pry in the route that your form is sending the information to.
        e. You can also place a binding.pry in a views file by using it within a erb tag.  
ex.) <%binding.pry%> 
        f. When using VS Code as your local environment, be sure to enlarge your terminal to at least ¾ of a page.  If you forget to do this, often pry will not follow through to where you can type in your terminal, causing you to delete the terminal altogether.
       g. If your terminal gets stuck, you can press q and it will continue and allow you to type an input or exit.


**7. ActiveRecord Validations**
    I found validations to be very fascinating and super easy to use.  
       a. I used ActiveRecord Validations to validate;
               i. That fake data is not being persisted to the database.  
               ii. To validate a user signup has a unique email, has a username that is longer than 2 characters, and a password that is between 6 - 20 characters in length and recognizes capitalization.
							 
              [ https://guides.rubyonrails.org/active_record_validations.html](http://)


**8. Take one route at a time.**
       a. Routes can be confusing.  By taking one route at a time, you are able to stay focused on what that specific route is doing and where it is going.
			 b. Check that each route is working before continuing on.


**9. Forms**
       a. While creating your form, the input id needs to be exactly the same as the label.
                        

 **10. Double check your work!**
       a. Test every route and link to make certain that they are working correctly.  
       b. In tux, you can call user = User.last.  This is how you can check that your password has been scrambled by looking at the attributes.  
       c. Try to break your own app every way possible.  
       d. Check that the error messages are coming back correctly for what you are inputting or not inputting!
       e. If possible, have a friend, parent, spouse, co-worker, or anyone you know use your app and listen to their feedback.  Four eyes are always better than two!
 

