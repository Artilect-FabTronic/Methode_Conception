> Date de Création : 23 septembre 2020
> Auteur initiale : Lilian Tribouilloy
> Licence : Creative Commonces BY NC SA

# Méthodologie de Conception d’un Objet Électronique

## Introduction

Ce document a pour but de proposer une méthodologie de conception d’un objet électronique à destination du hobbyste de l’électronique qui a peur de franchir le pas. Peur de se lancer dans la conception d’un objet originale qu’il aurait conçu de A à Z.

Il s’agit bien d’__une__ méthode et non pas de __la__ méthode. En disant cela je ne présume nullement détenir la vérité absolue sur le sujet. D’autant que je trouve dangereux d’imposer, et de façon définitive, une méthode prétendument indépassable. J’encourage tout le monde à rester critique et mieux que cela à se construire ces propres méthodes de travail. Celles qui vous conviennent parce qu’elles correspondent à votre façon de penser ou tout simplement à l’investissement en temps que vous souhaitez y consacrer. Travailler c’est « trouvailler » dit l’adage. Dès lors qu’on se laisse dicter les méthodes, on perd son métier. On perd l’opportunité de rentrer par soi‑même dans le chemin qui nous construit à force d’expériences.

Cet avestissement important étant entendu. Il faut toutefois admettre que le savoir est une valeur collective. Et qu’il est bon d’apprendre de ses paires pour ne pas se perdre trop longuement dans une science ou un art difficile. Les chemins déjà tracés doivent vous enseigner, vous inspirer, vous faire gagner du temps. Pas vous contraindre.

Ce document n’a pas vocation à vous apprendre les bases théoriques de l’électronique, ni à vous informer sur les avantages de telle ou telle technologie. Il propose simplement une méthode pas à pas pour transformer vos idées en réalisation concrète. Ce document n’a pas non plus pour prétention d’atteindre un niveau de rigeur industriel bien trop chronophage pour un hobbyste. Il liste les actions importantes à faire pour ne pas commettre d’erreurs anéreuses qui ruinerait votre projet. Toutefois, ce document sera parcemé de comparaison entre ce qui se pratique dans l’industrie et ce qui me semble plus raisonnable de mettre en œuvre pour un amateur. À vous de placer le curseur entre rigeur et plaisir et entre idéalisme et réalisme.

Ce document est à destination du public des _fablabs_, du _mouvement Maker_ et du _mouvement du Logiciel et matériel Libre_. Aussi les outils proposés en complément de la méthodologie sont tous des logiciels libres. À savoir : [KiCAD](https://kicad-pcb.org/) pour l’édition de schéma et le routage des cartes ; [FreeCAD](https://www.freecadweb.org/) pour la conception de la mécanique associée (simple boitier ou robot sophistiqué selon votre projet). Ce sont aujourd’hui les logiciels libres les plus avancés dans ces domaines mais on pourra d’aventure trouver des alternatives. Le choix de l’éditeur de code est laissé à votre sagassité tant la diversité dans ce domaine est grande.

À n’en pas douter il existe des logiciels propriétaires bien plus puissants que ceux que je propose ici. Mais la liberté n’est pas une question de performance. La liberté est d’ailleur une performance en soit par les temps qui court. C’est une question d’écosystème, une question de partage avec votre communauté. Comme le dit si bien Richard Stallman (fondateur de la Free Software Fondation, cocréateur de GNU/Linux, entre autres choses), et il le dit en français dans le texte : _«Je peux résumer ce qu’est le logiciel libre en 3 mots : liberté, égalité, fraternité.»_


------------------------------------------------------------------------

## C’est quoi au fait la conception ?

### Concevoir, un état d’esprit

On m’a une fois poser la question, au regard de mes créations, si j’étais un designer. Voici la réponse que j’ai apporté :


> _Suis‑je designer ? Si je me conforme à la définition française, oui. Le truc, c’est que je n’aime pas beaucoup cette définition. Je trouve que ça fait trop formule magique. Dès que je vois un mot anglais, j’ai mon détecteur de langue de bois qui clignote. Je m’explique._
>
> _Le mot designer est un mot d’emprunt de l’anglais qui veut dire concepteur. Comme tu le sais sans doute. Mais les français ont modifié le sens de ce mot pour y ajouter quelque chose de différent. Quelque chose que les anglo‑saxons, me semble‑t‑il, ne mettent pas du tout._
>
> _Conception vient du latin conceptus qui signifie «action d’accueillir et de contenir». Et C’est exatement le même mot en latin pour traduire la période de gestation des femmes. N’est ce pas ce qu’elles font pendant cette période pour parler basiquement ? Elles accueillent la «graine» et elles le contiennent jusqu’à ressortir l’enfant. Du reste, aujourd’hui encore dans la langue française, on dit concevoir un enfant. Et même dans la bible, on parle d’immaculé conception._
>
> _Et bien concevoir en technologie, c’est exactement ça mais avec des idées. (Que saurait‑il faire d’autre un homme…?) On accueille une idée. Parfois c’est sa propre idée, parfois c’est celle des autres. (Trop souvent dans l’industrie, c’est celle des autres…) Puis on la mette en gestion un certain temps et selon un processus créatif plus ou moins complexe. Jusqu’à obtenir une chose tangible, quelque chose de réelle._
>
> _Alors, oui, c’est exactement ce que je fais. Et définitivement, je suis un concepteur. Et si on le dit en anglais: I am a designer. Au sens strict._
>
> _Mais c’est un peu court pour décrire l’activité dans son détail. La question est : Je conçois quoi ? Et je mets en œuvre quel discipline ? Le quoi et le comment est, selon moi, la seule façon de ne pas se tromper dans la description de son métier._
>
> _Alors, posons les choses simplement. Je fais des claviers pour l’informatiques. Facile, ça tout le monde aura compris. Et je déploie les disciplines suivantes : électronique, mécanique, programmation, menuiserie, de l’ergonomie. Et quoi d’autre ? Quelle est donc cette substante subtile qui tend à identifier une esthétique. Et peut‑être pour certain une émotion ?_
>
> _Je ne vois pas ce que cela pourrait être d’autre que de l’art. Ou peut‑être de l’artisanat à la limite. Il me semble que c’est bien cela qui est ajouté en plus dans le mot designer à la française. Et à l’italienne aussi d’ailleurs._
>
> _La distinction entre art et artisanat est relativement tardive. Elle date de la Renaissance. Cette distinction est apparu en italie au moment précis où un petit groupe de gens est devenu très très riches. L’époque des grands explorateur, Marco Polo… Et la naissance des banques modernes. Et où ils ne savaient plus comment afficher, affirmer, leur distinction sociale. Alors ils ont demandé à avoir des choses, même inutiles, que personne d’autre pouvait se payer. L’art est né de cet acte d’orgueil._
>
> _La différence entre art et artisanat est très culturelle. Et il existe encore des cultures humaines où on ne fait pas la distinction._
>
> _Et c’est pour cela, que je tiens à préciser que dans ce que je fais il y a un peu d’art, de l’art utile. Et c’est là un jugement morale et une philosophie que j’assume._


Aussi, il subsiste dans l’acte de création quelque chose de mytérieux. Quelque chose qui dépose la simple raison. Aussi m’est‑il impossible de vous apprendre comment trouver l’idée d’un objet. Je ne peux que vous conseiller de bien prendre le temps de murir l’idée en vous et de passer le plus rapidement possible à l’expérimentation. D’écouter ce que les gens vous disent, tout en se méfiant de ce que les gens vous disent. L’intuision peut dépasser les préjugés.

Une idée n’est rien, seule compte sa réalisation tangible. Le signe quasi certain qu’une idée est bonne, est qu’elle ne vous lache pas, qu’elle vous hante continuellement. Mais le signe absolument certain qu’une idée est bonne, est qu’elle fonctionne réellement et que les gens l’utilisent.


### Concevoir un produit complet moderne, c’est mélanger plusieurs disciplines

Un objet électronique complet moderne est toujours constituer d’aux moins 3 disciplines : Électronique, Mécanique (au sens large) et Programmation.

Mais il arrive qu’il en compte bien d’avantage comme la chimie, la biologie, la menuiserie, la couture, l’architecture, l’art et que sais‑je encore. Il ne sera donc pas possible d’exposer toutes les techniques ou arts qu’il est possible de mettre en œuvre dans un objet électronique. Pour autant que l’électronique soit réellement au centre de l’objet ou qu’il serait qu’une fonctionnalité discrète.

Nous nous concentrerons ici donc que sur les trois premières disciplines sitées.

Doit‑on commencer le travail par l’électronique, la mécanique ou le logiciel ? Tout dépend de la nature du projet. Et du degré d’interaction entre les 3.

Si la mécanique n’est qu’un simple boitier. Alors l’interaction entre électronique et mécanique sera faible. Il y a dans ce cas assez peu de sujets à aborder : Dimension et emcombrement général ; Condition environnementale (température, vibration, étanchéité…) ; Dissipation thermique ; Isolation électrique et sécurité des personnes ; Connectique ; assemblage de la carte et du boitier. On pourra donc se contrer sur l’électronique en premier. Ce qu’il ne signifie pas que l’on ne peut pas se poser les questions précédentes au fil de l’eau.

Évidement si la mécanique est en faite un objet articulé complexe comme un robot par exemple. L’interaction entre électronique et mécanique sera forte. Et il sera bon de pousser les deux disciplines simultanément ou alternativement. Faire beaucoup d’itération entre les deux permet de limiter les erreurs.

L’interaction entre électronique et logiciel est presque toujours forte sur un objet moderne. Mais tout dépend de la complexité de l’objet. Là aussi, faire beaucoup d’itération entre les deux (ou finalement les trois) permet de limiter les erreurs. Dans l’industrie, on va jusqu’à faire des spécifications d’interface entre le Hardware (électronique) et le software (programmation) pour lever toutes les ambiguïtés. Et il peut y avoir des spécifications d’architecture pour coordonner les efforts des 3 métiers (quand il y en a seulement que 3). Aussi, si vous n’êtes pas tout seul sur le projet, ce qui n’arrive quasiment jamais dans l’industrie contrairement en mode hobbis, une bonne communication entre les différents métiers et absolument essentielle à la réussite du projet.

Quoi qu’il en soit vous ne pourrez pas faire l’économie de vous investir sérieusement dans les 3 (ou plus encore) disciplines. Et il sera bon de chercher de l’aide dès qu’un blocage se présente. Être concepteur, c’est passé sa vie à apprendre des choses, d’autant que les technologies ne saissent d’évoluer. Il est donc urgent d’apprendre à apprendre.

Les fablabs, les makerspaces ou les hackerspaces ou peut importe comment on les appelle, trouvent là tout leurs intérêts…


### Doit‑on Concevoir Seul ou à Plusieurs ?

{Brouillon}
À vous de voir. Il faut faire selon les envies.
Il faut pas que ce soit une contraite invivable.

C’est plus difficile, car ça demande forcément plus d’organisation.
Attention à bien se répartir les taches pour éviter la zizanie.
Attention il existe une dimension maximum à partir de laquelle ça ne fonctionne plus.
{/Brouillon}


### Cartographie des étapes de Conception

### Un travail de long haleine

### Proposition de Dossier d’étude

Voici une façon d’organiser votre dossier d’étude pour bien s’y retrouver.

* __00_Management__
	- Communication sur le projet
		+ Site Internet
		+ Logo
		+ Articles de presse
	- Achat outils
	- Licences utilisés
	- Feuille de Route

* __01_Système__
	- Documents Techniques
	- Spécification
	- Base de Données Composants
	- Suivi des Beugues

* __02_Électronique__
	- Justification Théorique
	- Schéma & Routage
		+ Carte 1
		+ Carte 2
	- Nomenclature
		+ Carte 1
		+ Carte 2
	- Gerber
		+ Carte 1
		+ Carte 2
	- Tests de Mise au Point
	- DFMEA

* __03_Mécanique__
	- Spécification Mécanique
	- Plan  2D
		+ Design Préliminaire
		+ Interface Méca / PCB
	- Plan  3D
		+ version 1
		+ version 2
	- Tests

* __04_Programmation__
	- Spécification Logiciel
	- Code Source
	- Pilote Spécifique
	- Tests

* __05_Fabrication__
	- Manuel de Fabrication
	- Achat Composants et Matériaux
	- Fichiers de Fabrication Partie Électronique
	- Fichiers de Fabrication Partie Mécanique
	- Téléchargement et Configuration Logiciel

------------------------------------------------------------------------

## Concevoir la partie Électronique

### Vu sur le flux de travail

{image sur le cycle en V industriel/}
0. ÉTUDE DE MARCHÉ
1. SPÉCIFICATION
2. JUSTIFICATION
3. SCHÉMA
4. ROUTAGE
5. FABRICATION DU PROTOTYPE
6. VÉRIFICATION
7. QUALIFICATION : Respect des Normes et Réglementation
8. VALIDATION
9. FABRICATION EN SÉRIE

Pour un projet hobbyste, je recommanderai la plus grande simplicité possible. À vous de définir vos outils de communication. Mais un dossier de partage, ou mieux une gestion de type GIT est souvent indispensable. Faite vous votre opinion rapidement sur les outils et imposait en commun accord.

Critique de celui‑ci.

{image sur ce qui correspond mieux à la façon réelle de penser}
0. IDÉE
1. SPÉCIFICATION
2. JUSTIFICATION
3. SCHÉMA
4. ROUTAGE
5. FABRICATION DU PROTOTYPE
6. MISE AU POINT
7. DOCUMENTATION POUR COMMUNAUTÉ

Commentaire 

### Une liste de questions à se poser

0. IDÉE
	La créativité est une chose mystérieuse. Personne ne peut prétendre donner une méthode générale pour trouver des idées. Il faudrat creuser au bout de vous même. Et vous faire confiance.


1. SPÉCIFICATION
	* Le but d’une spécification est de poser le besoin, idée, envie. Faites‑vous au moins pour vous même un petit texte pour expliquer ce que vous voulez faire. Faire des petits dessins. Faire une liste des caractéristiques essentielles.
	* Essayer d’indentifier clairement quel est le problème et comment on cherche à le résoudre.
	* Ensuite, il faut développer la solution en levant les ambiguïtés. Il faut déméler l’implicite de l’explicite. Et il faut écrire ce qui est tacite.
	* Faire un synoptique (schéma de principe sans les alimentations). Ce qui va permettre de clarifier l’architecture de l’objet. Il doit faire apparaitre des détailles, des fonctions nécessaire auxquelles vous n’aviez pas pensé au début. Refaire le symoptique jusqu’à ce qu’il semble complet.
	* Faire la liste de tous les sous‑blocs fonctionnels. Cette liste pourra servir à toutes les étapes de la conception. Une sorte de check‑list pour chaque question : alimentation, référence composant, justification, routage… On peut également identifier s’il y a des parties optionnelles au projet. Il faut peut être pouvoir imaginer des extentions futures.
	* Pour les fonctions principales fixer les choix de composants. Si ce ne pas claire, ne pas hésiter à faire de petite maquette pour éprouver la pertinence de la solution. Typiquement, le micro‑controleur est un composant qui ne sera pas interchangeable, il faut être certain qu’il pourra prendre en compte toutes les fonctions.
	* Quand les choix des composants principaux sont arrêtés. Acheter ces composants car il risque d’y avoir du délais. Il ne s’agit pas d’acheter toute la BOM. Ce n’est pas possible car la conception ne fait que commencer.

2. JUSTIFICATION
3. SCHÉMA
4. ROUTAGE
5. FABRICATION DU PROTOTYPE
6. VÉRIFICATION
7. QUALIFICATION
8. VALIDATION
9. FABRICATION EN SÉRIE

------------------------------------------------------------------------

## Concevoir la partie Mécanique

### Croquis de Design

### Plan 3D

### Exportation plan de pré‑implantation

### Fabrication

### Test de Mise au Point

------------------------------------------------------------------------

## Concevoir la partie Programmation

### Spécification

### Codage

### Instruction de téléchargement et Configuration


