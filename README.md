# vet-keith
This is my modified KEITHSDR to work with the VeteranSDR.
Some of the change is listed below.
regards Claus OZ2IE

Some of the dir in the SDR_RA8875 are removed to reduce size, yoy can find the missing dir from the origin SDR_RA8875 in the KEITHSDR project.

si570 is a modified driver trying to eliminate click when changing frequency.

Keithsdr-main is the Arduino project running the Veteran.

There is  "#define VETERAN" and  "#define VETERAN_SI570" that make the version for the veteran.

The selection of active #define in the RadioConfig.h to fit your needs.

Tuneer.cpp line 182 i have added "displayFreq();" to display the frequency change on the display. line 185 set-up of the veteran band filters.

VFO.CPP look for VETERAN_SI570.

SDR_RA8875 line 708 delay + clearscreen , to display the banner and call sign in a second, and to remove the banner from the screen before overwrite with the SDR window.
