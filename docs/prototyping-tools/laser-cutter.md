---
layout: page
title: Laser cutter
permalink: /prototyping-tools/laser-cutter/
---

# Laser Cutter

### Summary


![glowforge](../../media/lasercutter/glowforge.jpeg)


The lab's laser cutter is a [glowforge](https://glowforge.com/). The basic model without the built in filter.

- Tech Specs:
 - Material max dimensions: 45.7 X 51.8 cm (18 x 20.4 inches)
 - file formats JPG, PNG, SVG, PDF
 - 40W laser
 - can cut:


 |Cut||||
 |--|--|--|--|
 |Leather|Wood|Paper|Fabric|
 |Plexiglas (acrylic)|Delrin (acetal)|Mylar|Rubber|
 |Corian|Foods|||

 |Can engrave same as cut plus:||||
 |--|--|--|--|
 |Glass|coated metal|marble||
 |titanium|anodized aluminum|||



- Good for:
 - prototyping of large pieces


- Downside when things go wrong:
 - getting dimensions wrong wastes a lot of material!

## Using the laser cutter:

The lasercutter is operated via a webapp, which means the cutter needs to be connected to the internet during operation using the same network as the computer running the webapp.

Given the current location of the cutter, we needed an 4G access point. It is an EE box, with a pre paid data plan (10£ for 2Gb of data, that expires every 2 months).

The webapp can be accessed at: https://app.glowforge.com/

For login and password info, contact Tom or Andre.

- steps for actually cutting things:
  - Make a design in a software that can export in one of the following formats: JPG, PNG, SVG, PDF
  - upload it using the webapp interface.

   ![](../media/lasercutter/initial_page_glowforge.png)


  - when you select "print" the system is going to take a picture of what is inside the cutter.
   - place your design on the appropriate place on top of your material image.
   - make sure the system is focused (there is an autofocus button on the webapp)
   - wait for magic to happen

## a pipeline with openscad:  


[OpenScad](openscad.org) is normally used to design and export 3D designs, we normally use it for creating parts for [3Dprinting](./laser-cutter.md). As mentioned before, the laser cutter takes files in formats that are describing 2D shapes (eg PDF, JPG, etc).
To circumvent this we are leveraging libraries that other people wrote.

This pipeline works with https://github.com/bmsleight/lasercut library:

 - Create the box in the dimensions you want using one of the many possible functions. below is a code example from the library's github (holes and other specific things come later):

 ```
 include <lasercut.scad>;

 thickness = 3.1;
 x = 50;
 y = 50;
 z = 75;

 for (sides =[4:6])
 {
    color("Gold",0.75) translate([100*(sides-4),0,0])
        lasercutoutBox(thickness = thickness, x=x, y=y, z=z,
        sides=sides, num_fingers=4);
}
```

 - then export this using the libraries ```./convert-2d.sh``` function.

 - you can either export the newly generated file to SVG and finish working on your preferred 2D suit, or work on the newly generated file in OpenScad and then export it to SVG.

## other notes:
- In case the cutter needs to be reset, turn the machine one, and press the big button for 30 sec.



Cutting speed depends on many things:

    The Glowforge Pro and Glowforge Plus cut about 20% faster than Basic.
    The faster the laser moves, the more power is required.
    Thicker material requires more power and more time. Twice as thick takes more than twice as long to cut through.
    The chemical composition of the material makes a huge difference. Some 1/4" plywood cuts quickly; some 1/8" plywood is impenetrable.

This is why we offer Proofgrade™ materials - we want you to have consistent materials where you know that you can cut through every time, and you know how long it will take. If you use your own materials, you will need to do some experimentation.

For engraving, cutting speed depends on two things:

    How fast you move the laser head - slower makes the engraving deeper and, in some cases, darker.
    How big the area to be engraved is. The head must move over the area to be engraved, and while Glowforge is smart about setting its path, two dots an inch apart will take longer than two dots right next to each other.

The average print time is 12 minutes. The longest prints - full detailed engravings that cover the entire bed - can take up to 3 hours.
