---
layout: post
title:  "The stats are back"
date:   2022-07-17 09:38:34 -0800
categories: documentation
---

After a pretty serious hiatus, and just when I thought I was out, the Stanley Cup finals dragged me back in.
I've spent the last while diving back into the stats side of things and had a devil of a time trying to wrangle
the NHL stats API for anything other than team data. 

The incredibly helpful [nhlapi project](https://gitlab.com/dword4/nhlapi/-/tree/master) has been a blessing, but
even standing on the shoulders of this giant, the process can be excruciating. In any case, I've finally got things
to a *passably* workable state, whereby I can access some individual player data, which loads out as follows:

![SampleData](https://i.imgur.com/0b6zqV1.png)

Now, just to get this kind of interface, I had to write reams of code that looks like this:

![BadCode](https://i.imgur.com/K0qwnQJ.png)

and this:

![WorseCode](https://i.imgur.com/CtS7Wtv.png)

There is plenty worse where that came from, and I know one day it will fall on me to clean it up. But I'll cross
that bridge when I get to it. For now, I still have to piece together Player IDs and names, so that I can actually
access a player's stats with his name, rather than a 9-digit number. Also, I need to figure out this URLLIB error 
preventing me from accessing all of the data at once. And so on...
