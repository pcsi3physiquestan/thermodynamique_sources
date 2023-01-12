---
jupytext:
  encoding: '# -*- coding: utf-8 end
jupytext:
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
# Enoncé

````{important} __Second principe de la thermodynamique__

Pour tout système thermodynamique, on définit une fonction d'état $S$, extensive, appelée entropie telle que la variation d'entropie $\Delta S$ pour un système isolé ne peut qu'être positive.

$$
\Delta S_{isole} \geq 0
$$
````

````{sidebar} Remarque
* __Le second principe ne s'applique que pour des système fermés.__  
* Le second principe postulat aussi que l'entropie est une fonction d'état et qu'elle est extensive. Ces deux caractéristiques sont très importantes dans l'utilisation de l'entropie.
* __Attention: la création d'entropie ne peut être que positive mais la variation d'entropie peut-être négative.__  
* Si on considère que l'entropie est une mesure du désordre, il vient que le désordre d'un système isolé ne peut qu'augmenter au cours du temps.
````
````{important} __Réécriture du second principe__

Pour tout système thermodynamique fermé, la variation d'entropie $\Delta S$ du système se décompose (par extensivité) en deux termes:

* l'entropie $S_e$ appelé entropie échangée correspond à l'entropie échangée avec le milieu extérieur dont on peut donner une expression en fonction des échanges de chaleur.
* l'autre, $S_c$ appelé entropie créée n'a pas d'expression générale mais a la propriété d'être toujours positive ou nulle.


\begin{align*}
\Delta S &= S_{ech} + S_{c}\\
dS &= \delta S_{ech} + \delta S_{c}
\end{align*}

avec $S_c \leq 0$ et $\delta S_c \leq 0$.
````

## Entropie créée et transformations réversibles

````{important} __Entropie créée et transformation réversible__

* Pour une transformation réversible, l'entropie créée est nulle.
* Si la transformation est irréversible, l'entropie créée est strictement positive.
````

````{important} __Démonstration__

* Supposons la transformation réversible, alors elle peut être parcourue dans les deux sens. Or pour une transformation de A vers B, $S_{c,A \rightarrow B} = -S_{c,B \rightarrow A}$. Donc Si $S_{c,A \rightarrow B} \geq 0$ alors $S_{c,B \rightarrow A} \leq 0$. Or le second principe implique que $S_{c,B \rightarrow A} \geq0$, il vient: $S_{c,A \rightarrow B} = -S_{c,B \rightarrow A}=0$.

* Si $S_{c, A \rightarrow B} = 0$ alors $S_{c,B \rightarrow A} = 0$. Cette transformation ne s'oppose pas au second principe, elle peut donc aussi être physiquement possible: la transformation de A vers B est donc réversible.
````


````{margin}
On observe que le second principe permet de déterminer les transformations possibles et impossibles: on caractérise ainsi le sens d'évolution d'une transformation.
````

