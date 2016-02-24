---
layout: post
title: 'Lucky Guess'
image: /images/lucky-number/guess-my-number.jpg
subtitle: Machine learning is pretty much black magic
tags:
- data
---
For my latest magic trick (Metis project 3), I attempted to build a model that could predict hand written digits.

Using Tensorflow, Flask, and Heroku, I created an app that can guess numbers drawn on it.

<div class="12u$"><span class="image fit"><img src="/images/lucky-number/presentation.jpg" alt="" /></span></div>

Here's me presenting my app!

The model is a convolutional neural network trained on the MNIST data set.  The next step would be for me to store the drawn data and add it to my model... maybe when I have a bit more time.

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
