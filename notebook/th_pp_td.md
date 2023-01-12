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

## Compression et détente successives

````{admonition} Exercice 
:class: attention

On étudie les compressions et détentes successives d'un gaz parfait ($\gamma=1,4$). On suppose que les transformations sont quasistatiques.

Le gaz subit une compression isotherme (température $T_0 = 273\rm{K}$) de $P_0 = 1 \rm{bar}$ à $P_1 = 20 \rm{bar}$ puis une détente adiabatique jusqu'à $P_0$.

1. Représenter sur un diagramme de Watt les deux transformations. Justifier sans calcul que le gaz se refroidit.
1. Calculer la température $T_1$ après les deux transformations.
1. Calculer la variation d'énergie interne en fonction de $T_0$ et $P_0, P_1$. Calculer le travail W et le transfert thermique Q reçus par le gaz. Effectuer les applications numériques pour une mole de gaz.
1. On recommence l'opération. Calculer $T_2$ puis $T_n$ après n séries de transformations.


````

## Etude d'un cycle

````{admonition} Exercice 
:class: attention

On impose à une mole de gaz parfait les transformations réversibles suivantes ($V_2 > V_1 $ et $T_2 > T_1$).

1. isochore (1) de l'état $A(V_1,T_1)$ à l'état $B(V_1,T_2)$
1. isotherme (2) de l'état $B(V_1,T_2)$ à l'état $C(V_2,T_2)$
1. isochore (3) de l'état $C(V_2,T_2)$ à l'état $D(V_2,T_1)$
1. isotherme (4) de l'état $D(V_2,T_1)$ à l'état $A(V_1,T_1)$


1. Tracer le cycle des transformations dans un diagramme (P,V). Repérer les états A,B,C et D. En déduire le caractère moteur ou récepteur du système.
1. Calculer: la pression $P_1$ dans l'état A, la variation d'énergie interne au cours du cycle, le travail pour les transformations (1) et (3) puis pour les transformations (2) et (4), le travail total W et le transfert thermique pour le cycle.
1. Calculer le rendement du cycle $\rho = \frac{W_2}{Q_1 + Q_2}$


````

## Chauffage d'une double enceinte

````{admonition} Exercice 
:class: attention

On étudie le système représenté ci-après supposé dans un état d'équilibre au départ. On suppose que les enceintes contiennent des gaz parfaits, que la paroi entre le deux enceintes est mobile et que l'enceinte A est parfaitement calorifugée. Le thermostat impose à B sa température à l'équilibre. On note $\gamma = C_P / C_V$. On chauffe l'enceinte A jusqu'à la température $T_1$ par la résistance chauffante. Les transformations seront considérées quasistatiques.

```{figure} ./images/double_enceinte_chauffage.jpg
:name: fig_276
:align: center

```

1. Déterminer le volume et pressions finales des deux enceintes.
1. Calculer la variation d'énergie interne de chacune des deux enceintes ainsi que celle de l'ensemble de deux enceintes.
1. Quelle est la nature de la transformation de l'enceinte B? En déduire le calcul du travail échangé entre les deux enceintes et le transfert thermique $Q_1$ entre l'enceinte B et le thermostat.
1. Déterminer le transfert thermique $Q_2$ fourni par la résistance.


````

## Enceinte et ressort

````{admonition} Exercice 
:class: attention

On considère le dispositif de la figure ci-parès: un piston calorifugé est mobile dans un cylindre calorifugé horizontal (section $S = 500 \rm{cm^{2}}$). Le compartiment de gauche contient $0,01\rm{mol}$ de gaz parfait ($\gamma = 1,4$) dans le compartiment de droite règne un vide poussé. Le piston est relié au point fixe O par un ressort de raideur $k = 10^5 \rm{N.m^{-1}}$.

```{figure} ./images/double_enceinte_ressort.jpg
:name: fig_277
:align: center

```

1. Le piston est coincé par une butée et le ressort n'est pas tendu, la pression $P_0 = 0,214 \rm{bar}$ et la température $T_0 = 290 \rm{K}$. Calculer $V_0$.
1. On supprime la butée. Le système évolue vers un nouvel état d'équilibre. Déterminer l'allongement $x_F$ du ressort, le volume $V_F$ occupé par le gaz, sa température $T_F$ et sa pression finale $P_F$.
````


## Surfusion

````{admonition} Exercice 
:class: attention

Soit un composé dont la température de solidifcation est $\theta_0 = 44 \rm{^{\circ}C}$. On place le liquide à la température $\theta < \theta_0$, sans solidification. On produit alors une petite perturbation et le liquide en surfusion se solidifie.

Donner la température finale du solide pour $\theta = 25 \rm{^{\circ}C}$ et $\theta = -20 \rm{^{\circ}C}$.

On donne $L_{fusion} = 63 \rm{J.g^{-1}}; C_S = 1.03 \rm{J.K^{-1}.g^{-1}}; C_L = 1.17 \rm{J.K^{-1}.g^{-1}}$.

````

## Fonte de glace

````{admonition} Exercice 
:class: attention

Un cylindre de $1 \rm{dm^{2}}$ de section est fermé par un piston situé à $50\rm{cm}$ du fond. Il contient de l'air sous une pression de $75\rm{cm}$ de mercure. Il est immergé dans un calorimètre isobare contenant de l'eau et de la glace. On enfonce le piston de $20\rm{cm}$ d'une façon réversible. Calculer la masse de glace qui a fondu.

Données: chaleur latente de fusion de la glace à $1 \rm{bar}$: $L_f = 334.4 \rm{J.g^{-1}}$; 76cm de mercure = 101325 Pa.

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