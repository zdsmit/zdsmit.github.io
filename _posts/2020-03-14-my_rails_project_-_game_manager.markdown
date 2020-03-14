---
layout: post
title:      "My Rails Project - Game Manager"
date:       2020-03-14 15:25:47 +0000
permalink:  my_rails_project_-_game_manager
---

As another module comes to an end, the time has come to reflect on my third portfolio project. This one was quite a challenge for me, but overall, I believe I found it more approachable than my Sinatra project. I spent a lot of time on this, both in planning and development, and I learned a lot of things along the way that I'd like to talk about.

The first thing I would like to put emphasis on is planning. When you are told to take your time to plan everything out before you start a project, that's no joke. I took a full day to sketch out my models, their attributes, and their relationships before I even started writing code. And even then, once I started, I found myself adjusting my plan on the go. 

My project was Game Manager, an app for creating, buying, and selling video games. As one of my favorite hobbies, I figured this would be a good idea to work from. By the time everything was said and done, I had my app running on four models with corresponding database tables: Game, User, Genre, and Transaction.

A game belongs to a genre, belongs to a developer (I'll come back to that), has many transactions, and has many users through transactions. It has a title, description, price, and has a genre_id, developer_id, and user_id.

A user has many transactions and has many games through transactions. In the database, they have a name, password_digest through bcrypt, an amount of money, and a boolean box to determine whether they are a game developer or not. I took this particular idea from the Rails Amusement Park lab leading up to the project. They also have a uid, email, and image to use with OAuth login.

Transaction is the join table between the two. It belongs to a game and belongs to a user, and has a user_id and game_id. The model also contains the logic used to buy a game. It has a method called 'purchase', which returns an error message if the desired game's price exceeds the user's money. If not, it subtracts the price of the game from the user's funds, and adds the same amount to the game developer's funds.

The method I used to let a game know who its developer is was a simple one. 

  1. In the game model, I included the following code: `belongs_to :developer, :class_name => "User", :foreign_key => "user_id"`. This told the model to look for a particular User instance and save it as an attribute called :developer.
  2. I made the page to create a new game only accessible to Users with "true" for the developer boolean.
  3. I included a line in the GamesController#create method to save the current user as the game's developer.

I had no idea before this that it was possible to give a model two different relationships with another model in this way. Overall, I think that was the single biggest hurdle I crossed, despite how simple the solution turned out to be.

I learned a lot from this project, maybe even more than the previous ones. But best of all, this has given me a lot of motivation to always be reaching out to find greater tools for the task at hand. I hope my future projects go even better.
