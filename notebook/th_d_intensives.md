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

### Température: Définition

````{important} __Définition : Température (thermodynamique)__

Soit un système dont l'entropie est notée S, l'énergie interne U et le volume V. On définit la température du système par la grandeur:

\begin{equation}
T = {\left(\frac{\partial U}{\partial S}\right)}_{V}
\end{equation}
````


Il s'agit d'une définition très abstraite qui nous servira peu par la suite. Nous allons voir d'autres interprétation de la température (qui sont parfois considérées comme des définitions) et qui permettront de faire des interprétations physiques de la températures.


### Température cinétique

````{important} __Fondamental : Température (cinétique) - Admis__

L'énergie cinétique moyenne de translation des particules d'un gaz s'écrit en fonction de la température sous la forme:

\begin{equation}
\overline{E_c} = \frac{3}{2}k_B T
\end{equation}
On parle pour interprêter cette température de "température cinétique".

$k_B$ est la constante de Boltzmann.
````


On rappelle que cette interprétation permet de relier la température à la vitesse quadratique moyenne et donc à l'agitation des particules: ce qu'on appelera __agitation thermique__.



__Equivalence :__  
L'équivalence entre la définition thermodynamique de la température et son interprétation cinétique est admise.


````{dropdown} Remarque : __Thermalisation__  

On remarquera que le passage des aspects microscopiques à la notion de température fait "perdre" de l'information. On a en effet accès la valeur moyenne de la vitesse quadratique et non à sa statistique.

Considérons par exemple deux gaz parfaits aux températures $T_1$ et $T_2$ contenus dans deux enceintes séparées par une paroi amovible. On peut calculer l'énergie cinétique moyenne par particule du système composé des deux gaz etlui associer une "température cinétique":

\begin{align*}
\overline{E_c} &= \frac{N_1}{N_1 + N_2} \overline{E_{c,1}} + \frac{N_2}{N_1 + N_2} \overline{E_{c,2}}\\
&= \frac{3}{2}k_B\left(\frac{N_1}{N_1 + N_2} T_1 + \frac{N_2}{N_1 + N_2} T_2\right)\\
T_C &= \frac{2}{3 k_B} \overline{E_c}\\
&= \frac{N_1 T_1 + N_2 T_2}{N_1 + N_2}
\end{align*}
Cette température n'a pas forcément de sens, notamment si la paroi est calorifugée, c'est-à-dire qu'elle ne laisse pas passer la chaleur. Dans ces conditions, la statistiques des vitesses va garder la présence de deux "pics" de densité autour des vitesses quadratiques moyennes de chaque gaz.

Par contre, supposons maintenant que la paroi laisse passer la chaleur. Alors le système va évoluer vers une température uniforme dans les deux enceintes. Pour la calculer, il suffit de remarquer que le système constitué des deux gaz est isolé (on néglige l'énergie interne de la paroi) de sorte que l'énergie cinétique de translation totale est celle calculée précédemment et la température finale est la moyenne calculée précédemment.

La différence est que d'un côté, ce calcul a un sens (il correspondrait à la mesure donné par un thermomètre) et de l'autre elle n'en a pas (cas la température n'est pas homogène). Dans le cas où la paroi laisse passer la chaleur, la statistique des vitesse va évoluer pour ne faire apparaître qu'un seul "pic" autour de la nouvelle vitesse quadratique moyenne globale.

On remarquera que pour passer de deux températures séparées à des températures égales, les deux gaz s'échangent de l'énergie par l'intermédiaire de la paroi: les particules plus énergétiques (plus chaudes) dans un gaz perdent un peu d'énergie au contact de la paroi et cette énergie, a lieu d'être restituée au même gaz sera prélevée par le second (cet effet est statistique sur un grand nombre de chocs). On parle de thermalisation.
````

### Température: Propriétés et mesures

````{important} __Fondamental : Principe zéro__

Tous les systèmes en équilibre thermique avec un système donnée sont en équilibre entre eux. Ce principe se vérifie expérimentalement. On dit alors que tous ces systèmes sont à la même température.

Ce principe sera démontré pour la température thermodynamique au moyen du second principe.
````


__Thermomètre :__  
Ce principe 0 est la base des premiers principes de mesure de la température: on place le système étudié en contact thermique avec une appareil de mesure(un thermomètre) et on atteint __l'équilibre thermique__. La température du thermomètre est alors celle du système. On s'arrange alors pour que l'influence de T sur le thermomètre soit quantifiable.

Par exemple, dans le cas des thermomètres "classiques" il s'agit d'un fluide qui se dilate dans un tube capillaire sous l'effet de la température. On associe à T une hauteur de dilatation.



__Thermomètres modernes :__  
Si la majorité des thermomètres "grand public" nécessite encore une mise en contact thermique, certains thermomètres modernes peuvent s'en passer en utilisant une mesure par rayonnement thermique.


### Température absolue


A l'inverse de la température cinétique qui donne une interprétation microscopique, la température dite "absolue" permet une interprétation en terme de mesure expérimentale et donc une vision macroscopique.

Cette interprétation vient du besoin, après l'utilisation de très nombreuses échelles de mesures (les plus persistentes sont le Celsius et le Farenheit) de créer une "définition" (ça a été une définition) de la température basée sur des propriétés fondamentales et non sur des phénomènes particuliers subjectifs (on choisit aribitrairement de placer le 0$\circ$C au gel de l'eau à température ambiante mais ce 0 n'a pas de valeur "absolue".

Avec la température absolue (dont l'unité sera le Kelvin K), on définit un 0 issu de propriétés fondamentales et comme valeur limite basse (il ne peut y avoir de température négative). Il restera à choisir une échelle (arbitraire).


````{important} __Fondamental : Expérience de Boyle-Mariotte__

```{figure} ./images/thermo_amagat.jpg
:name: fig_270
:align: center

```

On dispose d'une masse m donnée de gaz maintenue à température constante dans une enceinte thermostatée. On peut faire varier la température $\theta$ (définie comme une température relative --- échelle de Celsius) du thermostat. Un système de vase communiquant permet de faire varier le volume et la pression du gaz. L'expérience consiste à suivre l'évolution du volume V et de la pression P du gaz pour une température $\theta$ donnée.

Boyle et Mariotte ont montré qu'on pouvait interpoler la valeur limite du produit PV quand P tendait vers 0 par une valeur $PV_{P=0}$ qui ne dépendait que de la température $\theta$, quel que soit le gaz considéré. On dit que le comportement des gaz est alors parfait.
````

````{important} __Définition : Température absolue__

On définit la température absolue à partir d'un point de référence $T_R = 273,16 \rm{K}$ au point triple de l'eau et telle que $T=0$ quand pour un gaz, $PV_{P=0} = 0$. La température T "absolue" est alors définie comme la limite du produit $\frac{PV}{nR}$ lorsque P tend vers 0 pour un gaz.

````

````{dropdown} Remarque : Le point triple

Le choix de la valeur du point triple de l'eau permet de garder la même échelle que pour les Celsius: une variation de $100^\circ$C correspond à une variation de 100K.

En pratique, l'utilisation de cette définition de manière empirique passe par l'emploi d'un thermomètre à gaz:on met le système dont on veut mesurer la température en contact thermique avec un gaz dont le comportement est parfait et dont on mesure la température (au moyen de la loi des gaz parfaits).

La définition précédente est cohérente (admis) avec la définition de la température thermodynamique. On parlera de température sans préciser sa définition par la suite.
````

## Pression

### Pression: Définition

_Rappel : Définition empirique : On rappelle qu'on peut définir la pression de manière empirique comme la force surfacique exercée par le fluide normalement à la surface de contact. $\overrightarrow{dF} = P \overrightarrow{dS}$_


_Rappel : Origine microscopique : On rappelle que la pression peut-être vue comme un transfert de quantité de mouvement par unité de surface et de temps normalement à la surface de contact (on parlera de flux)._

Comme on l'a déjà précisé, cette interprétation sera surtout utilisée pour exprimer la pression d'un fluide sur une paroi. On parle de __pression cinétique__. On peut calculer la force moyenne exercée par une particule sur la paroi puis sommer les forces exercées par l'ensemble des particules qui heurtent la paroi par unité de temps. Un tel calcul sera réalisé dans le cadre de l'étude de la pression cinétique d'un gaz parfait.


````{important} __Définition : Pression thermodynamique__

Soit un système dont l'entropie est notée S, l'énergie interne U et le volume V. On définit la pression du système par la grandeur:

\begin{equation}
P = - {\left(\frac{\partial U}{\partial V}\right)}_{S}
\end{equation}

````


Cette dernière définition est relativement abstraite et ne sera pas (peu) utilisée dans la suite. Il s'agit néanmoins de la définition fondamentale. On admettra la cohérence de cette définition avec les deux premières.


````{dropdown} Remarque

__Pression des gaz :__  
En général, on considérera que la pression des gaz est uniforme. Cela est justifié pour des systèmes de tailles "normales" puisqu'on a vu précédemment que la pression ne variait que faiblement sur des distances de l'ordre du mettre.

Pour les fluides incompressibles, on fera plus attention à la __possible__ nécessité de travailler avec une pression non uniforme.
````

### Méthode: Calculer une pression


Très souvent, on sera amené à caractériser un état d'équilibre, c'est-à-dire à déterminer les variables d'état (pression volume, température) dans l'état considéré

La mise en équation nécessaire passe par l'écriture des équilibres: thermiques (égalité de température), chimiques (en ...  chimie) et mécanique. On se propose ici d'utiliser ce dernier pour déterminer la pression d'un gaz.


````{admonition} Exercice 
:class: attention

On considère un gaz contenu dans une enceinte fermée sur un côté par un piston de section S et de masse M glissant sans frottement sur les paroi de l'enceinte. De l'autre côté du piston se trouve une atmosphère à pression $P_0$.

1. Déterminer la pression du gaz à l'équilibre en fonction de M,g, S et $P_0$ suivant que le piston se trouve sur une face latérale ou sur la face supérieure de l'enceinte.
1. Déterminer le volume de l'enceinte à l'équilibre en supposant que la température du gaz est maintenue à $T_0$ et que le gaz suit le modèle du gaz parfait.


````
````{dropdown} Méthode : Utilisation d'un équilibre mécanique

>Un équilibre mécanique est traduit par un théorême de la résultante dynamique à l'équilibre sur la paroi mobile - ici le piston. On travaille dans le référentiel de l'enceinte supposée galliléen.
>
>On note Ox l'axe vertical ascendant et Oy un axe horizontal.
>
>Les actions qui s'exercent sur le piston sont:
>
>* l'action de la paroi. Elle n'a pas de composante suivant le déplacement du piston puisqu'il n'y a pas de frottements.
>* l'action de __l'atmosphère extérieure.__  
>* l'action du gaz
>* l'action de la pesanteur.
>
>
>Cas horizontal. On projette suivant Ox (dirigé du gaz vers l'extérieur):
>
>\begin{align*}
0 &= PS - P_0 S\\
P &= P_0
\end{align*}
>Cas vertical. On projette suivant Oz:
>
>\begin{align*}
0 &= PS - P_0 S - Mg\\
P &= P_0 + \frac{Mg}{S}
\end{align*} 

```{attention}

Plusieurs erreurs fréquentes sont rencontrées lors de l'établissement de l'équilibre mécanique.

* Très souvent, l'étudiant écrit directement $P = P_0$ sans tenir compte des autre action.
* De nombreuses erreurs de signe peuvent se produire.


```


_Calcul des forces de pression :_ En thermodynamique, on sera souvent amené à étudier des forces de pressions uniformes sur des surfaces planes. Il n'est pas nécessaire dans ce cas de passer par un calcul intégrale: la force de pression est directement la pression multipliée par la surface (reste à l'orienter correctement).

````

## Exemple : Etude d'un gaz


Cet exercice se propose de mettre en relation les caractéristiques microscopiques et macroscopiques d'un gaz pour en connaître les ordres de grandeurs.


````{admonition} Exercice 
:class: attention

Considérons une mole d'argon ($M = 39,9 \rm{g.mol^{-1}}$) considérée comme un gaz parfait contenu dans un récipient de volume $V=22.4\rm{L}$ et à une température $T=273,15\rm{K}$.

1. Déterminer la pression du gaz.
1. Déterminer le nombre de particules et la distance moyenne entre deux particules proches.
1. Déterminer l'énergie cinétique moyenne et la vitesse quadratique moyenne des particules.
1. En déduire un estimation du temps entre deux chocs sur une paroi. Commenter le principe de calculer une force "moyenne" pour étudier une force de pression.
1. On définit le __libre parcours moyen__ d'une particule comme la distance moyenne que parcourt la particule entre deux chocs. On peut montrer qu'il vaut $l=\frac{1}{\sqrt{2}n^* \pi d^2}$ où d est le diamètre des particules et $n^*$ la concentration en particule.
    1. Reexprimer le libre parcours moyen en fonction de la pression, de la température et de d.
    1. A température ambiante et pression ambiante, le libre parcours moyen est d'environ 100nm. Représenter qualitativement la trajectoire d'une particule. Commenter.
    1. Estimer le diamètre des particules. Commenter.


````

````{dropdown} Résolution

>__Pression__  
>$P = \frac{nRT}{V} = 10^5 \rm{Pa}$.
>
>
>
>__Distance inter atomique__  
>$N = n N_A = 6 \times 10^{23} \rm{particules}$
>
>On peut estimer le volume moyen libre entourant une particules par $V^* = \frac{V}{nN_A}$. En assimilant ce volume à un cube, la distance moyenne entre deux particules proches se de l'ordre de $d \sim {\left( \frac{V}{nN_A}\right)}^{1/3} = 3 \times 10^{-9} \rm{m}$.
>
>On remarque que cette distance est grande devant la taille des atomes. Dans une modélisation en terme d'interaction entre dipôle électrostatique, on pourrait considérer que cette distance suffit à négliger les interactions à distance entre particules.
>
>
>
>__Vitesse quadratique moyenne__  
>On utilise l'interprétation cinétique de la température $\overline{E_c} = \frac{3}{2}k_B T = 5 \times 10^{-21} J$ (on pourra remarquer que cette énergie est faible devant 1eV).
>
>Pour calculer la vitesse quadratique moyenne, on a besoin de la masse d'un atome d'argon qu'on va déterminer à partir de sa masse molaire: $m = \frac{M}{N_A}$
>
>Il vient une vitesse quadratique moyenne $v = \sqrt{\frac{2 \overline{E_c}N_A}{M}} = 1.2 \times 10^2 \rm{m.s^{-1}}$
>
>On remarquera qu'il s'agit de vitesses très importantes. Ce déplacement n'est pas "visible" car il se fait dans toutes les directions de sorte que la vitesse moyenne de déplacement reste faible.
>
>
>
>__Fréquence des chocs__  
>Pour un volume V, on peut considérer que la taille caractéristique de l'enceinte est $L = V^{1/3}$. La distance parcouru entre deux chocs sur une même paroi par une particule est de l'ordre de 2L et donc le temps deux chocs sur une paroi pour une particule est de l'ordre de $\frac{2L}{v}$. Avec N particules, la fréquence des chocs est donc de l'ordre de $f_{choc} \sim \frac{Nv}{2L} \sim 1.2 * 10^{26} \rm{Hz}$.
>
>On observe qu'il y a donc un très grand nombre de chocs. Pendant une durée infinitésimale (mais associée à une échelle mésoscopique) dt, on pourra considérer que ce nombre reste grand et motive une étude statistique. On travaillera ainsi avec des forces moyennes exercées par les particules.
>
>On pourra remarquer aussi que les fréquences des chocs est bien plus grandes que la fréquence de mesures que peut prendre un capteur de pression. Ce dernier mesure donc aussi une force __moyenne.__  
>
>
>
>__Libre parcours moyen__  
>De l'équation d'état des gaz parfait, il vient que $n^* = \frac{N}{V} = \frac{PN_A}{RT} = \frac{P}{k_B T}$ (on retiendra que $R = N_A k_B$). Il vient $l = \frac{k_B T}{\sqrt{2}\pi d^2 P}$.
>
>Il s'agit donc d'une trajectoire erratique, on parlera de chaos moléculaire. On peut par contre remarquer que cette distance est grande devant la taille des atomes.
>
>$d = \sqrt{\frac{k_B T}{\sqrt{2}\pi P l}} \sim 3 \times 10^{-10} \rm{m}$. Il s'agit donc à peu près de la taille d'un atome. Elle est légèrement plus grande du fait qu'on tient compte de la portée de l'interaction entre particules.

````

