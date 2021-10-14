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
# Moteurs thermiques

## Moteur: Généralités


Dans le cas d'un moteur, c'est le travail fourni $\vert W \vert$ qui est la grandeur utile et la machine thermique fonctionne car on lui apporte de l'énergie sous forme de chaleur: c'est la chaleur reçue de la source chaude Qc qui est l'énergie fournie.

Le reandement d'un moteur ditherme s'écrit donc:

\begin{equation}
\rho = \frac{\vert W \vert}{Q_c}
\end{equation}

````{admonition} Fondamental : Rendement de Carnot du moteur ditherme
:class: attention

Le rendement maximal d'un moteur ditherme est obtenu pour un cycle réversible. Il ne dépend que des températures des sources chaudes et froides et pas de la façon dont les échanges d'énergie s'effectuent. Il a pour expression:

\begin{equation}
\rho_C = 1 - \frac{T_f}{T_c}
\end{equation}
On l'appelle rendement de Carnot d'un moteur ditherme.
````


__Démonstration__  
Le but est d'exprimer le rapport $W/Q_c$ en valeur absolue. On doit donc en premier lieu éliminer $Q_f$. L'écritures des deux principes suggèrent d'utiliser plutôt le second (il n'y a pas $W$). On veut une inégalité permettant de chercher un maximum de $\rho$. On peut comprendre que c'est la positivité de l'entropie crée qui va nous le donner.

Du second principe, il vient: $Q_f = -\frac{T_f}{T_c}Q_c - T_f S_c$. En divisant par $Q_c$ le premier principe, il vient:

\begin{align*}
\rho &= -\frac{W}{Q_c}\\
&= 1 + \frac{Q_f}{Q_c}\\
&= 1 - \frac{T_f}{T_c} - \frac{T_f S_c}{Q_c}
\end{align*}
Comme $S_c \geq 0$, ce rendement est maximal pour $S_c =0$ c'est-à-dire pour une transformation réversible et $\rho_C = 1 -\frac{T_f}{T_c}$.


````{dropdown} Remarque

__Analyse__  
On peut remarquer que le rendement de Carnot est toujours inférieur à 1 et augmente avec l'écart de température entre la source chaude et la source froide.

Pourquoi compter W et pas uniquement le travail des temps moteurs fourni au système mécanique qui nous intéresse? Tout simplement parce qu'en général, les machines thermiques sont conçues de manière à ce que le travail mécanique fourni par le système dans les temps moteur va servir au travail récupérable ET au travail à fournir durant les autres moments récepteurs du cycle (cf. cycle Beau de Rochas). Il vient que le travail récupérable se résume bien à W.
````

## Exemple: Cycle de Beau de Rochas


Il s'agit du moteur à explosion, c'est-à-dire un moteur à combustion interne.

```{figure} ./images/thermo_chap_7_moteur.jpg
:name: fig_292
:align: center

```



__Description du fonctionnement__  
__Principe général:__ Faire subir à une masse d'air et de carburant un cycle constitué de deux isentropiques et de deux isochores.

En pratique: ce moteur est réalisé par une chambre de combustion. Sa section est fermée d'un côté par un piston qui peut faire tourner un arbre au moyen d'un système bielle-manivelle (vilebrequin). On trouve de l'autre deux soupapes: l'une, la soupape d'admission, permet de faire entrer le mélange combustible, la seconde, la soupape d'échappement, permet l'évacuation des gaz une fois la combustion effectuée. Une bougie, commandée d'abord par un système électrique puis le seul fonctionnement du moteur s'allume de manière régulière pour déclencher la combustion.

__Description du cycle:__ Le cycle de Beau de Rochas peut s'effectuer en quatre ou deux temps, nous détaillerons ici le moteur à quatre temps.

1. Admission: le cylindre admet le mélange à travers la soupape d'admission dans un volume $V_1$. 
1. Compression-Explosion: Les soupapes fermées, le piston effectue une compression isentropique jusqu'au volume $V_2$ où se produit une explosion: la combustion de l'essence est une réaction chimique qui produit de la chaleur (réaction exothermique): elle joue le rôle de source chaude. La température augmentant à volume constant, la pression augmente aussi.
1. Détente: Le mélange se détend isentropiquement en repoussant le piston vers le bas jusqu'à sa position extrême exerçant un couple moteur sur l'arbre: c'est la partie motrice du cycle.
1. Evacuation: La soupape d'échappement s'ouvre et la différence de pression avec l'extérieur entraîne l'évacuation des gaz brûlés. Le gaz se détend de manière isochore: il se refroidit. C'est l'air "extérieur" qui fait alors office de source froide.



## Exemple: Cycle de Rankine


Le cycle de Rankine (ou le cycle de Hirn) est utilisé dans les centrales thermiques classiques ou les centrales nucléaires. Le fluide caloporteur (c'est-à-dire celui qui subit les différentes transformations du cycle) est cette fois de l'eau. Le principe de fonctionnement est à peu près le même, seul la manière d'apporter de la chaleur à l'eau diffère: dans le premier cas, c'est la combustion du charbon ou du gaz qui chauffe l'eau, dans le second cas c'est la fission des neutrons.



__Description__  
On considère de l'eau qui circule dans un circuit secondaire. Le circuit primaire est directement en contact avec la source de chaleur et ne sert qu'à transférer la chaleur provoqué par la combustion ou la fission au circuit secondaire.

1. __Phase AB:__ L'eau sous forme liquide sortant du condenseur est pompée de la pression P1 à la pression P2 de manière adiabatique et on le supposera réversible. En B, elle est à $290 ^{\circ}C$ sous 70 bars.
1. __Phase BB'C:__ Elle passe ensuite dans ensuite dans un échangeur thermique dans lequel il peut échanger de la chaleur avec le circuit primaire qui est chaud. La chaleur reçu provoque d'abord un échauffement isobare puis une vaporisation isobare (donc isotherme) et complète de l'eau.
1. __Phase CD:__ L'eau passe ensuite dans une turbine dans laquelle elle se détend de manière isentropique et une partie du gaz se liquéfie. On arrive à la pression initiale PA.
1. __Phase DA:__ En passant dans un condenseur, le système s'enrichit de manière isobare en phase liquide jusqu'à disparition complète du gaz. La pression de l'eau est alors de 50mbar et sa température de $32 ^{\circ}C$.




Les rendements des centrales nucléaires actuelles tourne autour de $30\%$ à $40\%$ alors que le rendement des centrales thermiques a été amélioré pour pouvoir dépasser plus de $50\%$. Pourtant, les centrales nucléaires produisent beaucoup plus de puissance malgré leur plus faible rendement.


