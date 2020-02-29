---
templateKey: blog-post
title: The Alexa skill made it
date: 2020-02-29T03:28:54.905Z
description: >-
  It's currently 2:30PM on Feb 29, so thank goodness for the leap day this year.
  Just barely managed to sneak a project in before the end of the month.
featuredpost: false
featuredimage: /img/alexa.png
tags:
  - alexa
  - skill
  - amazon
  - aws
  - lambda
---
This week was a bit of a push to get things across the line, but thank goodness there was a leap day this year! I managed to get the skill built before the end of the month, and it has been submitted to Amazon for review. There are only about 10 words in the database so far, because it turns out you can't just upload a CSV directly to DynamoDB, but other than that, things are working smoothly! Let me explain in a bit more detail what I put together this week

# The concept

The idea behind the skill is to have Alexa tell you a new German word every day. She would pull these words from a database of direct German-English translation, so she can only be as accurate as the sources that I found the words from, but still, most of the translations should be fairly good. Alexa will tell you a word each day, that is different from the previous days, up until she runs out of words in the database, at which point she will loop back. You can also ask her for a random word, and she will pick one out of the database.

# Changes in design

I found out early in the week that I wouldn't be able to make a flash briefing as I had hoped, because for some reason flash briefings don't support SSML tags... That meant I couldn't get Alexa to use her German accent when giving the flash briefing, which is rather unfortunate. I did briefly look into using Amzon Polly or Dialogflow to solve the problem, but sadly it was not meant to be. I'll potentially leave that for a future development!

# The database

DynamoDB provides a place for all the words to be stored. Each record contains the german and english versions of the word, as well as two booleans as to whether it has been used previously, and whether it is the word of the day. By setting up a scheduled lambda to change the word of the day, Alexa will be able to provide a different response every 24 hours. By keeping track of the words that have been used, back to back repetition won't be a problem as it could be if the words are simply randomised each day. Finally, when all words in the list have been used, the lambda will reset the used word booleans, and begin again. 

The data for the database currently only stands at 10 words, but I will continue to add more over time, so that there is greater variation in what you can learn.

# The end result

The aim of the project was to have something that could be completed in about a week, in order to have it completed by the end of Feb. Currently, it is still Feb 29, and the skill has been submitted for review, so I count that as completed! The skill may only provide a small degree of functionality, but the process of building it has taught me quite a lot. I am glad I managed to finish it off, I feel quite pleased with myself. Now we wait and see if Amazon approves of it, and hopefully next week's post will include a link to the live version of the skill!
