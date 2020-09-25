# Intro
These are going to be my "raw photography" running notes...in reverse cron order (latest on top).
# 9-24-20 First try with the reducer
## Quick EQ note
Okay, I need to prototype the equitoral platform.  Probably gonna make a new file to track my thoughts on that...but here's a good starting link:
http://www.reinervogel.net/index_e.html

## Moon Experiments

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
