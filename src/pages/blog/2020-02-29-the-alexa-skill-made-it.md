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

The idea behind the skill is 

# Changes in design

I found out early in the week that I wouldn't be able to make a flash briefing as I had hoped, because for some reason flash briefings don't support SSML tags... That meant I couldn't get Alexa to use her German accent when giving the flash briefing, which is rather unfortunate. I did briefly look into using Amzon Polly or Dialogflow to solve the problem, but sadly it was not meant to be. I'll potentially leave that for a future development!
