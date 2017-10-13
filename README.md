# Keithley IV sweeper
Python program that controls different Keithley source-measure units (SMU) to perform voltage and current sweeps.

Currently it partially supports voltage sweeps in Keithley's 2400, 2602B and 6430 SMU using different communication ports. Future work includes adding current sweeps and different measurement options.

Keithley 2602B
The code should work for al the Keithley 26XX SMUs, but has only been tested in a 2602B. Currently works throug TCPIP and serial protocols, GPIB not tested.
Currently Ethernet/GPIB only works in Linux (tested on RPi 3/Raspbian). Will change it in future versions.

Keithley 6430
Tested in a Keithley 6430 SMU both through GPIB and RS-232 ports. No Ethernet port in this model.

Keithley 2400
The current code is imported from a previous version, but some of the latest iterations haven't been tested in a 2400 SMU. The SCPI commands are similar to those of the 6430, which has been succesfully controlled, so if the K2400 module doesn't work it's worth trying the K6430.
Currently GPIB only works in Windows. Will change it in future versions.

Data is plotted in a pyplot window and automatically exported to the root directory. In the future we will add the option to save the files in a different folder (or at least save them in a data folder), and give the option not to save the files, as al the tryouts can cause confusion.

Required python modules:
  - pyserial
  - pyvisa
  - pyvisa-py
  - matplotlib
  - numpy
