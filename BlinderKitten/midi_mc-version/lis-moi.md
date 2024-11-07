## BlinderKitten Control et Feedback par MIDI avc TouchOSC et le Mackie Control Protocole
Puisque OSC-Feedback n'est pour l'instant toujours pas disponible dans BlinderKitten, j'ai créé une interface graphique Midi pour TouchOSC et BlinderKitten (basée sur le protocole Mackie-Control) qui nous permet d'obtenir beaucoup de "Feedback" et aussi du texte (par SysEx) etc... donc c'est parfait pour une télécommande mobile avec Feedback (tablette, iPad etc) !!

Ces deux layouts TouchOSC sont purement MIDI (il n'y a donc pas d'OSC dans ce cas) ; vous pouvez l'ouvrir avec TouchOSC et l'essayer avec votre session BlindeKitten... TouchOSC peut être téléchargé et testé gratuitement sur le [site Web Hexler](https://hexler.net/touchosc#get) .... si vous souhaitez intégrer TouchOSC dans votre Workflow et travailler en production avec, la licence est vraiment pas chère du tout.

Concernant les MC-Layouts, il y en a deux en fait, et il faut utiliser chaque layout avec son mochi dédié (sinon c'est le bordel pour le Feedback !! :) )
La V3 est celle que j'ai fait pour moi et mon workflow et elle est plus orientée création, encodage et production... mais pour du simple "play & go", la V2 est probablement plus pratique...
dans tous les cas il faut utiliser des Ports MIDI virtuels ; ils sont nativement disponibles sous iOS et MacOS ; on peut aussi envoyer du MIDI sur le réseau (et donc en WiFi par exemple), ce qui fait de ce layout un outil parfait pour une "utilisation mobile" (tablette ou iPad etc...)

Je vous conseille de mettre dans BK le Virtual-Port1 en IN et le 2 en OUT ; et donc dans TouchOSC l'inverse : Port-1 pour le "Send" et Port-2 pour le "Receive" (utilisez plutôt deux ports séparés car BK crée parfois des boucles bizarres qui peuvent créer divers bugs et bizarreries !!)

Pour Windows ou Linux, je ne sais pas comment ces ports virtuels peuvent fonctionner, car je suis totalement ignorant pour ces systèmes-là ; mais sur le site d'Hexler, il y a aussi un outil (gratuit) appelé "TouchOSC Bridge" qui crée un port virtuel pour le MIDI (également utilisable sur le réseau, donc en WiFi) ! si vous utilisez "TouchOSC Bridge" vous devez le configurer dans le Setup de TouchOSC ("Setup" -> "Connections" puis l'onglet "BRIDGE")... sous MacOS ou iOS vous pouvez utiliser directement l'un des ports virtuels disponibles nativement dans l'OS ! -> il vous suffit de le sélectionner dans "Setup" -> "MIDI" et "Connection1" !)

La meilleure façon "d'apprendre" comment fonctionne le layout, c'est de l'essayer et de jouer avec !! Si vous avez déjà utilisé un matériel sous protocole "Mackie-Control", vous vous y retrouverez très rapidement...

---
BlinderKitten est disponible gratuitement sur le [site Web BK](https://blinderkitten.lighting/)

TouchOSC peut être téléchargé sur le [site Web Hexler](https://hexler.net/touchosc)...
vous pouvez l'utiliser gratuitement ou payer la  licence à petit prix (environ 25 euros)

---
Contactez-moi si vous avez des suggestions, des demandes ou des requêtes et toute aide est toujours la bienvenue !!
Amusez-vous bien ...
