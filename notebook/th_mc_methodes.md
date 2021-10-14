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
# Méthodes d'études

## Méthodes d'étude d'une machine thermique


Il existe différentes méthodes d'étude d'une machine thermique suivant son fonctionnement et sa description.

La première, très générale consisteà décrire simplement les sources avec lesquelles la machine échange et le travail total W sur le cycle. On utilise en général les diagrammes proposés au début du chapitre. L'étude consiste à utiliser les deux principes sur le cycle complet. Les exemples sont ceux qui ont été donné précédemment, notamment dans le calculs des efficacités/rendement de Carnot.

L'intérêt de cette méthode est sa simplicité mais elle permet la description de la réalisation technologique qui peut donner des informations supplémentaires. Deplus, on perd la "temporalité" des transformations.

La seconde méthode consiste à décrire les étapes successives de la transformation du système contenu dans la machine thermique (carburant ou fluide caloporteur). Les descriptions précédentes du cycle de Beau de Rochas et du cycle de Rankine en sont des exemples. On distingue néanmoins l'étude de ces deux cycles.

* Dans le cas du moteur à explosion, le fluide est contenu dans un cylindre et ne se déplace pas durant les transformations. On applique donc les lois habituelles.
* Dans le cas du cycle de Rankine (et dans beaucoup de cas étudiés dans les machines thermiques), le fluide qui subit les transformations circule dans des conduites et passe par différents organes ou il subit détente, compression ou échange thermique. On __doit donc l'étudier comme un fluide en écoulement__.



## Moteur à explosion

````{admonition} Exercice 
:class: attention

On se propose d'étudier la modélisation proposée du cycle de Beau de Rochas

Dans la suite, nous allons faire une étude thermodynamique du gaz et nous supposerons que la capacité calorifiques du gaz avant et après la combustion est la même. Ceci n'est pas rigoureusement exact car la combustion de l'essence change la composition du mélange (par exemple apparition de CO2 et disparition de du carburant). Néanmoins, cette supposition, bien qu'inexacte donne une très bonne approximation car en réalité, le rapport air/essence est nettement en faveur de l'air dans les voitures (environ 16g/18g d'air pour 1g d'essence, sinon, on noie le moteur). On peut donc en première approximation assimiler le mélange à celle du gaz: l'air. On suppose le gaz parfait de coefficient $\gamma$

1. Dessiner le diagramme de Watt théorique du moteur? Rechercher des tracés approximatifs du diagramme réels. Commenter en terme de travail fourni.
1. La compression isentropique de la phase 2 est-elle un temps moteur ou récepteur? Préciser comment, dans la pratique, la puissance est-elle fournie au cylindre durant cette phase?
1. Déterminer le rendement du cycle en fonction du rapport des volumes $\alpha_{1,2} = \frac{V_1}{V_2}$.
1. Pour $\gamma=1,4; V_2 = 0,2 \rm{L}; V_1 = 1.8 \rm{L}$, déterminer le rendement $\rho$.


````

## Cycle de Rankine

````{admonition} Exercice 
:class: attention

Représenter sur un diagramme de Clapeyron le cycle de Rankine.

Un calcul de l'efficacité d'un congélateur utilisant un cycle de Rankine inversé et proposé en devoir libre.

````

