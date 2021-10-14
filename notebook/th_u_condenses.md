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

## Cas des fluides incompressibles

_Rappel : Fluide incompressible et indilatable_  
Un liquide est dit incompressible si son volume ne varie pas, quelque soit les changements de pression ou de température qu'il subit.


````{admonition} Fondamental : Energie interne et enthalpie d'un fluide incompressible et indilatable.
:class: attention

L'énergie interne et l'enthalpie d'un fluide incompressible ne varient qu'avec la température (puisque le volume ne varie pas et que la pression n'a pas d'effets important sur le volume).

\begin{align*}
\Delta U &\approx C_V \Delta T\\
\Delta H &\approx C_P \Delta T
\end{align*}
On considérera que la variation du produit PV étant négligeable, la variation d'enthalpie et d'énergie interne est alors identique, soit $C_V \approx C_P$ (qu'on notera souvent C et qu'on appellera capacité thermique sans précision).
````

````{admonition} Attention : 
:class: note

Cette fois on n'a pas d'expression des capacités thermiques contrairement au cas des gaz parfaits. A titre d'exemple (à retenir), la capacité thermique de l'eau est $4.18 \rm{kJ.kg^{-1}.mol^{-1}} = 1 \rm{kcal.kg^{-1}.mol^{-1}}$.

````

## Solides

````{admonition} Fondamental : Energie et enthalpie des solides
:class: attention

Comme pour les liquides incompressibles, on peut négliger les variations de volumes et du produit PV de sorte que la variation d'énergie interne et d'enthalpie seront à peu près égale et ne dépendront que de la variation de température.

\begin{align*}
\Delta U &\approx C_V \Delta T\\
\Delta H &\approx C_P \Delta T
\end{align*}
A nouveau $C_V \approx C_P \approx C$.
````

````{admonition} Compléments : Loi de Dulong-Petit (pas à connaître)
:class: hint, dropdown

En 1819, P. Dulong et A. Petit ont mis en évidence empiriquement que la __capacité thermique molaires__ des solides étaient sensiblement la même pour tous les solides et valaient 3R. En réalité, ceci n'est vrai qu'à partir d'une certaine température qui dépend du solide considéré. Pour les métaux, la température à partir de laquelle cette loi est valide est inférieure aux températures ordinaires.

Comment l'interpréter? On peut modéliser un métal comme un ensemble d'atomes fixes. Ceux-ci fonctionne comme des oscillateurs harmoniques spatiaux pour lesquels on a trois termes quadratiques qui correspondent aux énergies cinétiques des trois directions de l'oscillateur, soit trois degrés de liberté et trois degrés de libertés correspondant aux énergies potentielles élastiques de l'oscillateur dans les trois directions. En appliquant le théorème d'équipartition de l'énergie, on obtient le résultat mesuré expérimentalement. Comme pour les gaz, des températures trop basses vont "geler'' certains degrés de liberté (en réalité, on va ``geler" certains oscillateurs) d'où un écart à la loi de Dulong-Petit aux basses températures.
````

