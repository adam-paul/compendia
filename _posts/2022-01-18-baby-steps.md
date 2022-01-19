---
layout: post
title:  "Baby steps"
date:   2022-01-18 18:38:34 -0800
categories: documentation
---

I am trying to rediscover some growth mindset enthusiasm and imagine myself being able to learn
(and re-learn) things like SQL, Apache, and the other presumably necessary skill sets I'll have
to use for this project. 

The real question though is where the hell do I start? This is the "documentation" of the build,
so this isn't the actual place where stats or visualizations or whatever is being offered
would be accessed. So where is? I guess I have to get a domain name? 

But then what am I building first? A website with buttons? A statistics engine? A predictive
algorithm?

To start, I'm going to dredge up my old PHYS 555 project. In it, I did some data munging and
statistical analysis and a tiny bit of machine learning on NHL data that I figured out how
to pull from their JSON "API" (relevant data munging below):

![NHL API](https://i.imgur.com/kiujlqq.png)

This was a few years ago now, but it's pretty straightforward. All this really gets me
is NHL team data in a nicely workable `pandas` dataframe, but it's a good template
for any NHL data, at the player level or the season level as well. 

After that, I was able to do all the usual Python tricks, which is as good a place as any
to start this project. To give one tiny example, here is a plot I made to show the
"statistical path" of the Stanley Cup-winning team in the 2000-2001 season (the
Colorado Avalanche):

![COL-statpath](https://i.imgur.com/W3ahDUm.png)

Basically, each vertical tick along the *x*-axis is one of the team stats provided by
the NHL API (with a few cleaned out, and a few bugs probably too). Every dot above it 
represents a given team's value for that stat, normalized and mean-subtracted. If a
team scores +1, they had the highest value for that stat in the given year, and a -1
obviously then means they had the lowest value for that stat. 

Why does this matter? Well, objectively it doesn't (what does?). But it's a sort of
qualitative look at which stats might matter most for the Stanley Cup winner. Or
at least the ones that mattered most in 2000-2001.

It doesn't actually make a lot of sense, when you look a little closer, because a
team would *want* to have the lowest value of a stat like, say, `losses`, and in fact we
see here that Colorado was indeed the team with the fewest losses that season. So it
might be more relevant to add some kind of sentiment classifier for each stat, inverting
it if it's a "bad" stat to provide a more meaningful path. In that case, the best 
possible outcome would simply be a straight line right across the top. 
