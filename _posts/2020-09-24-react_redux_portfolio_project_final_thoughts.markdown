---
layout: post
title:      "React/Redux Portfolio Project: Final Thoughts"
date:       2020-09-24 17:09:59 +0000
permalink:  react_redux_portfolio_project_final_thoughts
---


Well, everyone, here we are at last, the final project. Working on this has been a lot of fun, but it has definitely not been without its challenges. Check out my repository here! [https://github.com/zdsmit/Bandroom-frontend](http://)

I named my app for this project Bandroom. It serves as an app where owners of music stores can upload information about their stores, including its location and inventory of instuments. As per the project requirements, it was made with a React/Redux frontend, tied to a Rails API on the backend. For my database setup, I used PostgreSQL rather than the SQLite that was used for most of the curriculum. Even if you don't expect your project to see much future activity, I would recommend at least familiarizing yourself with how to set up Postgres. It is required for launching with many services like Heroku, so it helps to know! You can find a good page for getting setup started at https://www.tutorialspoint.com/postgresql/postgresql_environment.htm.

Most of the frontend setup for this project was fairly standard and didn't take too much effort to figure out. What gave me some difficulty was incorporating the Thunk middleware for handling server requests. This is something that is covered in the Learn curriculum, but is still tricky to implement. What I ultimately did was this: I had an 'actions' folder under 'src' in my file tree. In this folder were individual files for each fetch action. For example, since I had two resources in my database, 'music stores' and 'instruments', I would name my files 'GetMusicStores', 'AddMusicStores', 'GetInstruments', etc. Each one has a function that takes the dispatch from the appropriate input form and uses it to fill in the content of the fetch request, which you can see in the repository linked above.

From there, all you need to do is import it in the appropriate component (in my case, it was the respective containers for MusicStores and Instruments) and pass it as the second argument in the 'connect' call (where 'mapDispatchToProps' would usually go). Then you can simply pass it down as a prop to the input form!

When I had everything functioning the way I wanted, I used an external theme to provide some good CSS styling. I mostly followed the steps laid out in Turbo 360's tutorial for using CSS in React. You can find the videos here:
  -Part 1: https://www.youtube.com/watch?v=FuMwBBamF8s
	-Part 2: https://www.youtube.com/watch?v=L_oe9A1Zk9Y&t=510s
	
I had a lot of fun working on this project, and I definitely feel like I have massively expanded my understanding of React and Redux as a result! As I worked on this, I leaned back heavily on the preceding Learn lessons for support when I didn't understand a concept. Definitely don't be afraid to go back and review what you've learned, or to look at the code you wrote for previous labs to help you. Keep up the good work, and soon you'll be well on your way to a great project!
