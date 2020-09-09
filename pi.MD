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
