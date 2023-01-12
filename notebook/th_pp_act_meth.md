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
# Activités - Cas du gaz parfait

_Nous allons étudier la mise en équation du premier principe et le calcul de diverses grandeurs thermodynamiques dans le cas du gaz parfait. On insistera notamment sur le cas des transformations adiabatiques quasi-statique et les lois de Laplace._

## Transformations d'un gaz parfait

````{admonition} Exercice 
:class: attention

On considère un gaz parfait de coefficient $\gamma$. Exprimer la variation d'énergie interne, d'enthalpie ainsi que le travail mécanique des contraintes extérieures W et le transfert thermique Q pour:

1. Un transformation isochore quasi-statique
1. Une transformation isotherme quasi-statique
1. Une transformation isobare quasi-statique
````

````{topic} Solution
1. $Q = \Delta U = \frac{nR}{\gamma - 1} \Delta T$; $\Delta H = \frac{\gamma nR}{\gamma - 1} \Delta T$
1. $\Delta U = \Delta H = 0$ avec $W = nRT \ln \frac{V_i}{V_f} = -Q$
1. $Q = \Delta H = \frac{\gamma nR}{\gamma - 1} \Delta T$; $\Delta U = \frac{nR}{\gamma - 1} \Delta T$; $W = \underbrace{\Delta U - \Delta H}_{\textrm{premier principe}} = -nR \Delta T$
````

### Cas d'une transformation quasi-statique adiabatique d'un gaz parfait

````{important} __Lois de Laplace__

Soit un système assimilable à un gaz parfait subissant une transformation quasistatique et adiabatique. Alors les produits suivants sont constants lors de la transformation:

\begin{align*}
T V^{\gamma-1} = cste\\
P V^{\gamma} = cste\\
T^{\gamma} P^{1-\gamma} = cste
\end{align*}
````

````{important} __Démonstration__

La transformation étant quasi-statique, on peut travailler sur une transformation infinitésimale durant laquelle température et pression son bien définie. Le premier principe s'écrit donc:

\begin{align*}
dU &= \delta W + \underbrace{\delta Q}_{=0}\\
\frac{nR}{\gamma - 1} dT &= - P dV \\
\frac{nR}{\gamma - 1} dT &= - \frac{nRT}{V} dV \\
\frac{dT}{T} &= -(\gamma - 1) \frac{dV}{V}
\end{align*}

soit en intégrant:

$$
\ln \frac{T_i}{T_f} = - (\gamma -1) \ln \frac{V_i}{V_f}
$$

soit:

$$
T_i V_i^{\gamma - 1} = T_f V_f^{\gamma - 1}
$$
On peut trouver les deux autres formes des lois de Laplace en utilisant l'équation d'état des gaz parfaits.
````

### Diagramme de Watt

````{admonition} Exercice 
:class: attention

On considère un gaz parfait subissant des transformations quasistatique avec pour état initial $(P_0,V_0)$. Représenterla transformation du système dans un diagramme de Watt pour:

1. une détente isochore puis une compression isochore
1. une échauffement isobare puis un refroissedement isobare
1. une détente isotherme puis une compression isotherme
1. une détente adiabatique puis une compression adiabatique


Comparer la température et la pression de la détente (puis de la compression) adiabatique et isotherme en supposant le volume final identique. Commenter.

Comparer la température et le volume de la détente (puis de la compression) adiabatique et isotherme en supposant la pression finale identique. Commenter.
````

>On pourra aussi étudier le cas d'un refroidissement/échauffement isochore et d'une détente/compression isobare et commenter la redondance.

```{important} __A retenir__

Comme $\gamma > 1$, la pente d'une transformation adiabatique réversible et toujours plus importante que la pente d'une transformation isotherme réversible.
```

````{admonition} Application au cycle 
:class: attention

On considère un gaz parfait subissant un cycle composé d'un ensemble de transformations quasi-statique. Il subit dans l'ordre

* une compression isotherme $A \to B$
* une détente adiabatique $B \to C$
* une évolution isobare $C \to A$


1. Représenter le cycle dans un diagramme de Watt et déduire si l'évolution isobare est un échauffement ou un refroidissement. Déduire aussi si le système est un moteur ou un récepteur.
1. Reprendre la question précédente en supposant que la première transformation est une compression adiabatique et la seconde une détente isotherme.
````

````{topic} Solution
1. La détente étant plus pentue que la compression, il vient que le volume $V_C < V_A$ donc $T_C < T_A$. Il y a donc une augmentation de température à pression constante, c'est un échauffement isobare. Le cycle est de plus parcouru dans le sens anti-horaire, le système est donc un récepteur.
1. On doit inverser le cycle et l'ordre entre $V_C$ et $V_A$, on a donc un refroidissement isobare et un moteur.
````

## Application à la calorimétrie

### Position du problème

````{important} __Calorimètre__

Un calorimètre est un récipient en général composé d'une paroi extérieure et d'une cuve intérieure. Le tout est fermé par un couvercle permettant d'introduire un agitateur, un thermomètre et une résistance chauffante. La cuve étant séparée de la paroi extérieure par de l'air, le système est relativement bien isolé et on peut négliger le temps d'une expérience les échanges thermiques avec l'extérieur.

En général, l'intérieur de la cuve ne maintient pas un volume contraint sur son contenu de sorte qu'on considère que l'évolution du système s'effectue en contact avec un atmosphère, donc à __pression extérieure constante__ (Il existe aussi des calorimètres isochores mais ce n'est pas l'objet de cette approche).

````

````{important} __Equation générale__

Ecrire de manière générale le prermier principe appliqué au système {calorimètre+contenu}.
````

````{important} __A retenir la méthode__

__Même s'il faut systématiquement le justifier.__ La transformation est monobare entre deux états d'équilibre, on a donc (adiabatique):

$$
\Delta H_{total} = W_{autre}
$$
avec $W_{autre}$ le travail autre que les forces de pression.
````

### Exercices

````{admonition} Méthode électrique
:class: attention

La méthode électrique consiste à plonger dans une masse $m$ de liquide (l'eau par exemple) une résistance chauffante R. L'ensemble est à l'instant initial à l'équilibre à une température $T_i$. La résistance chauffante est parcourue par un courant I constant pendant un intervalle de temps $\tau$. On mesure alors la nouvelle température $T_f$. Montrer qu'on peut obtenir à partir de ces grandeurs la valeur de la capacité thermique de l'ensemble {calorimètre +matériel} si on connaît la capacité thermique de l'eau.
````

````{topic} Solution
Ici $\Delta H = \Delta H_{calorimetre+materiel} + \Delta H_{eau} = C_{cal} (T_f - T_i) + m c_{eau} (T_f - T_i)$
et $W_{autre} = RI^2 \tau$ donc:

\begin{align*}
  C_{cal} (T_f - T_i) + m c_{eau} (T_f - T_i)$ &= RI^2 \tau\\
  C_{cal} &= \frac{RI^2 \tau}{T_f - T_i} - m c_{eau}
\end{align*}

````

### Méthode des mélanges

````{admonition} Exercice 
:class: attention

Dans un calorimètre, on introduit de l'eau liquide à température $T_0$ (on suppose que le calorimètre est à la même température). On plonge un corps de capacité massique $c_S$ inconnue, de masse $m_S$ connue et de température $T_S$ connue. On attend le retour à l'équilibre et on mesure la température $T_f$ finale. Montrer qu'on peut ainsi déterminer $c_S$ (on supposera la capacité du calorimètre et de ses accessoires connue).

````

````{topic} Solution
Ici $\Delta H = \Delta H_{calorimetre+materiel+eau} + \Delta H_{solide} = (C_{cal} + m c_{eau}) (T_f - T_0) + m_S c_{S} (T_f - T_S)$
et $W_{autre} = 0$ donc:

\begin{align*}
  0 &= (C_{cal} + m c_{eau}) (T_f - T_0) + m_S c_{S} (T_f - T_S)\\
  c_{S} &= \frac{(C_{cal} + m c_{eau}) (T_f - T_0)}{m_S (T_S - T_f)}
\end{align*}

````

## Application aux changements d'état

````{admonition} Exercice 
:class: attention

On s'intéresse au passage de la phase 1 à la température T à la limite de changement d'état seule à la phase 2 seule à la température T à la limite de changement d'état et on veut exprimer d'une manière général. Soit $\Delta h_{1 \rightarrow 2}$ l'enthalpie massique de changement d'état. On suppose l'évolution monotherme à température $T$.

1. Justifier que l'évolution est aussi monobare.
1. Déterminer la variation massique d'énergie interne ainsi que le transfert thermique massique $q$ et le travail mécanique massique reçu $w$.
````
````{dropdown} Démonstration
__Palier__  


__Durant toute la transformation, deux phases coexistent à la même température T__. La pression est alors imposée (pression de changement d'état à la température T) donc l'isotherme est aussi une isobare (donc $\Delta (Pv) = P_{ch} \Delta v$):

__Fonctions d'état__  
\begin{align*}
\Delta u &= \Delta h - P_{ch} \Delta v\\
\Delta f &= - P_{ch} \Delta v\\
\Delta g &= 0
\end{align*}

En supposant que le seul travail mécanique mis en jeu est celui des forces de pression extérieure:

__Transferts__  
\begin{align*}
q &= \Delta h\textrm{ car isobare }\\
w &= - P_{ch} \Delta v
\end{align*}
````

````{important} __A retenir__

On retiendra que lors d'un changements d'état, le caractère monotherme impose le caractère monobare et on utilisera donc le premier principe avec l'enthalpie.
````