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

# Expression des grandeurs

## Entropie échangée

### Expression générale (en ligne)

````{sidebar} Remarque

Cette expression n'est pas à connaître mais elle montre le fort lien entre entropie échangée et transfert thermique.
````
````{topic} __Entropie échangée - Expression générale (pas à connaître)__  
L'entropie échangée a pour expression générale:

$$
\delta S_{ech} = \iint_{M \in \textrm{frontiere}} \frac{\delta Q_{dS}}{T_{dS}}
$$
$T_{dS}$ est la température à la surface $dS$ et $\delta Q_{dS}$ le transfert thermique qui se produit à travers la surface élémentaire. L'expression générale n'est pas à connaître, mais les cas particuliers le sont.
````

### Cas d'une transformation adiabatique

````{sidebar} Maximum d'entropie
Une conséquence directe est que l'entropie S (égale alors à la seule entropie créée) ne peut qu'__augmenter lors d'une transformation adiabatique.__ Elle sera donc maximale à l'équilibre lors d'une telle transformation.
````
````{important} __Entropie échangée et transformation adiabatique__
L'entropie échangée lors d'une transformation adiabatique est nulle.
````

### Transformation réversible

````{important} __Entropie échangée - Cas d'une transformation réversible__

Dans une transformation réversible, $S_{ech} = \Delta S$ puisque $S_{c} = 0$.
````

````{important} __Adiabatique réversible et isentropique__

Il vient (second principe):
* Qu'une transformation adiabatique ET réversible est nécessairement isentropique.
* Qu'une transformation isentropique ET réversible est nécessairement adiabatique.
* ... Qu'une transformation isentropique ET adiabatique est nécessairement réversible.

````

### Contact avec un thermostat

````{important} __Thermostat__

Un thermostat (ou source de chaleur) est un système de capacité thermique infinie, n'échangeant pas de travail mais uniquement du transfert thermique avec l'extérieur. Il est caractérisé par sa température qui ne varie pas. Son évolution est considérée réversible.
````

````{margin}
Attention, il s'agit bien d'un thermostat, donc $T_{\textrm{thermostat}}$ doit être __constant__.

````
````{important} __Entropie échangée avec un thermostat__

Si un système fermé ne peut échanger de chaleur qu'avec un thermostat à température $T_{\textrm{thermostat}}$, l'entropie échangé est: $S_{ech} = \frac{Q}{T_{\textrm{thermostat}}}$ où $Q$ la chaleur totale reçue du thermostat.
````

## Entropie

### Généralités

````{topic} __Entropie: une fonction d'état__  
L'entropie est une fonction d'état. Cela signifie

* que sa variation dépend de l'état initial et de l'état final mais __pas du chemin parcouru__. On pourra donc __choisir le chemin parcouru pour la calculer__. L'expression trouvée __se généralisera à toutes les transformations possédant le même état initial et final__.
* que sa valeur dans un état donné est fonction d'autres variables d'état qu'on aura choisi (par exemple, on peut choisir d'exprimer $S(U,V)$). On peut la choisir comme variable et exprimer les autres grandeurs en fonction de S (écrire par exemple U(S,V) ou H(S,P), l'écriture de U(S,V) permet, rappelons le de définir la température et la pression "thermodynamique"). 


On peut aussi voir l'entropie comme une variable d'état comme l'est le volume ou la pression. A nombre de moles fixées, on peut alors considérer (pour un fluide) 2 variables d'état indépendantes: l'entropie et le volume.
````

````{margin}
L'identité thermodynamique permet en l'inversant d'obtenir une expression de dS puis de S.
````
````{important} __Identité thermodynamique__

En considérant l'énergie interne comme une fonction de $S$ et $V$ ($U(S,V)$) et sa différentielle s'écrit: 

$$
dU = \frac{\partial U}{\partial S}_V dS + \frac{\partial U}{\partial V}_S dV
$$
Cette relation amène la définition thermodynamique de la température et de la pression vues précédemment. On obtient alors __l'identité thermodynamique:__  

$$
dU = TdS - PdV
$$
````

### Entropie des gaz parfaits

````{important} __Entropie des gaz parfaits__

Pour un gaz parfait, l'entropie s'écrit:

\begin{align*}
S &= S_0 + \frac{nR}{\gamma-1}\ln \left(\frac{TV^{\gamma-1}}{T_0 V_0^{\gamma-1}}\right)\\
&= S_0 + \frac{nR}{\gamma-1}\ln \left(\frac{T^{\gamma}P^{1-\gamma}}{T_0^{\gamma} P_0^{1-\gamma}}\right)\\
&= S_0 + \frac{nR}{\gamma-1}\ln \left(\frac{PV^{\gamma}}{P_0 V_0^{\gamma}}\right)
\end{align*}
où $S_0$ est l'entropie du gaz à $(T_0,P_0,V_0)$
````

````{important} __Démonstration - Méthode 1__  

On utilise l'identité thermodynamique:

\begin{align*}
dU &= TdS - PdV\\
dS &= C_v \frac{dT}{T} + nR \frac{dV}{V}\\
\int_{i}^{f}dS &= \frac{nR}{\gamma-1}\int_{i}^{f}\frac{dT}{T} + nR \int_{i}^{f}\frac{dV}{V}\\
\Delta S &= \frac{nR}{\gamma-1} \ln \frac{T_f}{T_i} + nR\ln {\left(\frac{V_f}{V_i}\right)}\\
\Delta S &= \frac{nR}{\gamma-1} \ln \frac{T_f V_f^{\gamma-1}}{T_i V_i^{\gamma-1}}\\
\end{align*}
````

````{sidebar} Choix du chemin
Cette méthode est fondamentale dans la démonstration de nombreuses propriétés des fonctions d'état: on peut choisir le chemin de calcul, puisque c'est une fonction d'état.
````
````{important} __Démonstration - Méthode 2__  

Considérons la variation d'entropie sur une transformation infinitésimale réversible. __L'entropie étant une fonction d'état, la variation calculée se généralisera à toute transformation ce qui nous donnera une expression générale de la variation d'entropie__. Le second principe s'écrit:

\begin{align*}
dS &= \delta S_e + \delta S_c \\
&= \frac{\delta Q}{T} + 0 \\
&= \frac{dU - \delta W}{T} \\
&= \frac{dU + P dV}{T}\\
&= C_V \frac{dT}{T} + nR \frac{dV}{V}\\
&= \frac{nR}{\gamma-1} \frac{dT}{T} + nR \frac{dV}{V}
\end{align*}
soit en intégrant l'expression donnée $S(T,V)$. En utilisant la loi des gaz parfaits, on trouve les deux autres.
````


````{important} __Lois de Laplace__

* Lors d'une transformation isentropique, un gaz parfait suit les lois de Laplace (trivial à partir de l'expression de S).
* Lorsqu'un gaz parfait suit les lois de Laplace, sa transformation est isentropique (idem).
````

### Phases condensées

````{important} __Entropie des phases condensées__

Pour des solides et des fluides peu dilatables et peu compressibles, on peut écrire:

$$
dS \approx \frac{dU}{T} \approx \frac{dH}{T} \approx C \frac{dT}{T}
$$

_Cette expression s'obtient directement de l'identité thermodynamique sous l'hypothèse $dP = 0$ (peu dilatables) et $dV = 0$ (peu compressibles)._
````

### Changement d'état

````{important} __Entropie massique de changement d'état__
On appelle entropie massique de changement d'état à la pression P, la variation d'entropie $\Delta s$ du corps pur au cours du changement d'état complet d'un kilogramme du corps pur considéré à la pression donnée.

__Elle correspond à la différence d'entropie massique entre la phase finale pure et la phase initiale pure dans les mêmes conditions de pression:__

\begin{equation}
\Delta s_{ph1 \to ph2} (T_{sat}) = s_{ph2}(T_{sat}) - s_{ph1} (T_{sat})
\end{equation}
````

````{margin}
On observera que le signe de l'entropie de changement d'état est le même que celui de l'enthalpie de changement d'état.
````
````{important} __Relation entropie-enthalpie de changement d'état__

\begin{equation}
\Delta s_{ph1 \to ph2} (T_{sat}) = \frac{\Delta h_{ph1 \to ph2} (T_{sat})}{T_{sat}}
\end{equation}
````

````{important} Démonstration
On peut réécrire l'identité thermodynamique avec l'enthalpie:
\begin{align*}
  dh &= du + dPv\\
  &= du + Pdv + vdP\\
  &= Tds - Pdv + Pdv + vdP\\
  &= Tds + vdP
\end{align*}

Lors d'un changement d'état seul, si la température initiale et finale sont les mêmes, alors les pressions initiale et finale sont aussi les mêmes. On peut donc imaginer un chemin (S est une fonction d'état) où la transformation est isobare avec les mêmes états final et initial. Il vient $dh = T ds$ soit en intégrant ($T = T_{sat} = cste$):

\begin{equation}
\Delta s_{ph1 \to ph2} (T_{sat}) = \frac{\Delta h_{ph1 \to ph2} (T_{sat})}{T_{sat}}
\end{equation}
````

## Entropie créée

__Il n'existe pas d'expression permettant de calculer l'entropie créée sinon le second principe.__ A l'image du transfert thermique, on calculera l'entropie créée en utilisant la relation $\Delta S = S_{ech} + S_c$.

_L'autre cas est le cas d'une transformation réversible où l'on sait que l'entropie créée est nulle._
