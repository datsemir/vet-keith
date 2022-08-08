# vet-keith
This is my modified KEITHSDR to work with the VeteranSDR.
Some of the change is listed below.
regards Claus OZ2IE

Some of the dir in the SDR_RA8875 are removed to reduce size, you can find the missing dir from the origin SDR_RA8875 in the KEITHSDR project. K7MDL2/KEITHSDR

si570 is a modified driver trying to eliminate click when changing frequency, origin gaftech/ArduinoSi570 but suffers from problems in small/big change calculation.

Keithsdr-main is the Arduino project running the Veteran.

RadioConfig.h contain the GPIO used from the Teensy4.1 Ra8875 Backpack version. The PTT in and out is moved from 0 and 1 to 2 and 3 to free a serial port. Right now the Arduino don't support more serial but I will find a way to use it anyway!! 

There is  "#define VETERAN" and  "#define VETERAN_SI570" that make the version for the veteran.

The selection of active #define in the RadioConfig.h to fit the VeteranSDR.

Tuneer.cpp line 182 i have added "displayFreq();" to display the frequency change on the display. line 185 set-up of the veteran band filters.

VFO.CPP look for VETERAN_SI570.

SDR_RA8875 line 708 delay + clearscreen , to display the banner and call sign in a second, and to remove the banner from the screen before overwrite with the SDR window.
