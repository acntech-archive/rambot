# rambot 

A simple Twitter controlled webcam robot.

This project contains 2 Node-RED (nodered.org) flows:
* A flow that listens for #rambot tweets and converts these into robot commands (move, pan, tilt, take a picture)
* A flow that displays all #rambot tweets and the resulting pictures (tweet dashboard)

## Pre-requisites
A robot with a web-cam created using the code from this blogpost:
http://blog.ramon.no/2013/06/build-simple-internet-controlled-webcam.html

Node-RED must be installed on the robot:
http://nodered.org/docs/hardware/raspberrypi.html

Node-RED installed on a RaspberryPi connected to a screen (for the tweet-dashvoard)

## Deploy
### Robot
Inject the flow in [robot.flow](robot.flow) into the Node-RED instance running on the robot

### Dashboard
Inject the flow in [tweet_dashboard.flow](tweet_dashboard.flow) into the Node-RED instance running on the RaspberryPi connected to the screen

## Usage
Connect Rambot to a WiFi (currently configured: SSID=RambotAP, Pass:hackfest)

Launch a browser on the RaspberryPi connected to the screen: 
```
DISPLAY=:0 nohup midori -e Fullscreen -a http://10.110.66.177:1880/tweets &
```

Tweet using the hashtag #rambot one or more of the following commands:
* shwing	Left 45%
* shwang	Right 45%
* shwosh	Forwards 100cm
* shwash	Backwards
* shnapy	Take photo
* shne	Camera left
* shna	Camera right
* shnop	Camera up
* shnap	Camera down
