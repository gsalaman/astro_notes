# Intro
These are going to be my "raw photography" running notes...in reverse cron order (latest on top).
******
# 4-15-23 Redo Celestron Prime Calculation
Okay, found the error.  Crosspiece is about 250 pixels.  It spans 540 arc-seconds.  That's a little more than 2 pixels per arc-second (NOT 2 arc-seconds per pixel!!!).  Complete math yields .463 pixels per arc-second...or 27.78 pixels per arc-minute...which is close to the 22.25 number from 4/9.  WHEW!


# 4-11-23 Orion, Leo, Beehive, Sombrero
Good session down in lafayette.  My notes:
* The CLS filter is the bomb.  Only knocks out the mid Na and Hg lines...so you get decent transmission...as opposed to the UHC, which doesn't give ya the upper lines.
* Focusing is *TOUGH*.  Want a better scope with a dual-speed
* Star-hopping is also tough.  The crappy finder than came with the T70 is almost useless (even though I aligned it in daytime.  Best way was to go visual and eyepiece hop with a 20mm lens, then put in the camera, adjust focus again, and finish centering via the fine control knobs.  Got a reflex finder coming that should help.
* And speaking of the diagonal, it had trouble holding the eyepiece.   Cheap plastic.  :(  Another reason to get a better scope.

# 4-9-23  Nighttime T7 + Travel scope
Measurement:  the two stars around herc are 30 arc-minutes apart...the old pic with the telephoto yields 668 pixels.  That's 22.25 pixels per arc-minute.  Meaning my FOV is 267x180 arc-minutes...4.5x3 degree FOV...which matches my old calc.  Now, with the travel setup, its 958 pixels, or 32 pixels per arc-minute.  FOV is 187.5x125 arc-minutes, or about 3x2 degrees.  Better, but off by about a factor of 3 from my daytime calc.  Each pixel is about 2 arc-seconds.

# 4-9-23  Daytime T7 + Travel scope test
THIS CALC IS WRONG...SEE 4-15 above!!!

Crosspiece is ~260 pixels...field is 6000x4000 pixels.
At 540 arc-seconds for the cross-piece, that's about 2 arcseconds per pixel...meaning field is 3000x2000 arc-seconds, or 50x33 arc-minutes...a little less than a degree across and more than half a degree up.  This should be GREAT for galaxies, which run somewhere around 10 arc-minutes across!!!


# 8-30-22 Saturn and Jupiter from Fraser
Wanted to catch saturn a little higher...sky was 5-4-3.  Did multiple sets with between 30 and 35 deg.

Favorite parms are iso 400, f1/20.  Key is the focus...spend time dialing it in.  Hard with the orion focusers; need to try the feathertouch on the obsession.

Oh, and grabbed the red spot just starting to make an appearance before I pumpkined.

# 8-29-22 Morning - Jupiter and Saturn
Woke up at about 2:30 to take some pics of jupiter and saturn.  Jupiter was nice and high in the sky, but I was a little late for saturn....it was about 23 deg up.  Note that if I do midnight, I can get that up to 34...and jupiter was at 50 deg up.

Did a couple sets...started with Jupiter at an ISO of 400 and F1/80 (12.5ms).  Stacked 157 images; used 33% that were above the 50% quality line.
Jupiter try number two was with the ISO cranked to 6400...meaning I could take the speed down to F1/1250 (or 800us).  Had 205 frames of this...but quality was *MUCH* worse.  (25% av rather than 50%).  Used 33% of the frames again...didn't stack well at all.  Weird artifacts.  

Now, saturn.  
ISO 400 with f1/15 (66ms).  Stacked 170 frames; quality level was back to decent...about 1/3 above the 50% line, so stacked 33%.   Chromatic ab with this, so I went to creating luminecence to remove that artifact.  Also took out the first couple test pics...which altered the quality curve, so I stacked only 25%.  Okay result...no A-gap.

Next, the 6400 iso (f1/160 or 6.25ms).  128 frame stack.  Quality graph much better than the jupiter one...I wonder if I had test images that were messing things up there.  End stack result was the same as with the lower iso...maybe a hair better.

Went back and tried to be more selective on the 6400 jupiter...yup....quality graph much better.  took top 25% (of 200).  Hmmm...still had the blotch.  And higher iso is definitly grainer.


# 5-8-22  V3 EQ thoughts

Time to start thinking about the EQ platforms again.  My main problem right now is slip...both with the big VS platform and the smaller pan-tilt.  The effect is less pronounced with the smaller one (I can usually get 2ish minutes of exposure), but would like something more solid.

My current diagnosis is that the drive between the "wheel" and the "wedge" is the problem...it's a friction mount.  Instead of going cable drive, I'm thinking of trying a direct gear on the rotation point rather than the wedge.  I'll start with another rev of the small platform, get it happy, and then upscale.

Soooooo...first questin is gears.  Servocity has 27:1 worm gears...if I get two of those, I can get a 729:1 gear ratio.  Add in a 5:1 driver, and I'm in the 3000s.  Now, some math:

The original cs mount had an outer wedge circumference of 57.0325" (18.154" diameter).  
This was being driven by a .3125 diameter bearing, which then gives you a gear ratio of about 58.  
That then had a 5:1 with the stepper...putting that ratio up to about 290.  

Soooo....that means going with the 2 worms will be already more than my 290...in a compact form factor.  I think I like it...

...and, if I need more, I can go to that planetary gear.  It's got 10180 steps per rotation (rather than 3200 for the standard stepper).  

Next, I'm gonna need to see some pixel drift.  Probably want something around the celestial equator...and use the T7 telephoto zoomed in.  I've got some of those measurements below, but would be good to double check.

Then, may be interesting to see if I can get the travel scope "stable"...but using the T7 rather than the Pi.  Check pixel drift there.

Step size is going to be an interesting goldilocks problem.  
Too big of a step, and you could have pixel drift between steps.  
Too small of a step, and you could have error with the controller.  
My gut feel is that I want something in the ~10ms range.

------
Another thought:  do I try and incorporate some sort of finder into the pan-tilt?  Maybe a laser pointer, maybe a dovetail for the orion finder?

And another crazy experiment...is the stellar "focus point" going to be at the same place for each "zoom" on the lens?  Put another way, can I figure out where my "nuts on" focus is for the telephoto zoom, and remember it?  Maybe even remember the stop point for each end of the two lenses?


******
# Camera focus by computer
* Lens goes to autofocus
* In live view screen:
  * Depth of field preview is ON
  * Quick Mode/Automatic mode is OFF
* should see "MF" on EOS screen.  If not, you should be able to toggle it.
* Looks like 6 << jogs == one <<< jog.

*****

# 5-5-21
Camera out in lafayette.

Align was tricky...the camera live-view didn't pick up on polaris.  Instead did it by taking two frames and comparing through the mac "finder" window...not too bad.

The computer controlled focus kept jumping back to the "auto" mode...even though the settings said differently.  Means that to get a crystal focus, I really need to decrease the aperature (f10), meaning more exposure time.  The more I'm zoomed in, the harder the focus.  Although I *can* get it with smaller ap values...

Got decent leo triplet, whirlpool, and herc.

Oh, and dew was an issue.  That might have been some of the trouble with my polaris align and focus...



*****
# 4-4-21
More VS EQ tests....confirmed app and program were happy during the day.  I'm a little worried that my 15 min calc was off.

Aligned, did some experiments on Mizar and Arcturus.  Tracking did not cancel the motion...and was tough to get it to go faster to "reverse" the motion.  Playing with Arcturus, looks like 26ms was the "still" speed...but wasn't consistent.

Switched over to the T7...got some pics for measuring raw pixel drift.  Note:  focus point for barlow is almost all the way out, but camera liveview does decent here (unlike for lenses).  Turned on tracking, same issues.  Took a peek at the bearings, and yup, tape is having issues.  I'm gonna need to do steel.  :(

Practiced Leo triplet, sombrero, and whirlpool hops for next fraser adventure.

Pixel drift measurements:
10s Mizar = 420 pixels.
20s = 807
30s = 1220

## other "post" notes
Did another series of tracking tests inside.  While it looks like the 15 min quick steps "mostly" goes the distance I want, when I change it to the 42ms per step, it only moves half way.  

My theory:  there's enough slip/friction that every slow step doesn't really catch on the wedge...in fact, it looks like we only go about half way...which would correlate to that 26 ms number above...and wouldn't give us an accurate track.

Tried doing a cable-drive...the cable tangles without the channels.  Putting that on hold.

Tried moving the bearings inwards to reduce the angle between wedge and bearing (and got more plasma cutter practice).  Still have some slip...need more tests after I tighten everythiing down.  

Should try the planetary again...are more/smaller steps more resillent to slip?  (overcome friction?)

Or, is it time to go with a circle segment for simplicity...


*****
# 3-31-21 Galaxy Prep (lafayette)
Dragged out the camera and EQ tonight.  Notes:
* Even cranking shutter speed doesn't let you go past a certain point...so it's easier to just take pics and look at them when star-hopping.
* You really want to start with the small lens, center the object, then switch to telephoto.  Knowing the star hops helps.
* Played some with the computer controlled focus.  I think this is gonna be the way to get pin-point....will learn how many "clicks" for each lens position
* Leo triplet:  look for the stick under Theta!
* Whirlpool...yeah, probably one of my more famliar hops

...and then the laptop battery didn't like the cold, and I powered down everything by mistake when trying to plug it in.  Calling it a night...

### Post observe math
m51 @ 75mm was 50 pixels long...giving me about 13 arc seconds per pixel.   Previous calcs were at about 10...
At 300mm we've got 182 pixels...giving me about 3.6 arc seconds per pixel.  Previous calcs were 2.7. 

Those are both pretty close...


*****
# 1-31-21 Travel scope night tests
Notes from tonight:
* I'm getting better at the polar alignment
* even with pan-tilt, travel scope is WAAAAY too hard to point.  Time to go to the big EQ platform and do this with the dob...point with eyepiece, turn on tracking, then go to camera.
* The delay on the RPI cam is annoying.  Wait 6 minutes for a 1 minute exposure???
* On my 60s pic, I had a weird "dual mode" star thing going on.  Either vibration or I may have gotten stuck...
*****
# 1-30-21 Travel Scope Daytime Tests
With reducer, it takes 5 "nudges" to move an object from one side of the frame to the other.  Looking at the app, each (cw or ccw) nudge is 1 micro-step.  Math:
```
200 steps in a rotation
16 micro-steps in a step, means 3200 micro-steps around the circle (360 degrees).
Means each micro-step is 360/3200 = .1125 degrees, or 6.75 arc minutes.  
5 nudges means my FOV is 33.75 arc minutes wide.
```
Note that *doesn't* match my 70 arc-minute calculation...off by about a factor of 2.  Dug up a pic of the moon from 11/4:  moon was 1790 pixels in diameter.  Checking ephemeris:  moon was 1788 arc seconds.  That's pretty close to 1 pixel per arc second.  :)

I'm also worried about vibration.  Just typing at the chair made the scope wiggle...and it would eventually stabalize.  Is the action of the stepper gonna be too big a vibration?  What about wind?

Plan:
* Align on polaris with picam (wide field)
* switch to travel scope config (with reducer)
* star no-track streak: 10s, 30s.  Capella?
* star track test

Optional:
* M1 with and without ultrablock.
* M35
* M42 - travel scope
* M42 - try filter on T7

And, of course, I got clouded out...

*****
# 1-14-21 T7 Prime Daytime tests
Need to use 2x barlow to get prime focus.  :(

Crosspiece is 2227 pixels.
It's 540 arc seconds.  
Meaning we get 4.17 pixels per arc-second...more than Picam prime, but less than picam + barlow.

6000x4000 pixels gives us a FOV of 24'x16'.

*****
# 1-12-21 Daytime tests
## Laptop camera control tests
### Exposure
Looks like you can set the exposure (shutter speed) in manual mode and get increased brightness.  Bulb mode doesn't do anything.  To try at night:
* set ISO to 6400
* set Aperature to as wide as possible (smallest number)
* set Focus to infinity
* Set exposure (shutter speed) to at least 1s.  Should be able to go up to 30s...curious to try it.  

Do dark room test to confirm.

### Focus
To control the focus manually:
* Make sure switch is set to AF
* Want quick mode.
* Want manual selection, with OFF yellowed out.  If you turn this to ON, it tries to autofocus.
* Then, you can use the dial on the bottom to control focus.

*****
# 1-6-21 Fraser
Successful, albeit cold session from Fraser.  Here are my notes:
* Single digit night!  Means ski base layer, balaclava, hand-warmers...but next time, need better foot warming.  Boots?  Hand warmers in the shoes?  Note I *was* out there for about 3 hours...
* I can get polaris from the front deck, looking over the house.  Didn't try the vid mode (forgot about it)...still tough seeing the stars on the view finder.
* Temperature is an issue!!!  Camera did okay with full battery, but phone and laptop eventually decided it was too cold.  Phone could go in a pocket with a hand-warmer, but I needed to plug in the laptop...which means the power strip was full.
* Pan-tilt assembly needs to get soldered.  I think I had one case where a wire came out...and I had to move it inside to debug (mostly because of the cold).  I had some weird stepper effects as well...not sure whether that's due to a loose wire or the raw temperature.  
* Thinking about combining the pan-tilt with the eq driver...less hardware.  Probably a project for *after* I have my motor boards back.
* Did the experiment with streak...and the math is working out.  The elongated streaks from last time I bet were just vibration.
* Tried the manual focus control from the app (which requires autofocus on).  Had a case where it tried to focus itself...need to play with that to get it happy.  Could deal mostly by hand to get stars in focus, but it would be nice to have that final layer of control.

Future to-dos:
* check vid mode for align
* solder pan-tilt
* combined mount?
* safeties on the eq platform
*****
# 1-3-21 (night) Orion!
## pan/tilt
Pan/Tilt app completed durning the day.  Will want to tweak it...need something between a "nudge" and "go" that only does a little bit of a frame.  My math:
* 300mm (telephoto zoom in) FOV = 4.5x3 degrees.  Want steps of maybe half a degree for this?  200 steps * 16 microsteps / 360 degrees = 8.88 microsteps / degree
So maybe 4 steps pan, which means 20 steps tilt (because of the 5/1 gear).
* 75mm (telephoto zoom out) FOV = 16x10 degrees.  Steps of 2 degrees for this field?  18 pan, 89 tilt?

## Step 1:  no tracking
Started with Orion, no track.  The live view finder doesn't seem to react to aperature, so you can only barely see the brightest stars.  Still, was good enough to get my alignment on orion's belt.  Start zoomed out, took some pics.  
* 80mm gave both the belt and the sword, but even at 2s had pixel drift (looks like ~21 pixels)
* when zooming in with the telephoto, need to make sure target is centered in FOV first.  Because Live-view doesn't give full resolution, you need to do sample pics to get there.  Same for "star hopping" from your start to destination...but having a bigger, deteriministic "nudge" will help here.
* 300mm framed the nebula nicely.  
Which meant it was time for the EQ platform!!!

## Step 2: tracking!
Since the live view stars are dimmer, alignment is a little tougher.  The good news is that polaris *does* show up...and so I walked through my alignment just fine. 

I had noticed slip in the EQ bearings depeneding on where the camera was placed...so another test (which I think I'll always do now) is to generally point the camera at the target, and then go through "fast motion" to make sure we have no slip and the camera is stable.  Can then turn on "slow motion", (93ms for the circle EQ platform) and reset by hand...no other adustments needed.

Pointed over at orion, and...yeah.  Works great!  Notes:
* setup is very suceptable to vibration...so avoid wind and be light with your live-view clicks.  
* Focus is tricky to get spot-on.  Infinity got close, but I had to back it off by just a smidge to get it relatively crisp.  Note that closing down the aperature (bigger number) helps with that, but then you need to compensate with a longer exposure.
* speaking of focus, I did notice a couple shots where a star was bright in the center with dimmer "wings" that appered to be along the tracking line.  I'm wondering whether 93ms gives you enough drift to hit this kind of pixel effect....will need to do the math.
* was able to get the flame (barely!) but can't see the horsehead.  Need filter (waiting on step-down ring) and darker skies.

## Other randomness
I wonder if using a vid with preview mode will let me do alignment better than the live-view shot...need to experiment with that.

I should probably put safety "pins" in the circle EQ to prevent it from walking off either forward or back.  Can do this as a hole with nails so that they can be removed. 

One final note...the camera's battery does not like the cold!  Most of the session had "low battery" warning...and now I've got half strenght.  Need to look at the docs to see whether I can run with external power or heat the bottom or something else...but in any event, I'm going to want another battery.

## To-dos:
* safety device on EQ platform
* Math on 93ms pixel drift
* Tweak pan/tilt app for bigger nudges
* Try video preview

# 1-3-21  Early morning T7
Was going to go out and play last night, but too cold.  Woke up early, and did some tests from the living room out the big window.  Notes:

* Remember that smaller aperature F number is *larger* aperature.  So F5.6 is the widest (most light) my cam will go.
* ISO 6400
* Canon screen and EOS utility doesn't give as good a "live view" as the PiCam. You can see bright stars, but if you really want to check out where you are in the sky or fine tune your focus, you've got to take sample pics.
* The EOS utility lets you save pics to disk rather than SD card.  Very handy for the aforementioned preview.
* For basic alignment, start with Telephoto as wide as possilbe (zoomed out), F6ish apaerature, and 2s shutter speed.  The webcam tripod thing doesn't work very well...time to finish the pan-tilt.  Want focus at infinity for starters (all the way counter-clockwise).
* as you are zooming in, you may need to tweak the focus just a hair.  I went a little clockwise...and did some experimental pics to get the focus as close as I could.  Note smaller aperature gives tighter focus...so trade off aperaature with shutter speed.
* The camera does a good job with meta-data...in addition to ISO, aperature (f/5.6), shutter speed, it also knows which lens is on it, and what zoom (focal length) you are using.
* Will definitly need the eq platform.  5 second pic at 300mm gave a streak of about 32 pixels.  30s shot brings that to about 190.  Just a light smudge on the 2.5s shot.
* Wait time is SOOOOOOOOO much better than with the pi-cam.  Pics are ready less than a second after the exposure is done.

Next steps:  
* Finish pan/tilt
* Try Orion...zoomed 2.5s gonna be enough?
* Maybe beehive or double-double or perseids
*****
# 1-2-21  More T7 measurements
Wide-angle:  crosspiece is about 10 pixels.  Since it's 540 arc-seconds, that's 54 arc-seconds per pixel.  That means the widest FOV I've got is 6000 x 54 by 4000 x 54...90 Degrees by 60 degrees.  WIDE swath of the sky.

58mm Zoom:  crosspiece is 37 pixels.  Math works out to 15.88 arc-seconds per pixel.  That FOV is ~26 degrees by ~18 degrees.

Picam looks to be 22 degrees by 17 degrees...so a little narrower than that 58mm zoom...but worse resolution...about 20 arc-seconds per pixel.

Telephoto zoom out: crosspiece 56 pixels.  9.64 arc-seconds per pixel.  FOV:  16 degrees by 10.7 degrees.

Telephoto zoom in: crosspiece 198 pixels.  2.73 arc-seconds per pixel.  FOV:  4.5 degrees by 3 degrees.

*****
# 12-25-20 T7
Canon EOS Rebel T7 camera specs:
* 6k x 4k pixel field
* Telephoto moon shot yields 670 pixels
  * Ephemeris:  Moon is 1770 arc-seconds tonight
  * Means 2.6 arcseconds per pixel, or .38 pixel per arcsecond
  
  
Full field:  6000 x 4000 pixels, or 260 arcminutes by 173 arc minutes, or  4.3 by 2.8 degrees
*****
# 12-6-20 VS-11

## Daytime
Got the VS platform assembeld...motion tested inside during the day under load.  Comments:
* The planetary stepper is a little louder than the straight NEMA-14.  Had to tweak current to get it in a happy place.
* Motion on the wedges works for about 30 min...too far to one side, and the wedge is at about a 45 deg angle to the bearing, and the bearing can't quite move it.  
* That slip has a good news though...I can use that for polar alignment
* Speaking of polar alignment, I don't have feet on this thing yet (and it looks like the north end is a little lower than I want).  I'm going to shim it with blocks tonight under south...should be workable.
* Scope motion doesn't seem to shift the platform, as long as I'm generally careful.
* I'm curious whether the stepper induces vibration to the platform.

Tests:
* Start with polar alignment.  Going to try and use the finder for this rather than the pi-cam
* Pick a star (or mars!)  Start with a wide lens, and check the drift visually.  Turn on tracking; any vibration?  Hows the track speed?  Play with going to 14ms and 12ms...any noticable differenence?  
* Switch to higher mag...8mm ethos?  How are the effects?
* If all is good here, try lining up M52.  Start visually...bright enough?  If decent, try pi-cam with reducer.

## Nighttime
Started with polar alignment.  My presentation notes are *backwards!* I'm not sure why...but when you look here, you see the corret stuff:
http://www.astrosurf.com/aheijkoop/Equipment/EqPlatform.htm

Did my tests on Alcyone in the Pleiades...it's got a good triangle asterism nearby.  Started with 25mm plossi...siderial drift wasn't fast enough.  Switched to the 8mm ethos...could see the stars moving downward.  Turned on tracking...didn't seem to do anythiing.  Played around with it, finally going to "fast", and found that I wasn't actually moving the platform.  Fixed that, went back to fast, and observed Alcyone going "up" (yay!)  Definitly had some "slip" in the bearings.

Next steps:
* Verfy pulse timing on the scope.
* Tweak code to allow for us delays...and allow for various step sizes.  Also change such that we're doing a delta-t measurement rather than straight delay...that should make this more robust.
* Need a better bearing/wedge interface.  
  * First try adding aluminum
  * Do we have to go with Gunter's cable solution?
  
*****
# 11-30-20 Max's Camera
5184 x 3456 pixels.

Crosspiece is 29 pixels.  From earlier calcs, it's 540 arc seconds.  That's 18.62 arcseconds per pixel.  For comparison, the picam is 24 pixels for the crosspiece...or 22.5 arc-seconds per pixel.

This means that his camera's field of view is 5184x18.62 = 26 degrees by 18 degrees.

*****
# 11-25-20 Pan/Tilt notes
Got a Pan/Tilt kit from Servocity with a couple HS645MG servos.  Goals:
* Check out their design...may leverage pieces I like into my own pan/tilt
* See if servo control is sufficient for moving the travel-scope
* If I can get a stable star focus, check out the circle EQ platform at mag.

Design notes on Servocity's implementation
* the tilt platform is not along the COG...meaning that you are definitly torquing the servos.  Those 645s struggle at certain angles...and you can get jitter, even when running ext power.  
* For building the platform, they have you screwing in directly to the ABS plastic.  This isn't great, and means you get some slop in some of the connections. Go with heat set inserts!
* At mag, a one degree servo jump is too much.  I want to go stepper here for finer control.  There's also a little backlash on movement...probably due to the force on the servo.  Also want to try to see if I can pass fractional degrees to the adafruit driver.
* could upgrade the servos to give more torque, but that's $$$.  The 645s were a little over $30 each, with a stall torque of 100ish oz-in.  If I up the input voltage to 6v, I should be able to get 130 instead...I want to try that to see if that's good enough (guessing not).  If you go to the 5585, you get 236 oz-in for ~$70 each....and that needs 7.4v input.

But even with that, this will probably work as a pan-tilt for *just* the pi-cam.


*****
# 11-08-20 Celestron Day tests
camera needs reducer to fit in eyepiece.  Think about getting a 1.25" c mount with filter threads.

Cross piece, with reducer:  2869 pixels.  Cross piece length in arc-seconds (from below):  540
2869 / 540 = 5.3 pixels per arc-second.

Comparason notes 
Mars, assuming 20 arc seconds:
* 10" prime: 72 pixels
* 10" barlow: 174 pixels
* celestron w/reducer: 106

...meaning if I can get the reducer out of the equation, I get even better pixels!!!


*****
# 11-05-20 Fraser
Timing for pics:
* 120s exposure takes ~12 min for preview to come up, and then 2 min for capture.  Subsequent captures take ~3 min.
* 60s exposure takes ~6 min for preview, then anoother min for caputre.  Subsequent captures take ~2 min.



*****
# 11-04-20 70mm 
## Daytime tests
As a reference, the full cross piece through the 10" at prime focus is 2000 pixels.  Using 3.7 pixels per arc-second, that means the cross-piece is about 540 arc-seconds long.

Now, moving to the 70mm.  The cross piece is 632 pixels at prime focus.  Divide by 540 arc-seconds, and you get 1.17 pixels per arc-second...or in a 12MP image,  57x43 arc-mintues, or a little less than a degree.  Note prime focus is a litte tough...the focuser screws don't really lock on.  Look for a c-mount-to-1.25" focuser thinggy?

Then, with the reducer (that has the cool ability to drop in a 1.25" threaded filter), we're at 521 pixels...or .96 pixels per arc second.  In that 12mp image, thats 70'x 53'.

## Nighttime notes
Scope is rough to point...and even harder on the platform.  Want a way to lock the platform down...maybe rubber-band between north bearings.

Tripod is too high on the platform...really shows why you want a proper CG.

Green laser finder for scope?  Telrad is too big.

Custom alt/az mount?   Knobs for alt and Az?  Maybe on a 4x4?
*****
# 10-31-20 Mars and the moon
Two notes for tonight:

* even though the focal reducer doesn't cut the image by as much as I'd like, it's still useful for reducing the moon pics.
* Mars is possible on a seeing 2 night.  Took LOTS of pics (231)...quality wasn't great on most, but ended up with a good result.  See https://docs.google.com/presentation/d/1H1rkcFj8JzOPGpRq9-oWSxdFA9BwbMzXrY6bOx8FGn0/edit?usp=sharing

*****
# 10-30-20 Night exposure testing
(Almost) full moon, but good transparency.  Played around with various exposure settings *WITHOUT* the eq mount to see base streak.  These were based on an area near deneb, so we're talking declination of 45deg21'32"

* 10s image shows almost no streak...maaaaaaaybe 5 pixels.  Note I get that when either doing auto mode or md 3.  
* 30s image streak goes to 17 pixels.  
*  60s: 36 pixels  
* 120s: 62 pixels
* 180s: 98 pixels

Did some exposure shots of longs in the full moon...Max suggested to shoot in raw for better post processing.   He's right. 

*****
# 10-21-20 More calcs
Full FOV, based on orion's belt calc below:  22 degrees by 17 degeees.

*****
# 10-19-20 Fraser
Dodged the smoke to get almost new moon...stitching issues because of the boil.  Will try later.  Promising stream of jupiter, but then clouds/high level smoke rolled in.  But, then woke up at 2, and got some good windows in the sky with the camera!!!

Did not need the tracking mount, even when  doing 180s (3min) exposures.  Best results were to aim at something bright with an iso 400 and 1s exposure, aperature at about half to make focus easier.  Nail in focus, then start opening up aperature and dialing focus.  Can also do this at 5s or 10s, but your feedback loop is slower...so I did that *after* the initial dial in.  

Curious...the pi viewer seems to see differences in exposures over 10s, but when I bring them to the mac, it looks like it's limiting them.  Double check...hmmm...yeah, may need to specify `-md 3` on the command line.
**----> CONFIRMED!** 30s pic takes about a minute.  180s pic takes 16 min(!) to load pipeline, then 7 min per pic.


*****
# 10-16-20 Calcs
Processing some older photos, including fraser pics from 9/14.

Did the jupiter calc for the 12":  on 9/14, jupiter was 42.6 arcsecods.  Single frame prime focus image is 184 pixels...which gives 4.32 pixels per arc-seconod.

10" was 3.58 pixels per arcsecond.

This *should* be the ratio of the focal lenghts (1200mm vs 1500mm).  3.58/4.32 ~= 83%   1200/1500 = 80%.  Close enough.

Fun note:  the 18" obsession is a 1905mm focal length beast...meaning we'll have around 5.6-5.7 pixels per arc second on the big scope!!!  Makes me want to break it out sooner rather than later.

*****
# 10-12-20 Early Morning EQ Tests, orion, moon

## Full FOV
Orion's belt spans 2.736 degrees.  In our full FOV shot, that's about 490 pixels...meaning we've got 179 pixels per degree....or about 3 pixels per minute.

Double check:  the moon was 1901 arc-seconds last night...that's 31.68 arc-minutes...meaning it should have been just under 100 pixels.  Confirmed!!!

## Tracking notes
Align on polaris went pretty well...ISO 400, SS 1 sec to get the focus right, then you are decent to align the cam.  Platform 40 deg and eq lineup was pretty close.  Went over to the moon...and yup...it tracks decently at 93 ms!  In 25 minutes, I only got a drift of about 6 pixels!!!!!  

Looking at Andromeda, I see an uncorrected drift of 83 pixels over about 2 minutes...meaning it would have drifed over 1000 pixels in that 25 min!  Put another way, I've corrected a factor of around 167...two orders of magnitude!!!  Note that this isn't entirely accurate; the moon was at declination 18 degrees, and andromeda was at 41...but that means andromeda should have moved *LESS* than the moon (becase of the fact it's closer to polaris).

One other note here...my 93ms-per-step calculation was based on a 24 hr circle...when in fact, it's a 23 hr, 56 minute circle.  That isn't enough to change my 93ms stepper delay number.

However, the moon's "day" is 24hr 49 min...which means I need to slow down tracking. (I'm now at 0.00064" per second rather than 0.00066").  Do the math, that's 96ms-per-step rather than 93!!!

## Design Thoughts
Had the drive bearing come out of it's bracket at about 26 min in...need to clamp both sides.  And I really want to do the vertical segment for weight....with a "single point" south bearing rather than angled.  Translation:  get rid of all those 40/50 degree cuts!!!!


*****
# 10-10-20 EQ Platform notes
To help with align, raspistill has a -fw option (focus window)
*****
# 10-8-20 Meh
Mars, Jupiter, Saturn.  Seeing on the 2 end of 2-3...got some meh shots.
*****
# 10-6-20 Mars in better seeing
Went out at around 10pm for a "quick shot" of mars...the seeing was supposed to be 3 on it's way to 4, so I wanted to see the differences between captures tonight and a couple nights ago (when the seeing was 2-3).

Long story short:  makes a huge difference.  Was able to do a 2x barlow on the prime focus...have to back it out of the focuser tube to get it to actually focus, but it's worth it.  Image *much* better.

Pixel calcs:
Mars processed 2x barlow pic:  197 pixels.
Mars processed prime focus from 2 nights ago:  80 pixels.  So that's a little more than a factor of 2.

Ephemerous data:
22.5 arc seconds on 10/4.  
22.6 arc seconds on 10/6 (this is the biggest it's gonna get this opposition)  

Calculated prime pixels around Mars' diameter:  81 (3.58 pixels per arcsecod * 22.6 arc seconds)

Barlowed pixels per arc second:  197 / 22.6 = 8.7  
**This is more than a factor of 2 because the barlow is backed out of the focuser...increases focal length of the scope.**  
Likely the same reason I'm only seeing a factor of 80% in the focal reducer.

*****

# 10-4-20 Image Processing Breakthrough and more targets
The big news of the day:  for planets, using PIPP+Autostakkert+Registax is MUCH easier and yields much better results than photoshopping.  See https://github.com/gsalaman/astro_notes/blob/master/planetary_stacking.md

Tonight's targets, in rough order:
* Jupiter and the GRS, with moon captures
* Saturn, with moon captures
* ISS pass
* M31 with "just cam" before moonrise
* "Double-Double" "just cam"
* Mars
* Moon

Collected both vid and 12MP pics of most targets...will compare the stacking results, but the vid stream seems much more efficient.
--> *Spoiler:  I like the results from stills better*

## ISS pass notes
Tried prime focus...size of ISS will be good in this format, but catching and tracking it will be **HARD**.  Got focus on polaris for starters...that worked well cause polaris doesn't move.  :)  I think my shutter speed was too great (Did I use 10ms?) as I got *way* to much streaking...and it was BRIGHT!  If I want to try this next time, I need to have my shutter speed down sub-ms.  Maybe go ISO 100 and 1ms shutter speed?

The other option is to try and get it afocal with the Q32...the good news here is I can shut down the aperature with the dial on the lens.  This might be an easier way to go.

## Sizing notes
From the ephemerous generator, jupiter has an equatorial radius of 19.97 arcseconds tonight.  That's a diameter of 39.94 arcseconds.  

Measuring a 12MP frame, I get about 143 pixels for equatorial diameter...which translates to 3.58 pixels per arc-second...a little off the 4.6 number in the 9/20 daytime tests below...but I think that's becase my arc-seconds for jupiter was off.

Taking a single vid frame from raspivid (1080p), jupiter is 65 pixels wide.  65 * 4096 / 1920 = 140...so that math works out.

This means that I get more than double the pixels (in one dimension) for doing stills...but then I don't get as many frames-per-second, as it's not continously saving.  

## Capturing Saturn's Moons
To get Titan, I needed to crank the ISO and exposure WAAAAY up:  
* ISO 800
* 500ms shutter speed

Going to a 1s shutter speed gave me some streak at prime focus.  
At 100ms shutter speed, you could only sometimes barely get Titan.

## Seeing notes
After post-processing most images, it's obvious the seeing isn't as good as it was a couple nights ago.  Still, got a couple decent jupiters...but the cassini division doesn't "pop" on saturn...and the mars details are a little fuzzy.

## M31
Grabbed this before the moon came up...but after playing with the image, it's obvious that light-pollution is gonna be the limiting factor.  <sigh>
 
*****

# 9-28-20 First tries with "just camera" plus bonus planets and moon
## Summary
* Good experiements with putting the picam on a mini-tripod and taking pics of the sky...had an almost full moon.  Targets:
  * Moon over the barn
  * Jupiter and Saturn to the south
  * Cassiopia
  * M31
* Tried new settings on moon, jupiter, saturn, and mars.  Wow!!!

## Night-Cam
Best results:
* Start with aperature all the way open and camera focused at infinity.
* raspistill with `-ISO 800` and `-ss 1000000` (1 second)
  * note this has preview on...
* at this point, play with your aperature (move it down) and zero in your focus to get the stars as a crystal point.

For the moon itself, I was using ISO=50 with a shutter speed of 20 ms.  Had to bring the aperature WAAAAY down to get the detail.

For the East background, I brought up the exposure time to 200 ms.  That gave me a lighter sky wth the barn and posts.

My best south one was a 10 second exposure with iso 800...and the aperature was fairly open, making a pretty bright pic.  I then adjusted the curves to bring the background darker.

Casseopia with part of the double-double:  ISO only 200.  Exposure 30 seconds.  Focus and aperature tweaked by hand...don't remembrer where they ended up.

M31:  just mostly guessed in the sky, and found a little smudge.  Yes, that was it.  :)  60s exposure, ISO 400.  I *think* the anti-shake algos are doing some tracking for me...no trails in the pic!




# 9-26-20 Exposure and ISO tests
-fp says use capture for preview...but it looks like it doesn't work.  Driver just bails.

Iso's checked:  50, 25, 10!!!  Wow!  So time to try the moon with that 50!!!

Top range ISOs:   it seems to allow 1600 and 3200, but I don't see a pic difference from the 800...so I wonder if the 50 iso is actually doing anything...next test...50 to 100, yes.  10 to 50...maybe, maybe not...but that's a super low iso.  Just keep 50 as my floor.

Okay, now long exposures.  takes a LONG time for preview screen to come up....maybe do these "no preview" (-n)
All seem to work!!!  I had to close down my aperature to get it so I didn't get all white, but I see the difference between 1s 5s and 20s!!!!  Note the image save time is significant...was more than a minute for the 20s exposure.  But, I think I'm ready to try some night stuff!!!!




# 9-24-20 First try with the reducer
## Quick EQ note
Okay, I need to prototype the equitoral platform.  Probably gonna make a new file to track my thoughts on that...but here's a good starting link:
http://www.reinervogel.net/index_e.html

## Moon Experiments
Reducer worked really well here...and doing the align with photoshop is cool!  

First stack try was based on auto-exposure and shutter-speed (base raspi-still command)...and so you have exposure time variances (15-33 ms) and ISO variances (40, 50, and 64).  This means the color and "feel" of the stacks are off...but I did some other "fixed" shutter speed examples.  Note that the ISO is considerably less than what I've been doing by hand...and the camera is compensating by doing a longer exposure time.  I wonder if that's gonna work on, say, jupiter...

Next, trying with different shutter speeds...but I'm MUCH smaller than the auto-expose ones above...which leads me to a higher ISO.  For example, I'm in the 1ms to 500us range...and my ISO's (picked by raspi-still) are 200-400.  The best set seems to be 5ms ss...and those give me typically 200-320 ISO.  This gets me closer, but it's still a little off...yes, photoshop can almost blur it, but it would be better if I didn't have to do this.

...and then I found the "auto blend" in photoshop...it does a great job!  Can't tell much difference between stack and panorama...but I'm tending to panorama after arranging images in "best to worst".


## Tough to get Jupiter

## Mars coolness

## Obligatory Saturn

# 9-20-20 Daytime Tests
## First test: wide view
Set up camera on the mini-tripod...and point it at something outside.  Goals:
* What's the FOV?
* How does the 1080p streamer shot compare with the full 12mp shot?


### 1080p vs 12mp
The 1080p image crops the top and bottom of the image...so you are losing some of your FOV.  The right-to-left is also slightly cropped.  That means, for telescope tracking purposes, the 1080p isn't the best mode to use for vid.  1080p is a 16:9 format; the 12mp is a 4:3.

Zooming in on the "telephone pole" top, I'm expecting about 2x the pixel density for the 12mp (1920 vs 4056).  Telephone pole cross-piece is 30 pixels in the 12mp version, and only 14 pixels in the 1080p...which, yup, math works out.  

### Full FOV
(gonna come back to this one)

## Prime focus
This is really an easy mode to set up and focus.  If I look at the cross-piece of the telephone pole, it's about 2000 pixels.  Put another way, going from no telescope to prime focus gives me a magnification of 2000/30 or about 67x.  And yes, prime from the streamer gives me a little less than 1000 pixels...so that 2:1 mapping is working.

### Mapping prime focus to actual mag
Looking at a past 12mp pic of jupiter, it looks like it's 193 pixels.  Ephemerous data says jupiter is currently 42 arcseconds. 
From here...note that this specifies *radius* rather than *diameter*  https://pds-rings.seti.org/tools/ephem2_jup.html

Quick saturn check as well...17.4 arc seconds for the planet.  That's a little less than a factor of 3.
https://pds-rings.seti.org/tools/ephem2_sat.html

So, if that's all correct, my saturn diameter should be 193 * 17.4 / 42 = 80 pixels.  Check: yup!!!

Which means 193 pixels / 42 arcseconds = 4.6 pixels per arcsecond.  
--> **NOTE:  Different result calculated on 10/04 above:  3.58 pixels per arcsecond for prime**

Okay, one more:  mars!  It's currently 21 arcseconds, so the pic should be 96 pixels.  Yup!!!  Note:  It's gonna grow to 22.5 arc seconds...but that's only gonna be a few pixels more.  

Last computation:  4056 pixels / 4.6 pixels per arcsecond means this view is 882 arcseconds long, by 661 arcseconds high.  The moon is about half a degree...or 30 arc minutes, or 1800 arcseconds.  That means it's somewhere around 3x bigger than our prime focus...which seems to work out...

This wiki site has various arcsecond sizes:
https://en.wikipedia.org/wiki/Angular_diameter

### Barlowed prime
First, some math.  If the barlow is indeed 2x, the full crosspiece from the telescope should be 4000 pixels...about the full frame.  Unfortunately, my pic is rotated...and I can go middle to one end (2500 pixels). Checking the original prime, it's 1049.  So that's a factor of 2.3.

Note:  to get the barlow to focus, I had to back it out by about 1 pinky width (a little more than a centimeter?)  Also tracking is gonna be *tough* with this...and getting a crisp focus is also hard.  So only do this for really good seeing conditions.

## Specific Afocal Eyepiece notes
### General
First, get a general focus with the eyepiece visually.  Make sure your camera aperature is mostly open...but may tweak later.  

Lining up:  I found best results doing the left-right axis first, making sure the camera lens is in line with the eyepiece.  Want to be doing this with a light shining in (or in daytime) so you can see the "circle" of light.  Then get a general top-bottom.  Then move the camera in...and that distance is eyepiece specific.

### Q32
Good, tight mount from bracket to eyepiece.  A little tricky to get image centered, but not too bad.  Focusing was crisp.  

Cross-piece was 500 pixels...so that's a little less than half of prime focus...meaning I've got 2.1x the viewing area...so I'm now at 1850x1386 arcseconds...or about 31x23 arc minutes.  I'm now right about full moon...a little smaller.  

FUN THING TO TRY:  STITCH THE MOON PICS TOGETHER!!!!

### 25mm plossi
Probably the easiest ep to set up.  

Cross-piece is 657 px...1.5x the viewing area of prime.

### 32 Nagler
Don't bother.  Hard to mount, hard to align...
523 pixels larger than Q32...just use that one.

### 12 Nagler
Don't bother.  Just barely fits in mount, focus is tough.  

Cross-piece of ~1600 pixels...that's somewhere halfway between barlowed prime and regular prime. 

### 9 Nagler
This one was easier to mount than the 12...and easier to focus, but it's gonna be harder to track.  
Gotta do my math from the other side of the cross-piece...this one is 1060 pixels, as opposed to 285 for the Q32 or 590 for prime focus.  Doing math, that would be 1357...so it's less than barlowed prime.

### 8 mm ethos
Too hard to get aligned...can't get close enough.

### 6 radian
Good zoom...decent to align, but it's gonna be difficult to track!!

For pixels, we've got to go to a new feature...a standoff on the main pole.  Here it's 1592 pixels.  1132 pix for 9mm nagler.  635 for prime...meaining it would be 1460 for barlowed prime.  

## Takeaways
For widest field, do the Q32.

Standard zoom:  just do prime focus.

Big zoom:  First try barlowed prime.  Then 9mm nagler (a little less).  Then 6mm radian (a little more).


# 9-12-20 More planet tests
5/4/3

Goals:
* See if paracorr reduces prime focus distance
  * No.  Increases mag a little bit...and only one setting gave good focus.
* See if barlow increases prime mag
  * Maybe...barlow wouldn't focus.  Too much with the extender?  Besides, it's tough to track already.
* Play with new shutter speed to see if I can get a better pic of saturn and jupiter. 
  * YES!!!!!  1500us seems to be the best of jupiter bands.  I think I used 5 ms for saturn.
* Stretch goal:  will 1 second exposures get me dark sky?
  * Could *barely* get M13 at prime focus...if we're gonna do dark-sky, we need a tracking mount.  And probably equatorial.  Too much star-streak with prime focus.  Went to the 25mm plossi and afocal...1 sec had just a little streak, but anything more had way more. 
  
Also played around with trying to get the ring nebula...visual inspection showed it's *WAY* too dim for this method.  Double-double:  FOV was too narrow to really get this to pop.

Afocal:  shine red light into telescope tube to help camera alignment!!!

Note:  raspistill embeds ISO and ss in the jpg.  Want to modify astro_streamer to do the same.

Next step:  play with stacking on some of those jupiter and saturn images.

Future investigations/experiements:
* JUST tripod darksky...long exposures.  
* Mallincam research - tracking needed?
* What would it take to add tracking to the obsession?
* How much differenence does a bigger mirror make.
* Afocal: 
  * can I get the Q30 working?  Maybe try during the day.
  * Build a better rig:
    * fits on bigger eyepieces
    * swing camera in and out for checking
    * gear mechanism for fine adjustments?

# 9-11-20 PM - Planets and live stream tests
Started with align & setup; streamed saturn first.  Worked well!  May want to do a focus on a bright star next time first.
Iso 400 seemed to be the key. 

Jupiter next...a little bigger.  ONLY played with ISO...longer ISO gave me moons, but washed out bands.  Turns out you want different settings for each...see optics notes.

Tried afocal.  Tough to get the lens aligned in the dark, even though I'd practiced previously.  Many tries...unable to get decent image.  I think I need a better mount if I'm going this way.  Issues with current mount:
* doesn't fit well around bigger (nagler) eyepieces
* up-down-left-right hard to do in dark...and you need to be normal to the eyepiece plane.
* ...and the pi keeps getting in the way...

Tried prime on some deepsky...no good results.  I think I need to up the exposure time.  Add that to astro_streamer.py.

Note seeing tonight was a 2...so we had a bunch of boiling.

# 9-11-20 AM - More moon
Woke up early, tried prime and afocal with the moon.  I had practiced setup the day before.  I kept ISO at 400...seemed to do well.

Prime was super easy!  Take off the lens, stick the camera in the eyepiece, and off you go!  

Tried a couple eyepieces with Afocal:
* 8mm ethos:  good zoom.  May be what I use for planets
* 17 nagler:  very similar to prime focus.
* 26 nagler:  could get most of the moon in the camera FOV.  Didn't have the secondary shadow issues we had previously...maybe a better align?

Didn't have time to try the 32mm nagler...but I bet that hits the whole moon.

Keys to make Afocal easier:  
* focus goes to infinity
* aperature wide open

Challenges:
* Object centering.  Next time, do the full dual finder align.  That way you can track with the finder scope.
* Stream lag:  very likely due to laptop and pi on different wifi networks.  This made tracking and focus harder
* Focuser on the 10" isn't greaat.  Means use the feathertouch on the obsession when you *really* want good pics.
* Pi attachment.  Battery works well, and can be on the table, but with the short camera ribbon, the pi needs to be on the scope.  Figure out a better mounting system, and/or buy a longer camera cable.

Ideally, I think I want the streaming app to be able to take pics.  Look into dual streams for Picam and see if I can make that happen.  

Can't use VNC for default camera preview, but could I make an app that opened a "view" window?  The only alternative is to go keyboard, mouse, and monitor with the pi...yuck!!!


# 9-8-20 First experiments: Secondary mirror shadow?
On our first experiements, we got secondary mirror shadow with the moon.  Setup was:
* 10" orion 
* Afocal setup with canon DLSR & cell phone cameras
* 27mm nagler

Later research said to do ISO at 200 or 400 for the moon.  Focus should be at infinity.  Play wth aperature until you get something that looks good.

For the shadow, the best explanation I found was here:
https://www.cloudynights.com/topic/362932-secondary-obstruction-in-afocal-astrophotography/
(check out midnight dan's explanation)

Tried during the day with smaller eyepieces...the 17 nagler didn't look like it had the shadow with the phone.  Gotta try it with other eyepieces...
