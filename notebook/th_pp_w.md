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
# Travail mécanique

## Travail: Généralités

_Rappel : Calcul du travail mécanique_  
Le calcul du travail mécanique s'effectue au moyen des définitions classiques présentées dans le cours de mécanique.

Dans le cas (rare au programme) où il s'agit d'une action globale, on pensera bien à calcul le travail de chaque action ponctuelle puis de réaliser la sommation (en général une intégrale- cf. suite).

Dans le cas de force conservative, on peut utiliser l'énergie potentielle mais attention, elle fait partie de l'énergie totale et non de W.


````{dropdown} Remarque

__Action globale surfacique__  
On considère une action globale $\cal A$ regroupant des actions ponctuelles en plusieurs points M d'une surface $\Sigma$ du système. On modélise chaque action ponctuelle par une force $\overrightarrow{d^2F}(M)$ qui s'applique sur la petite surface $\overrightarrow{d^2S}(M)$ autour du point M.

Le travail élémentaire fournit par l'action ponctuelle autour de M pendant un temps dt s'écrit: $\delta^3 W = \overrightarrow{d^2F}(M)\cdot\overrightarrow{dl}(M)$ où M est le déplacement élementaire du point M (et donc de la surface $\overrightarrow{dS}(M)$.

```{figure} ./images/force_surfacique.png
:name: fig_272
:align: center

```

Le travail __élémentaire__ total fournit par l'action globale s'obtient par intégration sur la surface de contact:

\begin{equation}
\delta W = \iint_{M\in\Sigma} \overrightarrow{d^2 F}(M) \cdot \overrightarrow{dl}(M)
\end{equation}
Si nous serons pas amené à calculer une telle intégrale, il faut comprendre le sens des différents infinitésimaux utilisés ici. Pour la force, il s'agit d'un infinitésimal __spatial__ (un double infinitésimal puisque la force est surfacique). C'est ce double infinitésimal qu'on intégre (sur la surface donc).

Pour le déplacement élémentaire et le $\delta W$, il s'agit d'un infinitésimal __temporel__: un déplacement et un transfert énergétique durant un instant dt.
````

## Dipôle électrique

_Rappel : Puissance électrique reçue_  
Soit un dipôle électrique D parcouru par une intensité i et dont la tension à ses bornes est u en convention récepteur. Alors la puissance qu'il reçoit du reste du circuit est $P = ui$.

Si l'on isole le dipôle comme un système thermodynamique, il faut tenir compte de cette puissance mécanique (issue d'actions mécaniques de type électromagnétiques - on l'appelle parfois puissance électrique) quand on utilise le premier principe.

Le "travail électrique" reçu par le dipôle durant un temps fini sera donc:

\begin{equation}
W = \int_{t_1}^{t_2}u(t)i(t)dt
\end{equation}\end{rappel}

````{dropdown} Remarque

__Cas d'une résistance - Effet Joule__  
Dans le cas d'une résistance, __le travail reçu W__ se calcule en utilisant la loi d'Ohm (la puissance __reçue__ est $P = Ri^2(t)$).

Cette énergie est transformée à l'échelle microscopique de manière désordonnée, c'est __l'effet Joule__. __Une partie__ de cette est énergie va être transmise __par la résistance au système extérieur__ sous forme de transfert thermique Q.

Il est important de comprendre que a priori, __$W \neq Q$__. En effet, une partie de l'énergie reçu par travail électrique peut être conservée par la résistance pour augmenter son énergie interne. L'application du premier principe à la résistance donne bien $\Delta U = W + Q$ avec $\Delta U = C_V \Delta T$ en considérant que la résistance est un solide.

Il est important de bien considérer les échanges pour une résistance: elle __reçoit un travail__ et __fournit un transfert thermique__. Le type de transfert d'énergie à  considérer sera donc différent que l'on considère la résistance à l'intérieur ou à l'extérieur du système étudié.
````

## Cas des contraintes normales extérieures

_Comme on l'a vu en introduction, le cas des forces globales peut nécéssité un traitement différents à cause de la déformation du système. Il est un cas d'action que l'on va rencontrer très fréquemment en thermodynamique, c'est le cas du travail des forces de contraintes normales qui s'exercent à la surface extérieure du système de sorte qu'il est important de connaître les méthodes de calcul de ce travail et son interprétation._

On appelle souvent ce terme "travail des forces de pression extérieures" mais notons que ce terme est ambigü car l'action n'est pas nécessairement dû à l'action normale d'un fluide (associé à une pression) mais peut aussi concernant l'action normale d'un solide. Le principe des actions réciproques permet d'expliquer pourquoi on parle de force de pression (si le système étudié est un fluide, l'action réciproque est une force de pression) mais cela peut s'avérer trompeur... 

...  car la "pression" mise en jeu est la pression __locale__ du fluide au point de contact qui:

* n'est pas forcément définie (cas d'un fort déséquilibre)
* n'est pas forcément égale à la pression du fluide. C'et le cas d'un fluide un peu hors équilibre ou sous l'effet d'une action à longue portée comme le champ de pesanteur - cf. statique des fluide). Dans ce cas, il est même compliqué de parler de __pression du fluide__ (au mieux de champ de pression).


De plus, le terme de "pression" laisse à suggérer que son expression sera toujours une terme de pression d'un fluide. Or c'est faut, dans le cas d'une action d'une paroi mobile sur le gaz, l'expression de cette contrainte normale peut être plus complexe qu'un simple "P".

Par la suite, on utilisera le terme de "contrainte normale extérieure" pour désigner la force surfacique étudié ici mais il faut savoir qu'on trouvera souvent dans les ouvrages le termes de "pression extérieure"._

### Travail des contraintes normales extérieures: Généralités


Dans toute la suite, on considèrera les actions de contact comme normale à la surface, c'est-à-dire qu'on ne tient pas compte des frottements.



__Notation__  
On considère un système $\Sigma$ soumis en chaque point M de sa surface à une force $\overrightarrow{d^2 F}(M)$.

On peut associer à cette force une contrainte normale surfacique $\sigma_{ext}(M)$ telle que $\overrightarrow{d^2 F}(M) = - \sigma_{ext}(M) \overrightarrow{d^2 S}(M)$ avec $\overrightarrow{d^2 S} (M)$ le vecteur surface associé à la surface de contact autour du point M. Il est orienté vers l'extérieur du système par convention (d'où le signe moins car que l'action extérieure viennent d'un fluide ou d'un solide, elle ne peut que pousser le système).

Comme dans l'exemple général, on note $\overrightarrow{dl}(M)$ le déplacement de la surface de contact infinitésimal sous l'effet de la déformation du système. On peut reprendre le schéma proposé pour une force surfacique. Ici la force est normale à la surface (s'il y avait une contrainte tangentielle, il faudrait la traiter à part).

```{figure} ./images/travail_pression.png
:name: fig_273
:align: center

```


````{admonition} Fondamental : Travail des contraintes normales: Expression générale
:class: attention

Considérons l'évolution du système durant un temps dt, le travail élémentaire des forces de contraintes normales extérieures s'écrit:

\begin{align*}
\delta W &= -\iint_{M \in surface(\Sigma)} \sigma_{ext} \overrightarrow{dl}(M) \cdot \overrightarrow{dS}(M)\\
 &= -\iint_{M \in surface(\Sigma)} \sigma_{ext} dV_{balaye}(M)\\
\end{align*}
où $dV_{balaye}$ est le volume balayé par la surface durant la durée dt. Il est compté positivement s'il correspond à un gain de volume pour le système et négativement s'il correspond à une perte de volume pour le système
````


__Démonstration__  
La première formule est la simple expression du travail élémentaire.

La seconde vient du fait que $\overrightarrow{dl} \cdot \overrightarrow{n}$ donne en valeur absolue la hauteur du cylindre de base dS balayé par la surface dS lors de la déformation de sorte que le produit scalaire donne bien le volume balayé $dV_{balaye}(M)$par la surface dS.


````{admonition} Attention : Volume balayé
:class: note

Le volume balayé est __albégrique__ (à cause du produit scalaire).

* Si le système perd ce volume, cela correspond au cas $\overrightarrow{dl}\cdot\overrightarrow{n} < 0$ (cas de la figure). Le travail est alors positif. On pourra le comprendre en observer que le travail est nécessairement moteur (la contrainte normale extérieure est dans le même sens que le déplacement du point de contact).
* Si le système gagne ce volume, cela correspond au cas $\overrightarrow{dl}\cdot\overrightarrow{n} > 0$ (cas non représentée). Le travail est alors négatif. On pourra le comprendre en observer que le travail est nécessairement résistant (la contrainte normale extérieure est dans le sens inverse au déplacement du point de contact).


Ce point est fondamental dans certains calculs (cf. suite) et permet d'associer au travail des contraintes normales extérieures une interprétation en terme de variation de volume. Dans le cas d'une contrainte uniforme ($\sigma_{ext}$ ne dépend pas de M) sur les parois en mouvement, le lien entre la perte/gain de volume et le caractère résistante/moteur du travail global reste le même.

````


On rappelle que le $\delta W$ correspond à une variation infinitésimale dans le temps alors que l'intégration se fait dans l'espace à un instant t donné.


### Cas à connaître: contrainte uniforme.

````{admonition} Fondamental : Contrainte uniforme sur l'ensemble du système.
:class: attention

Si la contrainte normale $\sigma_{ext}$ est uniforme l'ensemble du système (plus précisément sur l'ensemble des parois mobiles), alors le travail de la contrainte normale devient $\delta W = - \sigma_{ext} dV$ où $dV$ est la variation de volume du système total.

Le caractère algébrique du système est relié au gain/à la perte de volume total.
````


__Démonstration__  
La contrainte normale étant uniforme, on peut la sortir de l'intégrale. Il reste la sommation des volumes balayés par chaque paroi qui correspond effectivement au volume total gagné par le système.


````{dropdown} Remarque

__Transformation finie__  
Il vient que lors du passage d'un état A à un état B, le travail reçu par le système des contraintes normales extérieures devient:

\begin{equation}
W = - \int_{V_A}^{V_B}\sigma_{ext}dV
\end{equation}
````

````{dropdown} Remarque
__Pression extérieure et abus de langage__  
Comme on l'a dit, on appelle, par abus de langage ce travail "travail des forces de pression extérieures". On ne revient sur les raisons qui font de ce terme un abus mais il faut savoir que $\sigma_{ext}$ est souvent noté $P_{ext}$ (il est effectivement homogène à une pression). Si cette notation est acceptée (elle sera même trouvée dans la majorité des ouvrages), il faut faire attention car __elle est très trompeuse__.

Ce n'est en effet PAS une pression et la manière de calculer $\sigma_{ext}$ ne se ramène pas simplement à le remplacer par P (la pression du système) ou par une pression extérieure notée $P_0$. Il faut __réfléchir au système étudié pour déterminer son expression.__  
````

````{admonition} Fondamental : Cas d'une transformation quasi-statique
:class: attention

Dans le cas d'une transformation quasi-statique, le travail des contraintes normales extérieures se réécrit:

\begin{equation}
\delta W = - P dV
\end{equation}
où P est la pression (interne) du système.
````


__Démonstration__  
Dans le cas d'une évolution quasi-statique, le système étant en quasi-équilibre mécanique à chaque instant, on peut définir la pression P du système __qui est la même dans tout le système.__.

La force normale qu'exerce alors le système sur le milieu extérieur est alors (en norme) PdS. Le principe des actions réciproques permet alors d'écrire $\sigma_{ext} = P$ (le signe des deux forces réciproques apparaît dans le vecteur directeur de la force, pas dans la contrainte) qui est uniforme.

Il vient que le travail élémentaire des contraintes extérieures s'écrit alors $\delta W = - P dV$.



__Intérêt du cas quasi-statique__  
Le cas d'une transformation quasi-statique présente plusieurs intérêts. Nous en citons deux ici:

* il ramène l'expression du travail à une expression ne dépendant plus que des paramètres d'état du système (on rappelle qu'on ne peut l'utiliser que si l'évolution est quasi-statique) ce qui permet souvent de calculer le travail reçu (calcul d'une intégrale) alors que dans le cas non quasi-statique, le calcul est souvent plus délicat (mais pas impossible - toute dépend des cas).
* Comme on le verra par la suite, le cas d'une transformation quasi-statique est souvent une transformation optimale.



### Diagramme de Watt

````{admonition} Attention : 
:class: note

Dans toute la suite, on considère le cas du travail des contraintes extérieures __dans le cas quasi-statique__. Dans ce cas, la contrainte extérieure est uniforme et égale à la pression P du système, on rappelle que dans ces conditions, le travail se réécrit $\delta W = - PdV$.

````

````{admonition} Définition : Diagramme de Watt
:class: tip

Un diagramme de Watt est la représentation de la pression du système en fonction du volume du système.

````

````{admonition} Fondamental : Interprétation géométrique du travail des contraintes normales extérieures
:class: attention

Dans le cas d'une transformation quasi-statique, on peut représenter la transformation entre un état A et un état B pour un chemin dans un diagramme de Watt. Le travail des contraintes normales extérieures y est alors représenté par l'opposé de l'aire sous la courbe ainsi dessinée.

La justification vient de l'expression du travail: $W = \int - PdV$.

L'orientation du chemin permet alors de savoir si le travail reçu par le système est moteur ou résistant:

* une augmentation de volume conduit à une aire positive et donc à un travail négatif donc résistant.
* une diminution de volume conduit à une aire négative et donc à un travail positif donc résistant.


```{figure} ./images/thermo_diag_watt.jpg
:name: fig_274
:align: center

```
````

````{admonition} Définition : Cycle
:class: tip

Un cycle est une transformation ou une série de transformations ramenant le système dans son état initial.

````

````{admonition} Fondamental : Grandeurs d'état et cycle
:class: attention

La variation d'une variable d'état sur un cycle est trivialement nulle.
````

````{admonition} Fondamental : Cas des cycles: Travail des contraintes normales
:class: attention

Dans une transformation quasi-statique cyclique, le travail fourni passe par des phases motrices puis résistantes. Le signe du travail globale défini si le système a reçu ou fourni de l'énergie. On relie ce signe au sens de parcours du cycle:

* Si le cycle est parcouru dans le sens horaire, $W<0$: le système est un moteur car il fournit un travail mécanique.
* Si le cycle est parcouru dans le sens anti-horaire, $W>0$: le système est un récépteur car il reçoit un travail mécanique.

````


__Justification__  
```{figure} ./images/thermo_watt_cycle.jpg
:name: fig_275
:align: center

```

Si le cycle est parcouru dans le sens horaire, on observe que le temps où le système est récepteur correspond à un travail mécanique $\left\vert W_{recepteur} \right\vert$ plus faible que le travail mécanique $\left\vert W_{moteur} \right\vert$ du temps moteur (aire sous la courbe plus faible): le travail total reçu sera donc négatif:  le système fournit de du travail mécanique, c'est un moteur.

Si le cycle est parcouru dans le sens anti-horaire, on observe que le temps où le système est récepteur correspond à un travail mécanique $\left\vert W_{recepteur} \right\vert$ plus grand que le travail mécanique $\left\vert W_{moteur} \right\vert$ du temps moteur (aire sous la courbe plus grande) : le travail total reçu sera donc positif:  le système reçoit de du travail mécanique, c'est un récepteur.


