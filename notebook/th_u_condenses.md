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
# Phases condensées

_Les phases condensées sont les phases non liquides et solides. Elles sont en général très peu compressibles, de sorte qu'on puisse considérer que leur volume (système fermé) et leur masse volumique ne varie pas._

## Cas des fluides incompressibles indilatable

* Un liquide est dit incompressible si son volume ne varie pas, quelque soit les changements de pressionqu'il subit.
* Un liquide est dit indilatable si son volume ne varie pas, quelque soit les changements de température qu'il subit.


````{important} __Energie interne et enthalpie d'un fluide incompressible et indilatable.__

L'énergie interne et l'enthalpie d'un fluide incompressible ne varient qu'avec la température (puisque le volume ne varie pas et que la pression n'a pas d'effets important sur le volume).

\begin{align*}
\Delta U &\approx C_V \Delta T\\
\Delta H &\approx C_P \Delta T
\end{align*}
On considérera que la variation du produit PV étant négligeable, la variation d'enthalpie et d'énergie interne est alors identique, soit $C_V \approx C_P$ (qu'on notera souvent C et qu'on appellera capacité thermique sans précision).
````

````{important} __Capacité thermique massique de l'eau__

La capacité thermique de l'eau liquide est $4.18 \rm{kJ.kg^{-1}.mol^{-1}} = 1 \rm{kcal.kg^{-1}.mol^{-1}}$.

````

## Solides

````{important} __Energie et enthalpie des solides__

Comme pour les liquides incompressibles, on peut négliger les variations de volumes et du produit PV de sorte que la variation d'énergie interne et d'enthalpie seront à peu près égale et ne dépendront que de la variation de température.

\begin{align*}
\Delta U &\approx C_V \Delta T\\
\Delta H &\approx C_P \Delta T
\end{align*}
A nouveau $C_V \approx C_P \approx C$.
````
