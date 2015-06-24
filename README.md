# Spectral
Beckman DU 7000 Diode Array Spectrometer commands list from Chapter 24 of the manual.
These spectrometers take serial character commands to get data. 

This manual uses "<" and ">" to indicate the start and end of commands, but these brackets should not be sent with the command.

OPERATION INSTRUNCTIONS:
1.Verify the machine is on and functional

2. Enter remote control Command mode:
   <ctrl W>   (decimal 23), <ctrl V> (decimal 22)

3. The instrument sends <r> <lf>, indicating the device is ready to recive remote commands
   the General format is: <ascii string> <lf>,  
   where ascii string is a string of up to 40 ascii characters, and lf is line feed. All non-printing commands except <lf> are ignored by the instrument.

4.When the instrument successfully executes a command, <s> <lf> is returned.
    if a command fails, or ends in error, <f> <lf> or <p> <lf> are returned.

5.To exit the remote control command mode use the command <x> <lf>. this may prompt you for an interaction with the mouse. Alternatively, the comand <exit> can be used to exit the remote control mode.

NOTE: <lf> is <ctrl J>
