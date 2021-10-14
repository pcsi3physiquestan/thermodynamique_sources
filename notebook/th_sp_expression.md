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

## Entropie échangée: Expression

### Entropie échangée: Expression générale


__Entropie échangée - Expression générale (pas à connaître)__  
L'entropie échangée a pour expression générale:

\begin{equation}
\delta S_{ech} = \iint_{M \in \textrm{frontiere}} \frac{\delta Q_{dS}}{T_{dS}}
\end{equation}
$T_{dS}$ est la température à la surface $dS$ et $\delta Q_{dS}$ le transfert thermique qui se produit à travers la surface élémentaire. L'expression générale n'est pas à connaître, mais les cas particuliers le sont.


````{dropdown} Remarque

Cette expression n'est pas à connaître mais elle montre le fort lien entre entropie échangée et transfert thermique.
````

### Entropie échangée: Cas d'une transformation adiabatique

````{admonition} Fondamental : Entropie échangée et transformation adiabatique
:class: attention

L'entropie échangée lors d'une transformation adiabatique est nulle.
````

````{dropdown} Remarque

Une conséquence directe est que l'entropie S ne peut qu'__augmenter lors d'une transformation adiabatique.__ Elle sera donc maximale à l'équilibre lors d'une telle transformation.
````

### Entropie échangée et transformation réversible

````{admonition} Fondamental : Entropie échangée - Cas d'une transformatino réversible
:class: attention

Dans une transformation réversible, l'entropie échangée s'écrit $\delta S_{ech} =\frac{\delta Q}{T}$ où $\delta Q$ est le transfert thermique global échangé durant le temps dt de la transformation et T __la température du système.__  
````


__Démonstration (pas à connaître)__  
Si la transformation est réversible, le système est en équilibre thermique à chaque instant et on peut définir sa température T qui est la même en chaque point, notamment à sa surface. La température sort alors de l'intégrale qui donne le transfert thermique global.


### Entropie échangée: Contact avec un thermostat

````{admonition} Définition : Thermostat
:class: tip

Un thermostat (ou source de chaleur) est un système de capacité thermique infinie, n'échangeant pas de travail mais uniquement du transfert thermique avec l'extérieur. Il est caractérisé par sa température qui ne varie pas. Son évolution est considérée réversible.

````

````{admonition} Fondamental : Entropie échangée avec un thermostat
:class: attention

Si un système fermé ne peut échanger de chaleur qu'avec un thermostat à température $T_{\textrm{thermostat}}$, l'entropie échangé est: $\delta S_{ech} = \frac{\delta Q}{T_{\textrm{thermostat}}}$ où $\delta Q$ la chaleur totale reçue du thermostat.
````

## Entropie: Expression

### Entropie: Généralités


__Entropie: une fonction d'état__  
L'entropie est une fonction d'état. Cela signifie

* que sa variation dépend de l'état initial et de l'état final mais __pas du chemin parcouru__. On pourra donc __choisir le chemin parcouru pour la calculer__. L'expression trouvée __se généralisera à toutes les transformations possédant le même état initial et final__.
* que sa valeur dans un état donné est fonction d'autres variables d'état qu'on aura choisi (par exemple, on peut choisir d'exprimer $S(U,V)$). On peut la choisir comme variable et exprimer les autres grandeurs en fonction de S (écrire par exemple U(S,V) ou H(S,P), l'écriture de U(S,V) permet, rappelons le de définir la température et la pression "thermodynamique"). 


On peut aussi voir l'entropie comme une variable d'état comme l'est le volume ou la pression. A nombre de moles fixées, on peut alors considérer (pour un fluide) 2 variables d'état indépendantes: l'entropie et le volume.

Toute fonction d'état est alors fonction de S et V: l'énergie interne notamment U(S,V) et sa différentielle: 

\begin{equation}
dU = \frac{\partial U}{\partial S}_V dS + \frac{\partial U}{\partial V}_S dV
\end{equation}
Cette relation amène la définition thermodynamique de la température et de la pression vues précédemment. On obtient alors __l'identité thermodynamique:__  

\begin{equation}
dU = TdS - PdV
\end{equation}

### Entropie des gaz parfaits

````{admonition} Fondamental : Entropie des gaz parfaits
:class: attention

Pour un gaz parfait, l'entropie s'écrit:

\begin{align*}
S &= S_0 + \frac{nR}{\gamma-1}\ln \left(\frac{TV^{\gamma-1}}{T_0 V_0^{\gamma-1}}\right)\\
&= S_0 + \frac{nR}{\gamma-1}\ln \left(\frac{T^{\gamma}P^{1-\gamma}}{T_0^{\gamma} P_0^{1-\gamma}}\right)\\
&= S_0 + \frac{nR}{\gamma-1}\ln \left(\frac{PV^{\gamma}}{P_0 V_0^{\gamma}}\right)
\end{align*}
où $S_0$ est l'entropie du gaz à $(T_0,P_0,V_0)$
````


__Démonstration - Méthode 1__  
On utilise l'identité thermodynamique:

\begin{align*}
dU &= TdS - PdV\\
dS &= C_v \frac{dT}{T} + nR \frac{dV}{V}\\
\int_{i}^{f}dS &= \frac{nR}{\gamma-1}\int_{i}^{f}\frac{dT}{T} + nR \int_{i}^{f}\frac{dV}{V}\\
\Delta S &= \frac{nR}{\gamma-1} \ln \frac{T_f}{T_i} + nR\ln {\left(\frac{V_f}{V_i}\right)}\\
\Delta S &= \frac{nR}{\gamma-1} \ln \frac{T_f V_f^{\gamma-1}}{T_i V_i^{\gamma-1}}\\
\end{align*}


__Démonstration - Méthode 2__  
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


````{admonition} Fondamental : Lois de Laplace
:class: attention

Lors d'une transformation isentropique, un gaz parfait suit les lois de Laplace.

Lorsqu'un gaz parfait suit les lois de Laplace, sa transformation est isentropique.

La preuve de ces deux propriétés découle directement de l'expression de l'entropie.
````

### Entropie: Phases condensées

````{admonition} Fondamental : Entropie des phases condensées
:class: attention

Pour des solides et des fluides peu dilatables et peu compressibles, on peut écrire:

\begin{equation}
dS \approx \frac{dU}{T} \approx \frac{dH}{T} \approx C \frac{dT}{T}
\end{equation}
````


__Démonstration__  
On s'entraînera à le démontrer en suivant le même principe de raisonnement que pour le gaz parfait. On fera __très attention à la rédaction__.


## Entropie créée


Il n'existe pas d'expression permettant de calculer l'entropie créée sinon le second principe.

A l'image du transfert thermique, on calculera l'entropie créée en utilisant la relation $\Delta S = S_{ech} + S_c$.

L'autre cas est le cas d'une transformation réversible où l'on sait que l'entropie créée est nulle.


