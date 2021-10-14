---
jupytext:
  encoding: '# -*- coding: utf-8 -*-'
  formats: ipynb,md:myst
  split_at_heading: true
  text_representation:
    extension: .md
    format_name: myst
    format_version: 0.13
    jupytext_version: 1.10.3
kernelspec:
  display_name: Python 3
  language: python
  name: python3
---
# Echelles d'étude

## Echelles de description d'un système


Le fait qu'un système thermodynamique contiennent un grand nombre de particule conduit à distinguer 3 niveaux de description du système. Nous verrons que l'on peut quelque fois définir les grandeurs physiques à ces différents niveaux. Le tout est que ce soit cohérent.


````{admonition} Définition : Echelle microscopique
:class: tip

L'échelle microscopique est l'échelle des particules élémentaires qui forment le système. Pour des molécules, elle sera de l'ordre de $10^{-10}\rm{m}$. A cette échelle, la matière est discontinue.

Son intérêt: exhaustivité. Si on connaît le comportement de toutes les particules, on connaît tout le système parfaitement.

Son principal inconvénient: sa complexité. Nous ne pouvons étudier de tels systèmes (par exemple 1 mole de gaz contient $10^{23}$ atomes à étudier) analytiquement, il faut passer par des résolution numérique (et même dans ce cas, le grand nombre de particules pose problème).

Ajoutons que d'un point de vue physique, les variations sont très faibles et très rapides. Elles ne peuvent être observées par nos capteurs. De plus, on sait aujourd'hui que lorsqu'on fait une mesure, on perturbe le système et que plus on cherche à être précis dans la mesure, plus on le perturbe (il s'agit d'une interprétation __très sommaire__ de la mécanique quantique). Il est donc impossible d'étudier complètement expérimentalement un système thermodynamique à l'échelle microscopique. On ne peut remonter qu'à des effets __statistiques__ dont nous reparlerons par la suite.

````

````{admonition} Définition : Echelle macroscopique
:class: tip

L'échelle macroscopique est notre échelle. Celle à laquelle, nous pouvons percevoir des détails, des objets, des variations...  A cette échelle, tout milieu constitué d'une seule phase paraît continu.

Son intérêt: sa simplicité. On a en général besoin de peu de variables pour décrire le modèle (par exemple pour la position d'un solide, 5 coordonnées suffisent). Et nous pouvons observer expérimentalement des changements.

Son principal inconvénient: on perd nécessairement de l'information. Nous verrons que cela a une grande importance dans l'évolution des système. De plus, à l'échelle macroscopique, il peut y avoir inhomogénéité du système, c'est-à-dire que les grandeurs vont varier à l'intérieur du système (ex: la température).

````

````{admonition} Définition : Echelle mésoscopique
:class: tip

L'échelle mésoscopique est une échelle intermédiaire. Elle correspond à un petit volume $d \tau$. Celui-ci est assez grand pour contenir un nombre important de particules et qu'on puisse considérer la matière comme continue et assez petit pour que les grandeurs macroscopiques observables (température, pression, densité, concentration... ) y soient uniformes. Pour cela, il faut que $d \tau$ soit grand devant le volume moyen occupé par une particule et petit devant les variations des grandeurs intensives.

Son principale intérêt: d'un point de vue mathématique, l'échelle mésoscopique correspond aux échelles du calcul infinitésimal.

D'un point de vue physique, on peut considérer que l'échelle mésoscopique correspond à une échelle plus faible (mais de l'ordre) des capteurs puisque les grandeurs mesurées à la surface d'un capteur font remonter une seule valeur et donc une impression d'homogénéité.

````

## Exemple: Gradient de température

````{admonition} Exercice 
:class: attention

On considère un tube de longueur $L$ dont les parois extérieures ne conduisent pas la chaleur. A l'intérieur du tube se trouve un gaz qui conduit la chaleur. On impose aux extrémités du tube des températures $T_1$ et $T_2$. On repère la position d'une section du tube par sa côté x sur un axe Ox horizontal. 

On peut montrer que la température dans le tube en régime permanent suit la loi: $T(x) = T_1 + \frac{T_2-T_1}{L}x$ (la preuve sera vue en deuxième année).

Estimer un ordre de grandeur de taille pour chaque échelle. On supposera que L = 1m

````
````{dropdown} Démonstration

 


__Tailles caractéristiques des différentes échelles__  
* Echelle macroscopique: C'est le système entier. Sa taille caractéristique est donc $\Delta x = L$
* Echelle microscopique: La taille caractéristique est la distance intermoléculaire: $\delta x \approx 10^{-9} \rm{m}$
* Echelle mésoscopique: On ne définit pas de taille précise, mais pour qu'elle ait un sens, il faut pouvoir choisir une taille caractéristiques telle que $dx \gg \delta x$ et $dx \ll \Delta x$. Ici c'est possible car les ordres de grandeur entre les deux sont grands.

La taille des capteurs de température étant de l'ordre du millimètre (moins pour certains capteurs très précis), une échelle de l'ordre de quelques micromètres est acceptable.


On peut généraliser cela: la définition de l'échelle mésoscopique est valable tant que les variations des grandeurs macroscopiques sont très supérieures aux dimensions de l'échelle microscopique. Dans toute les études que nous ferons par la suite, y compris en électromagnétisme, nous supposerons cette condition toujours vérifiée.



En général, nous étudions un système thermodynamique à une échelle macroscopique soit:

* en le découpant en de multiples morceaux mésoscopiques: cela revient à étudier des fonctions (scalaires en thermodynamiques, scalaires ET vectorielles en électromagnétisme) de l'espace qu'on supposera continues, la plupart du temps dérivables et qui décrivent les grandeurs macroscopiques du système. Nous l'avons déjà fait en statique des fluides
* soit en le prenant dans son ensemble. Cela est possible lorsque les grandeurs macroscopiques (les __variables d'état)__ sont homogène. Le système est alors __à l'équilibre__.


````

