# Mosaic notes

Okay, so I've got 6 panels of M31.  Each stacked, flat-and-dark calibrated in ASTAP.  Tried running those FITS panels through ASTAP in image stitching mode...a couple issues:
* Panel 2 ends up being too light compared to the others
* There are image artifacts, I *think* from the fact that I need to crop the processed panels.

Next try:  save all 6 panels as pngs, then bring into photoshop to crop.  Pass the resultant PNGs back to ASTAP.

Hey, wait, before I try that, ASTAP says there's a "crop image" function in the stack tab.  Trying that first, so that I can stack the FITS.  Also turned off "equalize background".  5% crop (based on my PNG math), and then merge backgrounds on, limit background correction on.

Heh.  Nope.  That's officially crap.

Turning back on equalize background, doing 5% crop again.
JUST equalizing background.

