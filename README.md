# My Notes on Disabling Android Dialer's Proximity Sensor Usage
## Why disable the proximity sensor?
My daily driver, at the current time of this writing, is a Nexus 4 circa 2012. The proximity sensor has been malfunctioning ever since I had the LCD/digitizer assembly replaced in 2014. By malfunctioning, I mean the sensor always returns a "near" value (i.e. 0.0) when polled. This is an issue during phone calls, as the Phone app (com.android.Dialer) uses the proximity sensor to determine when to turn the screen on or off. Because the sensor always reports "near", the phone would turn the screen off as soon as a call connects, hindering the ability to use the dialpad for things like voicemail, audio menus, etc.

Prior to figuring out how to build AOSP/Cyanogenmod, the only workaround was installing Xposed Framework and using a module called Sensor Disabler that allowed me to "fake" the value reported by the proximity sensor. That worked great for a couple of years, but it meant that I was stuck with whatever Android release that was supported by Xposed. At this time, Xposed does not work in Android Nougat/CM 14.0. So I decided it was time I learned how to build Cyanogenmod and fix the issue myself.

## Helpful Resources
http://forum.xda-developers.com/nexus-4/general/tutorial-build-cyanogenmod-11-vps-t2797703

https://wiki.cyanogenmod.org/w/Build_for_mako

http://projectmaxs.org/documentation/systemapp.html

https://forum.cyanogenmod.org/topic/130518-getting-started-with-cm141-tree/?do=findComment&comment=615018
