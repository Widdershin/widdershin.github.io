---
layout: post
title: "Dev Academy - Week 5 through 8: Subtitle undefined"
date: 2014-07-04 23:45:00 +1200
comments: true
categories: 
---

There was a certain logistical problem I never really considered when I decided I was going to write weekly Dev Academy blog posts. As Dev Academy goes on, the amount of things going on increases. This means that there is not only more to write about, but also less time to write about it. To maybe combat that issue, I've decided to try a little something different this time. Forget chronology, we're gonna check out some highlights. Less is more.

For the record, I'm sitting on my couch writing this on the Sunday night at the end of Week 7 of Dev Academy. As of tomorrow, two weeks remain until graduation. Feels a bit mad.

**Learning comes first**, both at Dev Academy and in this post. This is a maxim that has been drilled into us at Dev Academy. If the curriculum isn't working for you, throw it out. If there's something better you could be doing for your learning, do that instead.

I love this philosophy. I've found I work best in an environment where I can create my own structure. As we've moved into Phase 3 (the phase where we're treated more as developers, and less as students) we have more of an increased freedom to choose what we do. The first two phases of the course highly emphasized pairing (Pair Programming, two developers working together on the same computer on the same problem). Phase three is now solo optional all the time. I find that independent programming and then pairing on hard problems is a better way to work anyway.

<!--more-->

I appreciate the ability to direct my learning a bit more. I've been hard at work rewriting my website [NZ Skate Search](http://www.nzskatesearch.com/) in Ruby on Rails (a web framework that is the emphasis of the Ruby stream at Dev Academy). I originally wrote it in Python with Flask, but it was a bit of a hack job and had no tests. I've been working on writing the new version in the best way I can. I'm using heavy test driven development and emphasizing best practice. It's nice to be able to take this time to work on my craftsmanship.

That project is by no means strictly within the scope of the curriculum, but since I'm hitting all of my learning objectives, that's what counts. In the biggest team project yet (whole cohort), we were assigned tasks and roles tailored entirely around our learning objectives.

Sometimes the set work clashes with my ability to best learn. The curriculum licensed from Dev Bootcamp San Francisco isn't as up to scratch as was expected. This is not really a problem, as we (as a school) can steer ourselves. Samson, the teacher for the Ruby stream, consults us every morning as to what lectures or breakout sessions we would like today (if any). These are mostly optional, so we have effectively been left to our own devices.

I have to say that this has enabled some of the best learning I've seen so far this course. In the last week, Kendall and Andrew created an [open source template](https://github.com/kendallflutey/rspec-controller-testing) for testing website controllers in Ruby. Genevieve and Richard have been working on a website to help organize code tips and breakout sesssions. Everyone is up to different stuff, and I think that's really cool.

**Working 75+ hours a week is rough**, no matter who you are. This is on the lesser side of some of what my fellow cohorts members have been hitting, so credit to them.

I have been pretty tired for the last 3 weeks. Working so much every week gets to you. It makes it harder to get out of bed in the morning, and then to pay attention when I get to course. I've been trying to eat well (-ish) and get enough sleep, but 7.5 hours a night seems to be draining me.

I find Yoga to be an excellent way to unwind. We've had it twice a week since the start of the course. It's optional, and I think only around 5 of us out of 13 still partake. I often find I have quite a sore back, and Yoga really helps with that. I appreciate that it's a nice midpoint between meditation and exercise. It helps me to relax both my body and my mind (as cheesy as that might sound). I definitely want to keep up with it after EDA.

I also try and make some time for mindfulness. Although the Engineering Empathy curriculum finished at the end of Phase 2, Joshua, a teacher, still offers sessions for those who want to partake. Part of these sessions is mindfulness. Mindfulness exercises are simple. Find a comfortable place to sit, where you can find a balance between relaxation and alertness. Begin paying exclusive attention to your breath. Try to notice when your attention slips away, and gently refocus it on your breath.

The point of this exercise is simple. Improve your attention by exercising it. Improve your awareness of your attention by exercising that.

We do this for several minutes. I tend to shut my eyes. You can also try counting to see how long you can go without distraction. This is also a really good way to relax, and calm your mind.

*writing ceases for a week*

**Suddenly, it's Friday night, 5 days later.** I've been meaning to finish this post since Sunday, but have only just found the time. It's a week until the end of Dev Academy. If it feels like time has flown through these blog posts, then I feel that's only indicative of real life.

We've just started our final team projects yesterday. Richard, Taylor, Andrew and I are working on Skirmish. It's a multiplayer turn based war game (like Risk) played on Google Maps. Final projects are the most intense part of Dev Academy. We coded for around 11 hours today. Richard and Andrew were still going when I left. This is easily the largest and most complex application I've been involved in building.

We spent around 4 hours planning out our initial vision, user stories and architecture. Taylor (my flatmate and good friend) took the role of Architecture/Tech Lead. Since we want Skirmish to be multiplayer, we have to design the architecture with that in mind from the get go. 

![Imgur](http://i.imgur.com/GhvdbPk.jpg)
*Skirmish Architecture Planning*

Richard pitched the idea for Skirmish, and took on the role of project lead. He lead us in developing user stories for requirements. We decided what we wanted to include for the MVP (minimum viable product) and we ended up with a fairly large project still. We want a functioning game with multiplayer, where players can capture other cities and fight. Ideally an MVP is as simple as possible, but even our smallest vision has a lot of moving pieces.

We have until next Friday morning to do as much as we can on Skirmish. As always, learning comes first. It doesn't really matter if the product that comes out the other side is perfect, as long as you learned lots and had a good time. That said, we're working hard. Every member of our team will be working every day until it's over. Lots and lots of coding.

You can check out the code for Skirmish on [Github](http://github.com/rantgames).

I am barely awake at this point, so I figure I should just post this (good idea, right?). There is so much that could be written about that I have missed or forgotten. The last few weeks have been unique, to say the least. It's hard to express in English, so permit some Ruby code instead.

```
def how_have_i_been?
  week_adjectives = [
    'tiring',
    'interesting',
    'learning-y(?)',
    'hectic',
    'hard',
    'inspiring',
    'slightly crazy',
    'intense',
    'awesome'
  ]

  *all_but_last, last = week_adjectives

  all_the_adjectives = "#{all_but_last.join ', '} and #{last}."

  puts "The last couple of weeks have been #{all_the_adjectives}"
end

how_have_i_been?
```
Outputs: "The last couple of weeks have been tiring, interesting, learning-y(?), hectic, hard, inspiring, slightly crazy, intense and awesome."

*Yes Ben, I violated the Single Responsibility Principle for the sake of readability. Deal with it.*