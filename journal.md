# Intro
These are going to be my "raw photography" running notes...in reverse cron order (latest on top).
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
