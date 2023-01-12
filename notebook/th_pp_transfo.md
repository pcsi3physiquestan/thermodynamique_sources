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
# Activités - Etude de transformations

_On va étudier l'écriture du premier principe dans diverses transformations. On s'intéressera en particulier au cas des transformations monobares qui expliquent l'intérêt de l'enthalpie._

## Transformations diverses

````{admonition} Exercice 
:class: attention

Ecrire le premier principe dans le cas:

1. d'une transformation adiabatique.
1. d'une transformation isochore.
1. d'une transformation isotherme pour une phase peu compressible ou un solide.
1. d'une transformation isotherme pour gaz parfait.


On distinguera, pour le travail W, le travail associé aux contraintes normales $W_P$ du reste du travail $W_{autre}$.
````

````{topic} Solution
1. $\Delta U = W_P + W_{autre}$
1. $\Delta U = W_{autre} + Q$
1. $\Delta U = C_V \Delta T = 0 \Longrightarrow 0 = W_P + W_{autre} + Q$
1. $\Delta U = C_V \Delta T = 0 \Longrightarrow 0 = W_P + W_{autre} + Q$
````

## Cas des transformations monobares. Enthalpie.

_Rappel :Transformation monobare_
On rappelle qu'une transformation monobare est une transformation pour laquelle la pression extérieure (ou plus généralement la contrainte normale extérieure) est constante.

Si la transformation est de plus quasi-statique, elle devient isobare.


````{important} __Réécriture du premier principe pour une transformation monobare__

Soit un système fermé dont la pression extérieure agissante sur le système est maintenue constante $P_0$ passant d'un état d'équilibre à un autre. La variation d'enthalpie $\Delta H$ s'écrit:

$$
\Delta E_{M,macro} + \Delta H = Q + W_{autre}
$$
où $W_{autre}$ est le travail autre que les forces de pression.
````

```{margin}
Il s'agit d'une __réécriture du premier principe__ pour simplifier la mise en équation. On pourra faire le parallèle avec le passage du TEC au TEM mais cette fois pour __un type de transformation particulière (monobare)__.
```
````{important} __Démonstration__

>Le premier principe appliqué au système s'écrit: $\Delta U = W_{pression} + W_{autre} + Q$. Remarquons de plus qu'à l'état initial et à l'état final, la pression du système est $P_0$ puisque le système est en équilibre avec l'extérieur. On a:
>
>\begin{align*}
W_{pression} &= - \int P_{ext} dV = - P_0 \int dV = - (P_0 V_{final} - P_0 V_{initial})\\
&= - \Delta PV\\
\Delta U &= - \Delta PV + W_{autre} + Q\\
\Delta H &= \Delta(U + PV) = W_{autre} + Q
\end{align*}
````

````{topic} Interprétation

* __Capacité thermique__
L'écriture du premier principe avec l'enthalpie pour une transformation monobare entre deux états d'équilibre permet de comprendre le sens donné à la capacité thermique à pression constante comme __l'énergie à fournir pour augmenter la température de 1K à pression constante.__.

En effet, quand on fonctionne à pression constante, celà signifie en général qu'on dispose d'un système fermé par une partie mobile (piston) qui permet d'ajuster le volume du système pour maintenir la pression constante. Cet ajustement se fait "naturellement" au contact d"un atmosphère suffisamment grand pour sa pression soit constante. Mais le travail échangé par la contrainte normale n'est pas maitrîsé. Ce qu'on fournit réellement, c'est le $W_{autre} + Q$.

Cette interprétation permet aussi de comprendre pourquoi la capacité thermique à pression constante est plus grande que la capacité thermique à volume constant. En effet, quand la température du système augmente, son volume augmente à pression constante (coefficient de dilatation isobare). Il vient que les contraintes normales (qu'on appelera force de pression extérieures puisqu'elles sont exercées par une atmosphère à pression constante sur le piston) exerce un travail des forces de pression résistant: le système doit __fournir__ un travail mécanique à l'atmosphère. Cette énergie doit être fournie en plus de celle à apporter pour augmenter la température d'où $C_P > C_V$.

* __Changement d'état.__
Un changement d'état monobare (ou isotherme donc isobare) permet d'écrire le premier principe avec l'enthalpie:

$$
\Delta H = Q + W_{autre}
$$

En général $W_{autre} = 0$ donc le transfert thermique correspond à la variation d'enthalpie soit en divisant par la masse : $\Delta h =q$. L'enthalpie massique de changement d'état vaut la chaleur échangée, ce qui explique l'appelation "Chaleur latente de changement d'état" qu'on utilisait auparavant.

__On notera aussi l'écriture du premier principe dans le cas d'un changement d'état.__
````

