
# ZWO 533 on TV-85

MATH:  206.265*(pixel size in um)/(fl in mm) = arc-seconds per pixel  
So, on the TV-85 with the 533 cam:  
(206.265*3.76/600) = 1.29 arc-seconds per pixel.  3008x3008 pixels would give 3883 arc-seconds of view, or just over a degree.  That matches.  

 
 | Setup | Arcseconds/pixel | Pixels/arcsecond | FOV | Jupiter | Saturn | notes |
 | ------ | ------- | ------- | ------- | ------- | ----- | ----- |
 | prime | 1.29 | 0.775 | ~65 arc-min square | 37 pixels |  | Confirmed with astrometry.net | 
 | 2x barlow | 0.645 | 1.5 | 32x32 arc-min  | ~75 pixels | | |
 | 3x barlow | 0.43 | 2.3 | 21x21 arc min | ~110 pixels |  | |
 | 4x powermate | .3225 | 3.1 | 16x16 arc min | ~150 pixels| | confirmed 3/25/25...but jupiter was only 36.8 arc seconds, so smaller |
 
 
 # ZWO 533 on Celestron Nexstar8

| Setup | Pixels/Arcsecond | Arcseconds/pixel | FOV | Jupiter | Saturn | notes |
| ------ | ------- | ------- | ------- | ------- | ----- | ----- |
| prime | .38 | 2.62 | ~19 arc-min square | ~130  |  | calc at 50 arc seconds | 
| 2x barlow | .19 | 5.14 | just under 10 arc-min square  | ~260 pixels | | |

Note this may also be good for smaller targets...but then the 10 arc-sec of periodic error may (will) affect long exposure.


# T7 Optics
| Setup | Pixels/Arcsecond | Arcseconds/pixel | FOV | Jupiter | Saturn | notes |
| ------ | ------- | ------- | ------- | ------- | ----- | ----- |
| 18 mm | 1/54 | 41 | 68 deg x 45 deg | | | astrometry.net calc | 
| 55 mm | 1/15.88 | | 26 deg x 18 deg | | | |
| 75 mm | 0.1 | | 16 deg x 10 deg | | | |
| 300 mm | 0.38 | 2.7 | 4.5 deg x 3 deg | | | confirmed with astrometry.net |
| Cel. Travel prime | | 1.92 | 3.2 deg x 2.13 deg | | | calc from astrometry.net |
| TV-85 prime | .78 | 1.28 | 2.13 deg x 1.42 deg | | | confirmed with astrometry |
| 10" prime |  | | | | | cant get prime focus.  Try 2" extender! |
| 10" prime barlow | ~4 | | 24' x 16' | ~190 pixels | ~175 (rings) | |
| 12" prime |  | | | | | |
| 12" prime barlow | ~5.2 | | | ~250 pixels | ~215 (rings) | |
| 18" Obsession | | | | | | |



# Orion 10" dob
1200mm focal length  
254mm aperature  
Focal ratio: f4.7 (1200/254)
Max useful magnifiction:  2x254mm ~500x.  Seeing will definitly limit that.
Mag = focal length / eyepiece mm.
So for 32mm nagler, it's 37x.

# HQ cam chip specs
6.287mm x 4.712mm (7.9mm diagonal)

# prime focus FOV
see http://www.johnrcrilly.com/LX200-14/FOV.pdf  

ONLY based on focal length of telescope and dimensions of ccd chip. 

decent approximation:  chip_mm * (3000 / telescope_fl)
So for the dob, it's 7.9mm * 3000 / 1200 or ~17 arc minutes.
Note the moon is about half a degree big, so that's 30 arc minutes.
This means prime focus will give me about *half* the moon...and may give
decent planets.

My math:  jupiter is around 50 arcseconds...so just under an arc minute.  That's 1/17 of our total FOV.
I think inserting a 2x barlow will double that.

Saturn is currently 18.3 arcseconds...about 1/3 of an arc-minute.   May be too small for prime focus.

10/21/20 Math:  
Doing the full CCD calculation shows we're 15.72 arc minutes by 11.78 arc minutes...so for 4056x3020, that comes out to 4.3 pixels per arc second for both dimensions....still a little big.  Did a double check on the moon from 10/04; 6600 pixel diameter, ephemeris shows 1763 arc seconds...which gives 3.74 pixels per arc second.  

# iso
Sensitivity of CCD sensor to light.  Lower iso is "darker" but less noise.

# aperature
Think of a piece of glass as a "slice" of space that is in focus.  The smaller the aperature, the thicker this piece of glass...but the less light coming in.
For astro, since you are focused at infinity, it's cool to open up aperature as much as possible...but if you are doing standard photography, you want to define how much of your shot is "in focus" vs "out of focus.

Usually expressed as "fstop"...a fraction.  F/16 means only 1/16th of the light is getting through...so bigger f numbers mean smaller light and "wider" range of focus.

# Planetary settings
From http://soggyastronomer.com/how-to-photograph-the-gas-giants-jupiter-and-saturn/

* ISO = 800
* Shutter speeds:
  * Jupiter's moons:  1 sec
  * Jupiter's bands:  1/20 sec (50 ms)
  * Saturn: 1/5 sec (200 ms)
