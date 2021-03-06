---
layout: post
title: 'Predicting Numbers'
image: /images/lucky-number/guess-my-number.jpg
subtitle: Neural Networks producing red hot predictions
tags:
- data
---
Lately I've been building a model that can read your mind... or just your handwriting.

Using Tensorflow, Flask, and Heroku, I created an app that can guess numbers drawn on it.

<div class="12u$"><span class="image fit"><img src="/images/lucky-number/presentation.jpg" alt="" /></span></div>

Here's me presenting my app!

The model is a convolutional neural network trained on the MNIST data set.  The next step would be for me to store the drawn data and add it to my model... maybe when I have a bit more time.

It kinda sucks at guessing 9s and 0s, a consequence of a model that's over fit to its specific training data.  Maybe adding some deformations to the dataset would improve performance.

The instructions are simple, just click on the grid and draw a number.  

<iframe
 src="https://number-predictor.herokuapp.com/"
 width="100%" height="800">
  <p>
    <a href="https://number-predictor.herokuapp.com/">
      Fallback link for browsers that, unlikely, don't support frames
    </a>
  </p>
</iframe>

If you want to see the code check out [my github.](https://github.com/mdlai/digit_recognition)
