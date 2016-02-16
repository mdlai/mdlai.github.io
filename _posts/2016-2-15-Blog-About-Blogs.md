---
layout: post
title: 'HTML5 To Jekyll'
image: /images/blog-about/blog-about.png
subtitle: A blog post about making blogs
tags:
- code
---
I just finished my 5th week at Metis, so I decided what better way to celebrate than spend my weekend re-working my blog!

Making Jekyll work with HTML5 is a bit of a headache.  I hope my pain can be your gain.

There's a great tutorial on how to convert a theme to [here](http://jekyll.tips/guide/setup/) but I'll toss a few things that I found would've helped past me.  I'm giving tips from the perspective that you at least skimmed this guide.

### Basics
1. Find an HTML5 template you like.
2. Get Jekyll running.
3. Add the necessary folder structure and config files to your template.
4. Customize.

### Tips
I'll skip to number three since the first two should be pretty straight forward.  The best tip I have for past me is to break up each section into an \_include.html.  It adds a lot of flexibility in how your layouts are designed.  

For example having a header is necessary, but adding specific HTML for say a specific menu allows you to have slightly different headers to suit your needs.

In terms of customization, I spent far too much time wresting with the liquid code.  I really hope I didn't miss the easy way, but finding indexes and going through arrays was a monstrosity.  
<pre><code>
  #Finds the index of the current page as well as the total for the number of posts.
  {% for post in site.posts %}
    {% assign max = forloop.length | minus : 2 %}
    {% if page.url == post.url %}
      {% assign current = forloop.index %}
    {% endif %}
  {% endfor %}

  #If the post is less than 3 from the start or greater than 3 from the end, use the first 5 pages or last 5 respectively.
  {% if current < 3 %}
    {% assign current = 3 %}
  {% elsif current > max %}
    {% assign current = max %}
  {% endif %}

  #For each post use two posts forward in time and two backwards in as the links in the sidebar.
  {% for post in site.posts %}
    {% assign last = current | plus : 3 %}
    {% assign first = current | minus : 3 %}
    {% if forloop.index > first and forloop.index < last %}
      <!-- Show Post -->
    {% endif %}
  {% endfor %}
</code></pre>
This little bit was necessary just to create chronologically adjacent sidebar links further than 1 post away.

Finally, copy elements from other themes.  Tons of HTML5 based themes are available [here](http://jekyll.tips/templates/) and they're already fit for jekyll

### Conclusion
Liquid is really annoying and Jekyll is really amazing.


[E-mail me.](mailto:Michael@mdlai.com)
