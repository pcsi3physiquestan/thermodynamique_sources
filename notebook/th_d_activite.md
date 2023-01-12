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
# Activités

## Vitesse quadratique moyenne

````{admonition} Exercice 
:class: attention

Une système est isotrope si __aucune direction dans l'espace n'est privilégiée__.

1. La statistique des grandeurs microscopiques est globale au système. Si le système est à l'équilibre, que peut-on dire de la statistique d'une grandeur?
1. Si le système est de plus isotrope, que peut-on dire des statistiques des composantes de vitesse dans les trois directions $v_x, v_y$ et $v_z$? Que peut-on aussi dire de leur moyenne?
1. Même question concernant la statistique des carrés des composantes $v_x^2, v_y^2$ et $v_z^2$? En déduire une relation entre $\overline{v_x^2}$ et $u$ la vitesse quadratique moyenne.
1. Exprimer l'énergie cinétique moyenne par particule lié à la translation des particules. En déduire une utilité de la vitesse quadratique moyenne. On supposera que toutes les particules sont identiques.
````

````{important} A retenir
* A l'__équilibre__, la distribution statique ne varie pas.
* Sous l'hypothèse d'__isotropie__ les vitesses moyennes (et au carré) sont les mêmes dans toutes les directions de l'espace.
* Sous l'hypothèse d'__isotropie__, il vient:

$$
\overline{v_{z}^2} = \overline{v_{y}^2} = \overline{v_{x}^2} = \frac{1}{3}u^2
$$
où $u$ est la vitesse quadratique moyenne.

* La vitesse quadratique moyenne est reliée à l'énergie cinétique moyenne des particules:

$$
E_c = \frac{1}{2} m_{particule} u^2
$$
````