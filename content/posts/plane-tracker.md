+++
title = "Airplane Tracker"
description = "Building a robot that can acquire and track nearby airplanes"
tags = []
categories = []
series = ["Themes Guide"]
aliases = ["migrate-from-jekyl"]
+++

Software for me has always been about the web. First it was webpages, then web apps, iPhone apps, now Mac apps. But what about building something that moves in the physical world. 

For this project, I wanted to combine my interest in the airplanes flying overhead (I live near SFO and OAK) -- and build my first "robot" that moves in the real world.


<object data="https://s3.us-east-2.amazonaws.com/projects.wasauce.com/wferrell-files/raspberrpi-laser-tracker.png" width="690px">
    <embed src="https://s3.us-east-2.amazonaws.com/projects.wasauce.com/wferrell-files/raspberrpi-laser-tracker.png">
    </embed>
</object>

<!--more-->

First, the plane tracker lives in a room with no windows -- so no this didn’t shine in any eyes nor distract any pilots.


#### So what are we seeing:

1. The Raspberry Pi is using [ADS-B](https://www.faa.gov/nextgen/programs/adsb/) to track flights.

<object data="https://s3.us-east-2.amazonaws.com/projects.wasauce.com/wferrell-files/code-view-laser.png" width="690px">
    <embed src="https://s3.us-east-2.amazonaws.com/projects.wasauce.com/wferrell-files/code-view-laser.png">
    </embed>
</object>

2. The code (see above a screenshot of the log output) is constantly searching for nearby flights (via the SRD on my roof). Once it finds a plane, it gets the reported lat/long and then calculates the angle of elevation from the position of the RaspberrPi. 
3. With this information, and knowing the orientation of the RaspberrPi (i.e. is the Pan/Tilt when zeroed out X degrees off North) -- now we can calculate the Pan degrees and Tilt degrees to point at the current position of the Airplane.
4. This code runs in a loop until the Airplane is out of range, then it finds the next one.

Take a look in this video:

{{< youtube q5BcP4a-B4w >}}


