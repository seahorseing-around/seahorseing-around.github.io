---
layout: page
title: Pucket Puzzle
description: This is a puzzle box I made for my friend John. I think he's yet to crack it but maybe if he finds this site he'll get a clue!
img: assets/img/pucket/header.png
importance: 1
category: fun
---

This project started when my friend John surprised me with a gift at the end of a Frisbee tournament. The gift in question was a handmade cardboard puzzle box. Having become interested in locking mechanisms he constructed the puzzle from a shoebox, spinning cardboard locks, lollypop sticks and party poppers for extra excitement. The puzzle was solved by deciphering clues on the box to spell out the codeword "Netherland", our ingenious Ultimate Frisbee play from Freshers year at Grey in Durham.

TODO photo JOhn
TODO photp john's puzzle 


I had a great time solving this and the only way to respond was in kind. Fortuitously in 2020 I found myself at home with too much time on my hands any things escalated...

## Design

I knew I wanted a layered puzzle, so the design process began with brainstorming things I knew John would like. This meant games, preferably ones which could be played with friends. I also wanted it to be something he could enjoy repeatedly after having solved it. This naturally led me to traditional wooden pub games. _The other advantage of these is they don't require any delicate woodworking_

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

Pucket is pretty simple, a box with a playing area divided by a bridge and I could easily find a way to hide a mechanical lock that opens the box. So that's the easy part - a wooden box, the next layer was something more challenging. 

One day inbetween lectures a poor recruiter offered john a chance to play one of these reaction based button pressing games. The aim of the game is to press buttons as they light up and press as many as you can within 30 seconds. John proceeded to spend all day trying to get the high score, scaring off any other potential recruitees and I suspect never even finding out himself what the company was he spent all day with.

<div class="row justify-content-sm-center"fgx>
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.html path="assets/img/6.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
        TODO add photo of button pressing game
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.html path="assets/img/11.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    You can also have artistically styled 2/3 + 1/3 images, like these.
</div>

OK so lots of buttons which you have to press when they light up, and if you get a high enough score in 30 seconds the stage is completed. However that seemed too easy and I still needed a way to trigger the start of a game of button pressing. I knew it would be fun to include a magnet in one of the pucks and given it would already be electronic I realised I could use a magnet sensor. 

At this point I needed to actually have a final goal to be acheived, and decided on a drawer which could be released as the final stage - this would make a suitable hiding space for a birthday present. 

## Mechanism
By this point you may be wondering how the whole thing would operate, enter the Raspberry Pi. I had:
* 1 x magnet sensor
* 1 x solenoid
* N x led + button (2 GPIO per item)

Ideally I would have had a full set of TODO NUMBER buttons, however in the interests of not complicating the electronics with TODO thing that allowes more device than GPIO a I decided to simply wire each button / led to its own GPIO. This allowed for TODO number LED + button combos, enough to mke a good game, and convenienetly leave a gap in the middle, hopefully giving a clue as to how to trigger a game.  

Sadly I have no photos of the electronics but the code can be found on my Github and can be summariesed as follows:
* Runs automaticlly on startup & displays a fanfare of lights for fun, and so you know it's on
* Triggers a 30s game if the magnet is detected
* 'Backdoor' drawer release if a certain set of buttons is held down

The most complicated part of the electronics was keeping track of all the wires! In the end I used a set of screw in connectors to allow me to wire in the many wires and buttoms afterwards simplifying assembly.  

## Woodworking

The woodworking was ultimately the harder part of this project. I came up with a mechanism where a part that looked like piece of the foot could be slid out, unlocking the entire ennd of the puzzle and allowing the pucket base to slide out revealing the button game. This was difficult in 2 ways:
1. Not giving away the release mechanism with visible gaps for sliding pieces
2. Tolerances for sliding elements. 

Ultimately many new tools were required: a router for accurate grooves, better chisels for more accurate sculpting, accurate parking and measuring tools to ensure everything was within tolerance. 

# Problems solved while building
## weight

## Drawer release



<!-->
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
-->
