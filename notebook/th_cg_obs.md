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
# Observations expérimentales

_Jusqu'à présent, nous avons toujours supposer que les différents corps étudiés restaient sous la même phase au cours de la transformation. Ceci n'est pas toujours vérifié et on peut même chercher à vaporiser un gaz (climatisation des terrasses) ou à le liquéfier pour diverses utilisation (transport, refroidissement... ). Nous nous proposons ici d'étudier le comportement d'un corps pur lors d'un changement de phase. En première année, nous nous intéressons simplement aux changements de phase d'un corps pur ou à la coexistence de plusieurs phases d'un même corps (corps pur)._

## Différentes phases et transitions

### Phases: Définitions

````{admonition} Définition : Phase
:class: tip

Une phase est un système (ou un sous-système) dans lequel les paramètres intensifs sont continus. A l'équilibre ces paramètres sont uniformes.

Un système composé d'une phase est appelé système monophasé.

````


__Description des phases__  
* La phase gazeuse est un état où le corps occupe tout l'espace qui lui est offert, les interactions entre particules sont faibles devant leur agitation thermique (gaz de Van der Waals) ou négligeables (gaz parfait). C'est un état très désordonné.
* La phase liquide est un état où le volume est limité par des interactions entre particules plus importantes. Les fluides sont en général peu compressibles, plus dense que le gaz correspondant et épousent la forme des récipients, sous l'effet de la pesanteur.
* La phase solide correspond à l'état le plus ordonnée: les déplacements des particules sont très limités par les interactions importantes qui les lient. Le solide garde donc sa forme.



### Transitions de phases

````{admonition} Définition : Transitions des phases
:class: tip

Les différents noms des changements d'état sont à connaître. 

```{figure} ./images/thermo_chap_6_nom_chang.jpg
:name: fig_279
:align: center

```

````

## Diagramme (T,P)

_On peut représenter sur un diagramme (T,P) les zones où peuvent exister de manière stable les différentes phases d'un même corps pur. En réalisant l'étude expérimentale complète des états possibles, on peut déjà faire quelques observations qui vont se retrouver sur  le diagramme. Ces observations expérimentales sont à connaître._

### Observations expérimentales

````{admonition} Fondamental : 
:class: attention

```{figure} ./images/thermo_chap_6_diag_pt.jpg
:name: fig_280
:align: center

```
````

````{admonition} Fondamental : Observations générales
:class: attention

* Observation 1: L'existence stable des différentes phases dépend des données de température et de pression du système. Pour un couple (T,P), il n'existe qu'une seule configuration (1, 2 ou 3 phases données) pouvant exister de manière stable.
* Observation 2: L'existence stable d'un système monophasé n'impose aucune relation entre température et pression: les zones d'existence seront donc des surfaces sur le diagramme.
* Observation 3: La coexistence de deux phases à l'équilibre impose une relation entre la température et la pression. Autrement dit, si on impose la température (réciproquement la pression) d'un mélange de 2 phases données, on impose alors la pression (réciproquement la température): les zones de coexistence de 2 phases seront donc des courbes sur le diagramme. Ces courbes sont appelées courbe de changement d'état. 
* Observation 4: La coexistence des trois phases d'un même corps pur ne peut exister que pour un couple de température et pression. Le point ainsi défini sur le diagramme est appelé point triple. Ses coordonnées varient suivant le corps considérés. (Ce point peut ne pas exister: c'est le cas de l'Hélium)
* Observation 5: Pour des températures et pressions suffisamment élevées, le passage de l'état liquide à l'état gazeux et inversement s'effectue de manière continue, c'est-à-dire qu'on observera pas deux phases distinctes séparées par un ménisque lors de la transformation. Le point dont les coordonnées terminent la courbe de changement d'état liquide-vapeur est appelé point critique. On parle généralement de fluide hypercritique pour désigner l'état au-delà du point critique car liquide et gaz sont alors indiscernables.

````

````{admonition} Exemple : Point triple
:class: tip, dropdown


| Composé | T(K) | P(Pa) |
|:-|:-:|:-:|
| Eau | 273.15 | 611 |
| Dioxyde de carbone | 216.5 | 519 |
| Diazote | 63.16 | 12868 |

Le point triple du dioxyde de carbone présente un intérêt: la pression Pr est supérieure à la pression atmosphérique. Cela veut dire qu'à pression atmosphérique, le $CO_2$ ne peut que se sublimer. C'est l'intérêt de la neige carbonique. Le $CO_2$ à très basse température est solide à pression atmosphérique. Du gaz sous pression projeté sur des flammes va se détendre et diminuer sa température: il se solidifie. Il va alors étouffer les flammes (en raréfiant l'air en dioxygène) mais contrairement à l'eau, l'augmentation de température ne le transforme pas en liquide mais en gaz à pression ambiante: il ne stagne pas sur le matériel touché par le feu et ce dernier sera moins détérioré. Le CO2 est surtout utilisé pour les feux de classe B et C.
````

````{admonition} Exemple : Point critique
:class: tip, dropdown

| Composé | T(K) | P(Pa) | $\rho(kg.m^3)$ |
|:-|:-:|:-:|:-:|
| Eau | 647.3 | $22.12 \times 10^6$ |  |
| Dioxyde de carbone | 304.45 | $22.12 \times 10^6$ | 0.46 |
| SF6 | 318.65 | $3.76 \times 10^6$ |  |

Le point critique est défini par la donnée de $T_c$ et $P_c$. Le volume massique critique $v_c$ est alors fixé, on peut utiliser cette propriété pour élaborer des systèmes simples permettant de se placer au point critique: pour une quantité de matière n fixée, on en déterminer le volume critique correspondant et on place le corps pur seul dans une enceinte de volume $V_c$. On peut en faisant varier la température se placer à $T_c$, on est alors automatiquement à $P_c$, donc au point triple: on appelle ce montage un tube de Natterer.
````

### Tracé du diagramme (T,P)

````{admonition} Fondamental : Tracé
:class: attention

```{figure} ./images/thermo_chap_6_diag_pt.jpg
:name: fig_281
:align: center

```
````


__Analyse__  
* Place des phases: Le placement des phases s'obtient par un raisonnement simple: à pression constante, l'augmentation de température entraîne le passage vers des phases présentant moins de cohésion.
* Nom des courbes: En général, on parle de courbe de sublimation, de saturation (ou de vaporisation) et de solidification (ou de liquéfaction).
* Frontière liquide-vapeur: Elle est toujours croissante car le gaz est moins dense que le liquide, on l'appelle __courbe de saturation__. On appelle la pression $P_{sat}(T)$ où coexistent gaz et liquide à une température donnée __pression de vapeur saturante__. Il existe certaines expressions de la fonction $P_{sat}(T)$ pour certaines corps et certaines gammes de température (ex: formule de Duperray pour l'eau). Aucune n'est à connaître. La frontière liquide-vapeur est bornée en bas par le point triple et en haut, elle est bornée par le point critique.
* Frontière solide-liquide: Elle est beaucoup plus pentue. Pour la plupart des corps, elle est croissante: cela veut dire qu'en comprimant le corps (en diminuant son volume), il se solidifie: __le solide est ainsi en général plus dense que le liquide__. Deux corps en particulier font __exception: l'eau__ et le bismuth. Pour ces deux corps, la frontière est décroissante et on fait fondre le solide quand on compresse: __le solide est donc moins dense que le liquide pour l'eau__. Les liaisons hydrogène expliquent en grande partie ce phénomène pour l'eau. La frontière n'a pas de limite supérieure connue mais possède une limite inférieure: le point triple.
* Frontière solide-gaz: Elle est aussi croissante (le gaz est moins dense que le solide). Elle possède une limite supérieure: le point triple. Cette frontière peut être en réalité un ensemble de frontière successive quand le corps possède plusieurs variétés allotropiques solides. Sauf indication, on pourra tracer une courbe simple.



````{admonition} Exemple : Diagramme de l'eau
:class: tip, dropdown

```{figure} ./images/thermo_chap_6_diag_pt_eau.jpg
:name: fig_282
:align: center

```

Ce phénomène (pente inversée) s'observe de deux façons:

* la première est simplement la flottaison des glaçons dans l'eau (cf. Statique des fluides)
* la seconde est l'expérience du regel de l'eau: on place sur un glaçon un fil tendu par deux masses suspendues à ses extrémités: la pression imposée fait fondre localement la glace et le fil s'enfonce. Mais la pression exercée est locale est une fois le fil descendu, la pression redescend et l'eau regèle: on observe ainsi un fil qui s'enfonce dans la glace qui se referme petit à petit derrière lui.

````

### Variétés allotropiques

````{admonition} Définition : Variétés allotropiques
:class: tip

Il existe des corps qui possèdent plusieurs état correspondant à une même phase, on parle alors de variétés allotropiques d'un corps.

Très souvent, les corps possèdent des variétés allotropiques solides: il s'agit de différents arrangements cristallins possibles des différents atomes (cf cours de Cristallographie en chimie).

````

````{admonition} Exemple : Variétés allotropiques diverses
:class: tip, dropdown

La glace possède 7 variétés allotropiques différentes. Un zoom sur sur le diagramme (T,P) permet de faire figurer ces différentes variétésOn peut s'en convaincre en regardant un glaçon sorti du congélateur, le contour est transparent (c'est un arrangement laissant passer la lumière) alors que le centre est opaque (c'est un arrangement qui ne laisse pas passer la lumière).

```{figure} ./images/thermo_chap_6_diag_pt_glace.jpg
:name: fig_283
:align: center

```

Le fer possède deux arrangements cristallins solides à pression atmosphérique: cubique centré et cubique face centrée. Le passage de l'un à l'autre en présence de carbone est appelé austénisation (terme qui n'est pas à connaître) et est à la base de la formation d'un acier dur.

L'hélium 4 est un exemple de corps possédant des variétés allotropiques liquide appelées hélium fluide (Type I) et hélium superfluide (Type II). Le second existe à très basse température et ne possède pas de viscosité (frottements): il peut monter par capillarité le long des parois d'un verre.
````

## Diagramme de Clapeyron

### Diragramme de Clapeyron et Isotherme d'Andrews

````{admonition} Définition : Diagramme de Clapeyron
:class: tip

Un diagramme de Clapeyron et un diagramme où l'on représente la pression du système en fonction du volume massique total du système.

Une isotherme d'Andrews correspond au tracé d'une transformation isotherme d'un corps pur donné sur un diagramme de Clapeyron.

````

````{admonition} Fondamental : Observation
:class: attention

Quand 2 phases coexistent à température constante (sur une isotherme d'Andrews), la pression est fixée. On parle de __palier__.

Mais le volume massique total du système peut encore varier (et donc le volume aussi).
````


__Description des isothermes__  
```{figure} ./images/thermo_chap_6_diag_pv.jpg
:name: fig_284
:align: center

```

* Parties liquides et solides: On remarque que dans la zone où le solide existe seul, la pression augmente très fortement pour une faible variation de volume massique: cela signifie que soumis à des contraintes "normales", le volume d'un solide varie très peu. Il en est de même pour la phase liquide (cf zoom): on parle alors de __fluide incompressible__.
* Partie gazeuse: Dans les zones où seul le gaz existe, les variations sont plus faibles, on peut essayer de modéliser ces variations (gaz de Van der Waals ou développement du Viriel - cf. TP).
* Equilibre de deux phases: Dans les zones où deux phases sont en équilibre, on observe des paliers. On retrouve le fait que si on fixe la température, la pression au changement d'état est fixée. Le "point triple" correspond ici...  à une droite: on peut encore faire varier le volume massique.
* Point critique: Au dessus d'une température appelée température critique $T_C$, il n'existe plus de zone de coexistence liquide/gaz et on passe continuement d'un fluide à l'autre: il n'existe donc qu'un fluide discernable appelé fluide hypercritique.



### Cas de l'équilibre liquide-vapeur

_Rappel : Caractéristiques déjà observées._  
La zone entourant l'équilibre liquide vapeur est la zone à savoir tracer (avec notamment les courbes de rosées et d'ébullition). On retiendra qu'on a déjà vu:

* l'existence du point critique
* l'influence du caractère incompressible des liquide sur les isothermes.




__Courbes frontières et existence des phases__  
```{figure} ./images/thermo_chap_6_diag_pv_liqvap.jpg
:name: fig_285
:align: center

```

Aux faibles volumes, on trouve la zone de phase liquide. Aux forts volumes la zone de phase gazeuse. Entre les deux se trouve la zone de coexistence liquide-vapeur. Aux fortes pressions/fortes températures, une zone correspond à un état super-critique.

* __Courbe d'ébullition:__ C'est la courbe qui sépare l'état {liquide seul} de l'état {liquide+gaz}. Elle correspond à l'apparition de la première bulle de gaz dans le liquide. La masse volumique d'un point de la courbe d'ébullition à la température T (point I) correspond à __la masse volumique du liquide__ à cette température qu'il soit seul ou en équilibre avec le gaz.
* __Courbe de rosée__: C'est la courbe qui sépare l'état {gaz seul} de l'état {liquide+gaz}. Elle correspond à  l'apparition de la première goutte de liquide dans le gaz. La masse volumique d'un point de la courbe de rosée à la température T (point F) correspond à __la masse volumique du gaz__ à cette température qu'il soit seul en en équilibre avec le gaz.




__Types d'isothermes__  
* Isotherme supercritique $T > T_C$: Elles sont toujours descroissantes, sans point où la pente est nulle. On rappelle qu'on ne distingue alors pas de phase gazeuse ou liquide et qu'on parle de phase supercritique.
* Isotherme critique $T = T_C$: Elle passe par le point critique. La courbe a en ce point un point d'inflexion et la pente est nulle.
* Isotherme sous-critique à $T < T_C$: Au dessous de la température critique, l'isotherme d'Andrews passe par un palier à une pression donnée lors de l'équilibre liquide-gaz. Cette pression est appelée pression de vapeur saturante.



````{dropdown} Remarque

__Evolution des masses volumiques__  
On remarque d'abord que le volume massique du gaz est supérieure à le volume massique du liquide. Quand on est suffisamment loin de $T_C$, __le volume massique du liquide est souvent négligeable devant le volume massique du gaz__.

Par contre, la largeur du palier diminue quand la température augmente: cela signifie que les masses volumiques des deux fluides tendent à se rapprocher quand on se rapproche du point critique.
````

### Retard au changement d'état: Etat métastable

````{admonition} Définition : Etat métastable
:class: tip

Un état métastable est un état du système thermodynamiquement instable, c'est-à-dire ne pouvant exister dans les conditions de température et de pression données, mais pouvant exister sur un temps relativement long (on parle de stabilité cinétique).

Un très légère perturbation suffit en général à permettre au système de retourner dans un état stable. Ce retour est extrêmement rapide.

````

````{admonition} Exemple : Eau en surfusion
:class: tip, dropdown

Si l'on place une bouteille d'eau au congélateur, on peut, en refroidissant doucement obtenir de l'eau encore liquide à $T<0^{\circ}C$ et $P=1atm$. On parle de surfusion du liquide ou de liquide en surfusion (terme général). On pourra observer ce phénomène dans de nombreuses vidéos en ligne.
````

````{admonition} Compléments : Obtention d'un état métastable
:class: hint, dropdown

```{figure} ./images/thermo_metastable.jpg
:name: fig_286
:align: center

```

Un état métastable correspond par exemple à un état où le liquide devrait commencer à s'évaporer mais au lui de suivre l'isotherme d'Andrews sur le palier, le système reste entièrement liquide et la pression continue à diminuer quand le volume massique augmente. C'est pourquoi on parle de retard au changement d'état. Il peut se produire la même chose pour la vapeur (appelée alors vapeur sursaturée).
````

## Enthalpie de fusion

### Enthalpie de changement d'état


__Observations expérimentales__  
On considère un 1kg de glace à $-10 ^{\circ}C$. On le chauffe par apport constant de chaleur en maintenant la pression du système constante et on mesure l'évolution temporelle de la température. On observe l'évolution ci-après:

* Quand on observe la montée chute de température, le système est toujours solide.
* Au moment où la température se stabilise, la glace commence à fondre
* Quand la température recommence à monter, on a observé que la totalité de la glace s'était liquéfiée.


Interprétation: On peut considérer que l'expérience est monobare donc $\Delta H = Q >0$

* Pour les systèmes monophasés (eau seule ou glace seule), ce sont des phases condensés donc $\Delta H = C_V \Delta T$. Il est donc logique d'obtenir une augmentation de température.
* Pour le système diphasé, la température ne variant pas, ce n'est pas la source de variation d'énergie. Or l'enthalpie augmente nécessairement. C'est donc le changement d'état (fusion) qui nécessite un apport d'enthalpie.


__D'une manière générale, quand il se produit un changement d'état du système, l'enthalpie de ce dernier varie (positivement ou négativement).__  


````{admonition} Définition : Enthalpie massique de changement d'état
:class: tip

On appelle enthalpie massique de changement d'état à la pression P, la variation d'enthalpie $\Delta h$ du corps pur au cours du changement d'état complet d'un kilogramme du corps pur considéré à la pression donnée.

````


On parle aussi de chaleur latente massique de changement d'état. L'évolution lors du changement la pression est fixée (puisqu'on fixe la température par définition de la grandeur), l'évolution est donc nécessairement isobare et on peut écrire: $\Delta h = q$ au cours de la transformation.


````{admonition} Attention : 
:class: note

Même si on l'appelle "enthalpie", il s'agit bien d'une variation d'enthalpie. Sa valeur dépend du corps pur __et de la température__.

````

````{admonition} Exemple : Enthalpie de vaporisation
:class: tip, dropdown

La variation d'enthalpie en cours d'une vaporisation d'1kg de liquide est appelée enthalpie massique de vaporisation. On la note $\Delta h_{v}$ ou $l_{v}$. On pourra nommer chaque enthalpie massique de changement d'état de la même manière. On indice en général les enthalpie de changement d'état de manière claire pour préciser de quel changement d'état il s'agit.
````


__Ordre de grandeur__  
Pour l'eau à pression atmosphérique ($P=101,3\rm{kPa}$).

* Enthalpie de fusion (T=273K): 334kJ/kg
* Enthalpie de vaporisation (T=373K): 2830 kJ/kg


Il faudrait donc fournir 334kJ pour faire fondre 1kg de glace. A titre de comparaison, il faudrait fournir 4,2kJ=1kcal pour augmenter de 1K la température de l'eau liquide à température ambiante.



__Intérêt des changements d'état__  
On remarque que pour vaporiser du liquide, il faut fournir de l'énergie. Ce principe est utilisé dans des systèmes de climatisation des terrasses. On projette de fines gouttelettes d'eau dans l'air. Ce dernier étant plus sec, les gouttelettes vont se vaporiser mais pour cela elle vont capter l'énergie nécessaire au changement d'état au milieu extérieur. En prélevant ainsi de la chaleur à l'air ambiant, elle refroidissent l'air de la terrasse.

De manière générale, les grandeurs quantité d'énergie libérée ou prélevée lors d'un changements d'état encouragent à les utiliser dans des machines thermiques.



__Enthalpie de changement d'état et température__  
Il est important de savoir que l'enthalpie de changement d'état dépend de la température. Il existe certaines loi pour certains corps purs sur certaines gammes de températures mais aucune n'est à connaître.

L'enthalpie de changement d'état tend vers 0 quand on se rapproche du point critique.


### Diagramme p-H


```{figure} ./images/thermo_chap_6_diag_ph.png
:name: fig_287
:align: center

```


````{admonition} Définition : Diagramme p-H
:class: tip

Comme son nom l'indique, un diagramme p-H est un diagramme où l'on représente la pression en fonction de l'enthalpie. Plusieurs propriétés sont observées.

* Isotherme et isobare: On retrouve que les isotherme sont aussi les isobare __quand le système est diphasé.__.
* Isotherme de la phase liquide: En phase liquide (phase condensée), l'enthalpie ne dépend presque que de la température, donc les isothermes sont quasi-verticales.
* Isotherme de la phase gazeuse: En phase gazeuse suffisamment loin de la courbe de rosée, les isothermes sont quasiverticales, ce qui signifie qu'en première approximation, le gaz sui la deuxième loi de Joule.


````

## Synthèse dans un diagramme (P,V,T)


On donne à titre indictaif la surface des états possibles ainsi que les différentes phases dans un diagramme à 3 dimensions. Sa représentation ou son analyse ne sont pas à connaître.

```{figure} ./images/thermo_chap_6_diag_ptv.jpg
:name: fig_288
:align: center

```


