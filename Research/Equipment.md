
# Speedgoat PC

![[PXL_20230113_171807677.jpg]]
# ASCU

[[ASCU]]

- [ ] Fix multiple “ch” terminology: channels vs mapping indexes
- [ ] Storing profiles
	- [x] ASCU 9
	- [ ] ASCU 19



Mapping channels
- cmp 1 0 : channel 1 to nothing
    - 1 heel, 2 midfoot, 3 toes
- pcmp print contact map

Points of contact: Rachel Mann and John Schnell  

## Troubleshooting
 Can only upload new code when Tera Term is not open

![[Untitled 591.png]]

## Rachel Notes

For ASCU \#9, I noticed you said you were using AndroidLeSensory_v0p01.apk.  This is the oldest version.  Is there a specific reason you wanted to use this version?  When I put the most recent version of the app on the pixel 4a, I was able to get pairing.  I was also able to see stim output using the SNP start and stop buttons on the most recent app (AndroidLeSensory_v0p08.apk).  A step you may have forgotten was to specify the contact channel mapping. I used the command "cmpa 1 1 1 1 2 2 2 2 3 3 3 3" in the terminal.  Without this command, all of the contacts will default to "0", which is "off".  Channels in this default off setting will not stim.  I also set the max pulse widths for each channel to 255 by using the "setmx" command for each channel.  I believe these values are stored on the ASCU, so this system now works on startup, and you shouldn't have to retake these steps.

I was also able to get ASCU \#19 working with the most recent app.  I think you might've been missing similar steps as with ASCU \#9.  Another possibility is that the incorrect code was loaded onto ASCU #19.  John and I loaded test code onto ASCU #9 to check that the stim board still worked before I tried to use it with the app.  At first, I forgot to load the correct teensy code for use with the app.  When I tried to use the system, the woodstock signal would not show on the app because I had the incorrect code on the ASCU teensy.  Also, make sure to turn the ASCU on after opening the app, or right after opening the app.  If the ASCU is on for too long before the app is opened, the bluetooth module will stop advertising.  ASCU #19 also works upon startup.

For reference, the ASCU teensies have ReLLiNC-AscuAmputee.ino loaded onto them, and the phones have AndroidLeSensory_v0p08.apk.

  

ecent app apk file on Teams in the Code Drops folder, hidden in the 20210520_AndroidLeSensory_  
v0p08_AscuAmputee_0p11 f

  

Buttons: RED stops stim, start only possible from terminal or the app



# MSL Stairs / Vicon / WW

Turn on boxes, connect wires, wheels

Distance from origj n

Bottom left

Sides as you look going up

![[image-1689796293978.jpg3931479500884173701.jpg]]

Red wires with port labels

3 small ones, one for hand rails

  

Vicon cameras and force plates in WW always on

  

Cameras+FP+stairs+Rails

  

Gray amps: 1-3 force plates

- Zero in vicon

  

![[image-1689797399832.jpg6615109801018291460.jpg]]

  

Data under home going stairs biomechanics

  

  

SNP_tray_U/D_01

Static: in front of stairs

  

2 seconds on either side of start and stop

CounterClockwise to raise wheels

  

45 inc

![[image-1691603122791.jpg5584678927006931219.jpg]]

# Refs from Musa
1. R:\Triolo_Lab\Database\Projects\Other\Posters_and_Presentations\IROS 2023 Interesting Abstracts\

This contains abstracts and corresponding video presentations at the IROS Conference that I found interesting. A summary is in the attached file.

2. R:\Triolo_Lab\Database\Tutorials\OpenSim and Clusters

        This contains videos of tutorials that I have given to students/post-docs on how to use OpenSim and how to use the various clusters available to us at Case and OSU.



# ASCU App
ScreenSetLev: initialization for the percentages

Could not initialize class org.codehaus.groovy.reflection.ReflectionCache:
Reset distributionUrl=https\://services.gradle.org/distributions/gradle-6.3-all.zip in gradle-wrapper.properties for JDK 14 support 