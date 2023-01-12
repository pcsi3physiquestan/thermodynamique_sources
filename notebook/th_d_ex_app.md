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
# Applications

````{admonition} Etude d'un gaz parfait 
:class: attention

Un récipient cubique contient sous la pression $P_0 = 1.013 \times 10^5 \rm{Pa}$ et à la température $T_0 = 273.15 \rm{K}$, $1 \rm{mol}$ d'argon de masse molaire $M = 39.9 \rm{g.mol^{-1}}$. En considérant ce gaz comme parfait, on demande de calculer:

1. le nombre d'atome du gaz
1. la masse m d'un atome
1. le volume $V$ du récipient et son arête $a$
1. le nombre moyen $n_V$ d'atome par mètre cube.
1. l'ordre de grandeur de l'espacement moyen entre deux atomes voisins
1. l'énergie cinétique moyenne $\left\langle E_c\right\rangle$ d'un atome
1. la vitesse quadratique moyenne $u$


````

````{admonition} Compressibilité du mercure 
:class: attention

Le coefficient de compressibilité isotherme du mercure ne varie pas dans le domaine considéré et vaut: $\chi_T = -\frac{1}{V} {(\frac{\partial V}{\partial P})}_{T} = -36 \times 10^{-12} \rm{Pa^{-1}}$.

1. Etablir l'expression de la différentielle de la pression dP à température constante en fonction de $\chi_T$, de la masse volumique $\rho$ et de $d \rho$ (Indice: on pourra considérer un système fermé).
1. A la surface du mercure, $\rho = \rho_0$ et $P = P_0$. En déduire l'équation donnant $\frac{\rho}{\rho_0}$ en fonction de ,$\chi_T, P$ et $P_0$. Calculer la variation relative de masse volumique lorsque la pression varie de $50 \rm{bar}$.
````

````{admonition} Capacités thermiques d'un gaz parfait
:class: attention
Démontrer les expressions des capacités thermiques __molaires__ d'un gaz parfait en fonction de $R$ et $\gamma$.
````

````{admonition} Etude d'un diagramme de Clapeyron
:class: attention

On considère le diagramme de Clapyeyron de l'eau (partie liquide-vapeur) donné ci-après. Certaines isothermes ont été représentées. __Attention au type d'échelle.__

```{figure} ./images/thermo_clap_eau_pv.png
:name: td_clapeyron_td
:align: center
Diagramme de Clapeyron de l'eau
```

1. Expliquer pourquoi on observe des paliers de températures dans certaines zones et préciser les zones correspondant à l'état liquide, vapeur et équilibre liquide-vapeur. Déterminer les pressions de vapeur saturante pour 60°C, 100°C et 200°C.
2. Déterminer la température et la pression du point critique ainsi que de le volume critique massique de l'eau.
3. On se place à 100°C dans un équilibre liquide-vapeur.
    1. Estimer graphiquement le volume massique de la partie gazeuse. Quelle hypothèse peut-on faire sur le rapport volume massique du liquide sur volume massique du gaz ?
    2. On a mesurée une fraction massique de gaz $x_g = 0.6$. Situer l'état correspondant sur le diagramme de Clapeyron
````