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
# Introduction

## Grandeur conservative

_Rappel : Grandeur conservative_  
Une grandeur conservative peut-être est définie comme une grandeur qui ne varie pas dans un système isolé.



On a vu que pour un système mécanique, l'énergie mécanique n'est pas conservative puisqu'elle n'est pas constante pour une système isolé __si le solide est déformable__.

Or le principe de conservation est très important en physique car il permet de prévoir l'évolution des systèmes. C'est pourquoi, on va chercher à quantifier une grandeur - homogène à une énergie et fonction d'état - qui soit conservative.

Pour comprendre le cheminement vers le premier principe, on va analyser ce caractère non conservatif de l'énergie mécanique sur le cas d'un exemple.


## Contact entre deux solides.

````{admonition} Exercice 
:class: attention

Considérons deux solides 1 et 2 glissant l'une sur l'autre avec une force de frottements solides entre les deux $\overrightarrow{F}$. On va la supposer constante pour simplifier et que la résultante des forces extérieures est nulle (système pseudo-isolé mécaniquement).

1. Comment évolue l'énergie cinétique et l'énergie mécanique macroscopique du système total {1+2}? 
1. Comment, intuitivement, va évoluer l'énergie d'agitation thermique du système?
1. A quoi peut correspondre la variation d'énergie mécanique macroscopique $\Delta E_M$?
1. Comment réécrire la conservation de l'énergie?
1. Que devient alors le bilan d'énergie pour le solide 1?
````

````{dropdown} Démonstration

__Non conservation de l'énergie mécanique__  
Le théorème de l'énergie cinétique s'écrit pour le système {1+2}: $\Delta E_c = W(\overrightarrow{F}) < 0$ puisque c'est une force de frottements (on rappelle qu'on tient compte du travail des forces intérieures dans le TEC). Il vient que l'énergie cinétique va diminuer. Ici $E_m = E_c$: l'énergie mécanique va diminuer.



__Autres termes énergétiques__  
On peut penser qu'il va y avoir échauffer et donc augmentation de l'énergie d'agitation thermique du système (on rappelle qu'il s'agit d'une composante de ce qu'on a décrit comme l'énergie interne).

D'un point de vue mécanique, l'agitation thermique est un mouvement microscopique interne et chaotique. L'énergie associée est, comme on l'a vu une partie de l'énergie interne $\Delta U$. Remarquons au passage que l'énergie potentielle d'interaction (microscopique aussi) peut aussi varier durant le mouvement de 1 sur 2. On ne peut, avec des observations macroscopiques quantifier exactement la part de variation de chaque terme (potentielle et cinétique microscopique). Par contre, on sait (ou plutôt on postulera... ) que le système étant isolé, l'énergie mécanique n'est pas "perdue" mais transformée en énergie interne: $\Delta E_m = - \Delta U$.



__Vers une grandeur conservative.__  
On peut donc réécrire un principe de conservation de l'énergie totale incluant l'énergie interne: $\Delta E_m + \Delta U = 0$.

Attention l'énergie interne est le résultat de composante "mécanique'' microscopique (énergie cinétique et potentielle) mais le trop grand nombre de particules, l'imprécision sur les mesures de vitesses et positions rend impossible une étude exhaustive ``mécanique" de l'énergie interne. C'est pourquoi elle doit être particularisée. On a vu comment on pouvait, à l'échelle macroscopique, suivant les systèmes, exprimer l'énergie interne en fonction des autres variables d'état du système.



__Nouveau transfert d'énergie__  
Pour le solide 1, il y a échange d'énergie avec le solide 2, donc même en considérant l'énergie interne, l'énergie totale $E_m + U$ n'a pas de raison d'être conservée. L'échange d'énergie entre 1 et 2 se fait par l'intermédiaire de la force $\overrightarrow{F}$. On connaît déjà le travail mécanique $W=W(\overrightarrow{F})$. Sauf que ce travail est définit à partir des mouvements macroscopiques. Or en réalité, $\overrightarrow{F}$ est la résultante de multiples actions microscopiques. L'échange d'énergie via $\overrightarrow{F}$ aura une partie macroscopique $W$ qu'on sait calculer et une partie microscopique. A nouveau, on ne peut faire un calcul mécanique pour caractériser cette partie. On va simplement la regrouper dans un seul terme $Q$ qu'on appelera transfert de chaleur: $\Delta E_m + \Delta U = W + Q$.



__Conclusion__  
Donc, en tenant compte des phénomènes microscopiques, c'est-à-dire en ajoutant l'énergie interne dans le bilan d'énergie, on a fabriqué une grandeur (l'énergie totale E) qui est conservée pour un système isolé!

Il apparaît donc, si l'on veut faire un bilan énergétique complet en tenant compte des aspects microscopiques et macroscopiques qu'on doit tenir compte de forme de transfert d'énergie le premier correspondant au transfert mécanique "habituel" et l'autre correspondant à un transfert à l'échelle microscopique: on le définira par la suite comme le transfert de chaleur.

````

