---
layout: post
title: "Dev Academy - Week 3 &amp; 4: A New Era"
date: 2014-06-10 23:43:29 +1200
comments: true
categories: 
---

It's been a hectic few weeks since my last post. We've been hurtling through databases, team projects, web applications and more. I've been busy putting off writing this post for two weeks, but here I am. Let's do it.

The start of week 3 has become a bit hazy now, so bear with me as I recollect. We spent the first few days dedicated to learning about databases and SQL (a language for talking to databases). 

We started out by making applications that communicated with the database via raw SQL queries (not fun), then moved into making our own [ORM](http://en.wikipedia.org/wiki/Object-relational_mapping) (Object-relational Mapper, a way to work with databases at a more abstract level, with objects in code). This was definitely a cool exercise, as most people will never write an ORM (because there's no real need to write your own). We then moved from there to using the most popular ORM for Ruby, ActiveRecord. ActiveRecord is much easier and nicer to use than the ORMs we made ourselves, but it's definitely worthwhile to know how it works. Dev Academy often takes this approach, teaching you the internals out to flesh out your understanding. (I had made an ORM previously, called [ButterDB](https://github.com/Widdershin/butterdb). It lets you use Google Spreadsheets as a database, and was originally a joke project.)

We start off every week on Monday morning with a retrospective of the previous week. As a cohort, we go over how we felt about the previous week. What went well, what didn't go so well, and what we'd like to change going forward. We also cover the things we wanted to change from the previous week's retrospective, and make sure that they are happening. There have been changes like improvements to the coding challenges, adjustments of coach times and solo days. I think this is a super valuable process, and  I've found it novel to reflect in a group like that. It helps to ensure a feeling of participation and change.


On Thursday and Friday we had our second team project. We were told to build something we wanted to build, with some deadlines. We had a feature freeze (no adding features after that) at 3.30pm on Friday and a code freeze at 4.30pm. We were to give a presentation and demo at 5pm.

Our team (Richard, Hannah, Genevieve and myself) decided to build a text based adventure game (think [Zork](http://en.wikipedia.org/wiki/Zork)). We built the (very creatively named) [text-based-adventure](https://github.com/Widdershin/text-based-adventure) game by Friday afternoon. It's fully featured (including fighting, looting and death), but sparse on content. I think 5 rooms made it into the demo we had.

Here's what it looks like to play.

> λ ruby game.rb   
> Welcome to generic text adventure!  
> You are in the throne room. There is gold and ruby everywhere. You can see a corridor lined with spiderwebs to the west and there is a small water closet to the east. Make your move!  
> There are 50 gems in this room.  
> Health: 100, Gems: 0  
> \> loot  
> Health: 100, Gems: 50  
> \> go west  
> Health: 100, Gems: 50  
> \> look  
> Welcome and close the door. Hiding behind the cistern (what are you doing down there) is a box with silver chains in it. There is a small window to the north that leads out onto a firest rife with. The only other option is down the cistern but it appears to be blocked. Where would you like to go?  
> There are 3 gems in this room.  
> Health: 100, Gems: 50  
> \> go north  
> Health: 100, Gems: 50  
> \> look  
> You are in a forest. You hear a flapping of scaly wings. There are gold goblets and precious jewels in potholes in the smouldered ground. Take some and run if you dare, or face your doom.  
> There are 100 gems in this room.  
> Health: 100, Gems: 50  
> \> loot  
> Health: 100, Gems: 150  

(I think we forgot to include enemies in the demo, but they're in there somewhere)

I had a really great time working on this game. Our team worked really well together; we communicated and organized effectively. We had a big focus on automated testing, and I think that really helped on the tech side. 

Friday was the final day of Phase 1 of Dev Academy. The course is three phases, with the first covering general development, the second covering web development, and the third being project focused.

I'm still astounded at the immense growth and learning that my fellow cohort members have shown. The problems we're tackling now are so much harder than when we began, and they keep rising to the task. I learnt a lot of what I know on my own, and it's definitely much slower. I think Dev Academy's environment lends itself very well to rapid learning. You have the right mix of enthusiasm, passionate people and resources.

We celebrated the end of the phase with a sweet party, of course. It was cool to hang out with some of the other cohort members and relax, play some games on the project, and have some free food and drinks. It was really cool of the course (via course wizard/admin Rohan) to so generously provide food and booze.

Week 4 began and we kicked off phase 2 (the web development phase of Dev Academy). I know a lot of my fellow students were eager to move away from making command line applications, into something that more people can use and see. 

We spent the first few days learning the basics of web development, and making progressively more intricate sites. I found a couple particularly fun. One was on Tuesday, when we were tasked with creating a basic clone of Craigslist. It was a simple listing site, but it was cool piecing it together in a well designed way, and helping the other cohort members build one of their first proper websites.

The other particularly enjoyable challenge was to build a simple login system. I was pairing with Taylor, my friend and flatmate, and he and I decided to take a different tack. We ended up building an authentication system that would let you log in, and then send a link to your friends so they would be logged in as you. Not a good idea, but fun to make and humorous (if you're a programmer I suppose).

On Thursday and Friday we built our third team project. We were tasked with either building a functional clone of Twitter or a Flashcards web app. All three of the teams opted to build the Twitter clone.

We built another creatively named app, Twytter.
![Twytter](http://i.imgur.com/iCC8uPX.png)

Some minor styling issues aside, I was really happy with what we delivered at 5pm. All of the features (like tweeting, retweeting, following, the feed, etc) were functional and complete. We also managed to get in the bonus customer feature, favorite tweets. We were given that feature request late on Friday afternoon, to see how we handled changing requirements. 

I worked with Richard, Kendall and Tim. All of the teams were employing a method of building software called [Agile](http://en.wikipedia.org/wiki/Agile_software_development). Agile is a way of running software teams that helps rapid, flexible development. It's well used in the industry, and was a great way of running our project. It has nice ways of tracking progress (like [Kanban Boards](http://en.wikipedia.org/wiki/Kanban_board) and Sprints). I don't really want to go into detail here, so I definitely suggest readers do some reading if they're interested.

We definitely took a few lessons away from this team project. For one, we opted to deal with all of our presentation and styling at the end, rather than alongside feature building. This meant that it was more difficult than it needed to be to piece everything together.

We also made the mistake of not defining a clear scope of what we wanted to build, and by when. We were provided with a bunch of user stories (a way of phrasing a project feature or requirement, like 'As a user I can post a tweet.') We built all of those stories by the deadline, but as Richard pointed out, we could have dropped a feature in exchange for much more polish elsewhere.

I always enjoy the team exercises at Dev Academy. It's nice to work together with a larger group of people to make something that is hopefully more than the sum of its parts. I have been focusing on taking less of a leadership role during these projects, as I have a bit of a tendency to take that up if nobody seems too inclined. I want to let others take the lead more, and see how that goes.

On Thursday night we had another Dev Academy tech talk. Free pizza, beer and good company included, the entire evening was a treat. This time, Kirk Jackson (Xero's Security Officer) gave a talk about encryption and security, entitled "Tales from Beyond the Crypto". Patrick was an excellent speaker, and it was a well timed topic, as we had just started building authentication for our projects. A lot of programmers never learn about crypto or security best practices, so I think it's awesome the the Dev Academy students got a good exposure to it. I know it definitely inspired some of my fellow students to think more seriously about getting into security.

Well, that's about all I can muster the effort to say at this point. Hopefully I can crack the next post out next weekend, but definitely soon. As always, any feedback appreciated.
