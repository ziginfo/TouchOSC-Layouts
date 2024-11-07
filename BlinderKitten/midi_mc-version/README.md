## BlinderKitten  Control and Feedback by MIDI with TouchOSC  and Mackie Control Protocol 
While OSC-Feedback is still not available in BlinderKitten, I made  a Midi GUI for TouchOSC and BlinderKitten (based on the Mackie-Control protocol) which allows us to get a lot of "Feedback" and also some text (in SysEx) etc... so this is perfect for a mobile remote control with Feedback!!  

These two TouchOSC-layouts are pure MIDI (so there is no OSC in this case); you can open it with TouchOSC and try it with your BlindeKitten session ... TouchOSC can be downloaded and tested  for free on the [Hexler Website](https://hexler.net/touchosc#get) .... if you want to integrate TouchOSC into your Workflow and work in production with it, the license is really cheap at all.

About the MC-Layouts, there are two, in fact, and you must use each layout with its dedicated mochi (otherwise it's a mess for the Feedback!! :) )
V3 is the one I made for myself and my workflow and it's more oriented towards creation, encoding and production... but for simple "play & go", V2 is probably more practical... 
in any case you must use virtual MIDI Ports; they natively available in iOS and MacOS; you can also send MIDI over the network (and therefore over WiFi, for example), which makes this layout a perfect tool for "mobile use" (tablet or iPad etc...)

Its probably a good idea to set in BK the Virtual-Port1 in IN and the 2 in OUT; and therefore in TouchOSC the opposite: Port-1 for the "Send" and Port-2 for the "Receive" (use more likely two separate ports because BK makes weird loops which can create various bugs and oddities!!)

For Windows or Linux, I don't know how these virtual ports may work, because I am totally ignorant about these systems; but at Hexler Website, there is also a (free) tool called "TouchOSC Bridge" which creates a virtual port for MIDI (also usable on the network, therefore in WiFi)! if you use "TouchOSC Bridge" you must configure it in the TouchOSC Setup ("Setup" -> "Connections" and then the "BRIDGE"-Tab)... in MacOS or iOS you can directly use one of the virtual ports available natively in the OS! -> you just have to select it in "Setup" -> "MIDI" and "Connection1"!)

The best way to "learn" how the layout works, just give it a try ans play around with it !! if you've already used a hardware in Mackie-Control, you'll find your way around very quickly...

---
BlinderKitten is available for free on the [BK-Website](https://blinderkitten.lighting/)    

TouchOSC can be downloaded on the [Hexler-Website](https://hexler.net/touchosc)...    
you can use it for free or pay the fairely low Licence-Fee (about 25 euros)

---
Please contact me if you have any suggestions, demands or requests and any help is always welcome !!   
Have Fun ... 
