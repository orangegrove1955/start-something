---
templateKey: blog-post
title: The alternate project verdict
date: 2020-02-23T20:37:41.444Z
description: >-
  As mentioned last week, it's time to find a new project for the rest of
  February. It needs to be small enough to be completed in a week, but still
  public and useful. I think I've got just the thing...
featuredpost: false
featuredimage: /img/alexa.png
tags:
  - alexa
  - amazon
  - skill
  - voice
  - vui
---
It's been a long weekend of thinking, trying to determine what sorts of projects might be possible to smash out in a week. I've tossed and turned between websites, apps, something physical.... I do know that the best projects are always ones that solve an issue, so I decided to make something to solve an issue I've personally been having.

I started learning German recently, and I've been searching for something that will give me a new German word each day. I want to be able to hear it though, not just read it in an email, or have to download an entire app that needs to be opened to find the word.

So that got me thinking, how can I create something that speaks to me, and tells me a new word each morning? I have developed a few Alexa skills before, and I figure Alexa will be perfect for this. She speaks out loud, and I know there is SSML that should hopefully allow German pronunciation to be implemented when speaking the German version of the word.

I know that Alexa skills aren't too complex to develop, though I haven't done one on quite this scale yet... My plan is to find a large German-English data set, store it in DynamoDB, and then use a Lambda function to pick a word from the data set each day. Alexa will then have a standard format that she will read these out in. Each day, you'll be able to ask her for the word, and learn something new to start the day.

Potentially, I might even try to turn it into a flash briefing, and have Alexa tell you the word each morning without needing to be prompted. If all goes well, who knows, maybe I'll even expand out and make more skills in other languages! 

To start though, it's going to be German, one word per day, and fully automated, so I don't have to pick a word each day. Check back on Friday to see how the project turns out.
