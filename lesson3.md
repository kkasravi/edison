# Lesson 3 Command line usage of LIFX on the edison board

## ssh into your edison board
1. Go to https://developer.weaved.com/portal/members/home.php
It will provide a ssh login similar to
ssh -l LOGIN proxya.yoics.net -p 34141
2. Bring up a terminal window and type in the command above substituting LOGIN with your name

## Change a buddy's light using the lifx command
1. Type in 'lifx' and hit return to see its usage.
2. Run lifx to change the light of a buddy and redirect the output to a file called 'lesson3.done' in your home directory

## Query someone else's light status
1. Run lifx -q <name> to get the status of someone elses light
2. Repeat 2. above but append the output to your lesson3.done by using the '>>' operator
