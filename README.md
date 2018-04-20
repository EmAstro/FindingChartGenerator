# Finding Chart Generator
This is a ugly and dirty bash code to automatically create finding charts from Pan-STARRS1 images (https://panstarrs.stsci.edu/).

The use is quite simple, you need a text file with your target name, RA, Dec (in degrees) and run:
./GetFc -i radec.txt
This will download PS1 images in z-band and create a simple FC.
More useful is the option -o. The script will go through the NOMAD archive, select a star close to your target, check over PS1 that this is indeed a star (calculating the classical aperture mag -PSF mag), and print the file OffsetStar.txt with coordinates of the target, coordinates of the star, r-band PS1 magnitude of the star, RA and DEC offsets in arcsec, and PA in degrees.

This script use massively ds9 (http://ds9.si.edu/site/Home.html).

ALWAYS double check the output, there is no warranty for absence of bugs.

You can check for options with:
./GetFc -h
