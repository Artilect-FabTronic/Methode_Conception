> Date de Création : 22 novembre 2020  
> Auteur initial : Lilian Tribouilloy  
> Contributeurs : Voir le fichier CREDITS.md  
> Licence : Creative Commons BY SA  

# Comment Contribuer à ce Projet ?


## Une Démarche très Simple

Le processus pour contribuer à ce projet est très simple :
* Lire ;
* Bien réfléchir à votre critique (qui doit toujours être constructive) ;
* Proposer les modifications à l’auteur.

L’auteur garde toute liberté pour accepter ou non les propositions.

Le respect des contributeurs est garanti par les règles de bonne conduite décrite dans le fichier « CODE_of_CONDUCT.md ».


## Comment Transmettre vos Remarques ?

Les remarques doivent porter uniquement sur les fichiers au format markdown ou les dossiers annexes au manuel. La version imprimable du manuel est traitée par une autre méthode décrite plus bas.

Les corrections d’orthographe doivent être transmises uniquement dans le fichier markdown modifié en question.

### Pour les plus Geeks

* Créer un compte GitHub.
* Demander les droits d’accès par email à l’auteur : lilian@touchelibre.fr.
* Cloner le repository.
* Modifier votre copie locale.
* Envoyer un pull request.
* {Faire des Issues}

### Pour les plus Traditionnels

* Télécharger le dossier.
* Puis m’envoyer‑moi les remarques par courriel à cette adresse : lilian@touchelibre.fr


## Syntaxe Markdown

Ce manuel est écrit avec la syntaxe Markdown pour la version de travail. Ce langage de balise est assez simple, mais il faut le respecter. La variante “ GitHub Flavored Markdown ” est également acceptée.

On peut trouver toutes les informations sur ce langage ici :
* Version Originale du Markdown : <https://daringfireball.net/projects/markdown/>
* Standardisation précise du Markdown selon Common Mark : <https://spec.commonmark.org/>
* Version GitHub Flavored Markdown pour les fonctionnalités supplémentaires : <https://github.github.com/gfm/>

L’ajout de code HTML (comme le permet le markdown) pourra être acceptés lors de blocage technique ponctuel. Mais ne doit pas être généralisé.

Le logiciel [Abricotine](http://abricotine.brrd.fr/) est l’éditeur de texte markdown utilisé par l’auteur. Celui‑ci est chaudement recommandé pour ces qualités. Mais toute autre
éditeur de code peut être utilisé tant que la syntaxe est respecté.

En plus du Markdown, pour les annotations sur le travail en cours, ou les commentaires sur le contenu du manuel à revoir. Il a été adopté les conventions suivantes :
* On peut soit utiliser les accolades {Commentaire}, si on veut que les commentaires soient visibles lors de l’exportation vers une version imprimable préliminaire ;
* Ou, on peut utiliser la syntaxe HTML `<!--Commentaire-->` si on veut que ces commentaires soient invisibles.
* Mais, ces commentaires ont un caractère provisoire et devront être effacer sur la version finale.


## Formule Mathématique

Si le besoin s’en fait sentir, il est également possible d’écrire des formules mathématiques. Pour cela, il faut mettre la formule dans la balise double‑dollars. Et la formule doit être écrite selon la syntaxe LaTeX. 

Exemple avec `\displaystyle \sum_{k=0}^n k = \frac{n(n+1)}{2}` entre double $ on obtient :  
$$\displaystyle \sum_{k=0}^n k = \frac{n(n+1)}{2}$$

Cela ne fait pas partie du Markdown, mais est rendu possible grâce à des scripts (interne au site web) dédiés. Les plus connus sont MathJax et KaTeX. Pour l’exportation vers LibreOffice, il faut alors utiliser le plugin [TexMaths](http://roland65.free.fr/texmaths/).

Pour trouver pour apprendre à écrire des formules mathématiques avec la syntaxe LaTeX, voir ces sites :
* <https://fr.wikipedia.org/wiki/Aide:Formules_TeX>
* <https://fr.wikibooks.org/wiki/LaTeX/%C3%89crire_des_math%C3%A9matiques>

Plus d’information sur LaTeX, voir ces sites :
* <https://fr.wikipedia.org/wiki/LaTeX>
* <https://www.latex-project.org/>


## Management GIT

{À préciser}


## Correction d’Orthographe

Vous êtes les bienvenus pour faire des corrections sur les fautes d’orthographe et de grammaire. D’autant que l’auteur reconnait ces faiblesses sur le sujet. Mais, les moqueries sur les fautes d’orthographe et de grammaire, ainsi que les jugements de valeurs relatifs, sont intolérables et pourrons être le motif d’une exclusion du projet.

Les corrections d’orthographe doivent être reporté uniquement dans les fichiers markdown. Cela permettra un comparatif plus facile entre les versions. Aucun commentaire ne doit être ajouté pour corriger une faute d’orthographe.


## Usage de l’Orthotypographie

Par ailleurs, l’usage des règles d’[orthotypographie](http://www.orthotypographie.fr/) est recommandé. Ainsi par exemple, il faut utiliser les lettres majuscules accentuées comme : Ç, Œ, Æ, É, È, À, Ù, Ï, Ÿ. Les ponctuations typographiques sont également utilisées comme par exemple : les guillemets «» ou “”, l’apostrophe typographique « ’ », les points de suspension « … », l’espace insécable et l’espace insécable fine ou encore les différents tirets, dont le tiret insécable « ‑ », le tiret cadratin « — » et le tiret demi-cadratin « – ».

Ces différents caractéres Unicode ne sont pas disponibles sur un clavier traditionnel. C’est pourquoi le non usage de ces règles est toléré pour les contributeurs. Mais l’usage de clavier alternatif comme le [Bépo](https://bepo.fr/wiki/Accueil) ou le [Dvorak](https://fr.wikipedia.org/wiki/Disposition_Dvorak), par exemple, est applaudi et félicité chaudement.

L’écriture inclusive n’est pas utilisée.

Les titres sont écrits à l’anglaise. C’est à dire avec la première lettre de tous les mots importants sont en majuscule.

Les citations en français utilisent ce type de guillemet : «». Alors que les citations en anglais utilisent ce type de guillemet : “”.


## L’Exportation aux Formats ODT et PDF

Seul le logiciel [LibreOffice](https://fr.libreoffice.org/) est autorisé pour effectuer l’exportation. L’exportation au format ODT se fait manuellement. Pour cette raison, elle est faite que de façon épisodique.

Seul le logiciel LibreOffice est autorisé pour exporter au format PDF. Celui‑ci devra être un PDF hybride contenant la source ODT comme seul le permet LibreOffice.

Les polices de caractères choisies sont enregistrées à l’intérieur du fichier source ODT.

Seul l’auteur, ou une personne compétente en typographie et sur le logiciel LibreOffice, peut réaliser cette exportation. La modification des « Styles » du fichier template doit se faire avec précaution. Les règles d’orthotypographie doivent être mises en œuvre. Tout ceci est nécessaire pour garantir une bonne mise en page de la version imprimable finale.


## Autres Types de Contribution Possibles

### Participer à l’Élaboration des Dossiers Templates Projet

Le processus de contribution sur les dossiers templates projet n’est pas différent au cas des contributions portant sur le manuel à proprement parlé.

Les mêmes logiciels que l’auteurs doivent être utilisés. Ceux‑là sont d’ailleurs décrits dans le présent manuel.

Vous pouvez proposer de nouveaux fichiers templates pour aider à la conception.


### Participer à la Conception du Mini Projet Exemple

Le processus de contribution sur les dossiers templates projet n’est pas différent au cas des contributions portant sur le manuel à proprement parlé.

Les mêmes logiciels que l’auteurs doivent être utilisés. Ceux‑là sont d’ailleurs décrits dans le présent manuel.


### Promouvoir le Manuel

Comme le permet la licence de ce projet, le manuel peut‑être copier et distribuer sans restriction. Mais la communication doit se faire dans le respect des règles de bonne conduite décrite dans le fichier « CODE_of_CONDUCT.md ».

Toute communication dans l’espace public ou virtuel sur ce projet doit être signalé à l’auteur du manuel à l’adresse suivante : lilian@touchelibre.fr.

La cible pour la promotion de ce manuel est le public des fablabs, des makerspaces, des hackerspaces, des associations libristes et tout autre type d’association sur le bricolage ou les bricoleurs ou concepteurs isolés.

