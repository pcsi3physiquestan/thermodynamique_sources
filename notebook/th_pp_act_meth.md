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
# Activités méthodes

## Cas du gaz parfait

_Nous allons étudier la mise en équation du premier principe et le calcul de diverses grandeurs thermodynamiques dans le cas du gaz parfait. On insistera notamment sur le cas des transformations adiabatiques quasi-statique et les lois de Laplace._

### Transformations d'un gaz parfait

````{admonition} Exercice 
:class: attention

On considère un gaz parfait de coefficient $\gamma$. Exprimer la variation d'énergie interne, d'enthalpie ainsi que le travail mécanique des contraintes extérieures W et le transfert thermique Q pour:

1. Un transformation isochore quasi-statique
1. Une transformation isotherme quasi-statique
1. Une transformation isobare quasi-statique


````

### Cas d'une transformation quasi-statique adiabatique d'un gaz parfait

````{important} __Fondamental : Lois de Laplace__

Soit un système assimilable à un gaz parfait subissant une transformation quasistatique et adiabatique. Alors les produits suivants sont constants lors de la transformation:

\begin{align*}
T V^{\gamma-1} = cste\\
P V^{\gamma} = cste\\
T^{\gamma} P^{1-\gamma} = cste
\end{align*}
````


>__Démonstration__  : Réaliser la démonstration de cette propriété par une état d'une transformation infinitésimale. La démonstration doit être sue et maîtrisée.


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

```{important}
On retiendra la méthode de tracé ET la comparaison entre la transformation isotherme et la transformation adiabatique.
```

### Application au cycle


Nous allons utiliser les observations précédentes faites sur le diagramme de Watt pour étudier un cycle.


````{admonition} Exercice 
:class: attention

On considère un gaz parfait subissant un cycle composé d'un ensemble de transformations quasi-statique. Il subit dans l'ordre

* une compression isotherme
* une détente adiabatique
* une évolution isobare


1. Représenter le cycle dans un diagramme de Watt et déduire si l'évolution isobare est une compression ou une détente. Déduire aussi si le système est un moteur ou un récepteur.
1. Reprendre la question précédente en supposant que la première transformation est une compression adiabatique et la seconde une détente isotherme.


````

## Application à la calorimétrie

### Calorimétrie: Position du problème

````{important} __Définition : Calorimètre__

Un calorimètre est un récipient en général composé d'une paroi extérieure et d'une cuve intérieure. Le tout est fermé par un couvercle permettant d'introduire un agitateur, un thermomètre et une résistance chauffante. La cuve étant séparée de la paroi extérieure par de l'air, le système est relativement bien isolé et on peut négliger le temps d'une expérience les échanges thermiques avec l'extérieur.

En général, l'intérieur de la cuve ne maintient pas un volume contraint sur son contenu de sorte qu'on considère que l'évolution du système s'effectue en contact avec un atmosphère, donc à __pression extérieure constante__ (Il existe aussi des calorimètres isochores mais ce n'est pas l'objet de cette approche).

````

````{important} __Fondamental : Equation générale__

Ecrire de manière générale le prermier principe appliqué au système {calorimètre+contenu}.
````

### Méthode électrique

````{admonition} Exercice 
:class: attention

La méthode électrique consiste à plonger dans une masse $m$ de liquide (l'eau par exemple) une résistance chauffante R. L'ensemble est à l'instant initial à l'équilibre à une température $T_i$. La résistance chauffante est parcourue par un courant I constant pendant un intervalle de temps $\tau$. On mesure alors la nouvelle température $T_f$. Montrer qu'on peut obtenir à partir de ces grandeurs la valeur de la capacité thermique de l'ensemble {calorimètre +matériel} si on connaît la capacité thermique de l'eau.

````

### Méthode des mélanges

````{admonition} Exercice 
:class: attention

Dans un calorimètre, on introduit de l'eau liquide à température $T_0$ (on suppose que le calorimètre est à la même température). On plonge un corps de capacité massique $c_S$ inconnue, de masse $m_S$ connue et de température $T_S$ connue. On attend le retour à l'équilibre et on mesure la température $T_f$ finale. Montrer qu'on peut ainsi déterminer $c_S$ (on supposera la capacité du calorimètre et de ses accessoires connue).

````

