## Ableton Live  Remote Control et Feedback avec TouchOSC
Pour que ce TouchOSC Template puisse fonctionner correctement, vous devez d'abord télécharger et installer : [AbletonOSC](https://github.com/ideoforms/AbletonOSC) puis l'activer dans Ableton Live !!    
Cette librairie Python a été écrite et mis à disposition gratuitement par Daniel Jones; un grand merci à lui !!  

Les ports OSC sont configuré par défaut ! Ableton Live "écoute" sur le port 11000 et envoie des réponses et du feedback sur le port 11001 ; donc dans TouchOSC les ports doivent être réglés sur : Port d'entrée : 11001 et Port de sortie : 11000
Le contrôle  et le feedback peuvent se faire par Localhost (127.0.0.1) ou par n'importe quel "réseau privé" (routeurs Wi-Fi, etc.)  

---
#### La Version actuelle est la  V2.8.1
Les derniers ajouts...
Ajout d'une fonction de défilement sur la page Clips : haut et bas et gauche et droite.
Ajout de feedback pour les couleurs des pistes.
Il y a désormais également les niveaux Aux-Send disponibles. Veuillez noter qu'il n'y a pas de feedback automatique de la Live-Session pour ces niveaux ! Vous pouvez donc demander le feedback manuellement ou avec la boucle de requête (qui a trois temps de réitération de 0,5 à 3 secondes).
Il y a également du feedback des "devices" (instruments, plugins, etc.) et on peut contrôler depuis TouchOSC n'importe quel "device". Ici non plus, le Device-Parameter-Feedback de Live n'a pas de fonction listen to" pour envoyer des feedbacks en continue. Quand vous modifiez la valeur de "offset" des paramètres, cela demande également les nouvelles valeurs de paramètre de la session Live. Pour une demande de feedback manuelle, cliquez sur le champ Numéro de "offset". J'ai également ajouté une sorte de "requête automatique" avec des temps ajustables qui demandera à interval régulier du feedback de Live, donc lorsqu'il y aura des changements dans la session Live, cela sera également reflété dans TouchOSC.
Soyez prudent avec les demandes de feedback en général, car Live peut renvoyer une énorme quantité de données, ce qui paut entraîner un ralentissement du TouchOSC-Remote et/ou créera éventuellement des délais et de la latence. Dans cette optique, activez uniquement les feedback dont vous aurez besoin ! Par exemple, Stereo-Meter-Feedback renverra au moins 5 ou 6 fois plus de données que Mono-Meter-Feedback. Le feedback stéréo-mètre est affiché au niveau de crête et le feedback mono-mètre est affiché au niveau RMS.

Le contrôle des paramètres de l'appareil devrait fonctionner de manière assez fluide, mais pour éviter toute erreur et des actions de contrôle indésirables, il existe un bouton (sur la page "Device") où vous pouvez activer ou désactiver le "Contrôle global". Cela concerne donc ce qui sera envoyé depuis la page Device vers la Session-Live.

---
**Dans le Mixer-Tab les pastilles colorés ont la signification suivante :**
- La pastille Cyan Clair signifie que cette piste est une piste de groupe (non dépliée)
- Deep Bleu signifie : cette piste est un groupe replié (SEL ne fonctionnera pas pour les pistes "en pastilles jaunes" à droite !)
- La pastille Jaune signifie : cette piste fait partie d'un Groupe
- Les points colorés (violets) plus haut et à côté des Faders montrent simplement le point 0 dB du Fader

**Il existe quelques manques et limitations, ainsi que des problèmes cachés dus à la bibliothèque Python-OSC ; peut-être que certains d'entre eux seront corrigés à l'avenir..??**
- il n'est pas encore possible de lancer/déclencher des Scènes
- il n'y a actuellement aucun contrôle sur la piste "Master"
- pas de contrôle non plus pour les pistes Aux-Return (et ils ne sont même pas affichés dans la Track-List !)
- lorsqu'une piste fait partie d'un groupe, elle sera toujours affichée dans le TouchOSC-Layout, peu importe si le groupe est replié ou déployé ! Mais lorsque le groupe est replié (pastille bleu), les pistes à l'intérieur du groupe ne peuvent plus être sélectionnées par Remote (SEL) ! (Vous verrez que le bouton SEL reste allumé dans le layout TouchOSC). Pour pouvoir sélectionner une piste lorsqu'elle fait partie d'un groupe, le groupe doit être déplié (en pastille cyan)

---
**À propos du Feedback de la Session Live :**
Pour de nombreux Feedbacks, il existe une fonctionnalité "start_listen" qui indique à Live d'envoyer des Feedbacks dès qu'il y a des changements dans la session (par exemple : Noms, Volumes, Mutes, Solo etc etc). La plupart de ces "start_listens" sont activés automatiquement lorsque le TouchOSC est mis en Online avec Live. D'autres peuvent être activés manuellement avec le bouton "Sync Many".
Et certains paramètres et valeurs ne peuvent pas être suivis automatiquement. C'est le cas pour les niveaux "Device-Parameters" et pour les niveaux "Aux-Send" ; et aussi pour les feedback "Fired-Clips" (les clips qui jouent actuellement). Pour avoir des feedback continus également pour eux, j'ai ajouté une routine de feedback continus pour chacun. Vous pouvez régler le Feedback-Rate (de lent à rapide, classiquement à 3, 1 ou 0,5 seconde.

---
Si vous avez des suggestions ou des demandes, contactez-moi  et toute aide est toujours la bienvenue !!   
Amusez-vous bien....

Un grand merci spécial à [Daniel Jones](https://github.com/ideoforms) pour son Python-Remote-Script