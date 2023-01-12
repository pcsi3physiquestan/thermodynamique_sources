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
# Equilibre thermodynamique

## Equilibre thermodynamique

```{sidebar} Echelle microscopique
S'il n'y a pas de mouvement macroscopique interne, il y a quand même un mouvement des particules: il correspond à l'agitation moléculaire. On peut rapprocher l'équilibre thermodynamique de l'équilibre dynamique en chimie (ce dernier est d'ailleurs un cas particulier de l'équilibre thermodynamique).

Par contre, à l'équilibre, la statistique des grandeurs microscopiques est supposée constante.
```
````{important} __Equilibre thermodynamique__

Un système est en équilibre thermodynamique s'il est à la fois à l'équilibre mécanique (macroscopique), thermique et chimique.

Dans un état d'équilibre, les variables d'état sont indépendantes du temps. Il n'y a alors pas de mouvement macroscopique interne (déformation mécanique du système) ni de mouvement macroscopique global accéléré.

````

```{topic} Durée d'un état d'équilibre
Un équilibre thermodynamique n'est pas indépendant de la durée d'observation: on peut ainsi étudier un mélange d'eau et de glace dans une enceinte à l'équilibre pendant plusieurs minutes et le considérer comme un équilibre. Au bout de quelques heures en plein été, la glace aura fondu... 
```

## Equation d'état

````{sidebar} Exemple : Equation d'état d'un gaz.
Pour un gaz, il suffit de connaître 3 variables d'état parmi V,P,T et n. On peut par contre choisir quelles seront les variables considérés comme indépendantes (V,P et n par exemple). La température est alors déterminée par la fonction d'état du gaz qui s'écrit, de manière générale sous la forme: $f(n,T,P,V)=0$.

> Si le comportement du gaz est modélisé par le modèle des gaz parfait, alors l'équation d'état est $PV = nRT$.
> Nous avons aussi précédemment donné le modèle de Van der Waals pour les gaz.
````
````{important} __Equation d'état__

Dans un état d'équilibre, le nombre de variable d'état __indépendantes__, c'est-à-dire qu'on peut faire varier de manière séparées expérimentalement, est inférieure au nombre de variables d'état total.

A un modèle de système donnée, on associe une __équation d'état__ qui relie les variables d'état du système.

````
