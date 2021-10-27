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
# Premier principe: Enoncé

## Premier principe: Enoncé

````{important} __Fondamental : Premier principe: Enoncé__

Pour tout système fermé, on peut définir une fonction U des variables d'état, extensive, appelée énergie interne, telle que l'énergie totale E soit conservative, c'est-à-dire qu'elle est constante si le système est isolé:

\begin{equation}
E_{TOT} = E_{c,macro} + E_{p,macro} + U
\end{equation}
````


__Remarques__  
Le premier principe est énoncé pour de __systèmes fermés__.

Dans ce principe, on affirme aussi que l'énergie interne est une __fonction d'état__ (elle ne dépend que des variables d'état). Ceci n'a rien d'évident a priori.

Dans ce principe, on affirme aussi que l'énergie interne est __extensive__.

Si l'on part de la définition microscopique de l'énergie mécanique, la conservation de l'énergie totale se comprend rapidement (mais attention, ce n'est pas une démonstration).

On peut considérer ce principe comme une application particulière du bilan effectué pour une grandeur intensive: on précise que quoiqu'il arrive le terme de création est nul.


````{important} __Fondamental : Enoncé opératoire__

Puisque l'énergie totale est conservative, elle ne peut varier que s'il y a des échanges d'énergie. Nous décomposerons les échanges d'énergie en deux types:

* le travail W: c'est le travail défini en mécanique auquel peuvent venir s'ajouter d'autres types de travail: électrique ou électromagnétique. Ils ont tous la qualité de dépendre de grandeur macroscopique extérieures.
* le transfert thermique Q: c'est un terme supplémentaire.


Le premier principe s'exprime donc: 

\begin{equation}
\Delta E_{TOT} = W +Q
\end{equation}
````

````{attention}

On se place __TOUJOURS en convention RECEPTEUR pour écrire le premier principe__  

````

## Importance de la définition du système

````{attention}

IL EST IMPERATIF DE TOUJOURS DEFINIR LE SYSTEME D'ETUDE AVANT DE CHERCHER A APPLIQUER UN THEOREME OU UNE EQUATION (Théorèmes mécaniques, premier principe, équation d'état).

````

## Notations

````{dropdown} Remarque

__Notations__  
Les variables d'état et les fonctions d'état ne dépendant que de l'état d'équilibre du système: leurs variations sont donc des différentielles totales. On écrira donc $dU$ pour une variation infinitésimale et $\Delta U$ pour une variation globale. __De même, si l'on cherche des relations entre des fonctions d'état, on peut le faire en étudiant des transformations particulières. Ces expressions seront généralisées à toute transformation.__  

Par contre, les transferts d'énergie dépendent de la transformation considérée. Ce sont des formes différentielles. On doit les calculer sur la transformation réelle. On écrira donc $\delta W$ et $\delta Q$ pour une variation infinitésimale et W et Q pour une variation globale. __Ecrire dW, dQ ou $\Delta W$, $\Delta Q$ est une faute grave.__  
````

## Typologie des transformations

````{important} __Définition : Typopologie__

On distingue plusieurs types de transformations. Cette liste n'est pas exhaustive mais ces types de transformations sont à connaître:

* __transformation isotherme__: la température est constante
* __transformation isobare__: la pression est constante
* __transformation monotherme__: le système est en contact thermique avec un thermostat, c'est-à-dire un système à température constante. Une conséquence est qu'à l'équilibre, la température du système est imposée par le thermostat. Par contre, la température du système n'est pas nécessairement celle du thermostat __pendant__ la transformation (elle n'est peut-être même pas définie).
* __transformation monobare__: le système est en contact mécanique avec une système à pression constante. Une conséquence est qu'à l'équilibre, la pression du système est imposée par le système extérieur. Par contre, la pression du système n'est pas nécessairement celle du système extérieur __pendant__ la transformation (elle n'est peut-être même pas définie).
* __transformation isochore__: le volume est constant
* __transformation adiabatique__: pas de transfert thermique: $Q=0$.
* __transformation quasi-statique__: transformation qui passe par une succession continue d'états d'équilibre. Cela implique une transformation relativement lente.
* __transformation réversible__: une transformation est réversible si on peut "inverser le cours du temps" et revenir en arrière en repassant exactement par les mêmes états d'équilibre sans violer aucune loi/principe physique.


````

````{dropdown} Remarque

Une transformation réversibles est toujours quasi-statiques. La réciproque est fausse (ex: piston huilé: les frottements fluides rendent la transformation irréversible, même si on déplace le fluide très lentement).
````

