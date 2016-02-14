---
layout: post
title: Learning Hearthstone
tags:
- data
- games
---
In any competitive game information is a huge advantage.  Imagine if an opponent played with an open hand.  Planning your own turn and planning your future turns would be a piece of cake.

The big question is...

## How do we predict our opponent's next move?

Our data is going to be 50,000 games of data where we have our opponents sequence of cards played.

![png]({{ site.url }}/assets/learning_hearthstone/data.png)

To do this we're going to use n-grams.  N-grams, similar to the word engram, stores our data in a structure where we can easily recall it for relevant information.  

An N-gram is comprised of two components: the order and the level.  The level is the building block of our n-gram, the lowest level unit.  The order is the length of our n-gram, or the length, in units of our n-gram.

N-grams are comprised of continuous strings pulled from a longer continuous string.  Here's what our N-grams look like for our data.

![png]({{ site.url }}/assets/learning_hearthstone/n-gram.png)

Using the n-grams for prediction is just a stone throw away.  Suppose we want to know what comes after a leper gnome based on our data.

![png]({{ site.url }}/assets/learning_hearthstone/prediction.png)

Based on our data we see two cards that occur after a leper gnome.  So we apply equal weight and each has a 50% chance of being played next.

![png]({{ site.url }}/assets/learning_hearthstone/application.png)

Applying this model to Hearthstone requires a slight modification.  Since we can't interrupt our opponent's turn it's more important to predict what their next turn will be rather than what card they'll play next.  The application then looks like the following.

The guy that implemented the model few other small tweaks and you can read more about it [here!](https://www.elie.net/blog/hearthstone/predicting-hearthstone-opponent-deck-using-machine-learning "Predicting Hearthstone")

N-grams have other applications in things like spam filters, text prediction, voice recognition, and more.
