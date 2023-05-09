# T7 Optics
| Setup | Pixels/Arcsecond | Arcseconds/pixel | FOV | Jupiter | Saturn | notes |
| ------ | ------- | ------- | ------- | ------- | ----- | ----- |
| 18 mm | 1/54 | | 90 deg x 60 deg | | | | |
| 55 mm | 1/15.88 | | 26 deg x 18 deg | | | | | |
| 75 mm | 0.1 | | 16 deg x 10 deg | | | | | |
| 300 mm | 0.38 | | 4.5 deg x 3 deg | | | | |
| Cel. Travel prime | | 1.92 | 2.2 deg x 1.5 deg | | | calc from astrometry.net |
| TV-85 prime | .79 | 1.26 | 80' x 53' | | | moon measurement |
| 10" prime |  | | | | | | | cant get prime focus.  Try 2" extender! |
| 10" prime barlow | 4.17 | | 24' x 16' | | | | | |
| 12" prime |  | | | | | | | |
| 12" prime barlow | 5.25 |  | | | | | | |
| 18" Obsession | | | | | | | | |



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
