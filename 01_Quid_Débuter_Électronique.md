> Date de Création : 20 septembre 2020<br>
> Auteur initiale : Lilian Tribouilloy<br>
> Licence : Creative Commonces BY NC SA<br>

# De quoi a‑t‑on besoin pour débuter l’électronique ?

## Introduction
Ce document est un petit guide pour celui qui souhaite découvrir l’électronique (et ce qui tourne autour).
Il n’a pas vocation à être parfaitement pédagogique, ni exhaustif.
Mais il donne une idée de l’investissement en temps et en argent nécessaire.
Et ceci pour vous permettre de voir si vous êtes prêt à allez plus loin. (On va pas vous mentir l’électronique est une discipline difficile et chronophage)

Et si d’aventure vous êtes motivé, cela vous aide à construire votre boite à outil.
On donne une indication approximative du prix ou sinon la disponibilité au fablab [Artilect](https://artilect.fr/).


## Préalable indispensable
Le minimum que nous impose la modernité de notre société si on veut accéder à des informations et des outils à moindre coût.

* Ordinateur
* Connexion internet

L’adhésion à un fablab peut être un soutien fort appréciable pour le soutien communautaire et pour le prêt ou la location d’outillage.


## Niveau 0 ; Prix = 0€
Pour goûter sans dépenser.
Que du logiciels libre, gratuit et disponible sur tous les OS.
Des sources d’information pédagogique.
Des exemples de projet pour motiver.

* Logiciels pour l’Électronique : 
	- Kicad, éditeur de schéma électronique et routage de circuit imprimé
	- LT Spice, simulation base fréquence (pas dispo sur Linux)
	- QUCS, simulation haute fréquence et micro‑électronique (attention logiciel difficile)
	- QElectroTech, électricité domestique
	- Fritzing, routage sur carte de test (type breadboard)

__«L’électronique a deux super potes dans sa bande : la programmation et la mécanique.»__

* Logiciels pour la Programmation :
Il y a une grande diversité dans ce domaine. À vous de vous faire votre propre opinion.
	- Éditeur de code généraliste (Gedit, Sublime texte, Visual Studio Code…)
	- IDE pour les cas particuliers (IDE Arduino, Code::Block, Geany…)
	- Éditeur de fichier binaire (GHex, wxHexEditor…)
	- Meld pour comparer 2 codes.

* Langages de programmation recommandés pour le bas niveau (code directement en interaction avec l’électronique)
	- C, le langage de référence en bas niveau
	- C++, le complément «orienté objet» du C. Il est notamment utilisé pour les bibliothèques Arduino
	- Python, un langage de script à l’origine, ce langage a connu une popularité dans plein de domaines y compris en bas niveau avec son extension Micro‑Python.
	- GIT, pour le partage des sources et la gestion des versions

* Logiciels pour la Mécanique :
	- FreeCAD, conception en 3D, type paramétrique, génération de Gcode pour l’usinage.
	- LibreCAD, conception en 2D (attention prise en main difficile), manipulation de fichier DXF.
	- CAMotics, pour simuler le parcours d’une CNC.

* Logiciels divers de Dessin et Bureautique :
Ce qui peut être nécessaire en complément dans certain cas.
	- Gimp, dessin matriciel, retouche photo.
	- Inkscape, dessin vectoriel, pour donner à la découpe laser.
	- Blender, image de synthèse en 3D, imprimante 3D pour les objets modélisés par maillage.
	- LibreOffice
	- Calculatrice (SpeedCrunch)
	- Prise de note : traditionnel à la main ou informatisé (CherryTree)

* Sites où on trouve du contenu pédagogique
	- Youtube
	- Wikipedia
	- OpenClassRoom
	- https://www.arduino.cc/
	- https://www.tutorialspoint.com/cprogramming/index.htm
	- https://www.tutorialspoint.com/python/index.htm
	- https://les-electroniciens.com/cours-d-electronique
	- https://learngitbranching.js.org/?locale=fr_FR
	- https://github.com/github/opensource.guide/blob/master/_articles/fr/how-to-contribute.md
	- https://guides.github.com/activities/hello-world/
	- …

* Sites où les gens parlent de leurs projets
	- https://www.makery.info/
	- https://www.framboise314.fr/
	- https://create.arduino.cc/projecthub
	- https://ouiaremakers.com/
	- https://projects.fablabs.io/
	- http://libreobjet.org/index.html
	- https://www.lairdubois.fr/
	- https://wikifab.org/wiki/Accueil
	- reddit
	- pinterest
	- …

__Conseil : La curiosité n’a jamais été un défaut.__


## Niveau 1 ; Prix = 100€ à 300€
Vous êtes motivé, vous souhaitez commencer à mettre les mains dans le cambouis.

* Multimètre entrée de gamme (40€ à 60€)
* Un bloc d’alimentation secteur
* Fer à souder entrée de gamme (Dispo au FabLab)
* Outillage à main divers: pince coupante, pince plate, jeux de tournevis…
* Carte de développement : Arduino ou Rapsberry Pi ou autres…
* Composants de base selon le premier petit projet pédagogique (Résistance, LED, condensateur, fil, diodes, transistor…)

Où se procurer du matos :
* Conrad
* Radiospares
* Farnell
* Kubii
* AliExpress
* BangGood
* Mouser
* https://www.polytech-oscilloscopes.com/
* Amazon
* …

__Conseil : Pratiquer régulièrement. N’aillez pas peur de bidouiller et poser des questions.__


## Niveau 2 ; Prix = 100€ à 300€
La passion commence à vous gagner, alors plus de matos générals pour étoffer la caisse à outil.

* Un espace bureau adapté avec de quoi ranger le matos. (Quand on commence à bricoler il faut de la place…)
* Pince à dénuder
* Pince brucelle
* Cutter type scalpel
* petite lime ou ponçage
* Divers consommables
* Une station de soudage (on parle de brassage en fait), et les consommables associés.
* Une petite perceuse multifonction (type Dremel)
* 3ième main et/ou petit étaux
* Multiprise
* Un bon éclairage

__Conseil : Trouver vous un projet qui vous passionne, mais abordable selon votre niveau. Vous devez apprendre à apprendre, un fablab n’est pas une école.__


## Niveau 3 ; Prix = 400€ à 1000€
Les choses sérieuses commencent, il vous faut pourvoir débeuger les cartes efficacement.

* Organiser votre espace de travail.
* Alimentation de laboratoire (Dispo au FabLab)
* Analyseur Logique
* Sonde de débeug
* Loupe (mieux sur bras articulé)
* Fer à air chaud
* Thermomètre infrarouge

__Conseil : Lancer vous des défis avec des projets toujours de plus en plus complexe.__


## Niveau 4 ; Prix = 400€ à 1000€
On ne peut plus vous arrêter…

* Oscilloscope (Dispo au FabLab)
* Multimètre de laboratoire
* Microscope binoculaire
* générateur de signal BF (Dispo au FabLab)
* Charge active
* Caméra thermique
* pince ampèremétrique

Où faire fabriquer vos circuits à prix raisonnable ?
* https://jlcpcb.com/ : Le moins chers mais limiter à 6 couches. Et on est très limité sur l’empilage.
* https://www.pcbway.com/ : Plus de configuration possible, mais nettement plus chers.
* https://www.eurocircuits.com/blog/the-history-of-order-pooling/ : Fabriquant européen, service industriel plus facile, mais nettement plus chers.
* Sinon aller dans un fablab qui propose une CNC spécialisée pour les PCB (Printed Circuit Board). Attention limité à 2 couches.
* Sinon méthode traditionnelle de prototypage : plaque à trous, gravure au perchlorure de fer.

__Conseil : Réaliser vos rêves.__


## Niveau 5 ; prix = 1000€ à 20000€
Vous êtes définitivement un super geek de la mort.

* CNC gravure de PCB
* Imprimante 3D (Dispo au FabLab)
* Découpe laser (Dispo au FabLab)
* Fraiseuse numérique (Dispo au FabLab)
* Four à composant CMS
* Machine pick and place
* Analyseur de spectre
* Analyseur vectoriel de réseaux

__Conseil : Faite de votre passion un métier.__


## Niveau +++
Vers l’infini et au delà.

__Conseil : Il ne reste plus qu’à monter votre boîte…     ;-)__


