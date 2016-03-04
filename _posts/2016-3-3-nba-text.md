---
layout: post
title: 'NBA Player Descriptions'
image: /images/nba-text/mjwings.jpg
subtitle: An explosive high IQ scrappy tenacious athlete.
tags:
- data
---
Draftexpress.com does a lot of analysis.  Sometimes I wonder if it's all the same or if they're actually coming up with some new and novel way to describe people every time.

I scraped 761 player profile pages and used Latent Dirichlet Allocation (LDA) to model what topics writers were talking about.

![img]({{ site.url }}/images/nba-text/topics.png)

The chart below helped me better understand my data.

It's interactive!  Click on the vertical axis to filter out different lines.  It's an easy way to filter each cluster in terms of year, pick, position, height, and weight.

<iframe src="/images/nba-text/index.html" marginwidth="0" marginheight="0" scrolling="no" width="100%" height="800"></iframe>

After some fiddling I noticed a few things.  The clusters are well defined in terms of position and somewhat defined in terms of year.  The position makes intuitive sense.  Positions are amongst the most frequent words in each topic.

But the years was less obvious.  I dug around and found that the phrase midrange has an odd distribution over time.

![img]({{ site.url }}/images/nba-text/midrange.png)

The usage of the phrase mid range in describing players is going out of style.  Today's NBA is focused on efficiency, and it seems like writers are following that trend too.

No one cares about midrange basketball anymore.  So long Kobe and MJ.  Hello Steph Curry.
