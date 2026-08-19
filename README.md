RX-CW

Entraîneur de morse (CW) en ligne, gratuit et accessible directement dans le navigateur — aucune installation requise. Basé sur RobotCW.

Description

RX-CW est un outil web d'entraînement à la copie et à la manipulation en morse, pensé pour les radioamateurs francophones. Il tient dans une seule page HTML autonome, à ouvrir directement dans n'importe quel navigateur (ordinateur, tablette, mobile), sans serveur ni dépendance externe.

Deux modes principaux, basculables d'un clic :

📥 Réception — copier le morse entendu
Oscilloscope en direct du signal reçu
7 types d'exercices : Indicatifs, Mots français, Préfixes, Citations, Groupes, Groupes de lettres, Groupes de chiffres
Contrôles : Transmettre, Répéter, Révéler, Suivant
Saisie de la copie au clavier, avec raccourcis (Entrée = valider, Espace = rejouer, Tab = révéler)
Compteur de réécoutes par cible
Table morse de référence, affichable/masquable
Réglages : vitesse (WPM), tonalité, longueur des groupes, espacement Farnsworth, bruit de bande (QRM léger), affichage du texte pendant la transmission, indicatif personnel inséré en fin de session
Bilan de session (précision, statistiques) sauvegardé localement

📤 Émission — manipuler en morse
9 types d'exercices : Manipulation libre, Indicatifs, Mots français, Groupes, Groupes de lettres, Groupes de chiffres, Contest, QSO réaliste, QSO français
Manipulateur virtuel (DIT/DAH) cliquable à la souris/tactile, ou piloté depuis un vrai manipulateur physique (voir section matériel ci-dessous)
Mode de manipulation : Simple (droit), Iambique A, Iambique B
Oscilloscope de votre propre signal + décodage en direct de ce que vous envoyez
Contrôles : Nouvelle cible, Révéler, Répéter, Effacer, Valider
Réglages : vitesse de manipulation, vitesse d'écoute des réponses du programme, tonalité de retour (sidetone), espacement Farnsworth, nombre d'essais par session, réassignation des touches DIT/DAH, inversion des paddles (si manipulateur monté à l'envers)
Bilan d'émission : envois exacts, précision, caractères/minute réels, meilleure série
Utiliser un vrai manipulateur (paddle) au lieu du clavier

Par défaut, RX-CW reconnaît un manipulateur simulé au clavier (touches DIT/DAH réassignables, A/É par défaut) ou à la souris/au tactile. Pour utiliser un vrai manipulateur physique, deux solutions selon le réglage "Source du paddle" :

Clavier / souris + interface DIY (Digispark) : une carte USB très bon marché (quelques euros), programmable pour se faire passer pour un clavier (HID) et envoyer les touches DIT/DAH configurées quand on actionne le manipulateur. Solution économique, demande un peu de bricolage/programmation (Arduino IDE). ⚠️ Un montage mal isolé peut générer de faux appuis (rebonds électriques) : bien débruiter le signal côté matériel.
Winkeyer USB (pont) : pour un boîtier CW commercial de type WinKeyer, qui décode lui-même le morse en matériel. Lance le script fourni winkeyer_bridge.py sur ton PC (il fait le pont entre le port série du WinKeyer et la page web via WebSocket local, ws://localhost:8765), laisse la fenêtre ouverte, puis choisis "Winkeyer USB (pont)" comme source du paddle dans RX-CW. La page se reconnecte automatiquement si la liaison est coupée.
Utilisation
Télécharge le fichier .html de ce dépôt
Ouvre-le avec n'importe quel navigateur (double-clic suffit)
Choisis Réception ou Émission
Choisis un type d'exercice et règle la vitesse/les options
Lance la session

Aucune inscription ni installation n'est nécessaire — tout fonctionne en local, directement dans le navigateur. Les statistiques et préférences sont sauvegardées automatiquement dans le navigateur (aucune donnée envoyée à un serveur).

Auteur

F4GOP

RX-CW (English)

A free, browser-based CW (Morse code) training tool — no installation required. Based on RobotCW.

Description

RX-CW is a web-based Morse code copying and sending trainer, designed with French-speaking radio amateurs in mind. It's a single, self-contained HTML page you can open directly in any browser (desktop, tablet, mobile), with no server or external dependency.

Two main modes, switchable with one click:

📥 Receiving — copy Morse by ear
Live oscilloscope of the received signal
7 exercise types: Callsigns, French words, Prefixes, Quotes, Groups, Letter groups, Digit groups
Controls: Play, Repeat, Reveal, Next
Type your copy on the keyboard, with shortcuts (Enter = check, Space = replay, Tab = reveal)
Replay counter per target
Reference Morse alphabet table, show/hide
Settings: speed (WPM), tone frequency, group length, Farnsworth spacing, band noise (light QRM), text echo while sending, personal callsign inserted at the end of the session
Session scoring (accuracy, stats), saved locally

📤 Sending — key Morse yourself
9 exercise types: Free sending, Callsigns, French words, Groups, Letter groups, Digit groups, Contest, Realistic QSO, French QSO
Virtual paddle (DIT/DAH), clickable with mouse/touch, or driven from a real physical paddle (see hardware section below)
Keyer mode: Straight key, Iambic A, Iambic B
Oscilloscope of your own signal + live decoding of what you send
Controls: New target, Reveal, Repeat, Clear, Check
Settings: sending speed, listening speed (program's replies), sidetone frequency, Farnsworth spacing, trials per session, DIT/DAH key remapping, paddle swap (if your paddle is wired reversed)
Sending stats: exact sends, accuracy, real characters/minute, best streak
Using a real paddle instead of the keyboard

By default, RX-CW recognizes a simulated paddle from the keyboard (remappable DIT/DAH keys, A/É by default) or from mouse/touch. To use a real physical paddle, two options depending on the "Paddle source" setting:

Keyboard / mouse + DIY interface (Digispark): a very cheap USB board (a few euros) that can be programmed to act as a keyboard (HID) and send the configured DIT/DAH keystrokes when the paddle is pressed. Budget option, requires a bit of DIY/programming (Arduino IDE). ⚠️ A poorly debounced build can generate false keystrokes (electrical bounce): make sure to properly debounce the signal on the hardware side.
WinKeyer USB (bridge): for a commercial CW box such as a WinKeyer, which decodes Morse itself in hardware. Run the included winkeyer_bridge.py script on your PC (it bridges the WinKeyer's serial port to the web page over a local WebSocket, ws://localhost:8765), keep the window open, then select "WinKeyer USB (bridge)" as the paddle source in RX-CW. The page reconnects automatically if the link drops.
Usage
Download the .html file from this repository
Open it in any browser (just double-click it)
Choose Receiving or Sending
Choose an exercise type and adjust speed/options
Start the session

No sign-up or installation required — everything runs locally, right in your browser. Stats and preferences are saved automatically in the browser (no data sent to any server).

Author

F4GOP
