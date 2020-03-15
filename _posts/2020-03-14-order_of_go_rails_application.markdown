---
layout: post
title:      "Rails Project"
date:       2020-03-14 18:20:26 -0400
permalink:  order_of_go_rails_application
---

When I started my Rails project, I was uncertain as to where to begin. I decided to create an “Order of Go” to share with others who are feeling the same way as I did.

## **1. Use draw.io and cleary make a wireframing diagram flow chart for your project**. 

1. Include models, relationships, attributes, and validations 
2. Reminder: Singular Items: Model, class name, belongs_to :___ Plural Items: controllers, views, has_many :, has_many :, through: :___

## **2. In VS Code (or any other local environment that you would like to use) type gem install rails in your terminal.**
## **3. Run rails new name -T -d postgresql**
~Ex. rails new pet-app -T -d postgresql ~ It is convention to name your app all lowercase with a dash if you have more than one word. ex.) property-tracker
-T tells it not to include any tests -d means that you are selecting a specific database Postgresql is the database you are selecting

## **4. Run cd name**
Ex. cd pet-app In cd s in your terminal, run code . in the terminal. This will allow you to see and open your directories and files.

## **5. In the terminal, run rails db:create This will create your database. Note: This is not a command that you have to run with sqlite, but one that you will need to run if you are using Postgresql.**


## **6. Run rails s to confirm that you have everything set up correctly.**
NOTE: If you are getting an error, check to make sure that you have Postgressl installed and that you have initialized it. (Look for the elephant at the top of your screen on Macs)****

## **7. Create a new repository on github. (on github)**
Repository Name: Make sure that the repository names matches what you named your app in your terminal. ex.) pet-app Description: Write a short description about the app. This can be changed or updated at a later date. Choose either public or private. Do NOT check initialize with a Readme. A readme was created in rails when you created a new app. In termina l, run git init In terminal, run git status On github quick setup page, use the middle option (…or push an existing repository from the command line), 1st line (ex. git remote add origin git@github.com:COneal81/property-tracker.git) In terminal, paste git remote add origin git@github.com:COneal81/property-tracker.git In terminal, run git add . In terminal, run git commit -m ”initial commit” On github quick setup page, use the middle option (…or push an existing repository from the command line), 2nd line In terminal, run git push -u origin master Check repo to make sure everything commited over to github.

## **8. Implement Bootstrap**
https://getbootstrap.com How to use Bootstrap https://www.youtube.com/watch?v=EbZgUIyWyYE Add to gemfile, gem ‘bootstrap’, ‘~> 4.4.1’ run bundle install Add to gemfile, gem ‘sprockets-rails’, ‘~> 3.2’ Run bundle install and restart your server with rails s In app/assets/stylesheets/application.css, paste

// Custom bootstrap variables must be set or imported before bootstrap.

Rename file from app/assets/stylesheets/application.css to app/assets/stylesheets/application.scss In app/assets/stylesheets/application.css, removeall the lines that start with *=require: ex. *= equire_tree . and *= require_self Add to gemfile, gem ‘jquery-rails’, run bundle install, and restart the server with rails s In app/assets/javascripts/application.js paste //= require jquery //= require jquery_ujs

## **9. Add Gems Bcrypt, Pry to gemfile
## Run bundle install**

## **10. Add gem ‘dotenv-rails’, ‘~> 2.1’, ‘>= 2.1.1’**
Run bundle install Create a .env file in the root of your app Add the .env file to your gitnore file **VERY IMPORTANT** Add gem ‘omniauth’ Add gem gem ‘omniauth-google-oauth2’ Run bundle install Next, we’ll need to tell OmniAuth about our app’s OAuth credentials. Create a file named config/initializers/omniauth.rb Add to the config/initializer/omniauth.rb file Rails.application.config.middleware.use OmniAuth::Builder do provider :google_oauth2, ENV[‘GOOGLE_CLIENT_ID’], ENV[‘GOOGLE_CLIENT_SECRET’] end Log into https://console.developers.google.com Add a new project. Once you get the client id and the secret. Add them to the .env file. Add middleware in config/initializers/omniauth.rb to point to google oauth Draw your routes

## **11. Create Models and Migrations**
Run rails g resource Repair name:string payment_status:string –no-test-framework

Before running rails db:migrate, double check The users model has has_secure_password in it before you run rake db:migrate List associations in ALL models Spelling Foriegn keys Attributes default values and data types Associations in models

## **12. Rollback a Migration**
Rake db:migrate:status This gives you the version number of all of the migrations that you have made. Rake db:migrate:down VERSION=20200111213346(the number is the timestamp)

## **13. Seed the database**
Before running rake db:seed, be sure to double check ONLY use the .create method with bcrypt or else it will not accept password and only accept password_digest.
Double check that you have all attributes in the correct order and are set to local variables according to your associations.

## **14. Create Routes and Actions**
Create route Create controller actions Create view starting with index, new, show, edit, update, destroy Update validations in model Repeat this pattern until all crud functions are working

I hope this helps you get started building a rails application. Happy coding!!!








