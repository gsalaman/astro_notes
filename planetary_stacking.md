# Planetary Image Stacking

## Intro

## PIPP - Planetary Image PreProcessor
* Put all of your JPGs into a folder.
* Open up PIPP.
* Select "Add Image Files" button (bottom left), and select all those JPGs.  
  * You should see the output frame pop up in a separte window
* Click `Planetary` under `Optimise Options For:`
* Go to the `Output Options` tab and select BMP as the output format.
* Click on the `Test Options` button on the top right
  * The output frame should show you a single frame of what we're dealing with.
* Go to the `Do Processing` tab and click `Start Processing`
  * This will take a little bit, depending on how many frames you have.

You can now close PIPP and open Autostakkert.

## AutoStakkert - Stacking program
* Click on `1) Open` and select the output directory from PIPP.  
* Change the input type to "image files"
* Select all those BMPs and click "open"
  * You should now have a reference frame in the output window.
* Click the `2) Analyse` button.
  * This should populate the quality graph. 
* I like picking 1.5x drizzle (bottom right)
* Go to the output window and pick alignment points.  
  * Close to edge to help with things like saturn
  * 24 is a good default for number of align points.
* Now you should be able to click `3) Stack` in the main window.

You should now have a "fuzzy" image of your planet, but happily stacked in an AS_50 directory.  You can now close AutoStakkert.


## Registax - wavelet correction
* Click `Select` (top left) and pick that stacked bmp.
* Go to `Wavelets`
* We're gonna do 6 layers of wavelet adjustments.  Layer 1 should be .6 for both Denoise and Sharpen, Layer 2 .5 etc down to .1 for Layer 6.
* Move the Layer slider bar to make the image look good.  
  * Start with Layer 1 and see how far right you can move it. 
  * Repeat with Layer 2...but note you probaby don't wanna go past where layer 1 was.
* Click `Do All`
* Click `Save Image`
  

