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
# Travaux dirigés

## Etude d'un réfrigérateur

````{admonition} Exercice 
:class: attention

Un réfrigérateur à absorption est une machine frigorifique tritherme sans échange de travail avec l'extérieur. L'énergie est fournie sous forme thermique et à haute température à un bouilleur à $T_0$. Le condenseur est en contact thermique avec le milieu extérieur de température $T_1 < T_0$. L'évaporateur est en contact thermique avec la source de température $T_2 < T_1$. L'énergie est prelevé à la source froide au niveau de l'évaporateur. Définir et calculer l'efficacité frigorifique maximale, fonction des trois températures $T_0, T_1$ et $T_2$.

````

## Pompe à chaleur

````{admonition} Exercice 
:class: attention

Un fluide décrit des cycles réversibles du type pompe à chaleur entre une source froide de température constante $T_0 = 12 \rm{^{\circ}C}$ et un réservoir d'une tonne d'eau, dont la température initiale est $T_0 = 12 \rm{^{\circ}C}$, ne pouvant échanger de la chaleur qu'avec ce fluide. La capacité thermique massique de l'eau est $c = 4.18 \rm{kJ.kg^{-1}.K^{-1}}$.

1. Déterminer le travail $W$ fourni par le milieu extérieur quand l'eau du réservoir a atteint la température $47 \rm{^{\circ}C}$.
1. Quelle aurait été l'élévation de température si la même énergie avait été fournie directement par une résistante chauffante?


````

## Optimisation du chauffage d'un local

````{admonition} Exercice 
:class: attention

On souhaite maintenir la température d'un local à $\theta_1 = 20 \rm{^{\circ}C}$ alors que la température extérieure est $\theta_0 = 0 \rm{^{\circ}C}$. L'énergie thermique nécessaire est de $Q_c=32\rm{MJ}$ par heure. Par un système de chauffage central direct, on brûle $a$ litres de fuel par jours ($a$ est de l'ordre de 25 litres, sa valeur exacte n'intervient pas dans l'exercice).

1. On utilise une pompe à chaleur fonctionnant réversiblement entre le local et l'extérieur, le fuel servant à faire fonctionner le moteur de cette pompe, comme nous le décrit la question. Calculer l'efficacité de la pompe à chaleur. En déduire la puissance consommée par cette pompe.


Deux conseillers proposent chacun un dispositif qu'ils déclarent thermodynamiquement plus avantageux que le chauffage central:

* dispositif du conseiller 1: les $a$ litres de fuel sont brûlés, l'énergie thermique $Q$ récupérée permet d'assurer la vaporisation de l'eau d'une chaudière auxiliaire à la température $\theta_3 = 210 \rm{^{\circ}C}$ qui sert de source chaude à un moteur ditherme réversible dont la source froide est le local le travail fourni servant à faire fonctionner la pompe à chaleur étudiée à la question précédénte.
* dispositif du conseiller 2: le principe est le même mais la chaudière auxiliaire est à la température $\theta_4 = 260 \rm{^{\circ}C}$ et le moteur fonctionne entre cette chaudière et l'air extérieur.


Dans les deux cas, on suppose que toute l'énergie thermique $Q$ obtenue par combustion du fuel est fournie par la chaudière auxiliaire au fluide du moteur.

2. Dans les deux cas, calculer la durée $\Delta t$ pendant lequel le chauffage sera assuré avec les a litres de fuel.
2. Lequel de ces deux systèmes est le plus économique? Le système le plus économique tire-t-il son avantage de la température à laquelle fonctionne la chaudière auxiliaire ou cet avantage se maintient-il pour $\theta_3 = \theta_4$? Expliquer.
2. La durée de chauffage, pour une quantité de fuel donnée, augmentant avec la température de la chaudière auxiliaire, un troisième conseiller prétend qu'il pourra, en utilisant le même dispositif, augmenter la durée du chauffage. A-t-il tort ou raison? Pourquoi?


````

