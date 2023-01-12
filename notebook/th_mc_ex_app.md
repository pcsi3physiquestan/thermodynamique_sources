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
# Exercice d'application

## Moteur ditherme

````{admonition} Exercice 
:class: attention

Montrer qu'un moteur ditherme ne peut que fournir de la chaleur à la source froide et en prendre à la source chaude.

````

## Cycle de Joule
On considère une machine thermique constituée d'une mole de gaz parfait (coefficient $\gamma$) subissant le cycle suivant:
1. Une compression isentropique de $P_A = 1.0 \times 10^5 \rm{Pa}$ à $P_B = k P_A$. La température initiale est $T_A = 300 \rm{K}$.
2. Une échauffement isobare jusqu'à une température $T_C = 1000 \rm{K}$
3. Une détente isentropique avec un retour à la pression $P_A$
4. Une refroidissement isobare jusqu'à l'état initial.

Toutes les transformations sont supposées réversibles et $k=10$.

1. Représenter le cycle sur un diagramme de Watt et préciser son caractère moteur ou récepteur.
1. Exprimer $S(T)$ sur une transformation isobare et en déduire le tracer du cycle dans un diagramme entropique $(T,S)$
1. Exprimer les transferts thermiques reçus par le gaz sur chaque transformation. Commenter le signe des chaque transfert thermique.
1. En déduire le travail total W sur le cycle.
1. Déterminer le rendement (si c'est un moteur) ou l'efficacité de la pompe à chaleur (si c'est un récepteur).