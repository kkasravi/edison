# Lesson 5 A shell script to print your full name correctly when it's in reverse order

## ssh into your edison board
1. Go to https://developer.weaved.com/portal/members/home.php
It will provide a ssh login similar to
ssh -l LOGIN proxya.yoics.net -p 34141
2. Bring up a terminal window and type in the command above substituting LOGIN with your name
   * example `ssh -l freddie proxya.yoics.net -p 34141`

## Create a simple script called yourname
1. Create a subdirectory called lesson5
2. Change directory to go into the lesson5 directory
   * `cd lesson5`
3. Edit a new file using vi. 
   * `vi yourname`
4. Go into 'insert' mode 
   * press `i`
5. Type in the following
   * `#!/bin/sh`
   * `yournamebackwards="<last> <first>"`
   * `yourname=""`
   * `echo $yournamebackward`
6. Save the file 
   * `:wq`
7. Make the script executable
   * `chmod +x yourname`
8. Run the script
   * ./yourname

## Let's get the length of all the characters in your name using commands and unix pipes
1. Print your name to the terminal
   * `yournamebackwards="<lastbackwards> <firstbackwards>"`
   * `echo $yournamebackwards`
2. Pipe it to a word count command
   * `echo $yournamebackwards | wc`
3. Get the last number from the word count command
   * `echo $yournamebackwards | wc | awk '{print $3}'`
4. Count down from the number of characters in your name to 1
   * `seq $(echo $yournamebackwards | wc | awk '{print $3}') -1 1`

## Now let's go back into the program and create a loop that does a countdown printing each number per line
1. Edit the yourname file again
   * `vi yourname`
2. Go to the end of the file and open a line
   * `G`
   * `o`
3. Create a loop and print each number per line
   * `for i in $(seq   $(echo $yournamebackwards | wc | awk '{print $3}') -1 1);do`
   * `echo $i`
   * `done`

## Now let's go back into the program and print out each letter as we reverse your name
1. Edit the yourname file again
   * `vi yourname`
2. Go to where the `echo $i` line is and open a line
   * `/echo/`
   * `o`
3. Add the following lines
   * `nextletter=$(echo $yournamebackwards | cut -c$i)`
   * `yourname=$yourname$nextletter`
   * `echo $yourname`
4. Save the file 
   * `:wq`
5. Run the script
   * ./yourname
 

