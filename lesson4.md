# Lesson 4 Programming lifx using javascript

## ssh into your edison board
1. Go to https://developer.weaved.com/portal/members/home.php
It will provide a ssh login similar to
ssh -l LOGIN proxya.yoics.net -p 34141
2. Bring up a terminal window and type in the command above substituting LOGIN with your name
   * example `ssh -l freddie proxya.yoics.net -p 34141`

## Create a simple script that runs javascript
1. Create a subdirectory called lesson4
   * `mkdir lesson4`
2. Change directory to go into the lesson4 directory
   * `cd lesson4`
3. Edit a new file using vi. 
   * `vi colors.js`
4. Go into 'insert' mode 
   * press `i`
5. Type in the following
   * `#! /usr/bin/env node`
   * `console.log('You are awesome!!');`
6. Save the file 
   * `:wq`
7. Make the script executable
   * `chmod +x colors`
8. Run the script
   * `./colors`

## Make sure the local light is on
   * `lifx -c yellow kyler`

## Add to the script by programming the LIFX light to turn off
1. Open the colors command with vi
   * `vi colors`
2. Press capital g to go to the end of the file
   * `G`
3. Open a new line under the last line in the file
   * `o`
4. Type in the following
   * `var lifx = require('./lifx');`
   * `var lx   = lifx.init();`
5. Find out the name your bulb is by typing the following:
   * `var bulb=lx.bulbs.<tab>`
   * You should see something like  
```
> lx.bulbs.
lx.bulbs.__defineGetter__      lx.bulbs.__defineSetter__      lx.bulbs.__lookupGetter__
lx.bulbs.__lookupSetter__      lx.bulbs.constructor           lx.bulbs.hasOwnProperty
lx.bulbs.isPrototypeOf         lx.bulbs.propertyIsEnumerable  lx.bulbs.toLocaleString
lx.bulbs.toString              lx.bulbs.valueOf               

lx.bulbs.d073d5039c3f          
```
   * Type in the first letter of the last line after lx.bulbs (in this case it's d073d5039c3f) and press `<tab>` again
     - `d<tab>`
   * Turn the light off by typing in
     - `lx.lightsOff(bulb);`
   * Go back to 'command' mode (from insert mode)
     - Press `<escape>`
   * Save the file by typing in
     - `:wq`
   * Run the file
     `./colors`
 

