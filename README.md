# slicing-profiles


Our recommended setup methode is to follow the quick start guide. Just type "quick start" in the search bar of seemecnc.com

___________________________________________________________
Hello.  We hope you enjoy these profiles.  These free slicing profiles have been refined by the SeeMeCNC.  You will find default slicing profiles for various slicing softwares.  We have invested 100's of hours making sure you get off to a good start. 


> 2015-2017 Eris profiles for Eris models only
> 2015-2018 HE280 for printers with the HE280 hotend
> 2018-2021 SE300 for all printers with the SE300 hotend
> 2019-2020 XST SE300 for BOSSdelta's bigger heater block
> 2020-????


PLEASE FOLLOW THE ONLINE SEEMECNC CURA SETUP GUIDE FOUND UNDER

menu item  USPPORT > Quick Start












The folloowing notes are NOT intended for setup. Please see our guide.
_______________________________________________________________
SeeMeCNC DECEMBER 2020
Cura 4.6.2 Notes and printer setup

The slicing profile MUST HAVE retraction of 6.5mm set to work with these notes. 

PLEASE OPEN THE SEEMECNC CURA 4.6.2 PROJECT 3MF FILE.  :) 



;PRINTER SETUP BEGINNING GCODE <<<< DO NOT COPY THIS LINE

;=== SeeMeCNC PRINTER SETTINGS =========
;=== OPTIMIZED FOR CURA 4.6.2  =========
M203 Z10000  ;===PRINTER BEGIN G-CODE===
G28
G1 X0 Y-130 Z0.3 F8000
G1 F200 E3
G92 E0       ;==========================





;PRINTER SETUP ENDING GCODE <<<< DO NOT COPY THIS LINE

G91             ;============================
G1 Z0.3 F10000
G90
G92 E0
G1 E-3.5 F300
G92 E0
G1 E-150 F5000
G92 E0
T1 P0
T0 P0
M104 S0
M140 S0
M203 Z10000
G28             ;===== PRINTER END GCODE =====





;EXTRUDER 1  BEGINNING GCODE <<<< DO NOT COPY THIS LINE

G91           ;=======EXTRUDER 1 BEGIN GCODE=======
G1 Z1 F10000
G90
G1 X0 Y-130 F10000
T0 P0         ;=== SELECT TOOL DO NOT RUN MACROS ==
G92 E0
G1 E145 F4000
G92 E0
G1 E15 F500
G92 E0        ;====================================





;EXTRUDER 1 ENDING GCODE   <<<< DO NOT COPY THIS LINE

G91             ;====================================
G1 Z1 F10000
G90
G1 X0 Y-130 F10000
G91
G92 E0
G1 E-3.5 F300
G92 E0
G1 E-153.5 F5000
G92 E0
T-1 P0          ;DESELECT ALL TOOLS DO NOT RUN MACROS
;               ;=======END EXTRUDER 1 GCODE=========