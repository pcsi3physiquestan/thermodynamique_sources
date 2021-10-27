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
# Interprétations

## Enoncé de Clausius


Il s'agit de l'énoncé historique qui a conduit Clausius à élaborer le concept d'entropie.


````{important} __Fondamental : Enoncé historique de Clausius__

Considérons deux solides en contact thermique. Le premier est à température $T_f$ et le second à température $T_c > T_f$. Le transfert thermique ne s'effectuer spontanément (sans intervention du milieu extérieur) que du corps chaud vers le corps froid.
````


__Démonstration__  
Les caractéristiques du corps chaud (système $\Sigma_c$) seront notés avec un indice $c$ et celles du corps froid (système $\Sigma_f$) avec un indice $f$. Les grandeurs sans indices concernent le système total $\{\Sigma_f + \Sigma_f\}$

Considérons __le système $\{\Sigma_f + \Sigma_c$}__. Les deux principes s'écrivent appliqué à une transformation infinitésimale:

\begin{align*}
dU = dU_c + dU_f = \delta W + \delta Q = 0\\
dS = dS_c + dS_f = \delta S_e + \delta S_c = \delta S_c \geq 0
\end{align*}
Supposons la transformation réversible (__on calcule une fonction d'état donc on peut choisir un chemin__). Alors le second principe appliqué à chaque système pris séparément s'écrit:

\begin{align*}
dS_c &= \delta S_{ech,c} + \delta S_{c,c} = \frac{\delta Q_c}{T_c}\\
dS_f &= \delta S_{ech,f} + \delta S_{c,f} = \frac{\delta Q_f}{T_f}
\end{align*}
soit avec $\delta Q_c = dU_c + P_c dV_c$ et $\delta Q_f = dU_f + P_f dV_f$ (premier principe appliqué à chaque système pris séparément):

\begin{align*}
dS_c &= \frac{dU_c + P_c dV_c}{T_c}\\
dS_f &= \frac{dU_f + P_f dV_f}{T_f}
\end{align*}
Ces relations ne font intervenir que des variables d'état, elles peuvent donc être généraliser à toute transformation, même non réversible.Il vient donc dans l'équation du second principedu système total:

\begin{equation}
dS = \frac{dU_c}{T_c} + \frac{P_c}{T_c} dV_c + \frac{dU_f}{T_f} + \frac{P_f}{T_f} dV_f \geq 0
\end{equation}
__On a utilisé ici l'extensivité de l'entropie__.

On a montré que $dU_c = - dU_f$ et on travaille à volume constant (sinon il y aurait des travaux des forces de pression et le système ne serait pas isolé) $dV_c = - dV_f$ soit:

\begin{equation}
dS = (\frac{1}{T_f} - \frac{1}{T_c})dU_f + (\frac{P_f}{T_f} - \frac{P_c}{T_c})dV_f \geq 0
\end{equation}
Pour des solides, $dV_f = 0$ soit $(\frac{1}{T_f} - \frac{1}{T_c})dU_f \geq 0$ avec $(\frac{1}{T_f} - \frac{1}{T_c})>0$ si $T_f < T_c$. Il vient donc que $dU_f \geq 0$ soit $\delta Q_f = dU_f - \delta W_f = dU_f \geq 0$ et $\delta Q_c = - \delta Q_f \leq 0$. La chaleur ne peut donc bien passer que du corps chaud au corps froid.


Cette démonstration contient de nombreux points de méthodes extrêmement importants quand on étudie un système thermodynamique.

* Prise de recul: On est souvent amené à prendre l'intégrale des sous-systèmes dans un seul système pour ne pas avoir à étudier les échanges internes.
* Diviser pour mieux régner: A l'inverse, dans les systèmes composés de sous-ensemble on profitera de __l'extensivité__ de l'énergie interne et de l'entropie pour les calculer comme des sommes de grandeurs exprimables en fonction des variables d'état de chaque sous système (impossible pour l'ensemble si T ou P n'est pas identique).
* Fonction d'état: l'utilisation de la propriété de l'entropie (ou de U) d'être une fonction d'état est fondamentale dans de nombreuses démonstration. Elle permet de calculer leur variation sur un chemin choisi (réversible) puis de __généraliser ces expressions puisqu'elles ne dépendent pas du chemin parcouru__.

 

````{admonition} Compléments : Equilibre thermique
:class: hint, dropdown

Remarquons que les expressions précédentes font apparaître $S$ comme une fonction de $U_f$ et $V_f$ (et non plus de $U$ et $V$) et définit les dérivées partielles:

\begin{align*}
{(\frac{\partial S}{\partial U_f})}_{V_f} = \frac{1}{T_f} - \frac{1}{T_c}\\
{(\frac{\partial S}{\partial V_f})}_{U_f} = \frac{P_f}{T_f} - \frac{P_c}{T_c}
\end{align*}
On a vu que pour un système isolé, l'entropie ne pouvait qu'agmenter. Elle va donc atteindre un maximum à l'équilibre. Donc, à l'équilibre les dérivées partielles de $S$ sont nulles sont: $T_c = T_f$. __A l'équilibre, les températures de deux corps en contact thermique seront égales.__  
````

## Enoncé de Thomson


L'énoncé de Thomson est fondamental pour comprendre les limites des machines thermiques. Là où l'énoncé de Clausius s'intéresse à l'évolution interne d'un système et l'homogénéisation des grandeurs intensives, l'énoncé de Thomson traite de la dissymétrie entre le travail et le transfert thermique échangé.


````{important} __Fondamental : Enoncé de Thomson__

Un système en contact avec une seule source de chaleur (thermostat) ne peut, au cours d'un cycle, que recevoir du travail pour fournir de la chaleur.
````


__Démonstration__  
Notons $T_0$ la température de la source de chaleur. Les deux principe appliqué au système sur un cycle s'écrivent (les variations des fonctions d'état sont nulles sur un cycle):

\begin{align*}
\Delta U = 0 = W + Q & \Longrightarrow Q = -W\\
\Delta S = 0 = S_{e} + S_c = \frac{Q}{T_0} + S_c \geq \frac{Q}{T_0} & \Longrightarrow \frac{Q}{T_0} \leq 0
\end{align*}
soit $Q <0$ et $W > 0$.


