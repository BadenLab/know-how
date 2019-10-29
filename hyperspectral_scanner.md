---
layout: page
title: Hyperspectral Scanner
permalink: /basic-readings/
---

## Natural imaging with hyperspectral scanners


From Zimmermann*, Nevala*, Yoshimatsu* et al., 2018, Current Biology 28, 2018–2032. https://doi.org/10.1016/j.cub.2018.04.075  


To gather hyperspectral images, we used a custom made, water-proofed hyperspectral scanner (Nevala and Baden, 2019) built around a commercial spectrometer (Thorlabs CCS200/M, 200-1,000 nm). In short, two spectrally broad mirrors mounted on top of servo-motors were controlled by an Arduino Uno microcontroller to iteratively bring different positions in visual space into the active part of the spectrometer to build up a complete hyperspectral image (Baden et al., 2013). 1,000 Scan-points were spaced 1.6° and defined by a Fermat’s spiral, followed by a custom path shortening algorithm. Spectra were recorded using the spectrometer software OSA (Thorlabs). We used diving-weights to stabilize the scanner under water. In addition, the scanner-case was placed inside a hard-plastic box to maintain the upright position with a UV-transparent window pointing forward. After placing the scanner to its < 50 cm depth underwater position, we waited up to 5 minutes for any stirred-up debris to settle. All n = 31 scans were taken during the day between 11am and 5pm; the weather conditions varied from slightly cloudy to clear sky but remained constant for individual measurements. Time for one scan acquisition varied between 4 and 8 minutes, depending on the set mirror-move times (200-500 ms) and integration times (80-200 ms) which were adjusted for each measurement to yield an approximately consistent signal-to-noise independent of absolute light intensity in each scene. Finally, in each case in addition to the scan a 180° still image was taken approximately at the scanner position with an action camera (Campark ACT80 3K 360°). Stills were mapped to the 2D plane by a standard angular fisheye projection to 720x720 pixels (0.25° per pixel).

Detailed information of the method published in:
Nevala, NE and Baden, T. 2019. A low-cost hyperspectral scanner for natural imaging and the study of animal colour vision above and under water. Scientific Reports volume 9, Article number: 10799. https://doi.org/10.1038/s41598-019-47220-6
