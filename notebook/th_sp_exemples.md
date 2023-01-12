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
# Exemples d'application

## Transformations du gaz parfait.

````{admonition} Exercice 
:class: attention

Déterminer la variation d'entropie pour une transformation:

1. isochore
1. isobare
1. isotherme
````
````{topic} Solution

\begin{align*}
\Delta S_{isochore} &= \frac{nR}{\gamma - 1} \ln \frac{T_f}{T_i}\\
\Delta S_{isobare} &= \frac{\gamma nR}{\gamma - 1} \ln \frac{V_f}{V_i}\\
\Delta S_{isotherme} &= nR\ln \frac{V_f}{V_i}
\end{align*}
````

## Compression isotherme

````{admonition} Exercice 
:class: attention

Reprendre l'exercice de compression isotherme de cours du chapitre précédent sur la compression isotherme d'un gaz parfait et faire un bilan entropique pour le gaz dans les deux cas.

````
````{topic} Solution

__Bilan entropique__  

Un bilan entropique consiste à déterminer les valeurs des différentes grandeurs entropiques: variation d'entropie, entropie échangée et entropie créée.
 
* __Variation d'entropie__  
Il s'agit d'un gaz parfait et la compression est isotherme, donc: $\Delta S = - nR \ln \left( 1 + \frac{Mg}{M_0 g + P_0 S}\right)$.

* __Entropie échangée__  
Le gaz échange avec un thermostat à température $\frac{Q}{T_0}$.

* Cas brutal: $S_{ech} = - \frac{Mgh_0}{T_0}$
* Cas quasi-statique: $S_{ech} = - nR \ln \left( 1 + \frac{Mg}{M_0g + P_0 S}\right)$

* __Entropie créée__  
On utilise le second principe appliqué au gaz $S_c = \Delta S - S_{ech}$

Dans le cas quasi-statique, il vient que l'entropie créée est nulle: la transformation est donc __réversible.__  

Cas brutal:

\begin{align*}
S_c &= \frac{Mgh_0}{T_0} - \frac{\left(P_0 S + M_0 g\right)h_0}{T_0}\ln \left( 1 + \frac{Mg}{M_0 g + P_0 S}\right)\\
&= \frac{\left(P_0 S + M_0 g\right)h_0}{T_0}\left(\frac{Mg}{P_0 S + M_0 g} - \ln \left( 1 + \frac{Mg}{M_0 g + P_0 S}\right)\right)\\
&= \frac{\left(P_0 S + M_0 g\right)h_0}{T_0}\left(x - \ln \left( 1 + x\right)\right)\\
\end{align*}
où $ x =\frac{Mg}{P_0 S + M_0 g}$. On pourra étudier la fonction ainsi obtenue et montrer qu'elle est strictement positive pour x différente de 0. La transformation est donc __irréversible.__  

Parmi les causes d'irréversibilité, on peut noter l'inhomogénéité de pression au voisinage de la paroi.

````

### Changement d'état

````{admonition} Mélange eau-glace
:class: attention

Un récipient contenant un mélange de 0,5kg de glace à 273K avec 0,5kg d'eau liquide est placé dans l'air ambiant à la température $T_0 = 293\rm{K}$ sous une pression extérieure de $p_0 = 1 \rm{bar}$. On constante qu'au bout d'une durée $\tau$, on isole le récipient et on observe que 0,2kg de glace a fondu. Faire un bilan entropique du système. Les données numériques sont les mêmes que dans l'exercice précédent.

````
````{topic} Correction

__Bilan entropique__  

La transformation est un changement d'état (partiel) à pression extérieure constante et à température extérieure constante. On suppose que la pression du système ne varie pas de sorte que sa température reste à 273K. On va considérer que les états initiaux et finaux sont des états d'équilibre (on a soustrait le système du contact du thermostat).

La variation d'entropie ne dépend pas du chemin. Elle s'écrit $\Delta S = m_{fondue} \frac{\Delta h_f(T_{fus})}{T_{fus}}$.

La transformation se fait au contact d'un thermostat à $T_0$, l'entropie échangée s'écrit donc $S_{ech} = \frac{Q}{T_0} = \frac{m_{fondue}\Delta h}{T_0}$ (_la dernière expression vient de l'hypothèse d'une transformation monobare entre deux états d'équilibre_).

Le second principe permet de calculer l'entropie crée:

\begin{align*}
S_c &= \Delta S - S_{ech}\\
&= \Delta h_{f}(T_{fus}) \left(\frac{1}{T_{fus}} - \frac{1}{T_0}\right) > 0
\end{align*}
L'évolution est irréversible à cause de l'inhomogénéité de température.
 
````

