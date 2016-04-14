# Lesson 7 Create a pebble app that can talk to alexus

## ssh into your edison board
1. Go to https://developer.weaved.com/portal/members/home.php
It will provide a ssh login similar to
ssh -l LOGIN proxya.yoics.net -p 34141
2. Bring up a terminal window and type in the command above substituting LOGIN with your name
   * example `ssh -l freddie proxya.yoics.net -p 34141`

## Clone pebble-talk2web to  your directory
1. Create a subdirectory called lesson7
   * `mkdir lesson7`
2. Change directory to go into the lesson6 directory
   * `cd lesson7`
3. Clone the pebble-talk2web repo using git
   * `git clone https://github.com/kkasravi/pebble-talk2web'
4. Change to this directory
   * `cd pebble-talk2web`
5. Run an http server
   * `node server.js`

## Go to cloudpebble and clone pebble-talk2web
1. Log into cloudpebble.net
   * browse to https://cloudpebble.net
2. Create a project and import https://github.com/kkasravi/pebble-talk2web
   * `Select Import`
   * `Select Import from Github`
   * project name: talk2web
   * github project: https://github.com/kkasravi/pebble-talk2web
3. Compile and Install the project on the pebble
4. Configure the webserver
5. Run talk2web


 


