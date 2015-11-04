# Lesson 2

## ssh into your edison board
1. Go to https://developer.weaved.com/portal/members/home.php
It will provide a ssh login similar to
ssh -l LOGIN proxya.yoics.net -p 34141
2. Bring up a terminal window and type in the command above substituting LOGIN with your name

## More unix commands
1. Using vi - a text editor
1. Create a directory with your name
2. 'cd' into that directory
3. Output the date to a file called 'done' using the redirect operator 

## Changing a LIFX light to your color using the web interface
1. Go to `http://api.developer.lifx.com/docs/set-state`
2. At the bottom of the page click on the key icon and add your access key
3. Insert the following values in the fields
selector: all
power: on
color: <your color> saturation:1.0
brightness: 1.0
duration: 1.0
