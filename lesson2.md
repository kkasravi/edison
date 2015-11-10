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
5. If you do not have a .ssh/id_rsa.pub generate one by doing `ssh-keygen`
6. Save the file by doing `<esc>:wq`
7. Change the permissions of authorized_keys to read-only by you `chmod 600 .ssh/authorized_keys`
8. logout and log back in to confirm no password is required

## Seeing if you can get your light's state remotely
1. Go to `http://api.developer.lifx.com/docs/list-lights`
2. At the bottom of the page click on the key icon and add your access key
3. In the selector field type: all
4. Click on 'Try It'
5. You should get back something like 
```
[
    {
        "id": "d073d5039c3f",
        "uuid": "02425eb9-91b1-419c-9be4-da7e8408bfc0",
        "label": "LIFX bulb 039c3f",
        "connected": true,
        "power": "off",
        "color": {
            "hue": 0,
            "saturation": 0,
            "kelvin": 3500
        },
        "brightness": 0.5816739147020676,
        "group": {
            "id": "24ab5a25262b806f3afb542e6dbdd94c",
            "name": "My Room"
        },
        "location": {
            "id": "70282345444edd5e1a14f6c0bfd78808",
            "name": "My Home"
        },
        "product": {
            "name": "Original 1000",
            "identifier": "lifx_original_a21",
            "company": "LIFX",
            "capabilities": {
                "has_color": true,
                "has_variable_color_temp": true
            }
        },
        "last_seen": "2015-11-10T20:56:04.644+00:00",
        "seconds_since_seen": 0.003353778
    }
]
```
If you get back something like just 2 bracket symbols '[]' and nothing else [you need to upgrade your lights firmware](https://support.lifx.com/hc/en-us/articles/202996584-Original-LIFX-Firmware-update)

## Changing a LIFX light to your color using the web interface
1. Go to `http://api.developer.lifx.com/docs/set-state`
2. At the bottom of the page click on the key icon and add your access key
3. Insert the following values in the fields
  - selector: all
  - power: on
  - color: `<your color>` saturation:1.0
  - brightness: 1.0
  - duration: 1.0
4. Click on 'Try It'
