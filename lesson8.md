# Lesson 8 Modify alex repo with your alex security information and run AVS example

## ssh into your edison board
1. Go to https://developer.weaved.com/portal/members/home.php
It will provide a ssh login similar to
ssh -l LOGIN proxya.yoics.net -p 34141
2. Bring up a terminal window and type in the command above substituting LOGIN with your name
   * example `ssh -l freddie proxya.yoics.net -p 34141`

## Overview
![Request flow](https://github.com/kkasravi/edison/blob/master/diagram.png)

## Clone https://github.com/kkasravi/alexa.git
1. Create a subdirectory called lesson8
   * `mkdir lesson8`
2. Change directory to go into the lesson8 directory
   * `cd lesson8`
3. Clone alexa 
   * `git clone https://github.com/kkasravi/alexa.git`
4. Change to this directory
   * `cd alexa`
5. In browser log into your amazon account and access your edisonbot device
   * browse to `https://developer.amazon.com/edw/home.html#/avs/list`
6. Edit auth_code.sh and update CLIENT_ID, DEVICE_TYPE_ID and DEVICE_SERIAL_NUMBER using information from the browser
   * `vi auth_code.sh`
7. Run auth_code.sh
   * `./auth_code.sh`
8. Take the output from auth_code.sh and place it in the browser URL
9. Select 'Continue' in the browser
10. Copy the code part of the URL and edit auth_token.sh
   * `vi auth_token.sh`
11. Edit auth_code.sh and update CLIENT_ID, CLIENT_SECRET and CODE using information from the browser
   * `vi auth_code.sh`
12. Run auth_token.sh
   * `.\auth_token.sh`

## Clone AVS-server
1. cd to ~/lesson8
   * `cd ~/lesson8`
2. clone AVS-server
   * `git clone https://github.com/miguelmota/AVS-server`
3. build AVS-server
   * `cd AVS-server`
   * `npm install`
4. cd to AVS-server/config
   * `cd config`
5. move *.sample.json files to auth.json, deviceSecret.json and token.json
   * `mv auth.sample.json auth.json`
   * `mv deviceSecret.sample.json deviceSecret.json`
   * `mv token.sample.json token.json`
6. edit auth.json, deviceSecret.json and token.json and insert info from browser
7. run AVS-server
   * `npm start`

## Run AVS-client
1. cd to AVS-client
   * `cd /home/root/AVS-client`
2. run AVS-client
   * `gulp`
   * `cd /home/root/AVS-client`
  
 


