# Combining color channels in Photoshop

I'm starting with a stacked Oiii and Ha image of the veil nebula.  Already curve adjusted....didn't use the upscaled ones for this.

First step is to align the two images.  
Open both separately in photoshop, then pick one to paste into the other.  
Do a transformation to align (turning down the top layer's opacity), and then crop and save the combined image (so that you can use the two layers as starting points for the color channel combine.

## Method #1:
Make the Ha layer the top layer.  Turn down the opacity, then go into levels and do a standard level adjustment to bring out the reds (I did just RGB)

## Method #2:
Copy the Ha layer from that combined image, and copy it into a new image.  Make that greyscale.

Then, take the Oiii layer from the combined image, and make that a new (starting) image.

Open up the channel menu (under window), and select ONLY the red channel.  Paste the greyscale Ha image here.

Make sure you are *JUST* selected on the layer, and then you can do a red channel adjustment to bring everyting up.  

Probably want to bring blue up a smidge to compensate for reddish stars.

Then you can do a general curve adjust to bring the black back down.
