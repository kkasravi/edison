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
   * `var bulb=Object.keys(lx.bulbs)[0];`
   * `lx.lightsOff(bulb);`
5. Go back to 'command' mode (from insert mode) by pressing
   * `<escape>`
6. Save the file by typing in
   * `:wq`
7. Run the file
   * `./colors`
 

