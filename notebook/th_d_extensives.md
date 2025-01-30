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
# Variables extensives

_Le volume, la quantité de matière, la masse, l'entropie, l'énergie totale et l'énergie interne (on reviendra sur ces grandeurs par la suite) sont toutes des grandeurs extensives._

````{topic} Bilan d'une grandeur extensive
On rappelle que la variation d'une grandeur d'état X d'un système s'écrit $\Delta X$.

* Dans le cas d'une grandeur extensive, la variation de X a deux origines possibles: la quantité $X_e$ échangée avec l'extérieur et la quantité $X_c$ créée à l'intérieur du système. On peut toujours écrire le bilan d'un grandeur extensive X lors d'une transformation finie: $\Delta X = X_e + X_c$ ($X_e$ est la grandeur échangée de l'extérieur __vers__ le système).
* Dans le cas d'une variation infinitésimale, on écrira ce bilan: $dX = \delta X_c + \delta X_e$. L'utilisation de la notation $\delta$ est fondamentale pour les __termes d'échange et de création__: il signifie que ces deux termes __dépendent du chemin parcouru pour passer de l'état initial à l'état final alors que la variation dX ne dépend que des données de l'état initial et de l'état final et non du chemin parcouru lors de la transformation.__  

Ce bilan est général à toutes les grandeurs d'état extensives et notamment l'énergie et l'entropie. Nous verrons qu'une des caractéristiques des premier et second principe de la thermodynamique consiste à caractériser ces termes d'échanges et de création.
````

## Energie
### Energie interne (en ligne)


````{important} Energie interne
```{figure} ./images/qr_code/qr_thermo_u.png
:name: qr_thermo_u
:width: 150px
:align: right
:target: th_d_echelle.html#energie-interne-en-ligne
```
Le premier principe - que nous verrons par la suite - définit une grandeur appelée énergie interne U qui est une __grandeur d'état extensive.__
````

````{margin}
Il s'agit d'une interprétation de l'énergie interne qui nous permettra de la calculer dans certains cas simples mais il ne s'agit pas d'une définition.
````
````{topic} Energie totale et énergie interne

__Composantes énergétiques :__  
Prenons un système composé de particules (on les supposera identiques même si cela n'a que peu d'importance), nous supposerons pour simplifier ici qu'il n'y a pas de mouvement d'ensemble à l'intérieur du système: le centre d'inertie a un mouvement et les particules ont un mouvement chaotique dans le référentiel du centre d'inertie. Par définition, l'énergie du système est la somme de l'énergie de chaque particule. Pour le système complet, on peut distinguer plusieurs types d'énergie qu'on distinguera comme étant microscopique ou macroscopique.
* Les énergies cinétiques liés aux mouvement globaux du système:
* L'énergie cinétique de translation macroscopique, assimilable à l'énergie cinétique qu'aurait le centre d'inertie affecté de toute la masse.
* L'énergie cinétique de rotation macroscopique associée à la rotation global du solide. Si le système est à l'équilibre, cette composante est forcément nulle.
> Ces composantes sont associées à des mouvement macroscopiques observables à notre échelle. On parlera, pour désigner l'ensemble d'énergie cinétique macroscopique noté $E_{C,macro}$.

De plus :
* Chaque particule possède un mouvement chaotique microscopique qui n'est pas perçu à l'échelle macroscopique:
* un énergie cinétique de translation microscopiqe (qu'on appelle aussi agitation thermique): $E_{th}$ (pour thermique)
* si la particule n'est pas monoatomique (ponctuelle), on peut lui associer une énergie cinétique de rotation sur elle-même: $E_{rot,mic}$
* si la particule n'est pas monoatomique (ponctuelle), on peut lui associer une énergie cinétique de vibration des liaisons intramoléculaires: $E_{vib,mic}$
* Ces composantes ne sont pas visibles à l'échelle macroscopique en terme de mouvement mais peuvent avoir un effet global (on rappelle qu'on a relié l'énergie de translation microscopique à la température). Elles sont __internes__ au système.
* Le système peut-être soumis à des forces extérieures dérivant d'une énergie potentielle. Leur influence est observable à l'échelle macroscopique. On leur associe une énergie potentielle macroscopique $E_{P,macro}$
* Les particules du systèmes peuvent être en interaction entre-elles. Ces interactions (forces newtoniennes principalement) dérivent d'une énergie potentielle mais n'ont pas d'effets mécaniques visibles à l'échelle macroscopique. On parle d'énergie potentielle d'interaction $E_{P, int}$.

On peut donc écrire l'énergie totale d'un système:

$$
E = E_{C,macro} + E_{P,macro} + \underbrace{E_{th} + E_{rot,mic} + E_{vib,mic}}_{U}
$$
> Les termes microscopiques, $E_{P,int}, E_{th}, E_{rot,mic}, E_{vib,mic}$ ne sont pas observables/discernables à l'échelle macroscopique et leur participation à l'énergie totale ne peut être séparée. C'est pourquoi, on les englobe dans un seul terme énergétique: l'__énergie interne__ U.
````

### Autres grandeurs énergétiques 

_On définit plusieurs autres grandeurs énergétiques (qui ont la dimension d'une énergie) à partir de l'énergie interne. Leur intérêt sera précisé par la suite. On peut déjà expliquer que leur introduction permettra de simplifier l'écriture du théorème énergétique (le premier principe) comme le passage de l'énergie cinétique à l'énergie mécanique modifie et simplifie l'écriture du théorème énergétique en mécanique (passage du TEC au TEM)._

Toutes les grandeurs proposées ici sont des __fonctions d'état extensives.__  


````{important} __Enthalpie__

On définit l'enthalpie H par $H = U + PV$.

Comme on le verra, l'enthalpie simplifie le premier principe pour des transformations à pression constante.

````


```{topic} Autres grandeurs énergétiques
* On définit l'énergie libre F par $F = U - TS$
* On définit l'enthalpie libre G par $G = U - TS + PV = H - TS = F + PV$

L'énergie libre et l'enthalpie libre ne seront pas utilisées en physique mais deviennent très importantes en chimie (surtout l'enthalpie libre).
```


### Dérivées partielles et capacités thermiques.

````{topic} Dérivées partielles d'une fonction d'état
L'énergie interne, comme l'enthalpie, est une fonction d'état. Elle peut donc se définir comme une fonction de variables d'état indépendantes par exemple U(T,V,n) (en pratique on écrira en physique U(T,V) car on travaille avec des systèmes fermés où n peut être considéré comme un paramètre).

On peut alors s'intéresser aux variations de l'énergie interne causées soit par la température, soit par le volume: on est en train de parler de __dérivées partielles__: $\left(\frac{\partial U}{\partial T}\right)_V (T,V)$ et $\left(\frac{\partial U}{\partial V}\right)_T(T,V)$ (on rappelle explicitement ici que ces dérivées partielles sont des fonctions de T ET de V). On peut interprêter ces grandeurs comme:
* la première correspond à l'énergie qu'il faut fournir pour augmenter la température de 1K à volume constant.
* la seconde correspond à l'énergie qu'il faut fournit pour augmenter le volume de $1m^3$ à température constante.

Certaines dérivées partielles ont un intérêt plus grand et sont nommées.
````

````{margin} ATTENTION
__On dérive l'enthalpie et non l'énergie interne__ pour $C_P$. La justification de cette subitilité sera vue par la suite lorsqu'on utilisera le premier principe.
````
````{important} __Capacités thermiques__

On définit aussi quelques caractéristiques particulières associées à l'énergie:

* la __capacité thermique à volume constant__: $C_V = \left(\frac{\partial U}{\partial T}\right)_V$. Elle correspond à l'énergie qu'il faut apporter pour augmenter la température de 1K à volume constant. On lui associe la capacité thermique molaire/massique qui a l'avantage de ne pas dépendre de la taille du système.
* la __capacité thermique à pression constant__: $C_P = \left(\frac{\partial H}{\partial T}\right)_P$. Elle correspond à l'énergie qu'il faut apporter pour augmenter la température de 1K à pression constante. On lui associe la capacité thermique molaire/massique qui a l'avantage de ne pas dépendre de la taille du système.
````

````{topic} Compléments : Coefficients thermoélastiques
On définit d'autres dérivées partielles particulières (pas en rapport avec l'énergie). Leurs expressions sont données à titres indicatifs :

* le __coefficient de compressibilité isotherme__: $\chi_T = -\frac{1}{V}\left(\frac{\partial V}{\partial P}\right)_T$. On l'a déjà utilisé en statique des fluides: il permet de caractéristier le caractère incompressible lorsqu'il est très faible.
* le __coefficient de dilatation isobare__: $\alpha = \frac{1}{V}\left(\frac{\partial V}{\partial T}\right)_P$. Il sera moins utilisé mais en général on fait l'hypothèse de fluide incompressible __et indilatable__ pour les liquides. Ce second terme correspond à un très faible coefficient $\alpha$ (d'où le nom indilatable).
* le __coefficient de compressibilité isentropique__: $\chi_S = -\frac{1}{V}\left(\frac{\partial V}{\partial P}\right)_S$. On ne l'utilisera pas en première année. Il sera utilisé en seconde année pour étudier la propagation d'onde sonore.

_La division par V permet d'obtenir des coefficients qui ne dépendent pas de la taille du système (on remarquera qu'on peut remplacer le volume par le volume molaire/massique sans changer l'expression)._
````

````{topic} Expression des différentielles
On rappelle qu'on peut écrire une différentielle à partir des dérivées partielles. Si l'on considère l'énergie interne comme une fonction de T et V, alors la différentielle dU(T,V) s'écrit: 

\begin{align*}
dU(T,V) &= \left(\frac{\partial U}{\partial T}\right)_V dT (T,V) + \left(\frac{\partial U}{\partial V}\right)_T (T,V) dV
dU(T,V) &= C_V(T,V) dT + \left(\frac{\partial U}{\partial V}\right)_T (T,V) dV
\end{align*}
````

## Entropie

````{topic} Introduction
L'entropie S d'un système est avec l'énergie la grandeur extrêmement importante en thermodynamique. Le second principe de la thermodynamique donnera ses caractéristiques générales.

Il existe de nombreuses définitions de l'entropie (toutes cohérentes). On se propose de donner ici quelques caractéristiques et de donner une __interprétation__ "microscopique" de l'entropie, c'est-à-dire basée sur les données microscopiques et donc la statistique des grandeurs microscopiques. On parle __d'entropie statistique__.

Ce n'est pas la définition la plus utilisée durant cette année mais elle permet d'avoir de donner un sens "physique" à l'entropie.
````


````{sidebar} Cas du gaz parfait
On montrera que l'entropie d'un gaz parfait peut s'exprimer en fonction de T et P (ou P et V ou T et V):

\begin{align*}
S &= S_0 + \frac{nR}{\gamma-1}\ln \left(\frac{TV^{\gamma-1}}{T_0 V_0^{\gamma-1}}\right) \\
&= S_0 + \frac{nR}{\gamma-1}\ln \left(\frac{T^{\gamma}P^{1-\gamma}}{T_0^{\gamma} P_0^{1-\gamma}}\right) \\
&= S_0 + \frac{nR}{\gamma-1}\ln \left(\frac{PV^{\gamma}}{P_0 V_0^{\gamma}}\right)
\end{align*}
où $S_0$ est l'entropie du gaz à $(T_0,P_0,V_0)$.
````
````{important} __Propriétés__

L'entropie S d'un système est __une fonction d'état__. Elle est __extensive__.

En tant que fonction d'état, cela signifie que sa variation dans une transformation ne dépend pas du chemin mais des états initiaux et finaux ET que l'on peut l'exprimer comme une fonction d'autres variables d'état.
````

````{topic} Description de l'entropie
L'entropie est une mesure du __désordre__ d'un système. Nous verrons plus en détail la définition sous-jacente dans une activité. Pour l'instant, on peut comprendre le désordre de la manière suivante: plus il existe de façon de décrire un état d'équilibre macroscopique de manière microscopique différentes, plus le désordre est grand, donc plus l'entropie sera grande.
````


