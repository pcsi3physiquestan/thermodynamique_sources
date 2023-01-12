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
# Récepteurs

## Réfrigérateur

### Généralités

Dans une réfrigérateur, la grandeur utile est la quantité de chaleur prise à la source froide $Q_f$: l'intérieur du réfrigérateur. La source chaude est quant à elle l'atmosphère extérieure en général.

L'efficacité d'un réfrigérateur correspond donc au rapport entre la quantité de chaleur prise à la source froide et le travail fourni au système $e = \frac{Q_f}{W}$.


````{important} __Efficacité de Carnot__

L'efficacité maximale d'un réfrigérateur ditherme ne dépend que des températures des sources chaudes et froides. Il s'obtient lors d'un cycle réversible et a pour expression:

$$
e_{C} = \frac{T_f}{T_c - T_f}
$$
On appelle cette efficacité, efficacité de Carnot pour un réfrigérateur.
````

````{important} __Démonstration__  

Du second principe, il vient: $Q_c = -\frac{T_c}{T_f}Q_f - T_c S_c$. En divisant par $Q_c$ le premier principe, il vient:

\begin{align*}
\frac{1}{e} &= \frac{W}{Q_f} \\
&= -1 - \frac{Q_c}{Q_f} \\
&= - 1 + \frac{T_c}{T_f} + \frac{T_c S_c}{Q_f}\\
e &= \frac{1}{\frac{T_c}{T_f} - 1 + \frac{T_c S_c}{Q_f}}
\end{align*}
Comme $S_c \geq 0$, cette efficacité est maximale pour $S_c =0$ c'est-à-dire pour une transformation réversible et $e_C = \frac{T_f}{T_c-T_f}$.
````

````{topic} __Analyse__  
* Comme dans le cas de la pompe à chaleur, le rendement est d'autant plus grand que les température sont proches. Dans le cas d'un réfrigérateur, on peut imaginer qu'il est beaucoup plus facile et moins coûteux de refroidir l'intérieur si l'extérieur n'est pas trop chaud (on verra en deuxième année que les échanges thermiques dépendent fortement de la différence de température).Malheureusement, la température de la source "gratuites", l'atmosphère ne peut être choisie par l'utilisateur (par exemple quand on veut utiliser une pompe à chaleur, c'est généralement qu'il fait froid dehors!).

* On peut remarquer que $Q_f = -Q_c - W \leq -Q_c$ car on fournit du travail au réfrigérateur. Cela veut dire que quoiqu'il arrive la quantité de chaleur prise à la source froide sera toujours inférieure à la quantité de chaleur donnée à la source chaude. C'est pourquoi il est inutile d'ouvrir la porte d'un réfrigérateur pour refroidir une pièce: la quantité de chaleur libérée directement dans l'atmosphère sera toujours plus importante que la quantité de chaleur libérée dans le réfrigérateur: ouvrir un réfrigérateur ne va donc PAS refroidir la pièce, au contraire!
````

### Exemple (en ligne)

````{topic} Machine à fluide condensable
Beaucoup de réfrigérateur fonctionne sur le principe des machine à fluide condensable ou machine à condensation. Le principe est à peu près celui d'un cycle de Rankine mais parcouru à l'envers. Le fluide utilisé n'est plus de l'eau mais un gaz qui se liquéfie à des températures ambiantes. On peut utiliser du méthane ou du dioxyde de carbone. Les réfrigérateurs usuels utilisaient plutôt des gaz appelés CFC (chlorofluorocarbone) ou fréons. Néanmoins ceux-ci se fixent dans la couche d'ozone où ils sont lysés par le rayons UV. Les atomes de fluor et de chlore libérés sont responsables de la destruction de la couche d'ozone. C'est pourquoi leur utilisation a été restreinte par le protocole de Montréal en 1987. On utilise encore les HCFC, moins nocifs mais il est question de procéder leur remplacement, à condition de trouver un substituants. Principe:

* Dans les machine à fluide condensable, le fluide, liquide, subit une évaporation complète au contact avec la source froide: c'est au cours de cette transformation que le fluide prélève de la chaleur de l'intérieur du réfrigérateur $Q_f$.
* Ensuite, on réalise une compression qui est cette fois le long de la courbe de saturation dans un compresseur. Pour effectuer ceci, il faut fournir un travail W et on augmente la température pour qu'elle passe au dessus de celle de la source chaude.
* Le fluide passe alors dans le condenseur où il est en contact avec l'atmosphère extérieur, la source chaude. Il cède alors de la chaleur $Q_c$ à la source chaude. Le fluide se condense entièrement puis se refroidit.
* Il faut alors détendre le fluide pour le ramener à son état initial. On effectuer pour cela une détente isenthalpique dans un détendeur.

__Ordre de grandeur__  
Un kilogramme de fréon enlève par cycle, environ 100kJ à la source froide. On rappelle que cela correspond environ au refroidissement de 3K de 10L d'eau.
````

## Pompe à chaleur


Dans une pompe à chaleur, la grandeur utile est la quantité de chaleur cédée à la source chaude $Q_c$. Celle-ci peut-être par exemple une pièce à maintenir à température constante, un moteur...  La pompe à chaleur la plus utilisée est la pompe à air où grâce à un travail (initialement électrique mais qui est en général converti en un travail mécanique), la pompe prend de la chaleur à de l'air et en fourni à la pièce à chauffer. La chaleur prise à la source froide est donc d'une certaine manière "gratuite" et seul le travail apporté W correspond à l'énergie fournie.

L'efficacité d'une pompe à chaleur correspond donc au rapport entre la quantité de chaleur fournie à la source chaude et le travail fourni au système $ e = \frac{\vert Q_c \vert}{W}$


````{important} __Efficacité de Carnot__

L'efficacité maximale d'une pompe à chaleur ditherme ne dépend que des températures des sources chaudes et froides. Il s'obtient lors d'un cycle réversible et a pour expression:

$$
e_{C} = \frac{T_c}{T_c - T_f}
$$
On appelle cette efficacité, efficacité de Carnot pour une pompe à chaleur.
````

````{important} __Démonstration__  

Du second principe, il vient: $Q_f = -\frac{T_f}{T_c}Q_c - T_f S_c$. En divisant par $Q_c$ le premier principe, il vient:

\begin{align*}
\frac{1}{e} &= -\frac{W}{Q_c} \\
&= 1 + \frac{Q_f}{Q_c} \\
&= 1 - \frac{T_f}{T_c} - \frac{T_f S_c}{Q_c}\\
e = \frac{1}{1 - \frac{T_f}{T_c} + \frac{T_f S_c}{\vert Q_c \vert}}
\end{align*}
Comme $S_c \geq 0$, cette efficacité est maximale pour $S_c =0$ c'est-à-dire pour une transformation réversible et $e_C = \frac{T_c}{T_c-T_f}$.
````

````{topic} Analyse
* L'efficacité __maximale__ d'une pompe à chaleur est toujours supérieur à 1. Cela signifie qu'on fournir plus que W à la pièce à chauffer. C'est ce qui rend la pompe à chaleur intéressante. En effet, une résistance chauffante simple n'aurait pas pu fournir une chaleur supérieure à W. L'inconvénient est notamment le coût de l'installation et son entretien, il faut une installation importante pour rentabiliser une pompe à chaleur.

* Pourquoi compter W et pas uniquement le travail effectivement reçu $W_r$ au système mécanique qui nous intéresse? Cela signifie qu'on se place dans le cas le plus favorable où l'ensemble du travail qui serait fourni par le système dans les temps moteurs seraient entièrement réutilisé par le système. Dans la pratique, cela n'est pas toujours le cas.
````

