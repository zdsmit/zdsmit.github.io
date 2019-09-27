---
layout: post
title:      "CLI Data Gem Project: Before and After"
date:       2019-09-27 02:33:58 +0000
permalink:  cli_data_gem_project_before_and_after
---


Hi there, everyone! It's been a long road, but at long last I have arrived at my first portfolio project, the CLI Data Gem Project! It's been a struggle in recent months to keep up with the coursework consistently due to moving. But I'm happy to say I'm still on schedule (for now, at least), and things have settled down now, so time to get to work! Anyway, I want to take advantage of this blog post to detail the process I will be going through in order to construct my project.

  It's a little unusual, but I'm going to do this blog post in two parts. As of this writing, I am preparing to start my project. I will talk a little bit about my plans for the project before getting started, and later give more details once the project is finished. I hope this will give more insight into how my thinking process changes, and reveal things I can adjust and improve in my workflow.

**-Before project-**

  For the project, I'm going to be utilizing data from one of my favorite websites, TV Tropes (tvtropes.org)! For those not familiar, TV Tropes is a wiki that classifies and codifies tropes in fiction. For example, you can find an entire index of different types of characters or settings you might see in TV shows, books, movies, etc. Each individual trope has a page containing a picture and quote that represent it, as well as info on the trope and examples of the trope in different works.

  More specifically, I will scrape data from the index of different Plot tropes. My gem will contain three classes: A Scraper class, a Trope class, and a user interface class. The function will be as follows:

 -1. The Scraper class will take the url of the plot trope index and return each individual trope entry, along with the links to their individual pages
 -2. The Scraper class will then scrape a name, trope description, and page quote from each individual trope's page
 -3. The Scraper class will use this information to instantiate new instances of the Trope class, each containing a name, a description, and a page quote
 -4. The user interface will provide a list of tropes to the user, then will give additional information about a specific trope upon request

  This is just a fun project on a topic I really enjoy. It could be useful for people studying literature/media or writing stories of their own as a quick way to access many different common plots. Due to the structure of the website, it could also be easily retooled to work for other indexes too. I'm excited to get started! I will update this with additional information once I finish the project.

**-After project-**

 So after completing the project, I definitely have some new insights. The first part of the project was creating the scraper class and finding the appropriate CSS selectors to use. This was a trial and error process, but overall was exactly as learned in the labs and didn't take that much time. However, I hit a huge snag that ended up extending my time spent on the project by days. The one thing I can't emphasize enough is *separation of concerns*. If you're going through the course now, you've probably heard the term. But hoo boy, is it important here.

 To clarify, when I first built my scraper class, it had two methods: one to pull a list of tropes from a large list, and another to return information about each individual one. But the first method had a big problem – it wasn't just scraping data, it was using it to output a list of items. Remember that the idea of separation of concerns is to have each method, object, etc. performing one task. The role of the scraper class is to scrape data, not generate lists for a user. That role should be reserved for a CLI class. It was a trap I easily fell into, and I'm sure it could happen in other projects too, so be careful!

 If I learned anything else, it was the importance of patience. This project took me much longer than I expected. However, I was always making progress, and the pace I moved at allowed me to fully grasp what I was doing along the way. The course has said from the beginning not to worry about errors, as working through them is the nature of coding. I'm happy to say that this project finally made me realize how true that is! But at the end, the satisfaction of finally having a working app was totally worth it. I can't wait to learn more!
