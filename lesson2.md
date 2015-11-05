# Lesson 2

## ssh into your edison board
1. Go to https://developer.weaved.com/portal/members/home.php and select the edisonX_ssh service shared with you.
It will provide a ssh login similar to
ssh -l LOGIN proxya.yoics.net -p 34141
2. Bring up a terminal window and type in the command above substituting LOGIN with your name

## Enabling auto-login without a password
1. Create a directory called .ssh
2. Create a file called authorized keys by using vi
`vi .ssh/authorized_keys`
3. Change mode to 'insert' by pressing 'i'
4. Cut & paste the contents of your local .ssh/id_rsa.pub into this file
5. Save the file by doing `<esc>:wq`

## Changing a LIFX light to your color using the web interface
1. Go to `http://api.developer.lifx.com/docs/set-state`
2. At the bottom of the page click on the key icon and add your access key
3. Insert the following values in the fields
  - selector: all
  - power: on
  - color: `<your color>` saturation:1.0
  - brightness: 1.0
  - duration: 1.0
