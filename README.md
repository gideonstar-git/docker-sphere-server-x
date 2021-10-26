# Sphere Server X for docker

## About

This is the Ultima Online Server Emulator Sphere X for docker. If you're not
familiar with Ultima Online, this project is propably not for you.

## Install

### Directories

  * mkdir files/accounts files/logs files/mul files/save files/scripts

### Config

  * copy files/sphere.ini.dist to files/sphere.ini
  * add AGREE=1 in the [SPHERE] section
  * uncomment MulFiles
  * at the end of the config uncomment the External lines and change the IP to
    the IP of your docker host
  
### Install files

  * copy the mul files to files/mul/
  * git clone https://github.com/Sphereserver/Scripts files/scripts

### Build image and run server

  $ docker build . -t sphereserver\
  $ docker-compose up -d

Attach to the running server:
  
  $ docker attach sphereserver\
  account add \<user\> \<password\>\
  account <user> plevel 7\
  #\
  ctrl-p ctrl-q
