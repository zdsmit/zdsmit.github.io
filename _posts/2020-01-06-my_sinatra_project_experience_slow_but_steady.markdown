---
layout: post
title:      "My Sinatra Project Experience: Slow But Steady"
date:       2020-01-06 20:55:21 +0000
permalink:  my_sinatra_project_experience_slow_but_steady
---

Right before Christmas is hardly the ideal time to begin working on a new portfolio project, but that was the hand I was dealt with my Sinatra project, and so I got to work. It was difficult working on it during the craziness of the holidays, but from doing so I gained one valuable piece of advice: take it at your own pace! Many times I only managed to work for an hour or so a day. Others, I could sit down and work all day. But once I accepted that some days would move faster than others, I gained a lot more peace of mind in my work.

But rather than focus on broad advice, let me elaborate on what I did. My Sinatra app has the simple and self-explanatory title of "Sinatra Birdwatching". The idea behind the app was that it should allow users to do the following:

1. Create an account with username and password
2. Report bird sightings in their area
3. View an index of all bird sightings from all users
4. Edit and delete their own sightings
5. Log out

The first step to do this was to establish the database tables and the relationships of the corresponding models. I created three tables:

* Users, containing a username and password
* Birds, containing a species
* Sightings, a join table containing a User id, Bird id, time and place

As for the model relationships:

* A User has many Sightings, and has many Birds through Sightings
* A Bird has many Sightings and has many Users through Sightings
* A Sighting belongs to a User and belongs to a Bird

After this, I began building the controllers and views. I followed the same structure that was seen in the Learn labs leading up to the project, having a different controller file for each of my models, and an Application Controller file they all inherit from, which contains essential components such as `session_secret:`. This parent file also contained the helper methods `logged_in?` and `current_user`, which I borrowed from the Fwitter lesson. 

Throughout the rest of the process of writing my controller routes and views, I found myself relying heavily upon the previous lessons, reviewing the work I did there to guide me in writing everything correctly here. However, I hit one major snag when creating the main Sighting index page. I wanted each Sighting to display the name of the user who reported it with its other information. But no matter what I tried, it wouldn't work, coming up blank at best and at worst breaking the page completely. This problem had me held up for *days* before I discovered it was a simple extra space on the index page("user name" instead of "username"). The moral of this story is when in doubt, take a break! Nearly every time such an issue appeared, I solved it by walking away and coming back later when I had a fresh mind.

Overall, it's taken me three weeks to get my project working, but I'm happy with the result. I even have room to add extra functions, and managed to add a (small) amount of CSS styling to it. So if you're getting stressed about this project, take my advice: don't! Work on it as long as you can, and take breaks when you need it, and you'll have yours up and running in no time.
