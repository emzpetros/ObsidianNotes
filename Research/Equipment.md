
# Speedgoat PC

![[PXL_20230113_171807677.jpg]]
# UECU

## Multi-freq Stim
A student recently asked about stimulating with different frequencies on two different channels on a single Perc board. He has been using the approach where only one schedule is used, but two stim frequencies are realized by interleaving 0s. The channels with the interleaved zeros then have a stim frequency that is half the frequency of the other channels. I believe some of you have used this method in the past and it is a valid approach. However, we decided to do some testing to determine if another method is possible that makes use of more than one schedule.  Based on our testing, this is possible. 

I've attached an example model that makes use of 3 different variable schedules (IPIs of 35ms, 40ms, and 45ms). This model has Ts set at 35ms, but it also works if you set Ts at a different value such as 45ms.  Note that this makes use of 3 stim blocks (one for each schedule) with channels 0 - 3 using schedule 1, channels 4 - 7 using schedule 2, and channels 8 - 11 using schedule 3. Testing showed proper stimulation on all channels with this model. However, note that due to the nature of stimulating at different frequencies, the delays between channels on different schedules vary from cycle to cycle. For example a stim pulse on channel 0 (schedule 1) may occur very close to a stim pulse on channel 4 (schedule 2). Since the pulses are being generated on the same stim board, the pulses can not overlap, but they can occur less than 1ms apart.  The attached scope plot shows the closest that I saw two pulses occur during testing; 114us from one pulse ending to the next starting.  

I also made a version of this 3 schedule model using asynchronous and synchronous schedules.  The asynchronous schedule version behaved the same as the attached variable schedule model. However, the synchronous schedule version only worked properly if Ts was set at 45ms (the largest IPI). Testing showed that if the Ts of a multiple synchronous schedule model is not set at the slowest IPI, then the stimulation output on channels using the slower schedule(s) has inconsistent/variable IPIs. Another requirement for using multiple synchronous schedules is that the IPIs need to have a common divisor. The 3 synchronous schedule model worked with IPIs of 35ms, 40ms, and 45ms since they are all divisible by 5. However, when I tried to run a multiple synchronous schedule model with IPIs of 41ms and 45ms, there was no stimulation output. Note that IPIs of 41ms and 45ms work fine when using multiple variable schedule models.  

In summary, it looks like multiple schedules/stim blocks can be used for the UECU Perc Board as long as the variable pulse spacing between channels on different schedules is acceptable, but testing should be done to confirm that the stimulation output is what you expect. Note that this testing was done with the UECU in stand-alone mode, so it should probably be tested in Simulink RealTime/Speedgoat mode as well.

I'm not sure if this method of multiple schedules will work with implant and surface board UECU models, but testing can be done if there is an interest.    

Thanks.
John


# ASCU Application Specific Control Unit

[[ASCU Internal Code]]

- [ ] Fix multiple “ch” terminology: channels vs mapping indexes
- [x] Storing profiles
	- [x] ASCU 9
	- [x] ASCU 19
- [x] Change PA output message 
- [ ] Change the default percents to be all 0 default 
- [x] Add a warning message when you set PA to an invalid value above 2.0  


## ASCU App
ScreenSetLev: initialization for the percentages

Could not initialize class org.codehaus.groovy.reflection.ReflectionCache:
Reset distributionUrl=https\://services.gradle.org/distributions/gradle-6.3-all.zip in gradle-wrapper.properties for JDK 14 support 


## Programming
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



