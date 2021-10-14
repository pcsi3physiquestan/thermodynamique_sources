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
# Etude de transformations

_  On va étudier l'écriture du premier principe dans diverses transformations. On s'intéressera en particulier au cas des transformations monobares qui expliquent l'intérêt de l'enthalpie._

## Transformations diverses

````{admonition} Exercice 
:class: attention

Ecrire le premier principe dans le cas:

1. d'une transformation adiabatique.
1. d'une transformation isochore.
1. d'une transformation isotherme pour une phase peu compressible ou un solide.
1. d'une transformation isotherme pour gaz parfait.


On distinguera, pour le travail W, le travail associé aux contraintes normales $W_P$ du reste du travail $W_{autre}$.

````

## Cas des transformations monobares. Enthalpie.

_Rappel :Transformation monobare_
On rappelle qu'une transformation monobare est une transformation pour laquelle la pression extérieure (ou plus généralement la contrainte normale extérieure) est constante.

Si la transformation est de plus quasi-statique, elle devient isobare.


````{admonition} Fondamental : Réécriture du premier principe pour une transformation monobare
:class: attention

Soit un système fermé dont la pression extérieure agissante sur le système est maintenue constante $P_0$ passant d'un état d'équilibre à un autre. La variation d'enthalpie $\Delta H$ s'écrit:

\begin{equation}
\Delta E_{M,macro} + \Delta H = Q + W_{autre}
\end{equation}
où $W_{autre}$ est le travail autre que les forces de pression.
````


__Démonstration__  
Le premier principe appliqué au système s'écrit: $\Delta U = W_{pression} + W_{autre} + Q$. Remarquons de plus qu'à l'état initial et à l'état final, la pression du système est $P_0$ puisque le système est en équilibre avec l'extérieur. On a:

\begin{align*}
W_{pression} &= - \int P_{ext} dV = - P_0 \int dV = - (P_0 V_{final} - P_0 V_{initial})\\
&= - \Delta PV\\
\Delta U &= - \Delta PV + W_{autre} + Q\\
\Delta H &= \Delta(U + PV) = W_{autre} + Q
\end{align*}


__Remarques__  
Il s'agit d'une __réécriture du premier principe__.

On pourra faire le parallèle avec le passage du TEC au TEM. Ici aussi, on "fait passer" un terme (produit PV) de la gauche vers la droite et on redéfinit une nouvelle grandeur énergétique, ce qui simplique l'expression du premier principe.


````{admonition} Attention : 
:class: note

L'analogie précédente a ses limites car le passage du TEC au TEM est valable quelle que soit le système alors qu'ici la réécriture du premier principe avec l'enthalpie __n'est valable que si la transformation est monobare entre deux états d'équilibre__.

````

````{dropdown} Remarque

__Interprétation__  
L'écriture du premier principe avec l'enthalpie pour une transformation monobare entre deux états d'équilibre permet de comprendre le sens donné à la capacité thermique à pression constante comme __l'énergie à fournir pour augmenter la température de 1K à pression constante.__.

En effet, quand on fonctionne à pression constante, celà signifie en général qu'on dispose d'un système fermé par une partie mobile (piston) qui permet d'ajuster le volume du système pour maintenir la pression constante. Cet ajustement se fait "naturellement" au contact d"un atmosphère suffisamment grand pour sa pression soit constante. Mais le travail échangé par la contrainte normale n'est pas maitrîsé. Ce qu'on fournit réellement, c'est le $W_{autre} + Q$.

Cette interprétation permet aussi de comprendre pourquoi la capacité thermique à pression constante est plus grande que la capacité thermique à volume constant. En effet, quand la température du système augmente, son volume augmente à pression constante (coefficient de dilatation isobare). Il vient que les contraintes normales (qu'on appelera force de pression extérieures puisqu'elles sont exercées par une atmosphère à pression constante sur le piston) exerce un travail des forces de pression résistant: le système doit __fournir__ un travail mécanique à l'atmosphère. Cette énergie doit être fournie en plus de celle à apporter pour augmenter la température d'où $C_P > C_V$.
````

