# Introduction
Sans le contexte de notre seconde année de master MIAGE (Méthodes Informatiques Appliquées à la Gestion des Entreprises), nous participons à l'UE "Trans-10 Environnement socio-économique". Dans le cadre de cet UE nous nous intéressons au portefeuille de compétences. Ce porte-feuille de compétences est un outil, utile par exemple dans la recherche d'un poste dans un entreprise, qui permet de montrer et justifier un ensemble de compétences divers et variés, les mettre en valeur, ce qui peut, par exemple, compléter un CV.
Ce cahier des charges concerne donc l'élaboration de ce portefeuille de compétences.  

# Besoins
Le portefeuille doit remplir des besoins différents, autant que ce soit des besoins venant du créateur que ce soit du lecteur.
Le créateur doit pouvoir aisément construire son catalogue de compétences, justifié, construit autour d'expériences etc..  
Quant au lecteur, la lecture, pour lui, doit être rapide et simple, le support doit lui permettre d'identifier rapidement les compétences et justifications.
Nous devons donc définir ce qu'est une compétence, comment la justifié, et définir les éléments qu'il y a autour.  
<!--réflexion sur le porte-feuille de compétences-->

# Existant
Dans le cadre de ce projet, nous avons la présence d'existant.
Deux document word sont à notre disposition:
    - Document de structure d'une compétence
    - Document exemple de porte-feuille de compétence
Le premier document indique comment énoncé et présenter une compétence. Ce document constitue un bon début, cependant certains détails utiles peuvent manquer. Comme des codes d'identification de compétences référencé dans les normes européennes. 
Le second document est un exemple de porte-feuille de compétences. Il respecte la structure défini dans le premier document. Pourtant, le document manque d'esthétique et il n'y a pas de réelle emphase sur les compétences. Certains manques sont à palier afin de permettre une expérience utilisateur plus intéressante et proche des besoins énoncés.  

# Cahier des charges
<!--
- Description général
- Description fonctionelle
- Description de l'environnement technique
- charte graphique
- contraintes
-->
## Introduction

## Contexte
Le projet, le porte-feuille de compétences, est développé dans un cadre universitaire, et a aussi un intérêt personnel. Nous développons ce projet à deux, et dans un cadre universitaire, nous nous efforcerons de ne pas choisir de solutions qui pourrait induire un coût en argent.  
Nous devrons donc nous conformer aux exigences de l'université afin de satisfaire au mieux ce qui est demandé. Nous devons aussi pouvoir correctement présentés nos compétences.

Comme énoncé précédemment, voici nos existants:  
```markdown 
Deux document word sont à notre disposition:
    - Document de structure d'une compétence
    - Document exemple de porte-feuille de compétence
Le premier document indique comment énoncé et présenter une compétence. Ce document constitue un bon début, cependant certains détails utiles peuvent manquer. Comme des codes d'identification de compétences référencé dans les normes européennes. 
Le second document est un exemple de porte-feuille de compétences. Il respecte la structure défini dans le premier document. Pourtant, le document manque d'esthétique et il n'y a pas de réelle emphase sur les compétences. Certains manques sont à palier afin de permettre une expérience utilisateur plus intéressante et proche des besoins énoncés. 

Le porte-feuille de compétences doit pouvoir en outre être facilement présenté que ce soit pour présenter ses compétences ou bien pour décrire son fonctionnement.
¨Pour ce projet, nous n'avons pas de contraintes concernant le support ou la charte graphique, du moment que les critères et les besoins sont respectés.
``` 
Certains détails sont donc à compléter, concernant l'identification de compétences d'après des références, par exemple. Mais aussi sur l'esthétisme et l'emphase. Ces deux derniers points peuvent être importants pour le projet. Tout comme le CV, le porte-feuille de compétences est destiné à être revu et comparé avec d'autres, accroché le lecteur et lui donner des informations de manière rapide et effecace est stratégique.

Acteur:
- Créateur:
    - formuler/ajouter des compétences 
    - se valoriser
- Lecteur:
    - Pouvoir avoir une lecture rapide et efficiente
    - Avoir des informations qui permettent la comparaison
    - Avoir des références précises  

Lecteur:
<div class="mermaid">
graph TD
    P[Présentation]<-->Compétences
    P<-->Expériences
    P<-->Exemples;
</div>

<div class="mermaid">
classDiagram
class Compétences {
    +String contexte
    +String intitule
    +String codeNorme
}
class Expériences {
    +String Lieu
    +String contexte
    +outils
}
class Exemples{
    +outil
    +intitule
    +resume
    +lien
}
class CompExp
class CompExe
class ExpExe
Compétences -- "many" CompExp:Contains
Compétences -- "many" CompExe:Contains
Exemples -- "many" CompExe:Contains
Exemples -- "many" ExpExe:Contains
Expériences -- "many" ExpExe:Contains
Expériences -- "many" CompExp:Contains
</div>
<!--
- Description demandeur
- Origine besoin
    - Description existant
    - description problèmes
- Description générale du besoin
- Description des catégories de l'utilisateur (acteurs)
-->

## Description fonctionnelle
Un porte-feuille de compétences peut devenir quelque chose de très riche, et si toutes les informations sont sur une seule page, la quantité d'informations peut vite devenir peu digeste.
- création:
    - créer des compétences
    - créer des expériences
    - créer des références
    - créer des exemples
    - créer des liens entre toutes ces entités (si les liens existent) 
- lecture:
    - liste par expériences et exemples
    - liste par références
    - liste par exemples
    - détail d'une expérience
    - détail d'une compétence
    - détail d'un exemple  

Le but est d'avoir une lecture d'ensemble rapide et efficace sans surplus d'informations, avec le présence de liens permettant davantage d'informations sur un aspect, et d'autres liens. Ceci permettrait une navigation simple, d'éviter la perte d'informations (affichage simplifié mais pas de pertes) et d'y accéder rapidement.  

UML  
méthode MoSCoW
 
## Description technique
<!--existant et contraintes imposés par le client ou imposé par l'existant>
## Charte graphique

## Contraintes d'environnement
<!--
contraintes humaines, financières, temporelles, juridiques ...
-->
Comme précédemment évoqué, la solution choisie est totalement à notre appréhension. Cependant, elle doit être accessible, donc lisible sur différents supports. De plus, il faut choisir une solution qui n'induit aucun coûts financer.

# Conception
# Introduction
<!-- - Rappelé fonctionnalités -->
- création:
    - créer des compétences
    - créer des expériences
    - créer des références
    - créer des exemples
    - créer des liens entre toutes ces entités (si les liens existent) 
- lecture:
    - liste par expériences et exemples
    - liste par références
    - liste par exemples
    - détail d'une expérience
    - détail d'une compétence
    - détail d'un exemple  

## Logiciels Existant
Pour ce qui est des documents texte:
- Microsoft Word, qui fait partie de la suite 365, outil incontournable et référence du traitement de texte, la limite est que c'est un outil payant, et pas forcément abordable pour tout le monde

- Logiciel OpenSource, aussi ou presque aussi complet que Word, mais souvent bien moins appréciés que son conccurent au niveau de l'interface. Cependant cette solution a le mérite d'être gratuite.

-  Google docs, l'essor des services en ligne et du cloud l'ont propulsé dans les outils les plus utilisés. Comportant bien moins de fonctionnalités que les autres solutions proposées, il a cependant l'avantage de faciliter le partage de documents et le travail simultané.

Pour les slides, nous retrouvons les mêmes types de solutions, avec les mêmes avantages ou inconvénients:

- Microsoft PowerPoint
- Logiciel OpenSource
- Google Slide

Une autre solution serait le site web, statique bien entendu. Toutefois son élaboration peut prendre un certain temps s'il est créée de toute pièce. C'est pourquoi nous pouvons nous tourner vers des CMS (Content Management System). Les CMS, permette de créer facilement des sites web, comme des blogs par exemples, des sites vitrines etc.. Orientés édition de contenu, ils peuvent convenir aux besoins énoncés précédemment. De plus la mise en ligne d'un site web permet une grande accessibilité. Toutefois, il ne rend pas forcément plus facile la présentation du porte-feuille de compétences.
Il existent une multitude de CMS dans différents langages de programmation, en voici quelques uns parmi les plus présents:

- WordPress
- Joomla
- Drupal

## Hébergement/Serveur accessibilité
Pour les documents textes et les slides, il aurait pu être difficile de rendre le document accessible autrement que par support papier. Mais aujourd'hui, des solutions "cloud" sont nombreuses, bien souvent gratuite (Google Drive, DropBox..) et permettent de rendre accessible ces documents par internet. De plus, il est possible de joindre ces documents à un CV dans un mail, par exemple.

Concernant les sites web, l'hébergement est déjà plus compliqué. Les solutions d'hébergement gratuites sont peu nombreuses et mettent à disposition des performances plutôt pauvre. Toutefois, un porte-feuille n'engendre normalement pas un très gros traffic, et les performances sont amplement suffisante pour le projet. Le gros avantage de cette solution est la création facile des liens entre Compétences, Expériences, Exemples etc.. et la navigation que cela permettrait.
<!--Explication accessibilité-->
Voici quelques solutions d'hébergement:
<!-- 
Ouh la la téma les exemples..
-->
fr.000webhost.com, gratuit et déjà utilisé l'année dernière pour un projet. Constitue une solution intéressante.

https://www.wordpress-hebergement.fr/

https://www.hebergementwordpress.fr/hebergement-wordpress-gratuit/  
3 mois gratuit et 3.99€/mois ensuite.

## Impact et coûts
Le besoin en temps de développement du projet avec un CMS peut être relativement court. Toutefois, notre base de compétence sur le CMS n'es pas suffisante pour estimer précisément les durées des tâches. Le projet est un projet développé dans le cadre universitaire, donc il n'y aura pas de coûts liés aux développement même si on pourrait en donner une approximation hypothétique.

De plus les solutions techniques choisis sont gratuites. Les coûts engendré concerne seulement l'électricité par exemple.

Découpage des tâches:
1. Installer environnement: 40 min
    1. Installer Wamp/Mamp: 10-20 min
    2. Créer BDD: 10min
    3. Installer WordPress: 20min
2. Travail de recherche et choix préalable: 3h
    1. Trouver un thème qui colle le plus possible à la charte graphique: 1h
    2. Trouver les modules dont nous aurons besoins: 2h
3. Installation des outils Wordpress: 50min
    1. Application du thème: 10 min
    2. Intégrations des modules et paramétrage: 40 min
4. Créer contenu
    1. Créer des compétences: 1h
    2. Créer des Expériences: 1h
    3. Créer des exemples: 1h
5. Publication et mise en lien
    1. Publier le contenu: 10-20min
    2. Créer le contenu à afficher: 30 min
    3. Instaurer les différents liens: 30 min
6. Front-end
    - Modifier l'esthétique de la page 10min-2h (dépend du thème)

<div class="mermaid">
gantt
    title Planification optimiste
    dateFormat YYYY-MM-DD
    section Installation
    Wamp : crit,A1, 2021-01-20, 20m
    Créer BDD: crit,A3, after A1, 10m
    Wordpress : crit,A2, after A3 ,20m
    %%
    section Travail de recherche
    Trouver thème: crit,B1, after A2, 1h
    Trouver outils: B2, after A2, 2h
    %%
    section Installation des outils
    Application du thème : crit,C1, after B1, 30m
    Application module : C2, after B2, 40m
    %%
    section création de contenu
    Créer Compétences : crit,D1, after A2, 1h
    Créer Expériences : crit,D2, after A2, 1h
    Créer Exemples : crit,D3, after A2, 1h
    %%
    section Publication et mise en lien
    Créer la présentation: crit,E1, after D1, 2h
    Créer page CV: crit, E1,after D1,2h
    Créer page détail Compétence: crit,E1,after D1,2h
    Créer page détail Expérience: crit,E1,after D1,2h
    Créer page détail Exemple: crit,E1,after D1,2h
    Publier le contenu: crit,E2, after E1, 20m
    Instaurer liens: crit,E7, after E2, 30m
    %%
    section Front-end
    Modifier l'esthétique : F1, after C1, 3h
    %%
    %%section Jalon
    %%1er jet :crit, 2021-04-05, 1d
    %%Fin projet :crit,2021-06-13,1d
</div>

<div class="mermaid">
gantt
    title Planification étalée
    dateFormat YYYY-MM-DD
    section Installation
    Wamp : crit,A1, 2021-01-20, 0.333d
    Créer BDD: crit, A3, after A1,0.333d
    Wordpress : crit,A2, after A3 ,0.333d
    %%
    section Travail de recherche
    Trouver thème: crit,B1, after A2, 1w
    Trouver outils: B2, after A2, 2w
    %%
    section Installation des outils
    Application du thème : crit,C1, after B1, 30m
    Application module : C2, after B2, 1w
    %%
    section création de contenu
    Créer Compétences : crit,D1, after A2, 2w
    Créer Expériences : crit,D2, after A2, 2w
    Créer Exemples : crit,D3, after A2, 2w
    %%
    section Présentation Publication et mise en lien
    Créer la présentation: crit,E1, after D1, 1w
    Créer page CV: crit, E1,after D1,2w
    Créer page détail Compétence: crit,E1,after D1,2w
    Créer page détail Expérience: crit,E1,after D1,2w
    Créer page détail Exemple: crit,E1,after D1,2w
    Publier le contenu: crit,E6, after E1, 1d
    Instaurer liens: crit,E7, after E2, 1d
    %%
    section Front-end
    Modifier l'esthétique : F1, after C1, 2021-04-05
    %%
    section after 1er jalon
    individualisation projet : Z1,after jalon1,1d
    adaptation structure: Z2, after Z1,2021-05-31
    adaptation esthétique: Z3,after Z1,2021-06-13
    section Jalon
    1er jet :crit, jalon1, 2021-04-05, 1d
    Fin projet :crit, jalon2, 2021-06-13,1d
</div>

<div class="mermaid">
gantt
    title Planification étalée
    dateFormat YYYY-MM-DD
    section Installation
    Wamp : crit,A1, 2021-01-20, 0.333d
    Créer BDD: crit, A3, after A1,0.333d
    Wordpress : crit,A2, after A3 ,0.333d
    %%
    section Travail de recherche
    Trouver thème: crit,B1, after A2, 1w
    Trouver outils: B2, after A2, 2w
    %%
    section Installation des outils
    Application du thème : crit,C1, after B1, 30m
    Application module : C2, after B2, 1w
    %%
    section création de contenu
    Créer Compétences : crit,D1, after A2, 2w
    Créer Expériences : crit,D2, after A2, 2w
    Créer Exemples : crit,D3, after A2, 2w
    %%
    section Présentation Publication et mise en lien
    Créer la présentation: crit,E1, after D1, 1w
    Créer page CV: crit, E1,after D1,2w
    Créer page détail Compétence: crit,E1,after D1,2w
    Créer page détail Expérience: crit,E1,after D1,2w
    Créer page détail Exemple: crit,E1,after D1,2w
    Publier le contenu: crit,E6, after E1, 1d
    Instaurer liens: crit,E7, before jalon1, 1d
    %%
    section Front-end
    Modifier l'esthétique : F1, after C1, 2021-04-05
    %%
    section after 1er jalon
    individualisation projet : Z1,after jalon1,1d
    adaptation structure: Z2, after Z1,2021-05-31
    adaptation esthétique: Z3,after Z1,2021-06-13
    section Jalon
    1er jet :crit, jalon1, 2021-04-05, 1d
    Fin projet :crit, jalon2, 2021-06-13,1d
</div>

-----------------------------


- Logiciels existants/concurrence
- Étude logiciel développé
    - Type de solution
    - Environnement de programmation
    - Framework de développement
    - Serveurs/hébergement
    - Intégration au SI existant
- Étude impact de la solution choisie
    - coût de dev
    - coût installation et maintenance
    - coût organisationnelle
    - interop avec les SI
- Proposition d'une solution
- Découpage de la solution en sous système + diagramme de GANTT
- Modélisation front-end
    - charte graphique application
    - maquettage

<script src="https://cdn.jsdelivr.net/npm/mermaid/dist/mermaid.min.js"></script>

      