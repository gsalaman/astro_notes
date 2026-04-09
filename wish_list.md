# Wish List
* Some sort of autoguiding
* rack-n-pinion focuser for Carbonstar
* Light panel for calibration

## Autoguide notes
PHD2 is the recommended autoguide SW.  It can run under Mac and Windows.  There are two main configs:
1) ST4 port.  This one is the less-recommended path...you go USB from the guide camera to the computer running PHD2, and then the camera talks ST4 to the mount.
2) ASCOM support.  ASCOM is the common driver interface...you can use it to control the mount, this time NOT through the ST4 port, but through a USB on the bottom of the HDX hand controller.  In theory, you can integrate NINA and ASTAP to do auto plate solves and target acquisiton...and then PHD2 would send "pulse" commands to move the mount dirctly through that interface.

Main issue with #2 is that it is windows only.  Okay, some folks say you can get it happy on mac, but that's a non-std config, so if I go that way, I need a seperate windows laptop.

The auto-plate solve and target acquisition for #2 sounds cool though...would like to eventually get there. 

I think I'm gonna start with #1...less software, but with a config that can go to #2.


### iOptron integrated
[Link here](https://agenaastro.com/catalog/product/view/id/8605/s/ioptron-iguider-30mm-f-4-mini-guiding-scope-3361/?gad_source=1&gad_campaignid=17357599342&gbraid=0AAAAAD_aP9Lx4jLLkCHkjAcl20Z8gKzWA&gclid=CjwKCAjw-dfOBhAjEiwAq0RwIwEC0_ShPAzLehQ9UkYb61SWL1200-Au4nJKks6PpWhSh68I03dOxxoCGxUQAvD_BwE)

Resolution here is only 6 arc-sec per pixels.  Gonna have drift.


### 50 MM guide scope
Options:
[Williams Optics](https://www.highpointscientific.com/william-optics-uniguide-50mm-slide-base-guide-scope-with-1-25-rotolock-black-red?utm_campaign=&utm_content=&utm_source=google&utm_medium=cpc&utm_term=WYO-M-G50PB-BR&utm_source=google&utm_medium=cpc&utm_campaign=17934693297&utm_content=139942520099&utm_term=&gad_source=1&gad_campaignid=17934693297&gbraid=0AAAAAD-khUb-fQeTZdvJshj4UAvGP4x0p&gclid=CjwKCAjw-dfOBhAjEiwAq0RwI2ibOJY16BKK-Y8QnIjLRxcoWHI1Co-Pkp6Ub6uz0ZDezjySHaUdGhoCAekQAvD_BwE)



### Use exisiting finder?
This is gonna be my first investigation...can I run this with a decent camera?  Make sure it has a guide port so that I can do either ST4 or Pulse with PHD2, and evolve it.  

So what's the focal length of the finder?  And can I remove the "X"?


# OLD
Current prios:
1) get EQ platform going!
2) Upgrade focuser on 10"
3) New Astro cam for Ha with some sort of laptop.

## Mount
Sky-tracker does well.  Camera only config is great.  Celetron is under weight-limit, but putting on the TV-85 puts it RIGHT at limit.
Haven't tried serious tracking, but conventional wisdom is that for astrophotography, you want to be running at HALF weight limit.

So, put on the wishlist a new mount.    
For the TV-85, you'd want ~23 lb capacity.
If I wanted to someday upgrade to a TV-127, you are adding just under 10 lbs, which means you want to go with something 50lbs...and you aren't getting focal length/mag.

Sooo....this is longer term...if you want that kind of mag with aperature, you probably want to go with some sort of a Reichy-Cerrian or SCT. 

Or, if the goal is just mag for planets, I should really get the EQ platform going on the 10" dob.  Tracking isn't gonna be as great as polar alignemnt will be off some,
but I say do it and then try...

## Camera
So, the Canon DLSR has an internal IR filter...meaning we don't get the Ha line.  You can go dedicated...good sweet spot here is in the $1k range, but those all require WINDOWS PCs to drive them.  :(

## Focus!
Should upgrade focusers on the 10" and 12".  Probably start with the 10".
Orion's dedicated one is a safe bet, but it's continously back-ordered.  Maybe look at a better focuser?

## Planet Mag
So if I stick with the TV-85, I only get 1.35 arc-seconds per pixel.  This means:
* Jupiter:  60 arc seconds = 44 pixels
* Saturn:  20 arc seconds = 15 pixels

So, if I want to keep on this route, the right answer may be a powermate.  Need to do math to make sure the focus path isn't extended a bunch (the 2x barlow puts focus spot WAY outside focuser range).
