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
# Entrainement

## Effusion gazeuse

````{admonition} Exercice 
:class: attention

On considère deux compartiments de volume $V_1$ et $V_2$, l'ensemble est maintenu à la température T. Entre les deux compartiments, un petit trou de section $s$ a été pratiqué. Initialement on a $N_a$ particules d'un gaz parfait dans $V_1$. On note $N_1$ et $N_2$ les nombres de particules dans les volumes $V_1$ et $V_2$ et on adopte le modèle suivant pour lequel les particules ont toutes le même modules de vitesse v et que leur vitesse est suivant l'une des directions $\overrightarrow{e_x}, -\overrightarrow{e_x},\overrightarrow{e_y}, -\overrightarrow{e_y},\overrightarrow{e_z}, -\overrightarrow{e_z}$.

1. Quelle hypothèse peut-on faire en supposant que la section s est petite devant les autres grandeurs caractéristiques du système.
1. On se place dans l'hypothèse du chaos moléculaire. Quelle conséquence peut-on en déduire sur la distribution des vitesses des particules?
1. Quel est le nombre $dN_{1 \rightarrow 2}$ de particules passant de $V_1$ à $V_2$ entre $t$ et $t+dt$?
1. En déduire les équations différentielles vérifiées par $N_1$ et $N_2$ en fonction de $N_1, N_2, s, v$ et $V = V_1 =V_2$
1. Etablir les expressions de $N_1$ et $N_2$ au cours du temps. Définir un temps caractéristiques $\tau$.
1. Comment varie-t-il en fonction de la masse du gaz si on admet que $v = \sqrt{\frac{3RT}{M}}$.
1. Quelle peut-être l'application pratique de ce phénomène d'effusion gazeuse?


````

## Etude de diagramme de changement d'état

````{admonition} Diagramme (P-h)
:class: attention
On considère le diagramme enthalpique (ou diagramme des frigoristes) de l'eau ci-après. __Attention à l'échelle en ordonnée.__

```{figure} ./images/thermo_clap_eau_ph.png
:name: td_ph_diag
:align: center
Diagramme des frigoristes de l'eau
```

1. Déterminer la pression et la température au point critique ainsi que l'enthalpie massique critique de l'eau.
2. Déterminer l'enthalpie de vaporisation à 360K et à 520K.
2. On considère que le système est dans un état d'eau liquide saturée à 400K. Préciser la pression du système ainsi que son enthalpie massique.
3. On réalise depuis cet état une détente _isenthalpique_ jusqu'à une température de 320K. Tracer sur le diagramme des frigoristes cette transformation et en déduire
    * le caractère diphasé du système dans l'étt final
    * la pression du système
    * l'enthalpie massique de la partie liquide et de la partie gazeuse
    * la fraction massique de gaz formé en utilisant le théorème des moments.
4. L'allure des isothermes pour la phase liquide est-elle celle attendue ?
````

````{admonition} Diagramme (T-s)
:class: attention
On considère le diagramme entropique de l'eau ci-après (partie liquide-vapeur) représentant la température du système en fonction de son entropie massique.

```{figure} ./images/thermo_clap_eau.png
:name: td_ts_diag
:align: center
Diagramme entropique de l'eau
```

1. En vous aidant des différentes informations du diagramme, placer les zones correspondant à l'état liquide, vapeur et diphasé. Détermienr aussi la température critique et la pression critique de l'eau ainsi que l'entropie massique critique de l'eau.
2. Durant un changement d'état, l'entropie massique varie aussi. On peut ainsi définir l'entropie massique de changement d'état. Déterminer numérique l'entropie massique de changement d'état pour des pressions de 62,3kPa et de 37,6bar ainsi que les températures de changement d'état correspondantes.
3. Commenter l'allure des isenthalpiques pour la phase gazeuse.
2. On considère que le système est dans un état de vapeur saturée à 19.8 bar. Préciser la température du système ainsi que son entropie massique et son enthalpie massique.
3. On réalise depuis cet état une détente _isentropique_ jusqu'à une pression de 2.45bar. Tracer sur le diagramme entropique cette transformation et en déduire
    * le caractère diphasé du système dans l'état final
    * la température du système
    * l'entropie massique de la partie liquide et de la partie gazeuse
    * la fraction massique de liquide formé en utilisant le théorème des moments.
````

````{important} __A retenir__

On retiendra qu'on peut définir une entropie massique de changement d'état comme on a définit l'enthalpie massique de changement d'état et que le signe des ces entropies de changement d'état est le même que pour les enthalpies.
````