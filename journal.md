# Intro
These are going to be my "raw photography" running notes...in reverse cron order (latest on top).

# 9-12-20 More planet tests
Goals:
* See if paracorr reduces prime focus distance - jupiter?
* See if barlow increases prime mag - saturn?
* Play with new shutter speed to see if I can get a better pic of saturn and jupiter.  
* Stretch goal:  will 1 second exposures get me dark sky?  Try with M13 or andromeda.

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
