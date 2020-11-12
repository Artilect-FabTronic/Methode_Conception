> Date de Création : 11 novembre 2020<br>
> Auteur : Lilian Tribouilloy<br>
> Licence : Creative Commonces BY NC SA<br>

# Introduction

## But de Document

Ce document a pour but de proposer une méthodologie de conception d’un objet électronique à destination du hobbyste de l’électronique qui a peur de franchir le pas. Peur de se lancer dans la conception d’un objet originale qu’il aurait conçu de A à Z.

Il s’agit bien d’__une__ méthode et non pas de __la__ méthode. En disant cela je ne présume nullement détenir la vérité absolue sur le sujet. D’autant que je trouve dangereux d’imposer, et de façon définitive, une méthode prétendument indépassable. J’encourage tout le monde à rester critique et mieux que cela à se construire ces propres méthodes de travail. Celles qui vous conviennent parce qu’elles correspondent à votre façon de penser ou tout simplement à l’investissement, en temps, que vous souhaitez y consacrer. Travailler c’est « trouvailler » dit l’adage. Dès lors qu’on se laisse dicter les méthodes, on perd son métier. On perd l’opportunité de rentrer par soi‑même dans le chemin qui nous construit à force d’expériences.

Cet avertissement important étant entendu. Il faut toutefois admettre que le savoir est une valeur collective. Et qu’il est bon d’apprendre de ses paires pour ne pas se perdre trop longuement dans une science ou un art difficile. Les chemins déjà tracés doivent vous enseigner, vous inspirer, vous faire gagner du temps. Pas vous contraindre.

Ce document n’a pas vocation à vous apprendre les bases théoriques de l’électronique, ni à vous informer sur les avantages de telle ou telle technologie. Il propose simplement une méthode pas à pas pour transformer vos idées en réalisation concrète. Ce document n’a pas non plus pour prétention d’atteindre un niveau de rigueur industriel bien trop chronophage pour un hobbyste. Il liste les actions importantes à faire pour ne pas commettre d’erreurs onéreuses qui ruinerait votre projet. Toutefois, ce document sera parsemé de comparaison entre ce qui se pratique dans l’industrie et ce qui me semble plus raisonnable de mettre en œuvre pour un amateur. À vous de placer le curseur entre rigueur et plaisir et entre idéalisme et réalisme.

Ce document est à destination du public des _fablabs_, du _mouvement Maker_ et du _mouvement du Logiciel et matériel Libre_. Aussi les outils proposés en complément de la méthodologie sont tous des logiciels libres. À savoir : [KiCAD](https://kicad-pcb.org/) pour l’édition de schéma et le routage des cartes ; [FreeCAD](https://www.freecadweb.org/) pour la conception de la mécanique associée (simple boîtier ou robot sophistiqué selon votre projet). Ce sont aujourd’hui les logiciels libres les plus avancés dans ces domaines mais on pourra d’aventure trouver des alternatives. Le choix de l’éditeur de code est laissé à votre sagacité tant la diversité dans ce domaine est grande.

À n’en pas douter il existe des logiciels propriétaires bien plus puissants que ceux que je propose ici. Mais la liberté n’est pas une question de performance. La liberté est d’ailleurs une performance en soit par les temps qui court. C’est une question d’écosystème, une question de partage avec votre communauté. Comme le dit si bien Richard Stallman (fondateur de la Free Software Fondation, cocréateur de GNU/Linux, entre autres choses), et il le dit en français dans le texte : _«Je peux résumer ce qu’est le logiciel libre en 3 mots : liberté, égalité, fraternité.»_

Et pourquoi un tel ouvrage ? Il m’est apparût que le matériel libre (ou objet libre) est beaucoup moins développé que le logiciel libre. Et à n’en pas douter il y a des raisons à cela assez simples. Les objets libres représentent un défit plus grand encore que le logiciel libre pour les communautés libristes internationales. En effet, il y a d’abord le prix, si le logiciel libre peut donner l’illusion de la gratuité pour l’utilisateur ; avec un objet libre, il devient évidant que ça ne peut aucunement être gratuit. Sans oublier que la fabrication de n’est pas évidente car il faut être équiper en outils et il faut se forger du savoir, développer ses facultés manuelles.

Il y a aussi la difficulté, car un objet libre moderne et complet, c’est au moins trois disciplines, au logiciel, s’ajoute l’électronique et la mécanique. Et cela pose un défi collaboratif et organisationnel important. Car peu de gens sont suffisamment forts pour avoir un bon niveau de maîtrise dans ces 3 disciplines. Quand il n’y en a que 3… Il faut aller chercher les compétences nécessaires chez d’autres personnes et les motivés à travailler sur le projet. Motiver est une difficulté loin d’être négligeable.

Ainsi, ce manuel est aussi une modeste contribution pour favoriser une bonne organisation des projets objets libres et pour favoriser une bonne structuration de leurs dossiers d’étude associés. D’autant que je n’ai pas trouvé de sur le net de site qui explique comment concevoir concrètement un objet. Le peu que j’ai trouvé reste sur des grands principes qui ne sont pas forcément d’un grand renfort pour l’exercice réel. Ou bien au contraire pour un projet donné, la personne dit j’ai fait donne ça. Avec parfois une grande précision, certe, mais il ne se dégage jamais une vue d’ensemble sur une méthodologie.


## À Propos de l’Auteur

__Lilian Tribouilloy__

* __Formation :__ Ingénieur en électronique, diplômé de l’[ENSEA](https://www.ensea.fr/fr) en 2004.
* __Métier :__ Concepteur électronique spécialisé dans les radiofréquences et la CEM (Compatibilité ÉlectroMagnétique).
* __Exemples de produit conçu dans le cadre professionnel :__ Émetteur et Réémetteur pour la télévision numérique ; Amplificateur de puissance classe AB pour une modulation OFDM ; Calculateur entrées/sorties pour camion ; Tableau de bord pour véhicule spéciaux ; Boîtier de télématique pour la gestion de flotte.
* __Objet Libre conçu :__ [ToucheLibre](http://touchelibre.fr/), un clavier d’ordinateur ergonomique en bois. Aliant l’esthétique à l’utile, il s’inscrit dans des valeurs de liberté, d’écologie et de santé.


## Licences

Ce manuel est placé sous licence Creative Commons 

Dont vous trouverez la version originale ici : [Creative Commons BY-SA](https://creativecommons.org/licenses/by-sa/4.0/legalcode) 

Et la traduction française ici : [Creative Commons BY-SA](https://creativecommons.org/licenses/by-sa/4.0/legalcode.fr)

De plus, ce manuel utilise les polices de caractères suivantes :

* Exo2, créé par Natanael Gama sous licence SIL Open Font, accessible sur le site [Font Squirrel](https://www.fontsquirrel.com/fonts/exo-2)
* Cinzel, créé par Natanael Gama sous licence SIL Open Font, accessible sur le site [Font Squirrel](https://www.fontsquirrel.com/fonts/cinzel)

Ces polices devrons être installées pour voir l’ouvrage dans la forme voulu par l’auteur.

Vous pouvez accédérer aux sources du document soit sur le repository suivant sur [GitHub](https://github.com/LilyTouch/Methode_Conception), ou soit en ouvrant ce fichier « Méthode_de_Conception_d’un_Objet_Libre.pdf » avec LibreOffice.

En effet, ce fichier est un pdf hydride. C’est à dire qu’il embarque directement le fichier source odt, il peut être directement éditer par LibreOffice.


## Références Documentaires

Ouvrages qui ont été des sources d’inspiration et qui pourront vous servir à approfondir le sujet.

* [Résolu](https://framabook.org/resolu/)
* [Logiciels et Objets Libres](https://framabook.org/logiciels-et-objets-libres/)
* [Produire du Logiciel Libre](https://framabook.org/produire-du-logiciel-libre-2/)


## Convention Graphique
