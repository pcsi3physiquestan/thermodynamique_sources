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
````{dropdown} Démonstration

 


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
````{dropdown} Démonstration

 

__Bilan entropique__  

Un bilan entropique consiste à déterminer les valeurs des différentes grandeurs entropiques: variation d'entropie, entropie échangée et entropie créée.
 


__Variation d'entropie__  
Il s'agit d'un gaz parfait et la compression est isotherme, donc: $\Delta S = - nR \ln \left( 1 + \frac{Mg}{M_0 g + P_0 S}\right)$.



__Entropie échangée__  
Le gaz échange avec un thermostat à température $\frac{Q}{T_0}$.

* Cas brutal: $S_{ech} = - \frac{Mgh_0}{T_0}$
* Cas quasi-statique: $S_{ech} = - nR \ln \left( 1 + \frac{Mg}{M_0g + P_0 S}\right)$




__Entropie créée__  
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

