## ciclop-3D-scanner

A homebrew 3D scanner.

![ciclop](/images/ciclop.jpg)

## Background

The BQ Ciclop scanner is fully open source meaning that all of the source files for the hardware and software are made available online. That means you are free to make adjustments and upgrades to the Ciclop and then to share those changes with the community. This is the first open source scanner with open source software on the market.

How does Ciclop work? Ciclop is a 3D rotational laser triangulation scanner. That means that is makes use of two separate lasers and projects those lasers over the object you are scanning. Your object will rotate on the turntable and the lasers will catalogue both the geometry and texture of your object. Once you unbox the Ciclop, you can fully assemble the scanner in under an hour.

Start scanning large objects today and enjoy a scannable area of 250mm in diameter by 205mm tall. That means you can scan objects that are slightly smaller than a volleyball. The scanner captures textures and details with a precision of 500 microns. 

## Specifications

_3D scanning_

* Scanning precision: 0.5 mm
* Steps per rotation: 1600 max (1/8th microstepping)
* Maximum supported weight: 3 KG
* Typical scanning time (configurable): 2-8 minutes
* 3D scanning volume:
  - Diameter: 250 mm
  - Height: 205 mm

_Electronics_

* Control Board: ZUM BT-328
* Power board: ZUM SCAN
* Logitech C270 HD Camera
* 2 Class 1 line lasers
* Connection through USB-A cable
* 12V 1.5A power connector
* 1 NEMA stepper motor (1.7A 1.8 deg/step)

## Directory structure

 * `step`: The original Ciclop step files. This folder is frozen. Find the latest version in the `freecad` folder
 * `stl`: Ciclop STL files. It also contains parts with support for 3D printing
 * `dxf`: Ciclop DXF files. It contains all methacrylate pieces cutted with laser
 * `svg`: Ciclop SVG files. This folder contains all drawings for 2D printing
 * `freecad`: Ciclop source files in Freecad
 * `bom`: Ciclop Bill of Materials.

## Calibration

In order to successfully use the instrument, calibration needs to be done via this pattern.

![pattern](/images/calibration-pattern_sm.jpg)