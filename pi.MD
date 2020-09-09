# Loose requirements
Here are few modes/functionalities I'd like to experiment with:
## Imaging
With the HQ cam, it looks like I can do both prime focus and Afocal photograpy.  Try both of these in the daytime.

I'm going to SSH into the pi use `raspistill -k -o <file>%04d.jpg` to create the actual image files. 
Means adjusting the ISO via command line.

Play around with stacking.  How does photoshop do?  Is there a better astro stack program out there?
## Streaming
First phase is to just see what the camera is seeing.  I've got a simple script [here](https://github.com/gsalaman/simple_stream) that goes out port 8000.  And, I've got the hole in the router such 
anyone can log into my comcast IP at port 8000 and it tunnels to the pi.

Next step on the streaming app:  Add mqtt control to allow for adjusting the ISO on the fly.  Then I can add other params. Then, try adding an mqtt command to allow for me to take pics...that way I've got streaming and imaging at the same time...cool!!!

## Real time image stacking?
Can I use python and openCV to do this?  Check this link out:
https://github.com/maitek/image_stacking

Or, instead of CV, you can use scipi:
http://prancer.physics.louisville.edu/astrowiki/index.php/Image_processing_with_Python_and_SciPy#Correcting_and_Combining_Images


# Hardware notes
The HQ camera itself has a standard tripod mount, so I can use that for Afocal photograpy.  

When I remove the lens, the outer cover fits into a 1.25" eyepiece...I think I can use that for prime focus.

With both of these, the pi would be dangling by the camera cord.  I think I can go ghetto to start and put it in a little bag...but I'd also want batter.  Gonna see how much time I can get out of the portable pack.  

Eventually I could add the touch screen on the Pi to remove the laptop.
