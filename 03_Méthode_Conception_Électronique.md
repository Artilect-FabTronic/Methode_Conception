> Date de Création : 23 septembre 2020<br>
> Auteur initiale : Lilian Tribouilloy<br>
> Licence : Creative Commonces BY NC SA<br>

# Méthodologie de Conception d’un Objet Électronique

## Introduction

Ce document a pour but de proposer une méthodologie de conception d’un objet électronique à destination du hobbyste de l’électronique qui a peur de franchir le pas. Peur de se lancer dans la conception d’un objet originale qu’il aurait conçu de A à Z.

Il s’agit bien d’__une__ méthode et non pas de __la__ méthode. En disant cela je ne présume nullement détenir la vérité absolue sur le sujet. D’autant que je trouve dangereux d’imposer, et de façon définitive, une méthode prétendument indépassable. J’encourage tout le monde à rester critique et mieux que cela à se construire ces propres méthodes de travail. Celles qui vous conviennent parce qu’elles correspondent à votre façon de penser ou tout simplement à l’investissement en temps que vous souhaitez y consacrer. Travailler c’est « trouvailler » dit l’adage. Dès lors qu’on se laisse dicter les méthodes, on perd son métier. On perd l’opportunité de rentrer par soi‑même dans le chemin qui nous construit à force d’expériences.

Cet avertissement important étant entendu. Il faut toutefois admettre que le savoir est une valeur collective. Et qu’il est bon d’apprendre de ses paires pour ne pas se perdre trop longuement dans une science ou un art difficile. Les chemins déjà tracés doivent vous enseigner, vous inspirer, vous faire gagner du temps. Pas vous contraindre.

Ce document n’a pas vocation à vous apprendre les bases théoriques de l’électronique, ni à vous informer sur les avantages de telle ou telle technologie. Il propose simplement une méthode pas à pas pour transformer vos idées en réalisation concrète. Ce document n’a pas non plus pour prétention d’atteindre un niveau de rigueur industriel bien trop chronophage pour un hobbyste. Il liste les actions importantes à faire pour ne pas commettre d’erreurs onéreuses qui ruinerait votre projet. Toutefois, ce document sera parsemé de comparaison entre ce qui se pratique dans l’industrie et ce qui me semble plus raisonnable de mettre en œuvre pour un amateur. À vous de placer le curseur entre rigueur et plaisir et entre idéalisme et réalisme.

Ce document est à destination du public des _fablabs_, du _mouvement Maker_ et du _mouvement du Logiciel et matériel Libre_. Aussi les outils proposés en complément de la méthodologie sont tous des logiciels libres. À savoir : [KiCAD](https://kicad-pcb.org/) pour l’édition de schéma et le routage des cartes ; [FreeCAD](https://www.freecadweb.org/) pour la conception de la mécanique associée (simple boîtier ou robot sophistiqué selon votre projet). Ce sont aujourd’hui les logiciels libres les plus avancés dans ces domaines mais on pourra d’aventure trouver des alternatives. Le choix de l’éditeur de code est laissé à votre sagacité tant la diversité dans ce domaine est grande.

À n’en pas douter il existe des logiciels propriétaires bien plus puissants que ceux que je propose ici. Mais la liberté n’est pas une question de performance. La liberté est d’ailleurs une performance en soit par les temps qui court. C’est une question d’écosystème, une question de partage avec votre communauté. Comme le dit si bien Richard Stallman (fondateur de la Free Software Fondation, cocréateur de GNU/Linux, entre autres choses), et il le dit en français dans le texte : _«Je peux résumer ce qu’est le logiciel libre en 3 mots : liberté, égalité, fraternité.»_

Le défit du matériel libre.


------------------------------------------------------------------------

## C’est quoi au fait la conception ?

### Concevoir, un état d’esprit

On m’a une fois poser la question, au regard de mes créations, si j’étais un designer. Voici la réponse que j’ai apporté :


> _Suis‑je designer ? Si je me conforme à la définition française, oui. Le truc, c’est que je n’aime pas beaucoup cette définition. Je trouve que ça fait trop formule magique. Dès que je vois un mot anglais, j’ai mon détecteur de langue de bois qui clignote. Je m’explique._
>
> _Le mot designer est un mot d’emprunt de l’anglais qui veut dire concepteur. Comme tu le sais sans doute. Mais les français ont modifié le sens de ce mot pour y ajouter quelque chose de différent. Quelque chose que les anglo‑saxons, me semble‑t‑il, ne mettent pas du tout._
>
> _Conception vient du latin «conceptus» qui signifie «action d’accueillir et de contenir». Et C’est exactement le même mot en latin pour traduire la période de gestation des femmes. N’est ce pas ce qu’elles font pendant cette période pour parler basiquement ? Elles accueillent la «graine» et elles le contiennent jusqu’à ressortir l’enfant. Du reste, aujourd’hui encore dans la langue française, on dit concevoir un enfant. Et même dans la bible, on parle d’immaculé conception._
>
> _Et bien concevoir en technologie, c’est exactement ça mais avec des idées. (Que saurait‑il faire d’autre un homme…?) On accueille une idée. Parfois c’est sa propre idée, parfois c’est celle des autres. (Trop souvent dans l’industrie, c’est celle des autres…) Puis on la mette en gestion un certain temps et selon un processus créatif plus ou moins complexe. Jusqu’à obtenir une chose tangible, quelque chose de réelle._
>
> _Alors, oui, c’est exactement ce que je fais. Et définitivement, je suis un concepteur. Et si on le dit en anglais: I am a designer. Au sens strict._
>
> _Mais c’est un peu court pour décrire l’activité dans son détail. La question est : Je conçois quoi ? Et je mets en œuvre quelle discipline ? Le quoi et le comment est, selon moi, la seule façon de ne pas se tromper dans la description de son métier._
>
> _Alors, posons les choses simplement. Je fais des claviers pour l’informatique. Facile, ça tout le monde aura compris. Et je déploie les disciplines suivantes : électronique, mécanique, programmation, menuiserie, de l’ergonomie. Et quoi d’autre ? Quelle est donc cette substance subtile qui tend à identifier une esthétique. Et peut‑être pour certain une émotion ?_
>
> _Je ne vois pas ce que cela pourrait être d’autre que de l’art. Ou peut‑être de l’artisanat à la limite. Il me semble que c’est bien cela qui est ajouté en plus dans le mot designer à la française. Et à l’italienne aussi d’ailleurs._
>
> _La distinction entre art et artisanat est relativement tardive. Elle date de la Renaissance. Cette distinction est apparue en Italie au moment précis où un petit groupe de gens est devenu très très riches. L’époque des grands explorateur, Marco Polo… Et la naissance des banques modernes. Et où ils ne savaient plus comment afficher, affirmer, leur distinction sociale. Alors ils ont demandé à avoir des choses, même inutiles, que personne d’autre pouvait se payer. L’art est né de cet acte d’orgueil._
>
> _La différence entre art et artisanat est très culturelle. Et il existe encore des cultures humaines où on ne fait pas la distinction._
>
> _Et c’est pour cela, que je tiens à préciser que dans ce que je fais il y a un peu d’art, de l’art utile. Et c’est là un jugement morale et une philosophie que j’assume._


Aussi, il subsiste dans l’acte de création quelque chose de mystérieux. Quelque chose qui dépose la simple raison. Aussi m’est‑il impossible de vous apprendre comment trouver l’idée d’un objet. Je ne peux que vous conseiller de bien prendre le temps de mûrir l’idée en vous et de passer le plus rapidement possible à l’expérimentation. D’écouter ce que les gens vous disent, tout en se méfiant de ce que les gens vous disent. L’intuition peut dépasser les préjugés.

Une idée n’est rien, seule compte sa réalisation tangible. Le signe quasi certain qu’une idée est bonne, est qu’elle ne vous lâche pas, qu’elle vous hante continuellement. Mais le signe absolument certain qu’une idée est bonne, est qu’elle fonctionne réellement et que les gens l’utilisent.


### Concevoir un produit complet moderne, c’est mélanger plusieurs disciplines

Un objet électronique complet moderne est toujours constituer d’au moins 3 disciplines : Électronique, Mécanique (au sens large) et Programmation.

Mais il arrive qu’il en compte bien d’avantage comme la chimie, la biologie, la menuiserie, la couture, l’architecture, l’art et que sais‑je encore. Il ne sera donc pas possible d’exposer toutes les techniques ou arts qu’il est possible de mettre en œuvre dans un objet électronique. Pour autant que l’électronique soit réellement au centre de l’objet ou qu’il serait qu’une fonctionnalité discrète.

Nous nous concentrerons ici donc que sur les trois premières disciplines citées.

Doit‑on commencer le travail par l’électronique, la mécanique ou le logiciel ? Tout dépend de la nature du projet. Et du degré d’interaction entre les 3.

Si la mécanique n’est qu’un simple boîtier. Alors l’interaction entre électronique et mécanique sera faible. Il y a dans ce cas assez peu de sujets à aborder : Dimension et encombrement général ; Condition environnementale (température, vibration, étanchéité…) ; Dissipation thermique ; Isolation électrique et sécurité des personnes ; Connectique ; assemblage de la carte et du boîtier. On pourra donc se contrer sur l’électronique en premier. Ce qu’il ne signifie pas que l’on ne peut pas se poser les questions précédentes au fil de l’eau.

Évidement si la mécanique est en faite un objet articulé complexe comme un robot par exemple. L’interaction entre électronique et mécanique sera forte. Et il sera bon de pousser les deux disciplines simultanément ou alternativement. Faire beaucoup d’itération entre les deux permet de limiter les erreurs.

L’interaction entre électronique et logiciel est presque toujours forte sur un objet moderne. Mais tout dépend de la complexité de l’objet. Là aussi, faire beaucoup d’itération entre les deux (ou finalement les trois) permet de limiter les erreurs. Dans l’industrie, on va jusqu’à faire des spécifications d’interface entre le Hardware (électronique) et le software (programmation) pour lever toutes les ambiguïtés. Et il peut y avoir des spécifications d’architecture pour coordonner les efforts des 3 métiers (quand il y en a seulement que 3). Aussi, si vous n’êtes pas tout seul sur le projet, ce qui n’arrive quasiment jamais dans l’industrie contrairement en mode hobby, une bonne communication entre les différents métiers et absolument essentielle à la réussite du projet.

Quoi qu’il en soit vous ne pourrez pas faire l’économie de vous investir sérieusement dans les 3 (ou plus encore) disciplines. Et il sera bon de chercher de l’aide dès qu’un blocage se présente. Être concepteur, c’est passé sa vie à apprendre des choses, d’autant que les technologies ne cessent d’évoluer. Il est donc urgent d’apprendre à apprendre.

Les fablabs, les makerspaces ou les hackerspaces ou peut importe comment on les appelle, trouvent là tout leurs intérêts…


### Doit‑on Concevoir Seul ou à Plusieurs ?

{Brouillon}
À vous de voir. Il faut faire selon les envies.
Il faut pas que ce soit une contrainte invivable.

C’est plus difficile, car ça demande forcément plus d’organisation.
Attention à bien se répartir les taches pour éviter la zizanie.
Attention il existe une dimension maximum à partir de laquelle ça ne fonctionne plus.
{/Brouillon}


------------------------------------------------------------------

## D’abord un peu d’Organisation

### Un travail de long haleine

Concevoir une carte électronique peut‑être un long travaille. Surtout si on veut le faire bien et le documenter correctement pour le partager. C’est pourquoi il est important de bien s’organiser et d’être honnête avec soi‑même sur notre capacité de travail.

Une mauvaise organisation est une des première cause d’échec d’un projet. Il est d’autant plus difficile de s’organiser que l’on travaille à plusieurs. C’est pourquoi même dans l’industrie les équipes de développement, pour un projet donnée, sont relativement petites, rarement plus de 12. C’était d’ailleurs le chiffre que refuser de dépasser Steve Jobs. Même pour un produit aussi complexe que l’iPhone !

Quand on travaille à plusieurs il est très important de bien définir le rôle de chacun. Être à deux sur le même stylo est la première cause d’engueulade dans un groupe et la première cause de l’échec du projet.

Dans l’industrie, il existe de nombreux outils pour manager un projet: Mantis, Jira, ERP, Kanban, Management des exigences, Doors, ReqTify, planning, diagramme de Gantt, Réunions, Reporting, Revu de conception, Revu des coût, Cycle de développement en V, processus qualité… Trop de rigueur tue le désir, faire un projet en mode hobbyste doit rester un plaisir.

Pour un projet hobbyste, je recommanderai la plus grande simplicité possible. Une simple liste d’actions peut parfois suffire. À vous de définir vos outils de communication. Mais un dossier de partage, ou mieux une gestion de type GIT est souvent indispensable. Faite vous votre opinion rapidement sur les outils et imposait les en commun accord.


### Proposition d’un Dossier d’Étude

Avoir un dossier projet bien rangé pour pourrait sembler être futile ou pourrait nous faire passer pour des maniaques. Mais en fait, bien ranger le dossier, c’est aussi organiser sa méthode de travail, structurer les taches à faire, une liste de tâche sans date qui ne dit pas son nom.

Combien de fois, je suis tombé sur des projets sur GitHub ou GitLab, sans comprendre comment fonctionne leur source. Quoi est où ? etc… Bien structurer le dossier D’étude, c’est aussi permettre à d’autre personne de devenir des contributeur du projet plus facilement.

C’est pourquoi, il m’est parût pertinent de proposer une manière de ranger un projet. Je pense qu’une bonne façon de ci‑prendre et de s’organiser par métier, puis par type d’actions fondamentales dans le deuxième niveau hiérarchique.

Dans le dossier «Template_Dossier_Projet», je propose non pas un dossier template, deux dossiers templates (format 7zip). Le premier appelé «version débutant» et le second appelé «version rigueur». Pourquoi ? Car je pense, comme je l’ai précisé en introduction, qu’une méthode de travail, c’est quelque chose qui se construit dans le temps. Que ça sert à rien d’imposer d’emblée trop de complexité. Ces deux versions sont comme les deux points d’une trajectoire. Ainsi un débutant pourra commencer tranquillement par la version débutant ; puis au fur et à mesure que les choses apparaissent, il pourra aller chercher dans la version rigueur les éléments dont il a besoin. On comprend mieux les choses par l’expérimentation que par un cours magistral abstrait.

Dans la version rigueur, vous trouverez aussi des fichiers templates pour différente chose, comme par exemple une base de donné pour les composants, ou un fichier pour faire une BOM (Bill of Material = nomenclature composant). Et plein d’autres choses utiles.

Les deux versions ont les dossier suivant en tête, voici à quoi ils servent :

* __00_Management__ : Ce dossier n’a pas nécessairement vocation à être partagé au grand publique. Il sert surtout à l’équipe de développement pour s’organiser.
* __01_Système__ : Les éléments qui sont transverses à plusieurs métiers. Et en particulier, la spécification du produit et l’architecture du produit.
* __03_Mécanique__ : Dossier d’étude pour le métier mécanique.
* __02_Électronique__ : Dossier d’étude pour le métier électronique.
* __04_Programmation__ : Dossier d’étude pour le métier programmation.
* On pourra intercaler d’autres disciplines le cas échéant.
* __XX_Fabrication__ : Ce dossier est destiné à celui qui veut simplement fabriquer le produit sans se préoccuper de l’étude. Il est un peu l’équivalent de l’onglet «Téléchargement» pour un logiciel libre.

On trouve ensuite dans chaque dossier, d’autres dossiers qui correspondent aux étapes fondamentales de conception. Vous trouverai un petit «readme.md» pour comprendre à quoi sert ce dossier. Lire ensuite les paragraphes «Conception» qui suivent pour comprendre comment tout ça s’articule.


### Cycle de  Développement en V et Critique du Processus Industriel

Dans ce paragraphe, je détaille les grandes lignes du processus industriel pour mieux mettre en lumière ce qui applicable ou pas pour un hobbyste. Et ainsi expliquer qu’il est possible de faire les choses plus simplement.


#### Description du Cycle de Développement en V Industriel

Dans l’industrie, le mot conception est substitué aux mots «processus de développement». Et des théories émanant des qualiticiens donne le jour à une choses que l’on appelle cycle de développement en V (ou en W). 

![image sur le cycle en V industriel](images/cycle_en_V_industriel.png)


0. __ÉTUDE DE MARCHÉ :__ Il s’agit de l’étape commerciale en amont qui doit définir le besoin client et l’adéquation avec une solution que l’on appelle produit (ou service dans certain cas). Je ne parlerai pas dans ce document de ce qu’il faudrait faire à cette étape.
	
	
1.  __SPÉCIFICATION :__ Fixer sur le «papier», la définition du produit. Dans l’industrie, on découpe toutes les caractéristiques en petits éléments, qu’on appelle «exigence». Ainsi, on parle de management des exigences quand on mette en œuvre des actions pour s’assurer que toutes les exigences sont tenues une par une. Ces exigences sont numéroté pour être tracé dans une base de données. En particulier, le cahier des charges en amont est décliné en des spécifications métiers, puis des documents de justification théorique puis des documentation de vérification expérimentales. On parle alors d’une architecture documentaire. Dans cette architecture tous les éléments sont numérotés pour créer des liens entre spécification produit, les spécifications métiers puis les différent type de justification. On parle de «couverture des exigences».
	
	
2. __JUSTIFICATION :__ Le cœur de l’étude, mettre en confrontation ce qu’on a imaginé et ce qui est réellement possible selon les technologies disponibles. Il s’agit aussi, dans un document que l’on appelle parfois «dossier justificatif de définition», de clarifier, d’expliciter tout ce qui est de l’ordre l’implicite et d’écrire tout ce qui est rester dans le domaine de tacite. Il faut remettre en cause les incohérences de la spécification pour aboutir à une spécification plus précise. Il s’agit aussi et surtout de définir la solution technique et expliquer le choix technique d’une part. Et d’autre part, il s’agit de prouver théoriquement que la solution fonctionne et répond parfaitement à l’exigence.
	
	
3. __SCHÉMA :__ Dessiner concrètement le résultat de l’étude. C’est là qu’on fixe la solution technique avec la plus grande précision. Quel composant est connecté où et comment ? Et on donne la liste des composants nécessaires. On appelle cette liste une BOM ou une nomenclature.
	
	
4. __ROUTAGE :__ Dessiner le circuit imprimé et prendre en compte les contraintes liées au processus de fabrication d’un PCB. Le schéma qui est encore une certaine abstraction des choses et alors réalisé physiquement.
	
	
5. __FABRICATION DU PROTOTYPE :__ Prototype destiné au développement. Ce prototype peu tout de même être fabriquer industriellement ou pas selon le degré d’avancement. On parle d’industrialisation progressive ou processus d’industrialisation.
	
	
6. __VÉRIFICATION :__ Mise au point de tous les blocs fonctionnelles unitairement. C’est le moment de vérité pour le concepteur. On vérifie point par point que tout fonctionne comme attendu et selon toutes les conditions, conditions climatiques notamment. Il est quasiment impossible de faire tout bon du premier coup. Aussi les erreurs (problème, bug ou défaut) sont tracés dans un outil de suivi (par exemple, Mantis Bug Tracker ou Jira). Le traitement des défauts pourra se faire selon une méthodologie 8D dont on parlera plus loin. On aura consécutivement à la résolution des problèmes, une liste de solution à appliquer qui donneront lieu à un nouveau prototype. Et on recommencera le processus.
	
	
7. __VALIDATION :__ Validation fonctionnel de l’ensemble et validation de la cohérence documentaire. Vérification de la couverture des exigences. Même chose qu’à l’étape de Vérification, mais au niveau global produit. On pourra parler aussi de validation au niveau système qu’en le produit s’insère dans un ensemble plus grand. On parle de tests d’intégration système.
	
	
8. __QUALIFICATION :__ Respect des Normes, standards et Réglementations. Dans l’industrie, c’est souvent une équipe à part entière qui s’occupe de cette étape. Les normes forment un véritable labyrinthe documentaire à décliner selon tous les pays dans lesquels on souhaite vendre le produit. Cette étape donne lieu à des tests spécifiques qui visent à vérifier par exemple : la CEM (compatibilité électromagnétique), la tenue au ESD (décharge électrostatique), la tenue aux flammes, la robustesse dans les conditions climatique, vibratoire ou choc mécanique, le respect des standards de radiocommunication…
	
	
9. → _Puis on réitère entre 1 et 8, jusqu’à ce que tout soit OK._ ↺
	
	
10. __FABRICATION EN SÉRIE :__ La conception est terminée. Il s’agit maintenir de fabriquer efficacement le produit en masse. L’action en amont de l’industrialisation doit permettre de bien faire le passage de relais entre le monde de la conception et le monde de la fabrication.

Ce workflow (flux de travail) est écrit ici du point de vu de l’électronicien. Du point de vu du mécanicien et du codeur, les choses se déclinent différemment aux étapes 3, 4, 6 et 7.


#### Critique et ce qui se Pratique en Condition Réelle

Bien tout cela semblent parfaitement logique. Et il l’ai dans les grandes lignes. Il introduit pourtant une idée fausse qui est que tout se déroulerait linéairement dans le temps. Je connais aucun concepteur sérieux qui travaille exactement dans l’ordre des actions décrites précédemment. Je m’explique.

![image sur ce qui correspond mieux à la façon réelle de penser]()

L’image ci‑dessus décrit un cycle en V tel que typiquement réalisé dans la vie réelle pour un concepteur électronique. On commence bien
par une spécification, mais très rapidement vient se positionner en parallèle l’action de justification, puis peu de temps après se positionne l’action d’écriture du schéma. Et il est fortement recommandé de faire beaucoup d’itérations entre ces 3 éléments (Spéc / Justif / Schéma) pour converger efficacement vers une solution. Plus on prend le temps de bien se poser tous les questions pour ces 3 éléments, et moins on aura d’erreurs au moment des vérifications, validations et qualifications. Et il faut garder en tête que ces erreurs peuvent vous coûtez chers. Pas seulement en argent, mais aussi en temps. Par exemple, si on se rend compte que l’architecture du produit ne permet pas le répondre au besoin, c’est la catastrophe. Il faut tout recommencer. Et ça peux être 6 mois ou 1 an de perdue.

Il y a ensuite un biseau entre schéma et routage. Dans l’industrie, le routage est souvent réalisé par une équipe spécialisé. Il faut alors réaliser une spécification de routage en bonne intelligence entre les deux équipes. Il n’est pas complètement impossible de trouver des erreurs sur le schéma à cette étape. Et on peut aussi laisser des degrés de liberté au routeur pour facilité le routage. Par exemple, inversion de pin sur des fonctions équivalentes.

Mais sur des fonctions complexes le biseau schéma / routage peut aller plus loin. En effet, pour concevoir une fonction RF (radiofréquence), il faut carrément réaliser parallèlement, simulation (donc justification), schéma et routage. Car dans le domaine radio, un bout de piste devient équivalent à un composant à part entière, avec par exemple une impédance ou un couplage particulier.


#### Adaptation pour un Hobbyste

Alors comment faire pour un hobbyste ? Ayez confiance en vous. Ne vous lassez pas impressionné par toutes ces étapes. Gardez votre bon sens à chaque instant. Éliminez toutes les actions qui n’ont de sens que dans un cadre professionnel rigoureux. Soyez au clair avec vos ambitions. Ne vous laissez pas embarquer dans un planning trop précis. Les plannings sont des tue‑l’‑amour. Du reste, ils ne marchent jamais (même dans le cadre professionnel !). Laissez‑vous guider par vos envies. Concevoir doit rester un plaisir.

En revanche, et c’est là toute la difficulté, il faut sélectionner les actions essentielles qui vous permettrons d’arriver à bon port. Je vous propose dans les chapitres suivants les actions qui me semble les plus importantes. Mais comme je le disait en introduction, il vous faut faire des choix en fonction de votre niveau et de vos ambitions. La méthode que je propose ici est (je l’espère) conçu pour que vous ajustiez par vous même votre méthode de travail progressivement à mesure des expériences. Mais soyez bien conscient que personne ne peut placer le curseur entre rigueur et réalisme à votre place. Vous devez rester maître de votre propre méthode de travail.

Ne vous mettez pas la pression. Après tout, ne pas arriver tout à fait au bout n’est peut être pas si grave, si votre but et simplement d’apprendre. Et à n’en pas douter, vous ferez mieux la prochaine fois.


------------------------------------------------------------------------

## Du Bon Usage du Prototype

### Pour en finir avec les Acronymes

POC, MVP, modèle A, modèle B, C‑model, Ramp‑up model, prototypage (rapide ou pas)…


### Critique de la définition de l’OMC

L’OMC (Organisation Mondial du Commerce) a donné une définition de ce qu’est un prototype à des fins de promouvoir l’innovation. (Non mais de quoi je me mêle, Est ce que je me permet de leur expliquer ce que c’est une loi…). La voici :

> « Un prototype est un modèle original qui possède toutes les qualités techniques et toutes les caractéristiques de fonctionnement du nouveau produit. » (…) (OCDE, 1993, alinéa 115, p. 46).

Voyez vous le problème ? Ils sont en train de dire que le prototype a déjà toutes les qualités d’un produit fini. Ils veulent la charrue avant les bœufs. Hors un prototype ce n’est précisément pas cela.


### Étymologie du mot Prototype



### Les Prototypes, Simplement des Étapes dans la Conception


------------------------------------------------------------------------

## Concevoir la partie Électronique

### Vue Global sur un Flux de Travail Simplifié

0. IDÉE
1. SPÉCIFICATION / JUSTIFICATION (On abandonne l’idée qu’on peut séparer les deux pour simplifier la documentation.)
2. SCHÉMA
3. ROUTAGE
4. FABRICATION DU PROTOTYPE
5. MISE AU POINT
→ _Réitération des étapes 1 à 5 jusqu’à ce que tout soit OK._ ↺
6. DOCUMENTATION POUR LA COMMUNAUTÉ

{Commentaire} 


### Une Liste de Questions à se Poser

La liste suivante regroupe des actions essentielles, mais elles ne sont ni exhaustives, ni limitatives. À vous de vous faire votre propre opinion. Au cours de la conception, il y aura sûrement des sous‑tâches, qu’on ne peut pas prévoir à l’avance, qui vont apparaître.

0. __IDÉE__
	La créativité est une chose mystérieuse. Personne ne peut prétendre donner une méthode générale pour trouver des idées. Il faudra creuser au bout de vous même et vous faire confiance. Laissez‑vous guider par vos envies.

> Les points 1, 2 et 3 peuvent (devraient) être faite en parallèle par un processus itératif.

1. __SPÉCIFICATION / JUSTIFICATION__
	* Le but d’une spécification est de poser le besoin, idée, envie. Faites‑vous au moins pour vous même un petit texte pour expliquer ce que vous voulez faire. Faire des petits dessins. Faire une liste des caractéristiques essentielles.
	
	* Essayer d’identifier clairement quel est le problème et comment on cherche à le résoudre. (Le couple problème / solution.)
	
	* Faire un synoptique (schéma de principe sans les alimentations). Ce qui va permettre de clarifier l’architecture de l’objet. Il doit faire apparaître des détailles, des fonctions nécessaire auxquelles vous n’aviez pas pensé au début. Refaire le synoptique jusqu’à ce qu’il semble complet.
	
	* Faire la liste de tous les sous‑blocs fonctionnels. Cette liste pourra servir à toutes les étapes de la conception. Une sorte de check‑list pour chaque question : alimentation, référence composant, justification, routage… On peut également identifier s’il y a des parties optionnelles au projet. Il faut peut être pouvoir imaginer des extensions futures.
	
	* Vous pouvez éventuellement classer les sous‑blocs fonctionnels par catégorie : alimentations, cœur numérique, entrées, sorties, interfaces homme / machine, capteurs, communications filaires, radiocommunications… Cela permet de mieux planifier le travail ou de partager le travail dans une équipe.
	
	* Pour les fonctions principales fixer les choix de composants. Si ce n’est pas claire, ne pas hésiter à faire de petite maquette pour éprouver la pertinence de la solution. Par exemple, est‑ce que accéléromètre sera assez précis ?
	
	* Le micro‑contrôleur est un composant qui ne sera pas interchangeable, il faut être certain qu’il pourra prendre en compte toutes les fonctions. Pour cela faire la liste de tous les signaux à brancher et mettre en face les options d’affectations du micro‑contrôleur.
	
	* Quand les choix des composants principaux sont arrêtés. Acheter ces composants car il risque d’y avoir du délais. Il ne s’agit pas d’acheter toute la BOM. Ce n’est pas possible car la conception ne fait que commencer.
	
	* Faire un bilan de consommation. Les tensions nécessaires. Les courants pour chaque fonction. Quelle est notre source d’énergie et comment la gérer ? Est‑ce qu’il y a des priorités nécessaires pour la séquence d’allumage (souvent nécessaire pour le CPU) ? Est‑ce qu’on a besoin d’une alimentation permanente pour les fonctions en mode veille ?
	
	* Quelles sont les contraintes environnementales (température, étanchéité, vibration) ?
	
	* Si on veut vendre le produit, il est absolument nécessaire de se demander quels sont les normes CEM (Compatibilité ÉlectroMagnétique) à respecter. L’amateur pourra se passer de cette étape.
	
	* Avons nous une contrainte sur la durée de vie. Si oui calcul de fiabilité et AMDEC nécessaire. Étape nécessaire dans les milieux professionnelles. C’est nécessaire aussi si vous êtes sensible à la lutte contre obsolescence programmée. Cette étape n’est pas nécessaire sur les premiers prototypes.
	
	* Y‑a‑t‑il une contrainte de sécurité pour les personnes ? Analyse Safety nécessaire et AMDEC. Quelles sont les fonctions de sécurité à ajouter ou à mettre en redondance ? Étape nécessaire dans les milieux professionnelles. Mais faites tout de même attention à vous et les autres si vous êtes amateur. L’électricité, c’est dangereux, on ne le répète jamais assez.
	
	* Typiquement, ce qui est dangereux : les batteries (risque d’incendie en cas de court‑circuit), les tensions supérieures à 50Vac ou 120Vdc (limite entre la Très Basse Tension et la Basse Tension selon la norme) (risque d’électrocution), les éléments chauffants (risque de brûlure ou d’incendie), les moteurs ou les vérins (risque de mutilation), les produits chimiques nécessaires à la fabrication (risque d’intoxication)…
	
	* Faire une liste des risques projets. Quels sont les inconnus à lever plus tard ?
	
	* Ensuite, il faut développer la solution en levant les ambiguïtés de la spécification. Il faut démêler l’implicite de l’explicite. Et il faut écrire ce qui est tacite.
	
	* Justifier la pertinence de la spécification. Est‑ce qu’on répond de façon cohérente et efficacement au besoin ? (Dans les milieux professionnel on va jusqu’à faire une étude marché ou à soumettre un prototype à un client potentiel.)
	
	* Justifier les choix technologiques
	
	* Vérifier que le coût du produit est raisonnable. (En adéquation avec le business plan pour les professionnels.)
	
	* Justifier théoriquement que cela fonctionne. Par calcul, simulation, ou en mettant en lumière certain point de la documentation technique.
	
	* Si des inconnus subsistent, il peut être pertinent de faire une maquette et des tests pour un sous‑ensemble du produit.
	
	* Cette étude doit aboutir à une spécification plus précise.
	
	
2. __SCHÉMA__
	* Vérifier que l’architecture et les blocs fonctionnels sont OK.
	
	* Faire le cartouche la page et choisir la taille des pages en fonction de la quantité de composant à mettre par page.
	
	* Organiser vos pages pour faciliter la lecture et la maintenance du dossier. Faire toujours une première page de garde pour la gestion des variantes et des évolutions.
	
	* Ensuite il faut organiser le schéma par catégorie de fonction et en fonction de la complexité. En page 2, il est conseiller de mettre les connecteurs qui vont vers le monde extérieur ainsi que les blocs hiérarchiques. Dans les pages suivantes, on a le contenu de ces blocs. Il est préférable de faire une page au moins par catégories de fonctions. 
	
	* Dessiner le schéma.
	
	* Desiner le symbole (schematic part) des composants manquants
	
	* Numéroter les composants (Référence topologique).
	
	* Lancer l’algorithme de vérification DRC (Design Rule Check).
	
	* Créer une basse de données de vos composants.
	
	* Définissez les variantes ou options.
	
	* Associer à chaque composant une empreinte physique.
	
	* Penser à la testabilité ou debeug de la carte.
	
	* Générer la nomenclature des composants.
	
	* Vérifier le prix de la carte.
	
	* Faire l’analyse critique de schéma.
	
	* Corriger les erreurs.
	
	* Générer le fichier .net pour pouvoir commencer le routage.
	
	
3. __Routage__
	* Faire le plan d’interface Méca / PCB pour préciser la dimension et la géométrie de la carte, pour définir la position des vis, des connecteurs, des IHM et des radiateurs ou autres éléments dont il est nécessaire de fixer la position.
	
	* Avec FreeCAD, on peut générer un fichier svg que l’on peut transformer en fichier dxf avec Inkscape. Ce fichier dxf est le format que peut comprendre KiCAD.
	
	* Définir les hauteurs maximum selon la mécanique. Plusieurs zones peuvent être définies.
	
	* Il faut choisir le processus de fabrication. Lequel avait vous accès selon vos moyens. Est‑ce qu’on fait les soudures à la main ? Est‑ce qu’on fait le PCB avec une gravure chimique artisanal, une CNC ou on passe par un fabricant de PCB professionnel, etc ?
	
	* Cela va fixer la taille des pads de soudure et la précision de gravure et éventuellement le nombre de couche de cuivre auquel on a le doit. Et donc on peut alors écrire une spécification de PCB.
	
	* Définir l’empilage (Stack‑up) du PCB. Le nombre de couche choisi est un compromis entre le prix, la complexité ou densité d’interconnexion et la CEM. L’utilisation des couches doit être défini : plan de masse, plan d’alimentation, les couches signaux…
	
	* En cas de soudure en refusion, il faut lister les composants lourds et décider sur quelles faces ont les mets ou s’il faut les coller avant soudure ou si on les soudent à la main.
	
	* Dessiner les empreintes manquantes pour certain composants.
	
	* Définir dans KiCAD, la liste des piste et des vias.
	
	* Définir le cartouche et la taille des pages.
	
	* Importer le fichier méca au format dxf.
	
	* Fixer les repères pour faire la correspondance entre plan mécanique et le routage.
	
	* Importer le fichier net pour faire le lien avec le schéma électronique.
	
	* Faire le placement des composants, sans les pistes, pour appliquer les différentes contraintes. Et vérifier que tout rentre bien dans le volume définie (penser la surface _et_ à la hauteur).
	
	* Vérifier qu’il n’y a pas de collisions avec la mécanique.
	
	* Dessiner le contour de la carte avec une ceinture de masse pour la CEM.
	
	* Faire le routage à proprement dit. Dessiner les pistes et les vias.
	
	* Éventuellement, modifier le schéma si on trouve des simplification de routage (ou si on voit des erreurs).
	
	* Dessiner les plans de masse et d’alimentation.
	
	* Faire le remplissage de masse entre les pistes.
	
	* Lancer le DRC (Design Rule Check) pour vérifier le respect des règles IPC.
	
	* Corriger les infaisabilités, erreurs ou autres problème de fabrication.
	
	* Ajouter les éléments industriels, n°, mire, espace pour étiquette, méthode de détachement (timbre poste, V‑scoring ou usinage)…
	
	* Analyse critique de routage par les paires. Attention à la CEM.
	
	* Faire un 3D du PCB avec composant et le mettre dans le 3D mécanique pour vérifier qu’il n’y a pas de collisions.
	
	* Correction des problèmes.
	
	* Faire la mise en flanc. Combien on fabrique de carte à la fois ? Quel est le sens de convoyage pour la soudure en refusion ou à la vague.
	
	* Générer les fichiers de fabrication : .pos, .drl, .rpt, gerbers
	
	* Vérifier les gerbers avec le visualiseur KiCAD.
	
	* Générer les plans et la spécification PCB (selon le fournisseur).
	
	
4. __Fabrication__
	* Achat des composants (Attention délais)
	
	* Vérifier qu’on n’a pas de composant manquant.
	
	* Récupérer le PCB et vérifier qu’il est conforme à vos attentes (ouverture de vernis, inversion de couches…).
	
	* Éventuellement pour la refusion, vérifier le masque de pâte à braser.
	
	* Pour les pro, vérifier les continuités des pistes avec un testeur type Takaya.
	
	* Brasure des composants.
	
	* Vérifier que tout est correctement soudé.
	
	* Pour les pro, vérifier les caractéristique des composant avec un testeur type Takaya.
	
	* Séparer les différentes cartes du flanc.
	
	
5. __Vérification unitaire et mise au point__
	* Fabriquer les outils de validation ou de débeug.
	
	* Vérifier les alimentations. Attention à la fumée et les surchauffe.
	
	* Vérifier qu’on arrive à télécharger le logiciel.
	
	* Vérification rapide des fonctions pour avoir un aperçu du bon fonctionnement global.
	
	* Puis vérification détaillé de tous les blocs fonctionnels.
	
	* Vérification de la bonne tenue des performances.
	
	* Vérification de la tenue en température min et max de toutes les fonctions. (Il faut avoir une étuve…)
	
	
> _Les actions qui suivent n’ont de sens que dans un cadre professionnel._
> _Donc à vous de voir si vous voulez allez plus loin._
> _Sinon aller directement à l’étape 7 bis._
	
	
6. __QUALIFICATION__
	* Pour le pro, pour une mise sur le marché, conformité aux standards, aux normes et à la réglementation.
	
	* Tests aux perturbations conduites
	
	* Tests CEM
	
	* Tests ESD
	
	* Tests environnementaux du produit global
	
	* Vérification de la tenue aux vibrations ou chocs mécaniques.
	
	* Tests de vieillissement
	
	* Tests de vérification à la sécurité électrique
	
	* Tests de tenu aux flammes
	
	
7. __VALIDATION__
	* Pour les pro, validation que tous les exigences sont tenues point par point pour être sûr qu’on a rien oublier (management des exigences).
	
	* Vérifier que toute la documentation est complète en cohérente.
	
> Remarques : Il faut réitérer entre 1 et 7 jusqu’à ce tous soit jugés satisfaisants.
	
	
8. __FABRICATION EN SÉRIE__
	* Industrialisation, vérifier que le produit peut être produit industriellement.
	
	* Mettre en place les outils de fabrication industriel.
	
	* Mettre en place les outils de vérification du bon fonctionnement semi‑automatique ou automatique.
	
	* Écrire le document de méthode du fabrication.
	
	* Faire lancement de la première série pour vérifier que tout se passe bien.
	
	* Corriger les problèmes.
	
	* Produire en série.
	
	* Emballage du produit.
	
	* Livraison et logistique jusqu’au point de vente.	


> _Cette dernière étape est importante surtout si on s’inscrit dans une démarche de conception d’objet libre. Le but est de faire l’équivalent de l’onglet «Téléchargement» pour un logiciel libre._
> _Plus d’information sur cette démarche dans le fichier «04_Démarche_Matériel_Libre.md»_ 	


6. BIS. __DOCUMENTATION pour la COMMUNAUTÉ__
	* Remettre au clair les éléments essentiels qui permettent de fabriquer.
	
	* Faire la liste des composants et matériaux à acheter. Avec une liste de fournisseur possible, encore mieux, la liste avec plusieurs référence fournisseur possible pour tous les composants. On doit voir clairement combien coût l’objet au total.
	
	* Faire la liste des outils nécessaires à la fabrication.
	
	* Faire un dossier avec tous les fichiers nécessaire à la fabrication de la partie électronique.
	
	* Faire un dossier avec tous les fichiers nécessaire à la fabrication de la partie mécanique.
	
	* Faire un document qui explique très clairement comment on fait pour fabriquer l’objet étape par étape. L’utilisateur doit être capable de voir s’il est possible de faire des adaptations selon les moyens qu’il a à sa disposition.
	
	* Faire un dossier avec tous les logiciels à télécharger dans le ou les microcontrôleurs ou microprocesseur ou autre FPGA ou que sais‑je.
	
	* Faire un document qui explique étape par étape comment télécharger les logiciels et le cas échéant il faut faire les configuration ou les réglages.
	
	* Il faut faire un document pour expliquer comment vérifier le bon fonctionnement. Et si possible, donner une procédure sur comment dépanner.
	
	* Donner un contact pour les questions et pour obtenir un retour sur la satisfaction de l’utilisateur.



------------------------------------------------------------------------

## Concevoir la partie Mécanique

### Vue Global sur un Flux de Travail Simplifié

0. CROQUIS DU DESIGN
1. PLAN 3D
2. PROJECTION DES PLANS EN 2D
3. FABRICATION DU PROTOTYPE
4. MISE AU POINT
→ _Réitération des étapes 1 à 4 jusqu’à ce que tout soit OK._ ↺
5. DOCUMENTATION POUR LA COMMUNAUTÉ

{Commentaire}


### Une Liste de Questions à se Poser

La liste suivante regroupe des actions essentielles, mais elles ne sont ni exhaustives, ni limitatives. À vous de vous faire votre propre opinion. Au cours de la conception, il y aura sûrement des sous‑tâches, qu’on ne peut pas prévoir à l’avance, qui vont apparaître.

0. __CROQUIS DU DESIGN__


1. __PLAN 3D__


2. __PROJECTION DES PLANS EN 2D__


3. __FABRICATION DU PROTOTYPE__


4. __MISE AU POINT__


5. __DOCUMENTATION POUR LA COMMUNAUTÉ__


------------------------------------------------------------------------

## Concevoir la partie Programmation

### Vue Global sur un Flux de Travail Simplifié

0. IDÉE
1. SPÉCIFICATION & ARCHITECTURE LOGICIEL
2. CODAGE
3. DÉBEUG
4. VALIDATION FONCTIONNELLE
→ _Réitération des étapes 1 à 4 jusqu’à ce que tout soit OK._ ↺
5. DOCUMENTATION POUR LA COMMUNAUTÉ

{Commentaire}


### Une Liste de Questions à se Poser

La liste suivante regroupe des actions essentielles, mais elles ne sont ni exhaustives, ni limitatives. À vous de vous faire votre propre opinion. Au cours de la conception, il y aura sûrement des sous‑tâches, qu’on ne peut pas prévoir à l’avance, qui vont apparaître.


0. __IDÉE__
	La créativité est une chose mystérieuse. Personne ne peut prétendre donner une méthode générale pour trouver des idées. Il faudra creuser au bout de vous même et vous faire confiance. Laissez‑vous guider par vos envies.


1. __SPÉCIFICATION & ARCHITECTURE LOGICIEL__
	* Il est fort risquer de partir dans le codage de but en blanc sans avoir réfléchi au préalable. Comme pour l’électronique, il faut ici interroger la spécification et expliciter l’implicite.
	
	* Construire une architecture des fichiers ou fonctions nécessaires et mettre en lumière leurs interactions. La méthode de modélisation UML ([Unified Modeling Language](https://fr.wikipedia.org/wiki/UML_(informatique)) ) peut être d’une aide précieuse.
	
	* Choisir le cœur numérique (MCU, CPU, FPGA ou autres) selon la nature du projet.
	
	* Définissez les outils de débeug dont vous aurez besoin.


2. __CODAGE__
	* Le cœur du travail… Organiser votre travail en sous‑fonctions.
	
	* Commencer le code sur une démo board qui contient le MCU visé en attendant que la carte électronique arrive.
	
	* Préparer le terrain pour transférer ce premier code pour la vraie carte électronique.
	
	* Faire avec l’électronicien une revue des affectations au(x) cœur(s) numérique(s) pour mettre au clair les capacités des micro.
	
	* Passer en revue les mémoires pour vérifier que l’électronique prend bien en compte les besoins logiciels.
	
	* Vérifier que le choix des quartz permet bien de faire le travail attendu.
	
	* Vérifier que l’électronique met bien en œuvre l’accès aux pins de téléchargement et de débeug.
	
	* Lancer vous, pour de bon cette fois‑ci, dans le codage à proprement parler.


3. __DÉBEUG__
	* En programmation, le cycle en V n’est pas forcément une bonne modélisation du flux de travail. Une méthode de type [Scrum](https://fr.wikipedia.org/wiki/Scrum_(d%C3%A9veloppement)) ou [méthode Agile](https://fr.wikipedia.org/wiki/M%C3%A9thode_agile) est souvent mieux adapté.
	
	* Mettre en place les outils qui permettront de faire des téléchargement régulièrement. Car il y aura une itération très intensive entre codage et débeug.
	
	* Noter les fonctions essentielles dont l’électronicien à besoin pour faire la vérification unitaire et la mise au point. Électronicien et Codeur doivent travailler en bonne intelligence. C’est un point clé pour la bonne conduite du projet.


4. __VALIDATION FONCTIONNELLE__
	* Il s’agit de vérifier de façon systématique que toutes les fonctionnalités de la spécification sont parfaitement implémenter.
	
	* Faire les corrections nécessaires
	
	* Faire une livraison de master. Il s’agit de figer une version majeur du logiciel en vue de fixer la solution final du produit.
	
	* Pour les pro, faire une livraison d’une version de logiciel destinée à la qualification.
	
	* Prendre en compte les remarques et demandes des concepteurs ou des utilisateur. Et corriger les problèmes résiduels.
	
	* Faire une nouvelle remise de master. Et réitère, ce processus jusqu’à ce que l’on considère le résultat satisfaisant.


5. __DOCUMENTATION POUR LA COMMUNAUTÉ__
	* Il s’agit de faire une documentation qui explique comment fonctionne le logiciel pour pouvoir garantir une maintenance des problèmes constatés.
	
	* Faire un document qui permet à monsieur tout le monde de télécharger le logiciel dans l’objet.
	
	* Faire une procédure de réglage ou de configuration le cas échéant.
	
	* Donner un contact pour les questions et pour obtenir un retour sur la satisfaction de l’utilisateur.
