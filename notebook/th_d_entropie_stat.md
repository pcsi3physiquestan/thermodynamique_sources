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
# Approche statistique de l'entropie

_L’entropie définie par le second principe permet de prévoir le sens des transformations, elle peut se calculer au moyen de diverses expressions. Néanmoins, sa définition, quoique très utile, semble très abstraite et ad hoc. Comment l'interpréter ? Et surtout a-t-elle une signification microscopique ou est-elle une construction mathématique purement abstraite qui cache un aspect plus fondamental de la matière ?_

Jusqu’à présent, nous avions dit que nous ne pouvions étudié le comportement de chaque particule du système tant elles sont nombreuses. Néanmoins, les progrès mathématiques permettent une étude globale à l’échelle microscopique: on va faire des statistiques. Les concepts de valeurs moyennes, écart-type, variance...  vont intervenir en physique. Boltzmann va ajouter le concept de probabilité et de variabilité pour remonter à la vision macroscopique du système et surtout de l’entropie. C’est pourquoi, on parlera d’__entropie statistique de Boltzmann__.

## Macroétat et microétat

_Rappel : Macro-état_  
On appelle macro-état d’un système thermodynamique, l’état du système défini par les seules variables marocroscopiques du système (par exemple E,V,n).


_Rappel : Microétat_  
On appelle micro-état d’un système thermodynamique, un état du système décrit par les données de toutes les grandeurs microscopiques (vitesses et positions) des particules du système.



On rappelle que la connaissance d'un micro-état précis est impossible et que de plus, le micro-état du système change à chaque instant (sous le simple effet des déplacements).

A l'inverse, à l'équilibre le macro-état reste le même et est mesurable.


````{admonition} Définition : Microétat compatible
:class: tip

Pour un macro-état observé, les micro-états dont les données sont cohérentes avec le macro-état observé sont dits micro-état compatibles ou accessibles.

Pour un macro-état $\mathfrak{E}$donné, on notera le nombre de micro-état compatibles $\Omega(\mathfrak{E})$.

````

## Décompte des microétats

````{admonition} Exercice 
:class: attention

Prenons pour simplifier un gaz composé de 5 particules dans une enceinte rigide et calorifugée. On suppose que l’état de chaque particule du gaz n’est donné que par son énergie (pas sa position ou sa vitesse) qui ne peut prendre que deux valeurs 0 ou E1. Nous supposons de plus que l’état macroscopique du système est donné par la donnée de son énergie E totale.

1. Donner l’écriture d’un macro état puis d’un micro-état compatible.
1. On suppose que le système est dans l’état $E = 4E_1$. Recenser tous les micro-état accessibles.
1. Donner l’expression de la fonction $\Omega(E)$ pour chaque valeur possibles de E.


````

## Hypothèse microcanonique


Les différentes macro-état possibles n’ont pas tous le même nombre de micro-états compatibles. Si l’on attend suffisamment longtemps, on peut supposer qu’on va atteindre un état d’équilibre donc une valeur d’énergie particulière. Quelle valeur sera atteinte ? $E=3E_1$ ou $E=2E_1$ ? On pourrait le penser puisque ces états compte le plus de micro-états. Cela dit, il faut encore être sûr que chaque micro-état possède la même probabilité d’exister.

C’est pourquoi on doit faire une hypothèse fondamentale pour la physique statistique.


````{admonition} Définition : Système microcanonique
:class: tip

Un système pour lequel l’énergie du macroétat est imposé (système isolé) est appelé distribution microcanonique. Les variables privilégiées seront donc l’énergie E, le volume V et le nombre de mole n (ou le nombre de particules N).

````


Il existe d'autres types de distributions statistiques où l'on impose d'autres grandeurs (on peut imposer le volume et la température ou la pression et la température... )

On impose E, V et N mais les autres grandeurs peuvent parfaitement varier. Autrement dit, même si on fixe E,V et n, les autres grandeurs T et P ne sont pas forcément fixées. Il peut donc y avoir plusieurs macroétats possibles. Dans ces conditions, celui qui décrira le mieux le système à l’équilibre sera le macroétats le plus probables. L’hypothèse microcanonique assure que __le macroétat le plus probable__ est celui pour lequel la grandeur $\Omega(E,V,n)$. On appelle la fonction $\Omega$ nombre __d’états accessibles__.


````{admonition} Fondamental : Hypothèse microcanonique
:class: attention

Dans un système isolé, tous les états microscopiques, ou micro-états, possibles, c’est-à-dire correspondant à un macro-état donné sont équiprobables.
````


Qu’est-ce que ça veut dire ? Imaginons qu’on puissent distinguer tous les micro-états possibles d’un système quand on a fixé ses grandeurs macroscopiques (donc son macroétat). Si chaque état est équiprobable, cela veut dire que pendant un temps déterminer $\tau$, le système passe autant de temps dans chaque état du système. Plus généralement, si un microétat $\Sigma_1$ possède une probabilité p de se réaliser, le système, pendant un temps $\tau$ donné, passera un temps $p\tau$ dans le microétat $\Sigma_1$.


## Les billes

````{admonition} Exercice 
:class: attention

On suppose un ensemble de N billes situées dans une enceinte rigide et calorifugée. On a séparé l’enceinte en 2 parties de volumes égaux V/2. On note le compartiment de gauche 1 et celui de droite 2. On suppose que le macroétat est défini par le nombre de particules $N_1$ contenues dans le compartiment 1 (on peut imaginer que ce sont des billes suffisamment grandes pour qu’on puisse les compter par chronophotographie). La fonction de partition sera donc exprimée en fonction de N et $N_1$.

1. Déterminer la fonction $\Omega(N,N_1)$. La représenter.
1. Quel est le macroétat le plus probable ? En déduire l’état du système à l’équilibre ?
1. Dans l’hypothèse des grands ensembles de particules (N grand) la fonction  peut se réécrire: $\Omega(N,N_1)\approx 2^N \exp\left(-2 \frac{{(N_1 - 0.5 N)}^2}{N}\right)$. Déterminer la largeur à mi-hauteur du pic autour du maximum. Commenter sa largeur.
1. Déterminer le temps moyen passé par jour dans l’état {toutes les particules dans le compartiment de gauche}.


On retiendra que si les grandeurs non imposées fluctuent (ici la concentration à gauche, mais ce pourrait être la température, la pression... ), la largeur de fluctuation est tellement faible qu'il est légitime de les considérées comme constante à l'équilibre.

````

## Entropie statistique

````{admonition} Compléments : Entropie statistique
:class: hint, dropdown

On définit l’entropie statistique d’un système, dans un état macroscopique (ou macro-état) donné par la quantité: $S = - k_B \sum_s P_s \ln(P_s)$ où s est le microétat compatible avec le macroétat et $P_s$ la probabilité d'occurence de s.
````


Cette définition n'est pas à connaître.


````{admonition} Définition : Entropie statistique - Cas microcanonique (A connaître)
:class: tip

Dans le cas d'un système isolé, l'entropîe se réécrire en fonction de la seule fonction de répartition $\Omega$:

\begin{equation}
S = k_B \ln \Omega
\end{equation}

````


__Preuve (pas à connaître)__  
Pour un système isolé, l'hypothèse microcanonique conduit à une probabilité $P_s = \frac{1}{\Omega}$. En remplaçant $P_s$ par son expression, on trouve la relation donnée précédemment entre S et $\Omega$.


````{dropdown} Remarque

__Entropie de Boltzmann et vision macroscopique__  
La vision macroscopique de l'entropie est donnée par le second principe. Nous reviendrons par la suite sur ce dernier mais notons déjà que l'entropie est alors donnée comme une fonction d'état extensive.

La propriété d'être une fonction d'état pour l'entropie de Boltzmann est assez évidente. Le caractère extensif est par délicat puisqu'il est en pratique faux, un terme supplémentaire apparaît quand on mélange deux systèmes (entropie dite de mélange). L'hypothèse d'extensivité consiste à supposer ce terme négligeable, ce qui revient, comme pour l'énergie à considérer que les effets de surface sont négligeables. __On admettra que dans le cadre du cours, l'entropie de Boltzmann est cohérente avec la définition de l'entropie qui sera vue avec le second principe.__  
````

## Entropie d'un système isolé: Exemple des billes

````{admonition} Exercice 
:class: attention

On reprend le systèmes composé de N billes. A l'instant initial, toutes les billes sont dans la partie gauche.

1. Le système est-il à l'équilibre? Déterminer la valeur de l'entropie en supposant comme précédemment que la fonction $\Omega$ ne dépend que de N et $N_1$.
1. Lorsque l'équilibre est atteint, déterminer la valeur de l'entropie. Montrer que l'entropie a atteint à l'équilibre un maximum.


Le second principe va permettre de généraliser cette propriété: à l'équilibre, un système __isolé aura une entropie maximale__.

Cette propriété explique l'intérêt du second principe car il va permettre, à l'échelle macroscopique (sans passer par le dénombrement des microétat compatibles) et déterminer __le sens d'évolution possible d'une transformation__. On pourra ainsi expliquer pourquoi le transfert thermique s'effectue toujours du corps chaud vers le corps froid, pourquoi certaines réactions chimiques ont lieu dans un sens privilégié. Ces explications feronts directement intervenir l'entropie et son expression en fonction des variables d'état (vision macroscopique donc) et non un dénombrement à l'échelle microscopique.

````

## Entropie, désordre et information


__Entropie et désordre__  
La vision microscopique explique la notion de désordre introduit précédemment. Le "désordre" correspond au fait qu'un macroétat peut posséder de nombreux microétats compatibles et que le système va passer de manière désordonnée d'un microétat à un autre. Plus l'entropie est grand, plus il y a de microétat (dans le cas d'un système isolé) et donc plus le système est désordonné.

On interprète aussi l'entropie comme une mesure de l'information manquante (entropie de Shannon) puisque plus l'entropie est grand, plus il existe de microétats. Comme on ne sait pas dans quel microétat se trouve le système, on perd d'autant plus d'information.



