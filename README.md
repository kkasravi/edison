# edison

##setup wifi from serial terminal

configure_edison --wifi

configure_edison --password

configure_edison --name

## enable wifi on reboot
systemctl enable wpa_supplicant

## enable ssh w/ no password
scp ~/.ssh/id_rsa.pub to root@edison:~/.ssh/authorized_keys

## install java8
http://harmoniccode.blogspot.com/2014/05/java-8-on-intel-galileo.html

## join weaved 
https://developer.weaved.com/portal/index.php

## install weaved
https://developer.weaved.com/portal/members/edison.php

## install node.js
wget https://nodejs.org/dist/v4.2.1/node-v4.2.1-linux-x86.tar.gz

tar xzf node-v4.2.1-linux-x86.tar.gz

mv node-v4.2.1-linux-x86 /opt

update .bash_profile

export PATH=/opt/node-v4.2.1-linux-x86/bin:$PATH

## install node-red
npm install -g --unsafe-perm node-red
