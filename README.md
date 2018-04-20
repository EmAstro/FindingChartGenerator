# Finding Chart Generator
This is a ugly and dirty bash code to automatically create finding charts from Pan-STARRS1 images (https://panstarrs.stsci.edu/).

The use is quite simple, you need a text file with your target name, RA, Dec (in degrees) and run:

./GetFc -i radec.txt

This will download z-band PS1 images and create a simple FC.

More useful is the option -o. In this case, the script will go through the NOMAD archive, select a star close to the target, check over PS1 that this is indeed a star (calculating the classical aperture mag - PSF mag), and print the file OffsetStar.txt with: coordinate of the target, coordinate of the star, r-band PS1 magnitude of the star, RA and DEC offsets in arcsec, and PA in degrees.

This script uses massively ds9 (http://ds9.si.edu/site/Home.html).

ALWAYS double check the output and start from an empty folder. There is no warranty that this is a bug free code. If you find one, please contact me here: https://emastro.github.io/contact.html

You can check for other options with:

./GetFc -h

