---
layout: post
title:      "Order of GO!!!  ~ Rails Application"
date:       2020-03-14 18:20:26 -0400
permalink:  order_of_go_rails_application
---

Like any prject you build, whether it is a house or a web application, you need to have a solid method to your madness.  

When I started my Rails project, I decided to create an “Order of Go” to help organize my workflow.

## **1. Use draw.io and cleary make a wireframing diagram flow chart for your project**. 

*  Include models, relationships, attributes, and validations 
*  Reminder: Singular Items: Model, class name, belongs_to :___ Plural Items: controllers, views, has_many :, has_many :, through: :___

## **2. In VS Code, type gem install rails in your terminal.**

## **3. Run rails new name -T -d postgresql**
* Ex. rails new pet-app -T -d postgresql 
*  It is convention to name your app all lowercase with a dash if you have more than one word. 
     a.  ex.) property-tracker
*  Note:  -T tells it not to include any tests and -d means that you are selecting a specific database 
*  Postgresql is the database you are selecting

## **4. Run cd name**
* Ex. cd pet-app 
* In cd s in your terminal
*  run code . in the terminal. This will allow you to see and open your directories and files.

## **5. In the terminal, run rails db:create **
* This will create your database. 
*  Note: This is not a command that you have to run with sqlite, but one that you will need to run if you are using Postgresql.


## **6. Run rails s to confirm that you have everything set up correctly.**
* NOTE: If you are getting an error, check to make sure that you have Postgressl installed and that you have initialized it. (Look for the elephant at the top of your screen on Macs)****

## **7. Create a new repository on github. (on github)**
* Repository Name: Make sure that the repository names matches what you named your app in your terminal. ex.) pet-app 
* Description: Write a short description about the app. This can be changed or updated at a later date.
*  Choose either public or private. 
*  Do NOT check initialize with a Readme. A readme was created in rails when you created a new app. 
*  In termina l, run git init 
*  In terminal, run git status 
*  On github quick setup page, use the middle option (…or push an existing repository from the command line), 1st line (ex. git remote add origin git@github.com:COneal81/property-tracker.git) 
1. *  In terminal, paste git remote add origin git@github.com:COneal81/property-tracker.git 
2.  In terminal, run git add .
3.  In terminal, run git commit -m ”initial commit” 
4.  On github quick setup page, use the middle option (…or push an existing repository from the command line), 2nd line 
5.  In terminal, run git push -u origin master 
6.  Check repo to make sure everything commited over to github.

## **8. Implement Bootstrap**
* https://getbootstrap.com 
* How to use Bootstrap https://www.youtube.com/watch?v=EbZgUIyWyYE 
* Add to gemfile, gem ‘bootstrap’, ‘~> 4.4.1’ 
* run bundle install 
* Add to gemfile, gem ‘sprockets-rails’, ‘~> 3.2’ 
* Run bundle install and restart your server with rails s 
* In app/assets/stylesheets/application.css, paste

`// Custom bootstrap variables must be set or imported before bootstrap.`

* Rename file from app/assets/stylesheets/application.css to app/assets/stylesheets/application.scss
*  In app/assets/stylesheets/application.css, removeall the lines that start with *=require: 
1. *  ex. *= equire_tree . and *= require_self 
* Add to gemfile, gem ‘jquery-rails’, run bundle install, and restart the server with rails s 
* In app/assets/javascripts/application.js paste 
*` //= require jquery `
*` //= require jquery_ujs`

##  **9. Add Gems Bcrypt, Pry to gemfile**
* Run bundle install

## **10. Add gem ‘dotenv-rails’, ‘~> 2.1’, ‘>= 2.1.1’**
* Run bundle install 
* Create a .env file in the root of your app 
* Add the .env file to your gitnore file **VERY IMPORTANT** 
* Add gem ‘omniauth’ 
* Add gem gem ‘omniauth-google-oauth2’ 
* Run bundle install 
* Next, we’ll need to tell OmniAuth about our app’s OAuth credentials. Create a file named config/initializers/omniauth.rb 
* Add to the config/initializer/omniauth.rb file 
`Rails.application.config.middleware.use OmniAuth::Builder do provider :google_oauth2, ENV[‘GOOGLE_CLIENT_ID’], ENV[‘GOOGLE_CLIENT_SECRET’] end` 
* Log into https://console.developers.google.com 
* Add a new project. Once you get the client id and the secret. 
* Add them to the .env file. 
* Add middleware in config/initializers/omniauth.rb to point to google oauth 
* Draw your routes

## **11. Create Models and Migrations**
* Run rails g resource Repair name:string payment_status:string –no-test-framework

* Before running rails db:migrate, double check; 
1. The users model has has_secure_password in it before you run rake db:migrate 
2. List associations in ALL models 
3. Spelling 
4. Foriegn keys 
5. Attributes default values and data types 
6. Associations in models


## **12. Seed the database**
* Before running rake db:seed, be sure to double check the following;
1. ONLY use the .create method with bcrypt or else it will not accept password and only accept password_digest.
2. Double check that you have all attributes in the correct order and are set to local variables according to your associations.

## **13. Create Routes**
* Create routes
* In your browser, type http://local_host:3000/rails/info/routes to view all of the routes you have created.  You can also type rails routes in your terminal.


## **14. Create Actions in Controllers**
* Create view starting with index, new, show, edit, update, destroy 
* Update validations in model 
* Repeat this pattern until all crud functions are working

## **15. DRY up your application**
*  Use before_actions in controllers 
*  Use partials in views
*  Any logic that is present in your controllers should be encapsulated as methods in your models.


By creating a 'Order of Go', you will have organization to your thoughts and be able to execute your project faster.   I hope this helps you get started building a rails application and decreases the coding timeframe of your project.  Happy coding!!!








