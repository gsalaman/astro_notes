# Planetary Image Stacking

## Intro
Image stacking is the act of taking multiple pictures and using the best parts of each one to create a composite image.  This doc describes my findings.  We'll be using the following tools...all freeware, and all windows-based.  (although folks say they will run under wine)
* PIPP (Planetary Image Pre-Processor)
* Autostakkert (Image stacker)
* Registax (For wavelet corrections)

## Capture Strategy
There are two similar flows depending on your capture strategy.  Better pictures or videos generate better results, so aim for nights when the seeing is good.

### Video Capture
Most imagers capture a video stream.  This has the advantage that you are automatically grabbing many frames per second (depending on your setup) which gives a better chance of a good frame.  The picam's video stream is a 30 fps 1080p...and we can adjust ISO and SS as the object demands.  Start a capture with raspivid like this:
```
raspivid -t 0 -ISO 50 -ss 10000 -o outfile.h264
```
The `-t 0` means it'll capture until you hit ctl-c.  

### Frame Capture
If you want more resolution than that 1080p stream, you can use `raspistill` to grab frames, like this:
```
raspistill -k -p 1200,100,640,480 -ISO 50 -ss 10000 -o outfile_%04d.jpg
```
This gives an offset preview window, and takes pictures on keypresses until an "x" is entered.  Because you are manually taking the pics, you have fewer candidate frames than with the video option, but typical still sizes are bigger than a video frame.  For example, the picam's default still size is 12 MP (4k by 3x) which gives you more than double the pixel density in any dimension.   More pixels means it's easier to see features in your frames.

### Tradeoffs
With my telescope at prime focus, a 12MP frame captures 3-4 pixels per arcsecond...meaning jupiter's diameter is somewhere in the 150 pixel range.  Going to video, this shrinks to about 70ish pixels..and each pixel counts.  Because of this, I prefer the frame capture method to video capture.

-----
## "The Flow" - still frame version
Here are the steps I've been having success with:
* Get the stills off the Pi and into a directory on the PC
* Use PIPP to crop and center each image
* Use Autostack to generate a stacked output from those cropped files
* Use Registax to enhance the stacked output

### PIPP - Planetary Image PreProcessor
* Put all of your JPGs into a folder.
* Open up PIPP.
* Select "Add Image Files" button (bottom left), and select all those JPGs.  
  * You should see the output frame pop up in a separte window
* Click `Planetary` under `Optimise Options For:`
* Go to the `Output Options` tab and select BMP as the output format.
  * You can also do AVI if you want...this gives one file rather than many...and looks like they take the same disk space
* Click on the `Test Options` button on the top right
  * The output frame should show you a single frame of what we're dealing with.
* Go to the `Do Processing` tab and click `Start Processing`
  * This will take a little bit, depending on how many frames you have.

You can now close PIPP and open Autostakkert.

## AutoStakkert - Stacking program
* Click on `1) Open` and select the output directory from PIPP.  
* If you exported BMPs:
  * Change the input type to "image files"
  * Select all those BMPs and click "open"
  * You should now have a reference frame in the output window.
* If you exported an AVI, you only have one file to open...that avi generated above.
* Click the `2) Analyse` button.
  * This should populate the quality graph. 
  * In the output window, you can move the slider at the top to "browse" through the candidaate images.
* Decide what frame percentage to stack
  * Really what you are doing here is throwing out the worst frames...you don't want any with streaky effects, and the bad seeing ones don't help either
  * I've had success with as few as 25% and as much as 75%
* Normalize stack...if you check this, it's doing an auto-brightness calibration for each frame...it takes the brightest, and calibrates evertying to the specified percentage of that brightness.  75% or 80% seem like they work well.
* Sharpen:  I find this usually introduces a little too much noise in the pic....and the wavelet processing in the next step tends to do enough.  Play with it if you want...
* Drizzle: This will increase your image size, using some sort of pixel interpolation.  I've found best results keep this at "off", but some folks like doing 1.5x drizzle and then shrinking the output image at the registax save point.
* Go to the output window and pick alignment points.  
  * Close to edge to help with things like saturn
  * 24 is a good default for number of align points..see how many it produces.
* Now you should be able to click `3) Stack` in the main window.

You should now have a "fuzzy" image of your planet, but happily stacked in an AS_* directory.  You can now close AutoStakkert.


## Registax - wavelet correction
* Click `Select` (top left) and pick that stacked bmp.
* Go to `Wavelets`
* We're gonna do 6 layers of wavelet adjustments.  Layer 1 should be .6 for both Denoise and Sharpen, Layer 2 .5 etc down to .1 for Layer 6.
  * Once you do this, you can save this config so you don't have to keep typing them...
* Move the Layer slider bar to make the image look good.  
  * Start with Layer 1 and see how far right you can move it. 
  * Repeat with Layer 2...but note you probaby don't wanna go past where layer 1 was.
  * ...and repeat till yer done with all of them.
* You can adjust brightness and contrast here.  I have decent luck moving them both down a little.
* Click `Do All`
* Click `Save Image`
  
-----
## Video Flow
If you are doing videos, the flow is mostly the same...but you've got an added step of converting the .h264 file into something our toolchain understands.

## MP4Box
To convert an .h264 file into an MP4 on the Pi, you need MP4Box.  To install:
```
sudo apt install -y gpac
```

Then, to convert (well, wrap actually...):
```
MP4Box -add <source.h264> <dest.mp4>
```
## PIPP
PIPP will let you select that MP4 instead of a bunch of individual image files.  

The rest of the flow is the same.
