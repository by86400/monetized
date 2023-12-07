---
title: Why Are We Here?
date: 2023-12-06
description: A brief introduction and summary of the 11ty project so far.
tags:
  - hello
  - eleventy
  - 11ty
  - ghost
---

If, for some strange reason, you happened to have found this URL before a couple weeks ago, you would notice that there has been a sort of major change in format. Nobody is expecting you to have noticed this, but I originally set this blog up on Ghost, and now it is using eleventy.

## What's the deal with ghost?

Ghost is a blog, a newsletter, and a subscription manager, so theoretically you could have signed up and decided you were going to pay me for my thoughts. Honestly, I thought the subscription thing would end up being for something a little more fun, where I would mail you a trinket or something for your troubles, or maybe even set up a Fediverse thingy using takahe. None of that happened in the several months that the Ghost version of this site was up, so it seemed a little like overkill.

## What I learned from setting up Ghost

I am always trying to get the tools I own to do things that they're not exactly built for, and the Ghost set up was no different.  I had thought that using a cloud service like DigitalOcean would be a good way for someone with some web skills to set up multiple (toy) ghost blogs on a cheap droplet, and thereby save some money over paying for an actual Ghost subscription. 

The idea was always to try to cram more than one thing onto the droplet, because I didn't really plan to earnestly make any money off this, but that ended up being where the whole thing fell apart.  The first thing I tried was getting a droplet that came with Plesk on it. I am nominally capable of setting up my own apache config files, and I could probably muddle my way through nginx if I had to, but I'm not going to claim some ideological purity to editing text files over having a GUI that handles all of that nonsense for you.  

The trouble here was that I forgot about the whole "Oracle bought MySQL and now the nerds are using MariaDB because fuck those guys" thing.  Somehow, the developers of Ghost didn't get the memo, or were just fancy enough that they felt insulted that they might have to use a version of MySQL with the serial numbers filed off, and Ghost is configured out of the box to only work with the name-brand database.  Again, to the best of my knowledge, the two databases are very similar, so maybe I could have pulled off the programming equivalent of immunosuppressants and gotten Ghost to accept its new set of internal organs, but that was going to be a project all on its own, and I wanted to be focusing on the actual blogging and to some extent, the configuration of a Ghost blog. Given the size of obstacle that can trip me up (read to the end) this seemed like a bad choice and I deleted the droplet (as they call them) and tried again with a droplet specifically configured for Ghost.  

Even with all of that behind me, I still made myself go through a little command-line dance because I wanted to set up the SSL without using DigitalOcean for my DNS.  I eventually figured out how to get a free cert with CLI Let's Encrypt! but the specifics of that are in the history file of the instance I destroyed, so I'll just have to look it up again if it ever comes up.

Now that I had a blog, and I managed to pick a theme and customize it a little, I could write something about all the interesting things I had just done, right? Well, as it turns out, the theme I picked wanted a header image to go with every post to make it look all nice and professional, and I could not, for the life of me, decide what to do about that? That, as it turned out, was enough to scuttle my desire to make content, for the forseeable future.

After several weeks, I decided to try again and create raised.by86400.today to talk a little bit about being a maybe neurodivergent dad rasing probably-and-or-definitely neurodivergent kids.  It was at that point that I discovered that the installer for Ghost on the command line was so fancy that it did things like check the available memory before letting you move ahead, and the cheap virtual server I was renting from DigitalOcean did not have enough available memory to let me move forward.

Now, again, I could have tried shutting down the original blog, installing the new one, and seeing if they could both run at the same time. Clearly, they were not going to be getting a lot of traffic, so maybe it would be fine.  Maybe I could even trick the installer or tell it to specifically ignore that requirement, but see above about trying to clear the way for actually writing stuff down. 

So that was effectively the end of my use of Ghost for something that I didn't really expect to make money one.  The biggest takeaway I had from that experience was that __if you are going to set up a Ghost blog to run a newsletter, and you are actually doing okay with paid subscriptions, you're better off just stomaching the difference between self-hosting and using their official hosting platform.__  The lowest level of hosting on by Ghost covers up to 500 subscribers, and is defintely worth the difference.  From there, I assume that if you have over 500 subscribers, you have the money to keep upgrading and the convenience of not having to jump ship to self-host will win the day.

At the very least, you won't be contributing to Substack's bottom line, and that's got to be a good thing, right? Now, I didn't mean to leave this on a cliffhanger, but I'll have to cover the eleventy switch another time, I've got some lunches to pack.