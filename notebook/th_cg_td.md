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
# Travaux dirigés: Changements d'état

## Etat final d'un système

````{admonition} Exercice 
:class: attention

Dans une enceinte dont les parois sont parfaitement adiabatiques on introduit à la pression atmosphérique une masse $m_1 = 0.01 \rm{kg}$ de glace à $T_1 = - 8 \rm{^{\circ}C}$ et une masse $m_2 = 0.1 \rm{kg}$ d'eau liquide à $T_2 = 15 \rm{^{\circ}C}$.

Données numériques: Chaleur latente de fusion la glace à $0 \rm{^{\circ}C}$: $L_f = 334.4 \rm{J.g^{-1}}$, capacités thermiques massiques de la glace: $c_1 = 2.1 \rm{kJ.K^{-1}.kg^{-1}}$, de l'eau liquide $c_2 = 4.2 \rm{kJ.K^{-1}.kg^{-1}}$.

1. Décrire l'état final
1. Calculer la variation d'entropie totale.


````

## Fonte de glace

````{admonition} Exercice 
:class: attention

Un cylindre de $1 \rm{dm^{2}}$ de section est fermé par un piston situé à $50\rm{cm}$ du fond. Il contient de l'air sous une pression de $75\rm{cm}$ de mercure. Il est immergé dans un calorimètre isobare contenant de l'eau et de la glace. On enfonce le piston de $20\rm{cm}$ d'une façon réversible. Calculer la masse de glace qui a fondu.

Données: chaleur latente de fusion de la glace à $1 \rm{bar}$: $L_f = 334.4 \rm{J.g^{-1}}$; 76cm de mercure = 101325 Pa.

````

## Vaporisation réversible ou irréversible

````{admonition} Exercice 
:class: attention

On vaporise une masse de m=1g d'eau liquide des deux manières suivantes:

* la masse m et enfermée à $100 \rm{^{\circ}C}$ sous la pression atmosphérique, dans un cylindre fermé par un piston. Par déplacement lent du piston, on augmente le volume à température constante et on s'arrête dès que toute l'eau est vaporisée. Le volume est alors égal à $V=1,67\rm{L}$.
* on introduit rapidement la masse m d'eau liquide initialement à $100 \rm{^{\circ}C}$ dans un récipient fermé de même température, de volume $1,67\rm{L}$ initialement vide. La température finale est à $100 \rm{^{\circ}C}$.


1. Calculer $Q_{thermostat}$ et les variations d'énergie interne, d'enthalpie et d'entropie de l'eau dans chaque cas.
1. Calculer l'entropie crée lors du processus irréversible.


Données numériques: Enthalpie massique de vaporisation de l'eau est $L_V = 2.25 \times 10^6 \rm{J.kg^{-1}}$.

````

## Mélange eau-gaz

````{admonition} Exercice 
:class: attention

On étudie les transformations thermodynamiques d'un gaz parfait auquel on a ajouté $1\rm{g}$ d'eau. Dans l'état initial A, le volume du mélange gaz et eau est $V_A = 0.1 \rm{m^{3}}$, la température a pour valeur $27 \rm{^{\circ}C}$ et la pression $p_A = 10^5 \rm{Pa}$. On admet que, lorsqu'il existe de l'eau liquide, son volume peut être négligé. On suppose de plus que la vapeur d'eau sèche se comporte comme un gaz parfait.

1. Montrer que, dans l'état A, toute l'eau est vaporisée. On rappelle que l'eau est sous forme de gaz si sa pression partielle est inférieure à la pression de vapeur saturante.
1. On effectue une compression isotherme réversible AB telle que le volume final, dans l'état B soit $V_B = 0.01 \rm{m^{3}}$. Montrer que dans l'état B, une partie de l'eau est sous forme liquide et calculer la fraction $x_l$ de l'eau dans l'état liquide.
1. Calculer le travail et la chaleur reçus par le système dans cette transformation ainsi que la variation d'énergie interne et d'entropie.


Données: $M_{H2O} = 18 \rm{g.mol^{-1}}; p_{sat,A}=3.70 \times 10^3 \rm{Pa}; L_{vap} = 2.45 \times 10^{6} \rm{J.kg^{-1}}; C_{Vm,gaz} = C_{Vm,H20 gaz} = 5/2 R$

````

## Surfusion

````{admonition} Exercice 
:class: attention

Soit un composé dont la température de solidifcation est $\theta_0 = 44 \rm{^{\circ}C}$. On place le liquide à la température $\theta < \theta_0$, sans solidification. On produit alors une petite perturbation et le liquide en surfusion se solidifie.

Donner la température finale du solide pour $\theta = 25 \rm{^{\circ}C}$ et $\theta = -20 \rm{^{\circ}C}$.

On donne $L_{fusion} = 63 \rm{J.g^{-1}}; C_S = 1.03 \rm{J.K^{-1}.g^{-1}}; C_L = 1.17 \rm{J.K^{-1}.g^{-1}}$.

````

