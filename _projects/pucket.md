---
layout: page
title: Pucket Puzzle
description: This is a puzzle box I made for my friend John. I think he's yet to crack it but maybe if he finds this site he'll get a clue!
img: assets/img/pucket/header.png
importance: 1
category: fun
---

This project started when John surprised me with a gift at the end of a Frisbee tournament. The gift in question was a puzzle box he had made. Having become interested in locking mechanisms he constructed the puzzle from a shoebox, spinning cardboard locks, lollypop sticks and party poppers for extra excitement. The puzzle was solved by deciphering clues on the box to spell out the codeword "Netherland", our ingenious Ultimate Frisbee play.

Of course I had a great time solving this and the only way to respond was in kind... Only, for unstated reasons in 2020 I found myself at home with too much time on my habds any things escalated...

I knew I wanted a layered puzzle, so the design process began with brainstorming things I knew John would like. This meant games, either ones which could be shared or would challenge him personally. I also wanted it to be something he could enjoy after having solved it. This naturally led me to traditional wooden pub games. _The other advantage of these is they don't require any delicate woodworking_

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/pucket/skittles.png" title="Pub Skittles" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/pucket/pucket.webp" title="Pucket" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/pucket/quiotes.webp" title="Quiotes" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    On the left, pub skittles. Middle, Pucket. Right, Quiotes.
</div>

My clear favourite (based on enjoyment and tools available) is Pucket. It's an intense, 2 player, adrenaline fuelled game that demands speed and accuracy while threatening to crush finger tips between pucks. Great game! 10/10! 

Now that's the easy part, a wooden game the next part was something more challenging. 

One day inbetween lectures a poor recruiter offered john a chance to play

<div class="row justify-content-sm-center"fgx>
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.html path="assets/img/6.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.html path="assets/img/11.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    You can also have artistically styled 2/3 + 1/3 images, like these.
</div>


The code is simple.
Just wrap your images with `<div class="col-sm">` and place them inside `<div class="row">` (read more about the <a href="https://getbootstrap.com/docs/4.4/layout/grid/">Bootstrap Grid</a> system).
To make images responsive, add `img-fluid` class to each; for rounded corners and shadows use `rounded` and `z-depth-1` classes.
Here's the code for the last row of images above:

{% raw %}
```html
<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.html path="assets/img/6.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.html path="assets/img/11.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
```
{% endraw %}
