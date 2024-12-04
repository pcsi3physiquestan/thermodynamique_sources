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

## Echelles de description d'un système (en ligne)
```{figure} ./images/qr_code/qr_thermo_echelles.png
:name: qr_thermo_echelles
:width: 150px
:align: right
:target: th_d_echelle.html
```

````{topic} __Echelle microscopique__

L'échelle microscopique est l'échelle des particules élémentaires qui forment le système. Pour des molécules, elle sera de l'ordre de $10^{-10}\rm{m}$. A cette échelle, la matière est discontinue.

Son intérêt: exhaustivité. Si on connaît le comportement de toutes les particules, on connaît tout le système parfaitement.

Son principal inconvénient: sa complexité. Nous ne pouvons étudier de tels systèmes (par exemple 1 mole de gaz contient $10^{23}$ atomes à étudier) analytiquement, il faut passer par des résolution numérique (et même dans ce cas, le grand nombre de particules pose problème).

Ajoutons que d'un point de vue physique, les variations sont très faibles et très rapides. Elles ne peuvent être observées par nos capteurs. De plus, on sait aujourd'hui que lorsqu'on fait une mesure, on perturbe le système et que plus on cherche à être précis dans la mesure, plus on le perturbe (il s'agit d'une interprétation __très sommaire__ de la mécanique quantique). Il est donc impossible d'étudier complètement expérimentalement un système thermodynamique à l'échelle microscopique. On ne peut remonter qu'à des effets __statistiques__ dont nous reparlerons par la suite.

````

````{topic} __Echelle macroscopique__

L'échelle macroscopique est notre échelle. Celle à laquelle, nous pouvons percevoir des détails, des objets, des variations...  A cette échelle, tout milieu constitué d'une seule phase paraît continu.

Son intérêt: sa simplicité. On a en général besoin de peu de variables pour décrire le modèle (par exemple pour la position d'un solide, 5 coordonnées suffisent). Et nous pouvons observer expérimentalement des changements.

Son principal inconvénient: on perd nécessairement de l'information. Nous verrons que cela a une grande importance dans l'évolution des système. De plus, à l'échelle macroscopique, il peut y avoir inhomogénéité du système, c'est-à-dire que les grandeurs vont varier à l'intérieur du système (ex: la température).

````

````{topic} __Echelle mésoscopique__

L'échelle mésoscopique est une échelle intermédiaire. Elle correspond à un petit volume $d \tau$. Celui-ci est assez grand pour contenir un nombre important de particules et qu'on puisse considérer la matière comme continue et assez petit pour que les grandeurs macroscopiques observables (température, pression, densité, concentration... ) y soient uniformes. Pour cela, il faut que $d \tau$ soit grand devant le volume moyen occupé par une particule et petit devant les variations des grandeurs intensives.

Son principale intérêt: d'un point de vue mathématique, l'échelle mésoscopique correspond aux échelles du calcul infinitésimal.

D'un point de vue physique, on peut considérer que l'échelle mésoscopique correspond à une échelle plus faible (mais de l'ordre) des capteurs puisque les grandeurs mesurées à la surface d'un capteur font remonter une seule valeur et donc une impression d'homogénéité.

````

