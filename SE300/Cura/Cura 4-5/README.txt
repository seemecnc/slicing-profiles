2020-FEB-25 by SeeMeCNC

SPECIFICALLY FOR Cura 4.5 

We recommend removing all old software BEFORE install this new version.
seemecnc.com > SUPPORT tab > Docs & Guides > 

Lataer Cura version *might* work with these SeeMeCNC tested profiles. However,
  these profiles were developed for the version listed above. Be sure to 
  use the profiles and quickstart machine files for the correct Cura version.


A SeeMeCNC QUICK START file: 
----------------------------

Opening a file with extension  .3MF  will:
  > create or update a machine profile for Cura 4.5
  > create a slicing profile created by us, SeeMeCNC
  > put an STL model on the print bed



February 2020 updated: 

Notes for starting machine and extruder gcode. 
 
;PRINTER Start G-code
M203 Z14000
G28 ;Home
G1 X0 Y-130 Z0.3 F8000 ;Move the platform down 15mm
G1 Z5
G1 F200 E3
G92 E0

;PRINTER End G-code
T0 P0
M18 E1
G91
G1 Z0.3 F10000
G90
G92 E0
G1 E-3 F2000
G92 E0
G1 E-155 F5000
G92 E0
M104 S0
M140 S0
M203 Z14000
G28

;Extruder 1 Start G-code
G91
G1 Z1 F10000
G90
G1 X0 Y-130 F14000
T0 P0
G92 E0
G1 E145 F5000
G92 E0
G1 E15 F1000
G92 E0
M18 E1

;Extruder 1 End G-code
G91
G1 Z1 F10000
G90
G1 X0 Y-130 F14000
G92 E0
G1 E-5 F2000
G92 E0
G1 E-155 F4000
G92 E0

;Extruder 2 Start G-code
G91
G1 Z1 F10000
G90
G1 X0 Y-130 F14000
T1 P0
G92 E0
G1 E145 F5000
G92 E0
G1 E15 F1000
G92 E0
M18 E0

;Extruder 2 End G-code
G91
G1 Z1 F10000
G90
G1 X0 Y-130 F14000
G92 E0
G1 E-5 F2000
G92 E0
G1 E-155 F4000
G92 E0

	
