---
layout: post
title: 'Cleaning Pictures'
image: /images/cleaning-pictures/cleaning-pictures.jpg
subtitle: That time I tried to make my computer see
tags:
- data
---

This week I discovered that

### Image preprocessing is a ton of work.

My current project is creating a model that predicts digits using the MNIST data set.

To improve the performance of the my model I needed to touch up my digits with a two fold strategy.

1. Create a bounding box
2. De-Skew the image

Easy I thought.  Even with no experience doing image processing how hard could it be?  Well after step one I was feeling pretty confident.  A quick drop into the `skimage` library and my numbers were bounded and resized.
<pre><code>thresh = threshold_otsu(image)
image = image > thresh
binary = regionprops(image)[0].image.astype(float)
plt.matshow(resize(binary,(28,28)))
</code></pre>
<div class="row uniform">
  <div class="6u"><span class="image fit"><img src="/images/cleaning-pictures/six.png" alt="" /></span></div>
  <div class="6u$"><span class="image fit"><img src="/images/cleaning-pictures/pca.png" alt="" /></span></div>
</div>

Then I thought about de-skewing or rotating my image.  And I kept thinking.  For three days I had no real clue where to go.  After reading a ton of papers and consulting Professor Google countless times I finally came to a workable solution.

I would use PCA to determine a principal axis vector and use that to calculate an angle and rotate my image.  And it worked, sort of.  Maybe I'll get some better results next week.

If you have any methods or bits of knowledge you want to drop on me about image processing, I'd love to hear them.

[E-mail me.](mailto:Michael@mdlai.com)
