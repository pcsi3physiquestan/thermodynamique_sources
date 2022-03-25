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
# Second principe: Travaux dirigés

## Compression d'un gaz

````{admonition} Exercice 
:class: attention

Un gaz parfait occupe un volume $V_1 = 10 \rm{L}$ à une température $T_1 = 273 \rm{K}$ et sous une pression $P_1 = 10 \rm{bar}$. La pression tombe __brusquement__ de la valeur $P_1$ à la valeur $P_2 = 1 \rm{bar}$. La capacité thermique molaire à volume constant est $C_{Vm} = \frac{5}{2}R$.

1. Déterminer l'état final du gaz. On précisera les hypothèses faites sur la transformation.
1. Calculer la variation d'entropie.


````

## Sens d'un cycle monotherme

````{admonition} Exercice 
:class: attention

Une mole de gaz parfait ($\gamma=1,4$) subit la succession de transformations suivante:

* détente isotherme réversible de $P_A=2\rm{bar}$ et $T_A = 300 \rm{K}$ jusqu'à $P_B =1\rm{bar}$.
* évolution isobare jusqu'à $V_C = 20,5 \rm{L}$ toujours en restant en contact avec le thermostat à $T_A$.
* compression adiabatique réversible jusqu'à l'état A.


1. Représenter ce cycle en diagramme (P,V). S'agit-il d'un cycle moteur ou récepteur?
1. Calculer la température en C, le travail $W_{BC}$ et le transfert thermique $Q_{BC}$ reçus par le gaz au cours de la transformation BC.
1. En déduire l'entropie échangée avec le thermostat ainsi que l'entropie créée sur le cycle.
1. Calculer la valeur numérique de l'entropie créée au cours d'un cycle. Le cycle proposé est-il réalisable? Pouvait-on le prévoir? Le cycle inverse l'est-il?


````

## Détente irréversible d'un gaz parfait

````{admonition} Exercice 
:class: attention

Soit le dispositif de la figure suivante. Les parois et le piston sont calorifugées. La paroi interne est fixe et laissent passer la chaleur. Elle est percée d'un trou fermé par une fenêtre amovible. La pression extérieure est $P_0 = 1 \rm{bar}$. Initialement le volume A est rempli d'un gaz parfait ($P_0 = 1 \rm{bar}; T_0 = 300 \rm{K}; n = 1 \rm{mol}$) et le volume B est vide. Le rapport des capacités thermiques du gaz $\gamma$ vaut 1,4.

```{figure} ./images/Thermodynamique_TD4_EX6_1.jpg
:name: fig_278
:align: center

```

1. On ouvre la fenêtre. Décrire qualitativement ce qui se passe suivant la taille de l'enceinte B. En déduire l'existence d'un volume critique de B: $V_C$ que l'on ne pas de calculer pour l'instant.
1. On suppose $V_B < V_C$.
    1.   On appelle $V_1$ le volume final occupé par le gaz. Déterminer le travail reçu par le gaz en supposant le piston sans passe..
    1.   Déterminer l'état final du gaz $(P_1, V_1, T_1)$ en fonction de $P_0, V_A$ et $V_B$.
    1.   Calculer l'entropie créée. Conclure. Quelle est la cause de la création d'entropie?
    1.   Déterminer $V_C$. Effectuer l'application numérique.
1. Reprendre les questions précédentes dans le cas $V_B > V_C$.
1. On suppose maintenant que seul le piston est adiabatique et que le dispositif est maintenu à $T_0$ par un thermostat. On appelle $V_{C1}$ le nouveau volume critique.
    1.   Déterminer le nouveau volume critique $V_{C1}$.
    1.   Calculer l'entropie créée quand $V_B < V_{C1}$.



````
