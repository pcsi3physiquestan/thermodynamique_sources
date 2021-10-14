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
# Exercices d'application

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
