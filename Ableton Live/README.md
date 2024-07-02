## Ableton Live  Control and Feedback with TouchOSC
To get this OSC-Module run correctly, you must first donwload and install the free [AbletonOSC](https://github.com/ideoforms/AbletonOSC) Remote-Script and than activate it in Ableton Live !!   

OSC ports are set by default ! Ableton Live is listening on Port 11000 and sending Feedback on Port 11001 ; so in TouchOSC the ports must be set to : Input Port : 53001 and Output Port : 53000    
Remote Control and Feedback can be by Localhost (127.0.0.1) or any private Network (Wi-Fi Routers etc)  

This Layout is still WiP (work in progress) !  I will add some more features in the future. Takes a while to get it done as the OSC-library is quite complexe.   
It seems that Master-Track Scenes Control will not work for instance as those controls are not included in the AbletonOSC Python-Script ...
#### The latest Version is V2.4
I just added some more Feedback-Features...   
We have now Feedback from the Devices, still no control from TouchOSC to any Device though (I am working on...). Concerning the Device-Parameter-Feedback from Live, there is no "listen" function to assure contious Feedback; so this must me requested by the user. I added a sort of "auto-request" with ajustable times.       
Please be careful with Feedback-Requests in general as Live can send back a huge amount of Data which will cause the TouchOSC-Remote to slow down and/or create lags and latency. With this in mind please activate only the Feedback you'll need ! For example, Stereo-Meter-Feedback swill end back at least 5 or 6 times more Data than Mono-Meter-Feedback. Stereo-Meter-Feedback is Peak-Levels showing and Mono-Meter-Feedback is RMS-Levels showing. 

Please contact me if you have any suggestions, demands or requests and any help is always welcome !!   
Have Fun ...  

Special Thanks to [Daniel Jones](https://github.com/ideoforms) for his Python-Remote-Script

