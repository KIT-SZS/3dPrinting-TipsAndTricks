3dPrinting-TipsAndTricks
========================


This is a series of , well, tips and tricks related to 3d printing, most specifically at the SZS:




Introduction to 3d printing/ repraps:
============================

http://reprap.org/wiki/The_incomplete_reprap_beginner's_guide


Very general: 
http://www.3ders.org/3d-printing-basics.html


Machines(building machine!):
============================

Currently at the lab: 

- **K8200** : print quality is not perfect, reliability is ok 
- **Ultimaker 2**: print quality can be very high, almost "plug and print". Main issue : filament driver not putting out enough filament for prints with layer height >= 0.2. Best suited for 0.1 mm layer heights


**tip** both machines are standalone, with an LCD screen / controller and an sd card, as it is more reliable and faster than via USB.
LCD controllers also allow adjusting parameters *during* a print ("tune" menu): THIS IS ESSENTIAL !!

**tip** watch , analyze, adjust, instead of restarting the print : most prints can be "saved" : you will not have industrial quality parts from the start, but if a part "works" , all is fine !


Workflow:
=========

- download or create a 3d design
- slice it 
- print it
- if not satistfied , try again!

or in a single line:

 design -> slice -> print 


creating /downloading 3d models
===============================

- any design tool that can create STL files will do the job
- lots of online part libraries (http://www.thingiverse.com/, https://www.youmagine.com/)
- [OpenScad](http://www.openscad.org/) is a very powerful code-based parametric design tool (free & open source) can be used to modify some existing designs 

Slicing
=======

Slicing is the transformation of a 3d object file into a set of instructions (also called GCODE) for a *specific machine* (GCODE is NOT meant to be used on multiple different machines)

Once slicing is done, copy the GCODE file to the sd card, put it into the machine, and select the part you want in the machine's menu.


- **Cura** is a good and fast slicer, very beginner friendly, with quite a lot of advanced features if you need them
- **Slic3r** is also a very good slic3r, perhaps a bit harder for beginners

**tip** : I have already set up profiles for both machines in Cura , use them/modify them to taste (go into the "Machine" menu on top)

**IMPORTANT**: do not use GCodes meant for a machine in another machine : ***GCODE IS MACHINE SPECIFIC !!!***


Lots of online tutorials/guides are available, for example: (software evolves fast, so these are already partially outdated)

Cura:
http://www.3dgeni.us/getting-started-with-cura/
Slic3r :
http://richrap.blogspot.de/2012/01/slic3r-is-nicer-part-1-settings-and.html


Printing
========


Main issues:
- the object is brittle, fragile , seems to be missing mater:
   * slow the machine down (DURING PRINT at first, with the "TUNE" menu on the LCD screen) to see if it fixes the issue
   * increase flow
   * increase temperature (should never be above 230 °c for the Ultimaker 2 for PLA)

- if corners lift up :
   * put some "uhu" stick glue on the glass bed
   * increase the heat (between 50 °C and 60°C is perfect for PLA)

Overall tips
============

- do not hesitate to look for answers online : ultimaker or k8200 forums, reprap forums , google + etc: lots of helpfull people everywhere !



Philosophy:
==========

Both machines are [Reprap](http://reprap.org/) derivates ie *open source* : if you have an issue, look around online , lots of people have likely created great upgrades for the different parts of the machines.
And if you come up with a new upgrade, please share it with others, so everybody can benefit ! 
