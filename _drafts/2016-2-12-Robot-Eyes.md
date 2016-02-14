---
layout: post
title: 'Cleaning Pictures'
tags:
- data
image: /images/pic04.jpg
subtitle: That time I tried to make my computer see
---
Today marks the end of my 5th week at Metis, a 12 week data science boot-camp. The program has kept me plenty busy, but in an effort to blog regularly I'm going to start sharing some of my trials and tribulations for the week.

This week I discovered...
### Image preprocessing is a ton of work.

My current project is creating a model that predicts digits using the MNIST data set.

This visualization shows the average image for a given digit.
[img](a)
Each number has a clear and recognizable average image.  I think of it as a picture of the perfect set of digits.  

Here's a visualization of all the errors when fit to a K Nearest Neighbors model.  I think of this one as an average of horrific handwriting.
[img](a)

To improve the performance of the my model I needed to touch up my digits with a two fold strategy.
1. Create a bounding box
[img]()
2. De-Skew the image
