---
layout: post
title:      "'Night Of Mystery': A Javascript/Rails Project"
date:       2020-07-02 17:30:26 +0000
permalink:  night_of_mystery_a_javascript_rails_project
---


  It's been a rough few months dealing with the COVID situation for everyone. I'm no exception, and things have certainly slowed down a bit, so I hope everyone is doing okay! However, though it's taken a while, I have really enjoyed working on this project.

  Night Of Mystery is a text-based thriller adventure game with some mad-lib components, built using an HTML/CSS/Javascript frontend powered by a Rails API backend. The backend is pretty simple, having only three database tables - Scenario, Response, and User. A scenario has some text, and has many responses. A response also has some text, belongs to a scenario, and also has an additional integer for the "result". I'll come back to this a bit later. A user has only their name. Scenarios and responses are created through prewritten seed data, and are not created by the user.

  On the frontend, the app first renders a welcome screen when first loading the page. This allows a user to give their user name, then give several keywords that will appear in the game, such as the names of key characters. At the bottom is a list of past users who have played. This list was created using a "GET" fetch request and operating on the resulting JSON data to create an unordered list. Finally, there is a button to start the game.

  On clicking this button, three things happen:

    1. A new User is created using the given user name. This is accomplished by a "POST" fetch request.

    2. Another "GET" request is made to the server, and the dom is updated to show the opening scenario of the story, in which the main character is sitting at home and experiences an unexpected event. Below the scenario text, an ordered list shows each of the responses the player can choose. The number of options vary between scenarios, but for the first one, there are four.

    3. The key words given by the user create new Javascript objects corresponding to their role in the story. For example, the first key word is for a male first name. This is used to create a "Hero" object. This name will appear throught the story anywhere the main hero's name appears. As of now, this object only has a name, but it could be further expanded to have other data and behaviors, such as a hair color or catchphrase.

  At this point, the user can click on the response they wish to choose for the situation. Each response (which are "li" elements) has an event listener which will trigger the DOM to update with a new scenario. This is where the "result" integer on the backend comes in. When the "GET" request is made for the next scenario, the "result" integer indicates the scenario that should be rendered in response.
	
	The story is still incomplete, and ends with a variety of "to be continued..." scenarios which lead back to the beginning. I didn't want to get too caught up in things unrelated to the coding aspect, so I have left it this way for now. However, it is my hope that I can someday expand it to be more intricate and have many different endings. This combined with the "mad-lib" element will provide a huge variety of outcomes for people to enjoy.
	
	This project took me a lot longer than I expected originally. However, I am ultimately happy with the end result. As always, the best thing is to take your time to make things the best they can be. There are always huge roadblocks along the way, but if you keep at it, you will end up with a project you can be proud of!
