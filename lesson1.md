# Lesson 1 Getting Started

## Sign up for weaved
1. https://developer.weaved.com/portal/index.php
2. Send me your email that you used when signing up so I can add you to the edison remote login

## Sign up for lifx cloud account
1. Once you get your light you need to download the iOS or Android app to control it.
2. After downloading the app you can sign up at https://cloud.lifx.com/ to remotely control the light 
3. Generate a new token to control your lifx lights: https://cloud.lifx.com/settings
4. Send me the color you want to have when changing other friends light bulbs and well as your remote access token (from 3.):

> - Ian - yellow
> - Julian - blue
> - Kyler - red
> - Oliver - light green
> - Mason - deep pink
> - Matthijs - violet
> - Miles - orange
> - Nils - purple
> - Xander - pink

## ssh into your edison board
1. Go to https://developer.weaved.com/portal/members/home.php
It will provide a ssh login similar to
ssh -l LOGIN proxya.yoics.net -p 34141
2. (MacOS) Bring up a terminal window and type in the command above substituting LOGIN with your name
   * example `ssh -l YOURNAME proxya.yoics.net -p 34141`
3. (Windows) You'll need to install [putty]( http://www.putty.org/). Once installed you'll need to login using the Terminal panel and  the ssh login information for the host and port provided above


## do some unix commands
1. Create a directory with the name lesson1
   * `mkdir lesson1`
2. 'cd' into that directory
   * `cd lesson1`
3. Output the date to a file called 'lesson1.done' using the redirect operator 
   * `date > lesson1.done`

