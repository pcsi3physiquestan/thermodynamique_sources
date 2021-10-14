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
# Généralités

## Définition


Les machines thermiques sont la base de la révolution industrielle et d'une partie du fonctionnement industriel actuel. Leur but: effectuer une conversion d'énergie (ou de puissance) incluant un transfert thermique.

Leur fonctionnement général se base sur le principe simple d'équivalence entre travail et échange thermique (ou chaleur) --- c'est-à-dire le premier principe tel que l'a énoncé Joule. On peut donc voir une machine thermique comme un système, en général un fluide passant pour différentes transformation pour soit:

* prendre et donner de la chaleur à des corps pour fournir un travail mécanique: on parlera de __moteur__.
* à partir d'un travail mécanique reçu, effectuer un échange de chaleur qui ne peut se faire naturellement (refroidir en été, chauffer une pièce en hiver... ). On distinguera deux types de machines suivant leur utilité:
* les réfrigérateurs, servant à refroidir une source froide
* les pompes à chaleur qui fonctionnement sur le même principe thermodynamique mais qui servent à maintenir une pièce à une température chaude.



La suite de transformations permettant d'effectuer cette conversion ne dure en général pas plus de quelques secondes ou quelques minutes (quelques heures pour certaines machines très particulières). Or un réfrigérateur, un moteur de voiture...  doivent pouvoir fonctionner plusieurs heures voire plusieurs mois sans qu'on doivent relancer à chaque fois la machine. Il faut donc qu'à la fin de la transformation, on soit revenu au point de départ pour recommencer la série de transformation: les machines thermiques fonctionnent en général sur des cycles (ce qui ne veut pas dire qu'il n'y a pas des transformations non cycliques à l'allumage).


````{admonition} Définition : Machines thermiques
:class: tip

Une machine thermique est constitué d'un système (M) qui, en général décrit des cycles fermés successifs. Au cours du cycle, il échange du transfert thermique $Q_i$ avec des sources de chaleur $\Sigma_i$ à température $T_i$ et du travail mécanique $W_i$ avec les systèmes mécaniques (notés $Sm_i$).

```{figure} ./images/thermo_machine_modele.jpg
:name: fig_290
:align: center

```

````


__Rendement et efficacité__  
L'intérêt d'une machine thermique est mesurée par le rapport entre l'énergie utile récupérable par l'utilisateur et l'énergie à fournir à la machine. On parle de __rendement__ pour un moteur et d'__efficacité__ pour un récepteur.


## Relations générales

__Relations générales__  

La base de l'étude des machines thermiques est l'utilisation des deux premiers principe de la thermodynamique. Rappelons que la transformation se fait sur un cycle, donc la variation des fonctions d'état est nulle pour le système:

\begin{align*}
\Delta U &= 0 = \sum\limits_{i} Q_i + \sum\limits_{i} W_i\\
\Delta S &= 0 = \sum\limits_{i} \frac{Q_i}{T_i} + S_c \geq \sum\limits_{i} \frac{Q_i}{T_i}
\end{align*} 

## Cas d'une machine ditherme

_Rappel : Principe de Carnot_  
On rappelle ce corollaire de l'énoncé de Thomson: pour qu'un système décrivant un cycle fournisse du travail, il doit nécessairement échanger du transfert thermique avec au moins deux sources à des températures différentes.



Dans le cours, nous nous intéresserons uniquement à des machines dithermes, c'est-à-dire à des machines. Il faut bien comprendre le raisonnement pour être capable de le refaire si besoin est pour des machines en contact avec un nombre supérieur de thermostats. On regroupera de plus le travail échangé dans le travail total W. Nous verrons en partie pourquoi on peut travailler uniquement avec le travail total.

_Notation: Nous allons noter avec des indices f, les données relatives au thermostat de plus basse température, ce sera donc une source froide. Nous noterons avec des indices c les données relatives au thermostat de plus haute température, ce sera donc une source chaude._


__Modélisation et équation__  

```{figure} ./images/thermo_machine_dithermej.jpg
:name: fig_291
:align: center

```

\begin{align}
W + Q_c + Q_f &= 0\\
\frac{Q_c}{T_c} + \frac{Q_f}{T_f} &\leq 0
\end{align} 

````{admonition} Attention : 
:class: note

La dernière inégalité n'est valable QUE pour des thermostats parfaits, c'est-à-dire dont la température est la même à tout instant. Dans certaines cas, une des sources (ou les deux) ne peuvent être considérées comme des sources parfaites, il faut alors revenir à l'expression générale du second principe.

````

````{dropdown} Remarque

__Typologie des machines thermiques__  
On distingue les machines thermiques en fonction des grandeurs utiles et à fournir. Remarquons d'abord que tous les échanges ne peuvent être positifs. On laissera aussi de côté les cas inutiles.

* Moteur: $W < 0; Q_f < 0; Q_c > 0$. La grandeur utile est le travail mécanique fourni $\left\vert W \right\vert$ et la grandeur à fournir est la chaleur fournie par la source chaude $Q_c$.
* Réfrigérateur: $W > 0; Q_f > 0; Q_c < 0$. La grandeur utile est l'énergie prélevée à la source froide $Q_f$ et la grandeur à fournir est le travail mécanique $W$.
* Pompe à chaleur: $W > 0; Q_f > 0; Q_c < 0$. La grandeur utile est la chaleur fournie à la source chaude $\left\vert Q_c \right\vert$ et la grandeur à fournir est le travail mécanique $W$.

````

## Cogénération

__Principe général__  

On remarque que dans les machines dithermes, l'un des échanges thermiques est inutile. Par exemple, le moteur fournit de la chaleur à la source froide.

Dans un souci de récupération d'énergie, on essaie aujourd'hui de construire des machines thermiques permettant de récupérer cette énergie pour une utilisation:

* interne: par exemple dans le cas du moteur, une partie de l'énergie libérée est réutiliser au contact de la source chaude (cf le devoir sur le moteur de Stirling)
* externe: toujours dans le cas du moteur l'énergie thermique fournit à la source froide ou le surplus d'énergie thermique venu de la source chaude sert à un système de chauffage.


Lorsqu'une machine thermique est conçue pour l'énergie mécanique ET l'énergie thermique soient toutes les deux utilisées, on parle de __cogénération.__  
 

