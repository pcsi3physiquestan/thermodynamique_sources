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
# Grandeurs intensives

## Température

### Définition

````{margin} 
Il s'agit d'une définition très abstraite qui nous servira peu par la suite. Nous allons voir d'autres interprétation de la température (qui sont parfois considérées comme des définitions) et qui permettront de faire des interprétations physiques de la températures.
````
````{important} __Température (thermodynamique)__

Soit un système dont l'entropie est notée S, l'énergie interne U et le volume V. On définit la température du système par la grandeur:

$$
T = {\left(\frac{\partial U}{\partial S}\right)}_{V}
$$
````

### Température cinétique

````{margin}
L'équivalence entre la définition thermodynamique de la température et son interprétation cinétique est admise.
````
````{important} __Température (cinétique) - Admis__

L'énergie cinétique moyenne de translation des particules d'un gaz s'écrit en fonction de la température sous la forme:

$$
\overline{E_c} = \frac{3}{2}k_B T
$$
On parle pour interprêter cette température de "température cinétique".

$k_B$ est la constante de Boltzmann.
````

### Propriétés et mesures (en ligne)

````{topic} __Principe zéro__

Tous les systèmes en équilibre thermique avec un système donnée sont en équilibre entre eux. Ce principe se vérifie expérimentalement. On dit alors que tous ces systèmes sont à la même température.

Ce principe sera démontré pour la température thermodynamique au moyen du second principe.
````

````{topic} Thermomètres et principe 0
Ce principe 0 est la base des premiers principes de mesure de la température: on place le système étudié en contact thermique avec une appareil de mesure(un thermomètre) et on atteint __l'équilibre thermique__. La température du thermomètre est alors celle du système. On s'arrange alors pour que l'influence de T sur le thermomètre soit quantifiable.

Par exemple, dans le cas des thermomètres "classiques" il s'agit d'un fluide qui se dilate dans un tube capillaire sous l'effet de la température. On associe à T une hauteur de dilatation.

__(Note) Thermomètres modernes :__  Si la majorité des thermomètres "grand public" nécessite encore une mise en contact thermique, certains thermomètres modernes peuvent s'en passer en utilisant une mesure par rayonnement thermique.
````

### Température absolue (en ligne)

````{sidebar} Vision macroscopique
A l'inverse de la température cinétique qui donne une interprétation microscopique, la température dite "absolue" permet une interprétation en terme de mesure expérimentale et donc une vision macroscopique.

Cette interprétation vient du besoin, après l'utilisation de très nombreuses échelles de mesures (les plus persistentes sont le Celsius et le Farenheit) de créer une "définition" (ça a été une définition) de la température basée sur des propriétés fondamentales et non sur des phénomènes particuliers subjectifs (on choisit aribitrairement de placer le 0$\circ$C au gel de l'eau à température ambiante mais ce 0 n'a pas de valeur "absolue".

Avec la température absolue (dont l'unité sera le Kelvin K), on définit un 0 issu de propriétés fondamentales et comme valeur limite basse (il ne peut y avoir de température négative). Il restera à choisir une échelle (arbitraire).
````
````{topic} Expérience de Boyle-Mariotte

```{figure} ./images/thermo_amagat.jpg
:name: fig_270
:align: center
```

On dispose d'une masse m donnée de gaz maintenue à température constante dans une enceinte thermostatée. On peut faire varier la température $\theta$ (définie comme une température relative --- échelle de Celsius) du thermostat. Un système de vase communiquant permet de faire varier le volume et la pression du gaz. L'expérience consiste à suivre l'évolution du volume V et de la pression P du gaz pour une température $\theta$ donnée.

Boyle et Mariotte ont montré qu'on pouvait interpoler la valeur limite du produit PV quand P tendait vers 0 par une valeur $PV_{P=0}$ qui ne dépendait que de la température $\theta$, quel que soit le gaz considéré. On dit que le comportement des gaz est alors parfait.
````

````{important} __Température absolue__

On définit la température absolue à partir d'un point de référence $T_R = 273,16 \rm{K}$ au point triple de l'eau et telle que $T=0$ quand pour un gaz, $PV_{P=0} = 0$. La température T "absolue" est alors définie comme la limite du produit $\frac{PV}{nR}$ lorsque P tend vers 0 pour un gaz.

````

## Pression

### Définition

* _Rappel : Définition empirique : On rappelle qu'on peut définir la pression de manière empirique comme la force surfacique exercée par le fluide normalement à la surface de contact. $\overrightarrow{dF} = P \overrightarrow{dS}$_
* _Rappel : Origine microscopique : On rappelle que la pression peut-être vue comme un transfert de quantité de mouvement par unité de surface et de temps normalement à la surface de contact (on parlera de flux)._

Comme on l'a déjà précisé, cette interprétation sera surtout utilisée pour exprimer la pression d'un fluide sur une paroi. On parle de __pression cinétique__. On peut calculer la force moyenne exercée par une particule sur la paroi puis sommer les forces exercées par l'ensemble des particules qui heurtent la paroi par unité de temps. Un tel calcul sera réalisé dans le cadre de l'étude de la pression cinétique d'un gaz parfait.


````{important} __Pression thermodynamique__

Soit un système dont l'entropie est notée S, l'énergie interne U et le volume V. On définit la pression du système par la grandeur:

$$
P = - {\left(\frac{\partial U}{\partial V}\right)}_{S}
$$

````

