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

````{admonition} Définition : Etat d'une particule
:class: tip

A un instant t, on peut définir l'état d'une particule par différentes caractéristiques (qui sont microscopiques !): sa vitesse (3 coordonnées), sa position (3 coordonnées) et possiblement sa forme (vibration, rotation... ) si la particule n'est pas un simple atome (on ne s'intéresse pas ici à des phénomènes nucléaires).

````

````{admonition} Définition : Microétat
:class: tip

Pour un système dynamique, on appelle __microétat__ un état du système décrit par les données de toutes les grandeurs microscopiques de toutes les particules du système.

````


__Etude statistique__  
On ne peut décrire de manière exhaustive un microétat (on rappelle qu'une mole de gaz contient...  $10^{23}$ molécules/atomes... )

On peut par contre décrire la __statistique__ des différentes grandeurs associées à chaque particules.


````{admonition} Exemple : Statistiques
:class: tip, dropdown

On décrit en général le nombre de particule __par unité de volume__ qui possède une caractéristique donnée. Par exemple $n(v_x)$ donne le nombre de particules par unité de volume dont la composante de vitesse suivant x vaut $v_x$.

Comme nous le verrons par la suite, les hypothèses d'étude en théorie cinétique permettent d'obtenir des informations très utiles sur ces caractéristiques.

Les grandeurs utiles correspondent en général à la moyenne ou à la variance/écart-type qu'on relie à des grandeurs macroscopiques. Il faut par contre faire attention, à la différence des valeurs moyennes étudiées en électrocinétique, il s'agit ici de moyennes sur un __ensemble et non sur une durée__.
````

````{admonition} Définition : Vitesse quadratique moyenne
:class: tip

On définit la vitesse quadratique moyenne comme la racine carré de la moyenne de la statistique des vitesses (en norme) au carré.

\begin{align*}
u &= \sqrt{\overline{v^2}}\\
&= \sqrt{\frac{1}{N} \sum\limits_{i=1}^{i=N}v_i^2}
\end{align*}

où $v_i$ est la vitesse de la particule i.

````

## Vitesse quadratique moyenne

````{admonition} Exercice 
:class: attention

Une système est isotrope si __aucune direction dans l'espace n'est privilégiée__.

1. La statistique des grandeurs microscopiques est globale au système. Si le système est à l'équilibre, que peut-on dire de la statistique d'une grandeur?
1. Si le système est de plus isotrope, que peut-on dire des statistiques des composantes de vitesse dans les trois directions $v_x, v_y$ et $v_z$? Que peut-on aussi dire de leur moyenne?
1. Même question concernant la statistique des carrés des composantes $v_x^2, v_y^2$ et $v_z^2$? En déduire une relation entre $\overline{v_x^2}$ et $u$ la vitesse quadratique moyenne.
1. Exprimer l'énergie cinétique moyenne par particule lié à la translation des particules. En déduire une utilité de la vitesse quadratique moyenne. On supposera que toutes les particules sont identiques.
````

````{dropdown} Démonstration
__Statistique et équilibre__  
Pour un système à l'équilibre, les vitesses et positions de chaque particule peuvent changer mais la statistique de chaque grandeurs sera __constante__.

__Statistique et isotropie__  
Les statistiques des trois composantes doivent être __identiques__ puisqu'aucune direction n'est privilégiée. De plus il y aura autant de particules qui possède la composante $v_x$ que de particules qui possèdent la composante $-v_x$. Il vient que la valeur moyenne de chaque composante est __nulle__.

Les statistiques du carré des composantes sont aussi identiques. Notons que la valeur moyenne n'est cette fois pas nulle puisqu'on somme des valeurs positives. Par contre $\overline{v_x^2} = \overline{v_y^2} = \overline{v_z^2}$

On peut calculer la vitesse quadratique moyenne:

\begin{align*}
u^2 &= \frac{1}{N}\sum\limits_{i=1}^{N}v_{xi}^2 + v_{yi}^2 + v_{zi}^2\\
&= \overline{v_{xi}^2} + \overline{v_{yi}^2} + \overline{v_{zi}^2}\\
&= 3 \overline{v_{xi}^2} = 3 \overline{v_{yi}^2} = 3 \overline{v_{zi}^2}\\
\end{align*}


__Vitesse et énergie__  
Le calcul de l'énergie cinétique par particule se fait en sommant toutes les énergiés cinétiques des particules (uniquement la partie liée à la translation, on ne s'intéresse pas ici à la rotation des particules ou aux vibrations internes (liaisons intra-moléculaires)) et en divisant par N:

\begin{align*}
\overline{E_c} &= \frac{1}{N} \sum\limits_{i=1}^{N}E_{ci}\\
&= \frac{1}{N} \sum\limits_{i=1}^{N}\frac{1}{2}m v_i^2\\
&= \frac{1}{2}m \overline{v^2}\\
&= \frac{1}{2}m u^2
\end{align*}
On observe l'intérêt de la vitesse quadratique moyenne: elle est directement liée à l'énergie cinétique moyenne des particules. Nous verrons que cela a son importance lorsqu'on relie les grandeurs macroscopiques et microscopiques.

````

## Echelle macroscopique: Variables d'état

````{admonition} Définition : Variables d'état
:class: tip

Les variables d'état sont des grandeurs macroscopiques permettant de définir l'état du système à un instant donné à l'échelle macroscopique.

````

````{admonition} Exemple : 
:class: tip, dropdown

T (Température), P (Pression), V (Volume), n (nombre de mole), q (charge)... 
````


__Variables d'état et chemin parcouru__  
Un variable d'état ne dépend que de l'état du système. Donc sa variation d'un état A à un état B __ne dépend que des états A et B et pas du chemin parcouru entre les deux.__ A l'image de l'énegie (cinétique, potentielle ou mécanique), on notera leurs variations $\Delta T$ (transformation finie) ou dT (transformation infinitésimale).


````{dropdown} Remarque

__Représentations graphiques__  
Très souvent, nos systèmes ne "bougent" pas. Le passage d'un état A à un état B n'est pas représenté par une trajectoire dans l'espace. Néanmoins, les représentations graphiques sont souvent très utiles pour comprendre les phénomènes. C'est pourquoi, on représentera l'évolution du système dans des diagrammes spécifiques où l'on représente les grandeurs (certaines) qui varient. Par exemple, si P et T varient, on peut représenter les états A et B et le chemin parcouru pour aller de A à B dans un diagramme...  (T,P). Nous verrons par la suite plusieurs diagrammes utile et les informations qu'on peut tirer des trajectoires dans ces diagrammes.
````

## Du microscopique au macroscopique


La vision à l'échelle microscopique et la vision à l'échelle macroscopique doivent être cohérentes et l'on doit pouvoir passer de l'une à l'autre. C'est pourquoi on associe (pas définit mais associe) à la plupart des grandeurs macroscopiques un "sens" à l'échelle microscopique.

La compréhension "microscopique" des variables d'état est importante pour mieux comprendre la physique des systèmes.

Nous verrons pour plusieurs variables d'état le lien avec l'échelle microscopique.


````{admonition} Exemple : Température et vitesse quadratique
:class: tip, dropdown

Nous donnons à titre d'exemple __l'interprétation__ (pas la définition) de la température.

On peut montrer (HP) que pour un système maintenu à la température T, celle-ci est reliée à l'énergie cinétique moyenne de translation par particule: 

\begin{equation}
\overline{E_c} = \frac{3}{2}k_B T
\end{equation}
L'expression trouvée précédemment de l'énergie moyenne relie la température à la vitesse quadratique moyenne. On retrouve l'idée déjà vue dans les classes précédentes que la température est liée à __l'agitation moléculaire__ (on parle d'agitation thermique).
````

## Grandeurs extensives et intensives

````{admonition} Définition : Grandeurs extensives
:class: tip

Un grandeur est dite extensive si sa valeur considérée pour une portion de volume V d'un système homogène est proportionnelle à V.

````

````{admonition} Définition : Grandeurs intensives
:class: tip

Une grandeur est dite intensive si sa valeur considérée pour une portion de volume V d'un système homogène est indépendante de V.

````

## Grandeurs molaires et massiques


__Rapport de grandeurs extensives__  
Le rapport de deux grandeurs extensives est une __grandeur intensive__. Par exemple, la masse volumique m/V est une grandeur intensive.

Cette observation permet de définir les grandeurs molaires et massiques


````{admonition} Définition : Grandeurs molaires
:class: tip

Pour une grandeur $C$ extensive, on définit une grandeur dite molaire, c'est-à-dire rapportée à une mole. On la note par convention $C_{m}$.

````

````{admonition} Définition : Grandeurs massiques
:class: tip

Pour une grandeur $C$ extensive, on définit une grandeur dite massique, c'est-à-dire rapportée à une masse de $1 \rm{kg}$. On le note par convention $c$ (minuscule).

````

## Utilisation des grandeurs intensives


Un des intérêts des grandeurs molaires et massiques est qu'elles ne dépendent pas de la taille de système (principe même des grandeurs intensives). Il vient que leur utilisation permet de réécrire des équations pour certaines systèmes qui ne dépendent plus de la taille du système. On se propose de l'observer sur l'exemple de deux équation d'état des gaz.


````{admonition} Exercice 
:class: attention

1. On considère un gaz parfait dont l'équation d'état est $PV = nRT$. Réexprimer cette équation avec uniquement des grandeurs intensives en introduisant le volume massique et la masse molaire puis en introduisant le volume molaire.
1. On considère maintenant l'équation d'état d'un gaz de Van der Waals donnée comme $(P - \frac{a^2}{V_m^2})(V_m - b) = RT$ où $V_m$ est le volume molaire. Etablir l'équation de Van der Waals pour un volume V et un nombre de mole n.
````

````{dropdown} Démonstration

__1. De l'extensif vers l'intensif.__  

Pour obtenir des grandeurs massiques, il faut diviser par la masse. Il vient $P v = \frac{n}{m}RT$ soit $Pv = \frac{RT}{M}$.

Pour obtenir des grandeurs molaires, il faut divier par le nombre de moles. Il vient $PV_m = RT$.
 

__2. De l'intensif vers l'extensif.__  

On va remplacer le volume molaire $V_m$ par $V/n$ soit:

\begin{align*}
(P - \frac{n^2 a^2}{V})(\frac{V}{n} - b) &= RT\\
(P - \frac{n^2 a^2}{V})(V - nb) &= nRT
\end{align*} 
````

