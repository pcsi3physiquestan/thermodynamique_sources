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
# Variables d'état et variables microscopiques

_Pour étudier un système physique, on doit définir des grandeurs permettant de le décrire. Comme on peut travailler à plusieurs échelles, on définira des grandeurs différentes suivant l'échelle d'analyse. A l'échelle microscopique, les grandeurs utilisées donneront lieu à des études __statistiques__ tandis qu'aux échelles méso et macroscopique, on utilisera des grandeurs appelées __variables d'état__. Comme nous le verrons par la suite, on peut en général relier les grandeurs microscopiques aux grandeurs macroscopiques._

## Microétat

````{sidebar} __Microétat__

Pour un système dynamique, on appelle __microétat__ un état du système décrit par les données de toutes les grandeurs microscopiques de toutes les particules du système.
````
````{important} __Etat d'une particule__

A un instant t, on peut définir l'état d'une particule par différentes caractéristiques (qui sont microscopiques !): sa vitesse (3 coordonnées), sa position (3 coordonnées) et possiblement sa forme (vibration, rotation... ) si la particule n'est pas un simple atome (on ne s'intéresse pas ici à des phénomènes nucléaires).

On ne peut décrire de manière exhaustive un microétat (on rappelle qu'une mole de gaz contient...  $10^{23}$ molécules/atomes... ). On peut par contre décrire la __statistique__ des différentes grandeurs associées à chaque particules. Par exemple $n(v_x)$ donne le nombre de particules par unité de volume dont la composante de vitesse suivant x vaut $v_x$.
````

````{important} __Vitesse quadratique moyenne__

On définit la vitesse quadratique moyenne comme la racine carré de la moyenne de la statistique des vitesses (en norme) au carré.

\begin{align*}
u &= \sqrt{\overline{v^2}}\\
&= \sqrt{\frac{1}{N} \sum\limits_{i=1}^{i=N}v_i^2}
\end{align*}

où $v_i$ est la vitesse de la particule i.

````


## Echelle macroscopique: Variables d'état

````{sidebar} Exemple
T (Température), P (Pression), V (Volume), n (nombre de mole), q (charge)... 
````
````{important} __Variables d'état__

Les variables d'état sont des grandeurs macroscopiques permettant de définir l'état du système à un instant donné à l'échelle macroscopique.
````

````{topic} Variables d'état et chemin parcouru
Un variable d'état ne dépend que de l'état du système. Donc sa variation d'un état A à un état B __ne dépend que des états A et B et pas du chemin parcouru entre les deux.__ A l'image de l'énegie (cinétique, potentielle ou mécanique), on notera leurs variations $\Delta T$ (transformation finie) ou dT (transformation infinitésimale).
````


````{topic} Du microscopique au macroscopique
La vision à l'échelle microscopique et la vision à l'échelle macroscopique doivent être cohérentes et l'on doit pouvoir passer de l'une à l'autre. C'est pourquoi on associe (pas définit mais associe) à la plupart des grandeurs macroscopiques un "sens" à l'échelle microscopique.

La compréhension "microscopique" des variables d'état est importante pour mieux comprendre la physique des systèmes.

* Exemple : Température et vitesse quadratique  
On peut montrer (HP) que pour un système maintenu à la température T, celle-ci est reliée à l'énergie cinétique moyenne de translation par particule: 

$$
\overline{E_c} = \frac{3}{2}k_B T
$$
L'expression trouvée précédemment de l'énergie moyenne relie la température à la vitesse quadratique moyenne. On retrouve l'idée déjà vue dans les classes précédentes que la température est liée à __l'agitation moléculaire__ (on parle d'agitation thermique).
````

## Typologie des grandeurs

````{important} __Grandeurs extensives et intensives__
* Un grandeur est dite __extensive__ si sa valeur considérée pour une portion de volume V d'un système homogène est proportionnelle à V.
* Une grandeur est dite __intensive__ si sa valeur considérée pour une portion de volume V d'un système homogène est indépendante de V.

````

````{margin}
Le rapport de deux grandeurs extensives est une __grandeur intensive__. Par exemple, la masse volumique m/V est une grandeur intensive.
````
````{margin}
On pourra aussi définir des grandeurs volumiques.
````
````{important} __Grandeurs molaires et massiques__

* Pour une grandeur $C$ extensive, on définit une grandeur dite __molaire__, c'est-à-dire rapportée à une mole. On la note par convention $C_{m}$.
* Pour une grandeur $C$ extensive, on définit une grandeur dite __massique__, c'est-à-dire rapportée à une masse de $1 \rm{kg}$. On le note par convention $c$ (minuscule).
````
