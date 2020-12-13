> Date de Création : 11 novembre 2020  
> Auteur initial : Lilian Tribouilloy  
> Contributeurs : Voir le fichier CREDITS.md  
> Licence : Creative Commons BY SA  

# Construire sa Boîte à Outils

## Les Outils, c’est la Vie

L’Humain a une relation aux outils très particulières et sans équivalent dans le règne animal. Qu’on le veuille ou non les outils font partie de notre vie. Les musiciens savent cela, le médium influence le médiateur. Les outils influencent intimement nos créations. Ils font partie de la forge de notre savoir et de nos métiers. Comme je le disais plus haut pour faire l’épreuve du réel, il faut être concret. Et pour cela les outils sont une composante essentielle (avec les idées et les matériaux).

Comme disent les anglais : “ Shit input, shit output ”. Si vous n’avez pas de bons outils, vous ne ferez jamais rien de bien. Et un mauvais outil qui ne marche pas ça coûte trop cher. Bien sûr, on ne peut pas faire autrement que de faire avec son budget. Mais grâce au mouvement logiciel libre de super outils sont devenus gratuits. De plus, au développement des FabLabs, on peut accéder à des outils high‑tech pour le coût très raisonnable d’une location.

> « _Que dieux me débranche. Des machines qui créent des machines._ »		C3PO dans Star Wars 2.

Et si cela ne suffit pas, la démarche de se fabriquer ses outils est une excellente démarche et en soi des projets passionnants. D’ailleurs, se construire ses outils est une démarche très ancienne. Aujourd’hui encore, fabriquer ses outils fait partie de la formation initiale des compagnons du devoir. _Les projets autour de la conception d’outil sont, selon moi, un enjeu majeur pour le développement des objets libres._ Quelques fameux exemples sont donnés dans les paragraphes suivants.



## Comment Choisir ses Outils ?

Les outils ont selon moi quasiment autant d’importance que les méthodes. Vous devrez prendre la main sur le choix de ces outils. Vous ne devez pas vous laisser imposer aveuglément le choix des outils. Comme dit en introduction pour les méthodes, c’est à vous seul de faire le choix des outils. Mais là encore le savoir est une valeur collective. Et les propositions d’outils dispensées en suivant doivent vous aider à choisir, vous faire gagner du temps, en aucun cas vous contraindre.

{dans quel écosystème se situer…}

Il existe des outils pour tout. Et pour tout chose, il existe une diversité prodigieuse.
Action fondamental «couper»…

{
Il faut éviter les outils de type couteau suisse qui prétendre savoir tout faire.
https://fr.wikipedia.org/wiki/Matériel_libre
}


_____________________________________________________________

## Les Logiciels Libres dédiés la Conception

je vous recommande ceci. Il s’agit là de valeurs sûres, reconnues et largement utilisées. Bien sûr les choses évoluront dans le temps et cette liste pourra être revue.

### Pour l’Électronique

* Édition Schéma et Routage Électronique : [KiCAD](https://kicad.org/). Vous trouverez le manuel d’utilisation [ici](https://docs.kicad.org/)
* Éditeur de Schéma Électrotechnique ou Électricité Domestique : [QElectroTech](https://qelectrotech.org/)

{
	- Kicad, éditeur de schéma électronique et routage de circuit imprimé
	- LT Spice, simulation base fréquence (Dispo sur Linux en passant par Wine)
	- QUCS, simulation haute fréquence et micro‑électronique (attention logiciel difficile)
	- QElectroTech, électricité domestique
	- Fritzing, routage sur carte de test (type breadboard)
	- FlatCAM, pour graver un circuit imprimé à la CNC.
}

### Pour la Mécanique

* Conception Mécanique en 3D : [FreeCAD](https://www.freecadweb.org/?lang=fr). Vous trouverez le manuel d’utilisation [ici](https://wiki.freecadweb.org/Getting_started)

{

* Logiciels pour la Mécanique :
	- FreeCAD, conception en 3D, type paramétrique, génération de Gcode pour l’usinage.
	- LibreCAD, conception en 2D (attention prise en main difficile), en complément de FreeCAD pour manipulation de fichier DXF.
	- CAMotics, pour simuler le parcours d’une CNC.
}

### Pour la Programmation

* Éditeur de Code :
* 

{
* Logiciels pour la Programmation :
Il y a une grande diversité dans ce domaine. À vous de vous faire votre propre opinion.
	- Éditeur de code généraliste (Gedit, Kate, Vim…)
	- IDE pour les cas particuliers (IDE Arduino, Geany, Code::Block…)
	- Éditeur de fichier binaire (GHex, wxHexEditor…)
	- Comparateur de 2 codes (Meld pour Linux, Winmerge pour Window).
	- Compilateur (GCC = GNU Compilateur Collection)

* Langages de programmation recommandés pour le bas niveau (code directement en interaction avec l’électronique)
	- C, le langage de référence en bas niveau
	- C++, le complément « orienté objet » du C. Il est notamment utilisé pour les bibliothèques Arduino
	- Python, un langage de script à l’origine, ce langage a connu une popularité dans plein de domaines y compris en bas niveau avec son extension Micro‑Python.
	- GIT, pour le partage des sources et la gestion des versions
}

### Autres

{
* Logiciels divers de Dessin et Bureautique :
Ce qui peut être nécessaire en complément dans certain cas.
	- Gimp, dessin matriciel, retouche photo.
	- Inkscape, dessin vectoriel, pour donner à la découpe laser.
	- Blender, image de synthèse en 3D, imprimante 3D pour les objets modélisés par maillage.
	- LibreOffice
	- Calculatrice (SpeedCrunch)
	- Prise de note : traditionnel à la main ou informatisé (CherryTree)
}


_____________________________________________________________

## Outils de Laboratoire Libres
* All-in-one USB Oscilloscope, Signal Generator, Power Supply, Logic Analyzer and Multimeter basée sur l'Atmega32u4 , processeur bien connu ;) : [Site](https://espotek.com/labrador/product/espotek-labrador-board/) ; [github](https://github.com/espotek/labrador)
* [Open Source Multimeter](https://hackaday.com/2019/06/20/finally-an-open-source-multimeter/)
* [Open Source Transistor Tester](https://www.mikrocontroller.net/articles/AVR_Transistortester#Introduction_.28English.29)
* [Scope Fun](https://www.scopefun.com/) : un oscilloscope performant en développement libre. Voir également le [répertoire GitLab](https://gitlab.com/scopefun) pour les sources. Et pour soutenir le projet voir ce [Crowd Supply](https://www.crowdsupply.com/scopefun/open-source-instrumentation).

* Analyseur logique : https://sigrok.org/
https://pslab.io/
TS100 https://hackaday.com/2017/07/24/review-ts100-soldering-iron/


_____________________________________________________________

## Outils Informatiques
* [The Much More Personal Computer](https://mntre.com/media/reform_md/2020-05-08-the-much-more-personal-computer.html) : Un PC portable entièrement libre. Voir également leur [répertoire GiTea](https://source.mntmn.com/MNT) pour les sources. Et pour soutenir le projet voir ce [Crowd Supply](https://www.crowdsupply.com/mnt/reform).
* [ToucheLibre](http://touchelibre.fr)

{
Ordinateur

Dans le cas des ordinateurs, est considéré comme matériel libre la disponibilité en licence libre et à sources ouvertes des schémas fonctionnels et plans d'assemblage. Il n'est pas tenu compte ici de la licence des composants, comme dans le monde du logiciel libre, la licence du matériel sur lequel il tourne n'est pas prise en compte.

    Arduino : carte contrôleur programmable permettant de gérer différents types de matériel et de faire des robots et ses dérivés parfois nommés Duino Maple, Pinguino, etc..
    BeagleBone et BeagleBoard-xM : cartes mères fondées sur des SoC d'architecture ARM de Texas Instrument.
    Firefly-RK3288 (licence CC BY 3.0) : fondé sur un Rockchip RK3288 27.
    Novena
    OLinuXino : carte mère fondée sur différents SoC d'architecture ARM (Freescale iMX233 et AllWinner A13, A10S et A20).
    Parallella
    PowerPC : un ordinateur portable [archive] sous licence Open Hardware
    Pine64 (en) : ordinateurs monocartes et netbook.
    Radxa (licence CC BY 3.0)
    Simputer : assistant numérique conçu et lancé en Inde en 2004 afin de proposer un ordinateur simple, peu onéreux et multilingue aux populations rurales
    Touchbook : Smartbook/Netbook2
}


_____________________________________________________________

## Les Outils de Communication

{À ajouter}


_____________________________________________________________

## Construire son Atelier / Labo

### Son Espace de Travail

### Les outils physiques pour l’Électronique

### Les outils physiques pour la Mécanique


