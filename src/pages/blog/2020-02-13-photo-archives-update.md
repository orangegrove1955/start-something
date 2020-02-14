---
templateKey: blog-post
title: Photo archives update
date: 2020-02-13T22:01:21.441Z
description: >-
  Progress is underway on the photo archives, though it might not be enough to
  be on track for the end of the month
featuredpost: false
featuredimage: /img/archives.png
tags:
  - server
  - hosting
  - backend
  - progress update
  - Express
  - Angular
---
We're halfway through February now, and things are coming along. There has been some progress on the project, in terms of building a backend and a frontend. Primarily, work has been focused on the API, rather than the frontend implementation. There's still a lot of work to do, but here's where things are at for now

# Front end

The front end is being built with Angular, but for the most part, there has been very little progress this week. A simple Netlify page, linked to a subdomain, gives the view shown in the leading picture of this article. This is just a simple, single page component built to have a placeholder for when the backend is more functional. So, essentially, the front end progress is linking a subdomain to Netlify. 

# Back end

Now, this is where some serious work has gone in. Not only have I had to link the API subdomain, I've had to set up a physical server to host it, and create an Express server to run on that to actually distribute the files.

## Physical server

I had an old media computer lying around at home, not doing much, so I figured it would be the perfect opportunity to learn how to host your own server at home, rather than paying a monthly fee to use AWS or GCP. 

In terms of setup, the first thing to do was remove the old Windows XP software, in exchange for the latest version of Ubuntu server. After some SSH and Node setup, the server was good to go to prove basic functionality of the API locally. 

## Express.js

Now the system was ready to distribute files, I created a small Express server to send the files on my local network. I was successfully able to receive an image, so I scaled up to a fair few more images. 

I used a package called "serve-index" to create some simple routing, and I was able to see the folder structures of the API's files. Obviously, this is not functionality I want to expose to the world, so there will need to be some updates over the next week, in order to have the API in a more correct format, but I was still pleased with the progress.

## Dynamic DNS

The final aspect of getting this API set up was to have it available across the world, so that people who want to see the photos can do so from anywhere. Obviously this means I need to connect my server's IP address to the subdomain; unfortunately, I found out that my ISP doesn't provide static IPs, so I needed to find a workaround.

I came across the concept of a Dynamic DNS, which updates your dynamic IP address whenever it changes. I decided this would make an interesting topic for a Medium article (oh, btw, yes, [I write there](https://medium.com/@mt_williams) as well), so that will be another small project I work on this month or next. 

I managed to use Cloudflare, along with a cron-based script to update the IP address of my server, so that the API would be publicly available, and voila, the skeleton of the API is complete.

# What's next?

Now that the physical server is set up and working, it's time to actually get the backend under control and finalised. The week ahead will be a time for figuring out GraphQL, creating a database (probably MongoDB, because it plays nicely with Node) and then getting the API structure in place.

By finishing off the API this week, it will give me plenty of time later to finish off the front end (thank goodness for the leap year!), and have this thing looking nice by the end of February.
