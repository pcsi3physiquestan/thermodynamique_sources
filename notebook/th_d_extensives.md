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

## Variables extensives: généralités

_Rappel : Variables extensives_  
On rappelle qu'une variable d'état extensive est une variable d'état dont la valeur pour une portion V d'un système homogène est proportionnelle au volume V (on peut aussi ramener à la masse ou à la quantité de manière)s.


````{admonition} Exemple : Exemple
:class: tip, dropdown

Le volume, la quantité de matière, la masse, l'entropie, l'énergie totale et l'énergie interne (on reviendra sur ces grandeurs par la suite) sont toutes des grandeurs extensives.
````


__Bilan d'une grandeur extensive__  
On rappelle que la variation d'une grandeur d'état X d'un système s'écrit $\Delta X$.

Dans le cas d'une grandeur extensive, la variation de X a deux origines possibles: la quantité $X_e$ échangée avec l'extérieur et la quantité $X_c$ créée à l'intérieur du système. On peut toujours écrire le bilan d'un grandeur extensive X lors d'une transformation finie: $\Delta X = X_e + X_c$ ($X_e$ est la grandeur échangée de l'extérieur __vers__ le système).

Dans le cas d'une variation infinitésimale, on écrira ce bilan: $dX = \delta X_c + \delta X_e$. L'utilisation de la notation $\delta$ est fondamentale pour les __termes d'échange et de création__: il signifie que ces deux termes __dépendent du chemin parcouru pour passer de l'état initial à l'état final alors que la variation dX ne dépend que des données de l'état initial et de l'état final et non du chemin parcouru lors de la transformation.__  

Ce bilan est général à toutes les grandeurs d'état extensives et notamment l'énergie et l'entropie. Nous verrons qu'une des caractéristiques des premier et second principe de la thermodynamique consiste à caractériser ces termes d'échanges et de création.


## Variable extensive: Energie et énergie interne


__Composantes énergétiques__  
Prenons un système composé de particules (on les supposera identiques même si cela n'a que peu d'importance), nous supposerons pour simplifier ici qu'il n'y a pas de mouvement d'ensemble à l'intérieur du système: le centre d'inertie a un mouvement et les particules ont un mouvement chaotique dans le référentiel du centre d'inertie. Par définition, l'énergie du système est la somme de l'énergie de chaque particule. Pour le système complet, on peut distinguer plusieurs types d'énergie qu'on distinguera comme étant microscopique ou macroscopique.

* Les énergies cinétiques liés aux mouvement globaux du système:
* L'énergie cinétique de translation macroscopique, assimilable à l'énergie cinétique qu'aurait le centre d'inertie affecté de toute la masse.
* L'énergie cinétique de rotation macroscopique associée à la rotation global du solide. Si le système est à l'équilibre, cette composante est forcément nulle.


Ces deux composantes sont associées à des mouvement macroscopiques observables à notre échelle. On parlera, pour désigner l'ensemble d'énergie cinétique macroscopique noté $E_{C,macro}$.
* Chaque particule possède un mouvement chaotique microscopique qui n'est pas perçu à l'échelle macroscopique:
* un énergie cinétique de translation microscopiqe (qu'on appelle aussi agitation thermique): $E_{th}$ (pour thermique)
* si la particule n'est pas monoatomique (ponctuelle), on peut lui associer une énergie cinétique de rotation sur elle-même: $E_{rot,mic}$
* si la particule n'est pas monoatomique (ponctuelle), on peut lui associer une énergie cinétique de vibration des liaisons intramoléculaires: $E_{vib,mic}$
* Ces composantes ne sont pas visibles à l'échelle macroscopique en terme de mouvement mais peuvent avoir un effet global (on rappelle qu'on a relié l'énergie de translation microscopique à la température). Elles sont __internes__ au système.

* Le système peut-être soumis à des forces extérieures dérivant d'une énergie potentielle. Leur influence est observable à l'échelle macroscopique. On leur associe une énergie potentielle macroscopique $E_{P,macro}$
* Les particules du systèmes peuvent être en interaction entre-elles. Ces interactions (forces newtoniennes principalement) dérivent d'une énergie potentielle mais n'ont pas d'effets mécaniques visibles à l'échelle macroscopique. On parle d'énergie potentielle d'interaction $E_{P, int}$.



````{important} __Définition : Energie totale et énergie interne__

On peut donc écrire l'énergie totale d'un système:

\begin{equation}
E = E_{C,macro} + E_{P,macro} + \underbrace{E_{th} + E_{rot,mic} + E_{vib,mic}}_{U}
\end{equation}
Les termes microscopiques, $E_{P,int}, E_{th}, E_{rot,mic}, E_{vib,mic}$ ne sont pas observables à l'échelle macroscopique et leur participation à l'énergie totale ne peut être séparée. C'est pourquoi, on les englobe dans un seul terme énergétique: l'__énergie interne__ U.

````

````{attention}

Il s'agit d'une interprétation de l'énergie interne qui nous permettra de la calculer dans certains cas simples mais il ne s'agit pas d'une définition.

````


__Caractère extensif (anecdotique)__  
Le caractère extensif de l'énergie interne est postulé (partie du premier principe) mais n'est pas évident et est même en toute rigueur faux à cause des forces surfaciques. Le caractère extensif suppose les forces de surface négligeable, c'est-à-dire que la surface du système n'est pas trop grande (il ne doit pas y avoir une dimension du système qui soit très faible devant les deux autres).


## Energie interne

````{admonition} Exercice 
:class: attention

On considère un gaz non modélisable par le modèle du gaz parfait car les interactions à longue distance entre les particules du gaz ne sont pas négligeable. L'énergie totale se décompose en la partie macroscopique définie comme en mécanique et l'énergie interne. Un modélisation possible dite de Van der Waals consiste à écrire l'énergie interne du gaz à partir de celle du gaz parfait sous la forme $U = U_{GP} - \frac{n^2 a}{V} + U_0$ où $U_0$ est l'énergie interne aux conditions $(T_0,V_0)$ et $U_{GP}$ l'énergie interne d'un gaz s'il suivait le modèle du gaz parfait dans les mêmes conditions.

Préciser physiquement quel signe attend-on pour a.
````

````{dropdown} Démonstration

 


Les interactions dans un gaz de Van der Waals sont des interactions entre molécules neutres donc de ...  Van der Waals. Elles sont donc attractives. L'énergie potentielle d'interaction doit donc être croissante avec la distance entre particules et l'énergie potentielle d'interaction totale sera donc aussi croissante avec le volume V. La différence proposée ici entre les deux modèles est qu'on tient compte des interactions. On attend donc un terme correction croissant avec le volume donc un coefficient a positif.

````

## Autres grandeurs énergétiques 


On définit plusieurs autres grandeurs énergétiques (qui ont la dimension d'une énergie) à partir de l'énergie interne. Leur intérêt sera précisé par la suite. On peut déjà expliquer que leur introduction permettra de simplifier l'écriture du théorème énergétique (le premier principe) comme le passage de l'énergie cinétique à l'énergie mécanique modifie et simplifie l'écriture du théorème énergétique en mécanique (passage du TEC au TEM).

Toutes les grandeurs proposées ici sont des __fonctions d'état extensives.__  


````{important} __Définition : Enthalpie__

On définit l'enthalpie H par $H = U + PV$

Comme on le verra, l'enthalpie simplifie le premier principe pour des transformations à pression constante.

````


__Autres grandeurs énergétiques (pas à connaître en physique)__  
On définit l'énergie libre F par $F = U - TS$

On définit l'enthalpie libre G par $G = U - TS + PV = H - TS = F + PV$

L'énergie libre et l'enthalpie libre ne seront pas utilisées en physique mais deviennent très importantes en chimie (surtout l'enthalpie libre).


## Dérivées partielles et capacités thermiques.


L'énergie interne est une fonction d'état. Elle peut donc se définir comme une fonction de variables d'état indépendantes par exemple U(T,V,n) (en pratique on écrira en physique U(T,V) car on travaille avec des systèmes fermés où n peut être considéré comme un paramètre).

On peut alors s'intéresser aux variations de l'énergie interne causées soit par la température, soit par le volume: on est en train de parler de __dérivées partielles__: $\left(\frac{\partial U}{\partial T}\right)_V (T,V)$ et $\left(\frac{\partial U}{\partial V}\right)_T(T,V)$ (on rappelle explicitement ici que ces dérivées partielles sont des fonctions de T ET de V). On peut interprêter ces grandeurs comme:

*  la première correspond à l'énergie qu'il faut fournir pour augmenter la température de 1K à volume constant.
* la seconde correspond à l'énergie qu'il faut fournit pour augmenter le volume de $1m^3$ à température constante.


Certaines dérivées partielles ont un intérêt plus grand et sont nommées.


````{admonition} Compléments : Coefficients thermoélastiques
:class: hint, dropdown

On définit quelques dérivées partielles particulières:

* le __coefficient de compressibilité isotherme__: $\chi_T = -\frac{1}{V}\left(\frac{\partial V}{\partial P}\right)_T$. On l'a déjà utilisé en statique des fluides: il permet de caarctéristier le caractère incompressible lorsqu'il est très faible.
* le __coefficient de dilatation isobare__: $\alpha = \frac{1}{V}\left(\frac{\partial V}{\partial T}\right)_P$. Il sera moins utilisé mais en général on fait l'hypothèse de fluide incompressible __et indilatable__ pour les liquides. Ce second terme correspond à un très faible coefficient $\alpha$ (d'où le nom indilatable).
* le __coefficient de compressibilité isentropique__: $\chi_S = -\frac{1}{V}\left(\frac{\partial V}{\partial P}\right)_S$. On ne l'utilisera pas en première année. Il sera utilisé en seconde année pour étudier la propagation d'onde sonore.


La division par V permet d'obtenir des coefficients qui ne dépendent pas de la taille du système (on remarquera qu'on peut remplacer le volume par le volume molaire/massique sans changer l'expression).
````

````{important} __Définition : Capacités thermiques__

On définit aussi quelques caractéristiques particulières associées à l'énergie:

\begin{enumerate}
* la __capacité thermique à volume constant__: $C_V = \left(\frac{\partial U}{\partial T}\right)_V$. Elle correspond à l'énergie qu'il faut apporter pour augmenter la température de 1K à volume constant. On lui associe la capacité thermique molaire/massique qui a l'avantage de ne pas dépendre de la taille du système.
* la __capacité thermique à pression constant__: $C_P = \left(\frac{\partial H}{\partial T}\right)_P$. Elle correspond à l'énergie qu'il faut apporter pour augmenter la température de 1K à pression constante. On lui associe la capacité thermique molaire/massique qui a l'avantage de ne pas dépendre de la taille du système.

__On dérive l'enthalpie et non l'énergie interne__. La justification de cette subitilité sera vue par la suite lorsqu'on utilisera le second principe.


````


__Expression des différentielles__  
On rappelle qu'on peut écrire une différentielle à partir des dérivées partielles. Si l'on considère l'énergie interne comme une fonction de T et V, alors la différentielle dU(T,V) s'écrit: $dU = \left(\frac{\partial U}{\partial T}\right)_V dT + \left(\frac{\partial U}{\partial V}\right)_T dV$ ou $dU = C_V dT + \left(\frac{\partial U}{\partial V}\right)_T dV$


## Variable d'état extensive: Entropie


L'entropie S d'un système est avec l'énergie la grandeur extrêmement importante en thermodynamique. Le second principe de la thermodynamique donnera ses caractéristiques générales.

Il existe de nombreuses définitions de l'entropie (toutes cohérentes). On se propose de donner ici quelques caractéristiques et de donner une __interprétation__ "microscopique" de l'entropie, c'est-à-dire basée sur les données microscopiques et donc la statistique des grandeurs microscopiques. On parle __d'entropie statistique__.

Ce n'est pas la définition la plus utilisée durant cette année mais elle permet d'avoir de donner un sens "physique" à l'entropie.


````{important} __Fondamental : Propriétés__

L'entropie S d'un système est __une fonction d'état__. Elle est __extensive__.

En tant que fonction d'état, cela signifie que sa variation dans une transformation ne dépend pas du chemin mais des états initiaux et finaux ET que l'on peut l'exprimer comme une fonction d'autres variables d'état.
````

````{admonition} Exemple : Cas du gaz parfait
:class: tip, dropdown

On montrera que l'entropie d'un gaz parfait peut s'exprimer en fonction de T et P (ou P et V ou T et V):

\begin{align*}
S &= S_0 + \frac{nR}{\gamma-1}\ln \left(\frac{TV^{\gamma-1}}{T_0 V_0^{\gamma-1}}\right) \\
&= S_0 + \frac{nR}{\gamma-1}\ln \left(\frac{T^{\gamma}P^{1-\gamma}}{T_0^{\gamma} P_0^{1-\gamma}}\right) \\
&= S_0 + \frac{nR}{\gamma-1}\ln \left(\frac{PV^{\gamma}}{P_0 V_0^{\gamma}}\right)
\end{align*}
où $S_0$ est l'entropie du gaz à $(T_0,P_0,V_0)$.
````


__Description de l'entropie.__  
L'entropie est une mesure du __désordre__ d'un système. Nous verrons plus en détail la définition sous-jacente dans une activité documentaire. Pour l'instant, on peut comprendre le désordre de la manière suivante: plus il existe de façon de décrire un état d'équilibre macroscopique de manière microscopique différentes, plus le désordre est grand, donc plus l'entropie sera grande.


## Entropie: Analyse qualitative

````{admonition} Exercice 
:class: attention

On se propose ici de retrouver la monotonie de l'entropie d'un gaz parfait par un raisonnement qualitatif. On considère n moles d'un gaz parfait.

* Justifier que l'entropie du gaz va augmenter si l'on augmente la température à volume constant.
* Justifier que l'entropie du gaz va augmenter si l'on augmente le volume à température constante.
* Peut-on prévoir qualitativement l'évolution de l'entropie de l'entropie si l'on augmente le volume et qu'on diminue la température?


````
````{dropdown} Démonstration

 


Si l'on augmente la température, cela signifie qu'on augmente l'énergie cinétique des molécules. On peut donc considérer qualitativement qu'on augmente le désordre (on augmente la gamme de vitesses accessibles) et donc l'entropie. C'est ce qu'on observe avec l'expression de S(T,V).

Si l'on augmente le volume, on augmente la place accessible et donc les positions possibles pour les particules: le désordre augmente donc l'entropie aussi. C'est aussi ce qu'on observe avec l'expression de S(T,V)

Si le volume augmente tandis que la température diminue, on ne peut déterminer si l'entropie va augmenter ou diminuer. En effet, il y a plus de place accessible mais l''énergie cinétique moyenne va diminuer. L'expression de S nous permettra de remarquer qu'effectivement suivant les cas l'entropie va augmenter ou diminuer.

````

````{admonition} Exercice 
:class: attention

On considère un corps pur à une pression P et une température T de changement d'état (ici vaporisation). Il peut alors exister sous sa forme gazeuse ou liquide (P,T). Dans quelle phase l'entropie sera la plus grande?

Reprendre la question précédente pour les phases solides et liquides d'un corps pur à un couple (P,T) de solidification.

````
````{dropdown} Démonstration

 


Dans une phase gazeuse, les molécules peuvent se mouvoir sur de plus grandes distances avec peu d'interactions avec les autres particules: il naît donc un chaos plus important. L'entropie de la phase gazeuse sera donc plus grand (cela suppose évidemment qu'on compare la même quantité de matière).

De même l'entropie de la phase liquide, plus désordonnée, sera plus grande que l'entropie de la phase solide.

````

