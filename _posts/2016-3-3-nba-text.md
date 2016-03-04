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

After some fiddling I noticed a few things.  Positions, along with their desirable attributes, are amongst the most frequent words in each topic.

You can see that the topics accurately categorized each position.
![img]({{ site.url }}/images/nba-text/byposition.png)

There's also a very odd relationship between the clusters and the years that fall into those clusters.
![img]({{ site.url }}/images/nba-text/byyear.png)

Since the two clusters containing these years also both contained the phrase mid range, I dug into the frequency of the occurrence of midrange.

![img]({{ site.url }}/images/nba-text/midrange.png)

The usage of the phrase mid range in describing players is going out of style.  Today's NBA is focused on efficiency, and it seems like writers are following that trend too.

Apparently no one cares about midrange basketball anymore, not even NBA writers.  So long Kobe and MJ.  Hello Steph Curry.
