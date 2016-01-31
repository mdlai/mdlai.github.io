---
layout: post
title: 'Determiner Noun: Number'
tags:
- data
---
Since the dawn of time, humanity has sought the answers to what to name their movies if they want to make the most money.  Finally someone has nudged the the space of understanding.

Beginning with a data set of just movie Titles, Revenue, and Theaters the struggle began, to break down Titles into parts of speech to find the answers I was looking for.  In order to accomplish this I met a friend, "Spacey" that helped me smash my Titles into tiny parts of speech.

![img]({{ site.url }}/assets/luther_images/table.png)

Armed with my tiny parts of speech, I herded the Movies into bins based on their Total Theater counts.  In one bin small movies with 0-20 theaters, the next bin 20-1000, the final bin 1000+ theaters.  This way all the bins were of roughly equal size.

In order to put my Total Grosses in line, I mushed them all through a natural log, which oddly enough make them more normal.

![img]({{ site.url }}/assets/luther_images/bins.png)

As my quest for the answers progressed, I decided to cross my parts of speech with my bins.  Which gave me a new weapon: 56 features.  Again I had to normalize them, in order to make them the same size.  So they'd be a better fit, of course.

I took these features and trained them on a ridge (regression).  And what a beautiful ridge regression it was.  The lambda was all the way to 10.

After training them on the ridge regression, each feature produced a beta I knew I was close to finding the answers.

![img]({{ site.url }}/assets/luther_images/betas.png)

In order to bait out the answers, I subtracted the high betas minus the low betas for each part of speech.  This was because my low betas were disguised, and were actually the baseline for my comparisons.  

Huzzah!  The answers!

![img]({{ site.url }}/assets/luther_images/widerelease.png)

![img]({{ site.url }}/assets/luther_images/midrelease.png)

For wide release movies I discovered it was best to name a movie with a noun, number, and punctuation.  My guess is the number trend is a result of wide release sequels producing a lot of money.

For mid release movies, adpositions and verbs were the way to go.

While the results weren't everything I was looking for, they were something worthwhile.  Maybe I'll be able to find more in *Determiner Noun: Number + 1*!
