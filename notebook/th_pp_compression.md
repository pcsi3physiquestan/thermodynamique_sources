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
# Méthodes
## Compression isotherme d'un gaz parfait
_Nous allons voir comment déterminer un état final et comment calculer un travail et un transfert thermique.__

````{admonition} Exercice 
:class: attention

On considère un cylindre de section horizontale S fermé en haut par un piston de masse $M_0$ glissant sans frottements le long des paroi du cylindre. L'enceinte ainsi formée est remplie d'un gaz suivant le modèle des gaz parfait avec un coefficient $\gamma$.

Au dessus du piston se trouve une atmosphère à pression $P_0$. L'enceinte est de plus en contact thermique avec un thermostat à température $T_0$.

Dans l'état initial le système est à l'équilibre et la hauteur entre le fond de l'enceinte et le piston est $h_0$.

On pose sur le piston une masse $M$. On peut réaliser cette opération de deux manières:

* on pose brutalement la masse M sur le piston
* on rajoute progressivement des très petites masses sur le piston en attendant à chaque fois l'équilibre jusqu'à atteindre une masse M.


1. Déterminer dans chaque cas l'état final. Commenter la différence.
1. Déterminer dans chaque cas le travail reçu par le système {gaz}. Commenter la différence et le signe.
1. Déterminer le transfert thermique reçu par le gaz. Commenter le signe.
````

## Changements d'état

````{admonition} Transformation de la glace en eau 
:class: attention

On considère $m=1g$ de glace pris à la température de $T_1 = 250K$ sous pression extérieure constante $P_{atm}$ à 1bar. On supposera que la température de fusion de la glace est alors de $T_{fus} = 273K$. On chauffe la glace pour la transformer en eau liquide à $T_2 = 300K$. Calculer les variations d'enthalpie.

Données: $c_{glace} = 2,1 \rm{kJ.K^{-1}.kg^{-1}}, c_{liquide} = 4,2 \rm{kJ.K^{-1}.kg^{-1}}, \Delta h_f(T = 273 \rm{K}) = 335 \rm{kJ.kg^{-1}}$

````
````{topic} Solution
__Choix de la transformation__  

L'enthalpie est une fonction d'état, on peut donc choisir un chemin particulier pour calculer la variation $\Delta H$. Il est en de même pour la variation d'entropie $\Delta S$. Le chemin choisi se compose:

* d'un échauffement isobare de la glace jusqu'à 273K
* de la fonte totale de la glace à 273K
* d'un échauffement isobare de l'eau jusqu'à 300K

```{important}

Cette étape du raisonnement est fondamentale pour l'étude des changements d'état. Les transformations réelles sont rarement celles décrites pour l'étude - on parle de chemin fictif - néanmoins les propriétés des fonctions d'état sont ici très utile. Attention car on ne peut calculer ainsi un transfert thermique ou un travail. Le chemin fictif à choisir est toujours sur lequel on PEUT calculer la variation d'enthalpie ou d'entropie. Ce chemin est souvent imposé par les données du problème, notament la température à laquelle on connaît l'enthalpie de changement d'état.
```

__Bilan enthalpique__  

La glace est l'eau sont des phases condensées, donc $\Delta H = C_{V} \Delta T$. Pour les changements d'état, on utilisera l'enthalpie massique de changement d'état:

\begin{align*}
\Delta H_1 &= m c_{glace} (T_{fus} - T_1)\\
\Delta H_2 &= m \Delta h_{f}(T_{fus})\\
\Delta H_3 &= m c_{liquide} (T_2 - T_{fus})\\
\Delta H &= m ( c_{glace} (T_{fus} - T_1) + \Delta h_{f}(T_{fus}) + c_{liquide}) (T_2 - T_{fus})
\end{align*} 
````

````{admonition} Etat final d'un système
:class: attention

Dans une enceinte dont les parois sont parfaitement adiabatiques on introduit à la pression atmosphérique constante une masse $m_1 = 0.01 \rm{kg}$ de glace à $T_1 = - 8 \rm{^{\circ}C}$ et une masse $m_2 = 0.1 \rm{kg}$ d'eau liquide à $T_2 = 15 \rm{^{\circ}C}$.

Données numériques: Chaleur latente de fusion la glace à $T_{fus} = 0 \rm{^{\circ}C}$: $L_f = 334.4 \rm{J.g^{-1}}$, capacités thermiques massiques de la glace: $c_1 = 2.1 \rm{kJ.K^{-1}.kg^{-1}}$, de l'eau liquide $c_2 = 4.2 \rm{kJ.K^{-1}.kg^{-1}}$.

1. Décrire l'état final
````

````{topic} Correction

_Cette fois on ne connaît pas l'état final._ Commençons par appliquer le premier principe à l'ensemble de l'enceinte. La transformation est monobare ($P_{atm}$ constante) et adiabatique, donc:

$$
\Delta H = Q = 0
$$

Il ne reste plus qu'à exprimer la variation d'enthalpie. __On rappelle qu'on __peut__ choisir le chemin pour calculer $\Delta H$ puisque c'est une fonction d'état. Ce choix __ne se fait pas en fonction de la réalité de la transformation mais de la possibilité de calculer $\Delta H$ (transformation simple + données de l'énoncé).__ Ici, les seules données sur le changement d'état étant en $T_{fus} = 0°C$, on amènera tout système devant fondre ou se solidifier à cette température pour faire le changement d'état avant de remodifier la température.

De plus, on ne connaît pas l'état final (lui on ne peut le choisir arbitrairement), on doit donc __faire une hypothèse sur l'état final pour calculer $\Delta H$.__ Et il faudra __vérifier cette hypothèse.__. Si elle valide, on s'arrête et on conclut, sinon, il faut en faire une autre.

Trois hypothèses possibles:
* Etat final purement solide : on connait les fractions massiques finales de liquide (0) et solide (1) et on doit vérifier après calcul que $T_{finale} \leq T_{fus}$
* Etat final purement liquide : on connait les fractions massiques finales de liquide (1) et solide (0) et on doit vérifier après calcul que $T_{finale} \geq T_{fus}$
* Etat final diphasé : on connait la température finale $T_{finale} = T_{fus}$ et on doit vérifier que les fractions massiques finales de liquide (1) ou de solide (0) sont comprises entre 0 et 1.

Aux vues des données numériques, on va supposer que l'état final est purement liquide. On choisit donc un chemin où:
1. L'eau liquide passant de $T_2$ à $T_f$ la température finale recherchée tandis que la glace passe de $T_1$ à $T_{fus}$
2. La glace subit une fusion totale.
3. L'eau liquide nouvellement formée passe de $T_{fus}$ à $T_f$.

Il vient:

\begin{align*}
\Delta H &= m_1 c_1 (T_{fus} - T_1) + m_2 c_2 (T_f - T_2) + m_1 L_f + m_1 \underbrace{c_2}_{liquide} (T_f - T_{fus})\\
0 &= m_1 \left (c_1 (T_{fus} - T_1) + L_f - c_2 T_{fus}\right) - m_2 c_2 T_2 + (m_1 + m_2) c_2 T_f\\
T_f &= \frac{m_2 c_2 T_2 - m_1 \left (c_1 (T_{fus} - T_1) + L_f - c_2 T_{fus}\right)}{(m_1 + m_2) c_2}
\end{align*}

__Vérification de l'hypothèse.__
$T_f = 279 K > T_{fus}$ donc l'hypothèse est validée.
--FIN--

Note : 
__Et si... on avait choisi une autre hypothèse ?__
On va supposer qu'on a choisi l'hypothèse d'un état diphasé. On ne cherche plus $T_f$ (puisque $T_f = T_{fus}$) mais on doit vérifier l'hypothèse et donc déterminer la fraction molaire (de liquide ou de glace).

On choisit donc un chemin où:
1. L'eau liquide passant de $T_2$ à $T_{fus}$ la température finale recherchée tandis que la glace passe de $T_1$ à $T_{fus}$
2. La glace subit une fusion partielle : une masse $\Delta m$ fond. (Note : si c'est l'eau qui se solidifie, cela reviendra à considérer $\Delta m < 0$).

Il vient:
\begin{align*}
  \Delta H &= m_1 c_1 (T_{fus} - T_1) + m_2 c_2 (T_{fus} - T_2) + \Delta m L_f\\
  \Delta m &= -\frac{m_1 c_1 (T_{fus} - T_1) + m_2 c_2 (T_{fus} - T_2)}{L_f}\\
  x_{glace} &= \frac{m_1}{m_1 + m_2} + \frac{m_1 c_1 (T_{fus} - T_1) + m_2 c_2 (T_{fus} - T_2)}{L_f (m_1 + m_2)}
\end{align*}

```{margin}
On aurait pu se contenter de vérifier $-m_2 < \Delta m < m_1$
```
On trouve :
$x_{glace} = -0.08$ donc $x_{glace}$ n'est pas compris entre 0 et 1, l'hypothèse n'est pas validée, il faut en choisir une autre (par exemple la précédente qui serait alors validée).
````
