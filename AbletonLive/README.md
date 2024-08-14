## Ableton Live  Control and Feedback with TouchOSC
To get this OSC-Layout run correctly, you must first donwload and install the free [AbletonOSC](https://github.com/ideoforms/AbletonOSC) Remote-Script and than activate it in Ableton Live !!   

OSC ports are set by default ! Ableton Live is listening on Port 11000 and sending Feedback on Port 11001 ; so in TouchOSC the ports must be set to : Input Port : 11001 and Output Port : 11000    
Remote Control and Feedback can be by Localhost (127.0.0.1) or any private Network (Wi-Fi Routers etc) 

---
#### I just finished  V3   
added now two more Pages for Midi actions; one is a Keyboard-sort of controller; and the other one a sort of Drum-Pad-Controller
#### The other Version is V2.8
Some more new features...   
Added Scroll-Feature on the Clips-Page : Up & Down and Left & Right.    
Added Color-Feedback from the Tracks.   
We now have also the Aux-Send-Levels available. Please note that there is no automatic Feedback from the Live-Session for these levels ! So you may request Feedback manually or with the Request-Loop (which has three different Request-Rates from 0,5  to 3 seconds.   
We have also Feedback from the Devices (Instruments, Plugins etc), and we have control from TouchOSC to any Device. Here also, Device-Parameter-Feedback from Live has no "listen" function to send contious Feedback. When you change the Parameter-Offset-Value this requests also the new Parameter-Values from your Live Session. For manual Feedback-Request click on the Offset-Number-Field. I added also a sort of "auto-request" with ajustable Rate-Times which will request Feedback from Live frequently, so when there are changes in the Live-Session, this will also be reflected in TouchOSC.       
Please be careful with Feedback-Requests in general as Live can send back a huge amount of Data which will cause the TouchOSC-Remote to slow down and/or create lags and latency. With this in mind please activate only the Feedback you'll need ! For example, Stereo-Meter-Feedback will send back at least 5 or 6 times more Data than Mono-Meter-Feedback. Stereo-Meter-Feedback is Peak-Level showing and Mono-Meter-Feedback is RMS-Level showing.   

Control for Device-Parameters should work quite smooth, but to avoid any not-wanted errors and "controls" there is a button where you can enable or disable the "Global Control".

---
**In the Mixer-Tab the colored Dots have the following signification :**
- Light Cyan Dot means this Track is a (non-folded) Group-Track
- Deep Blue Dot means : this Track is a folded Group (SEL will not work for the "yellow-dotted" Tracks on the right!)
- Yellow Dot means : this track is part of a Group
- The colored (purple) Dots further up and beside the Faders just show the 0-db point of the Fader

**There are some lacks and limitations, and some hidden issues due to the Python-OSC-Library; maybe some of them will be fixed in the future..??**
- it is not yet possible to play/fire scenes
- there is at the moment no control on the Master-Track
- no control either for the Aux-Return-Tracks (and they are even not shown in the Track-List !)
- when a Track is part of a Group, it will always be shown in the TouchOSC-Layout, no matter if the group is folded or deployed ! But when the group is folded (blue-dotted), the channels inside the group cannot be selected anymore by Remote (SEL)! (You'll see that the SEL-Button stays lit in the TouchOSC-Layout). To select a Track when it is part of a group, the group must be unfolded (cyan-dotted)

---
**About Feedback from the Live-Session :**    
For many Feedbacks there is a "start_listen" feature which tells Live to send Feedback as soon as there are any changes in the session (for example : Names, Volumes, Mutes, Solo etc etc). Most of these "start_listens" are activated automatically, when the TouchOSC-Layout goes online. Others may be activated manually with the "Sync Many" Button.   
And there are some parameters and values that cannot be followed automatically. This is the case for the "Device-Parameters" and  for the "Aux-Send" Levels; and also for the "Fired-Clips"-Feedback To have continuous Feedback also for them I added a continuous feedback-request for each. You can set the Feedback-Rate (from slow to fast, classically at 3, 1 or   0,5 seconds.   

---
Please contact me if you have any suggestions, demands or requests and any help is always welcome !!   
Have Fun ...  

Special Thanks to [Daniel Jones](https://github.com/ideoforms) for his Python-Remote-Script
