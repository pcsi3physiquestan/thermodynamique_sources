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
# Transfert thermique

## Méthode de calcul du transfert thermique  

La seule relation faisant intervernir le transfert thermique en première année est donnée par le second principe: $Q = \Delta U - W$.

Pour déterminer le transfert thermique lors qu'une transformation, on ne possède que deux manières en première année:

* si la transformation est adiabatique: $Q = 0$: en général, il s'agit d'une __transformation suffisamment rapide pour que les échanges thermiques n'aient pas lieu__. A l'inverse, une transformation lente permettra la mise à l'équilibre thermique régulière et conduira à une transformation isotherme (dans laquelle $Q \neq 0$ probablement).
* sinon, on utilise le premier principe $Q = \Delta U - W$

 

````{important} __Mode de transfert thermique__

Si nous ne pouvons donner une expression générale du transfert thermique. On peut au moins voir comment il se produit. Comme on le verra en deuxième année, on peut distinguer plusieurs types de transferts:
*  le transfert par conduction (pas de mouvement de matière)
*  par convection (mouvement de matière)
*  rayonnement (échange d'énergie avec les ondes électromagnétiques, ex: le rayonnement solaire chauffe)
````

## Transfert thermique et température (en ligne)
````{topic} Mise en situation

On va voir ici __qu'il n'y a pas de lien entre le signe du transfert thermique reçu par le système et la variation de température du système.__  
Considérons deux solides A et B. Le corps A est en translation horizontale à la vitesse constante $\overrightarrow{v}$. Il glisse avec des frottements $\overrightarrow{F}$ sur un support fixe B sous l'action d'une force $\overrightarrow{F}$ extérieure à A et B qui fournit un travail $W>0$ entre les instants $t$ et $t+\Delta t$. On supposera que le deux solides sont en équilibre thermique entre eux à chaque instant (mais par forcément avec l'extérieur).

1. Exprimer le premier principe pour le système {A+B}.  
__Premier principe :__  
$\Delta E_m + \Delta U = W(\overrightarrow{F}) + Q = W + Q$ avec $Q$ l'échange de chaleur avec le milieu extérieur. Il n'y a pas de variation d'énergie potentielle macroscopique (la seule force extérieure dérivant d'une énergie potentielle et le mouvement est horizontal) et pas de variation d'énergie cinétique (les deux solides ont des vitesses costantes), soit:$\boxed{\Delta U = W + Q}$.

1. En déduire l'expression de la chaleur apporté au système {A+B} en fonction de W et de la variation d'énergie interne $\Delta U$ du système {A+B}.  
__Calcul de Q :__  
Il vient immediatement: $Q = \Delta U - W$

1. Comment va évoluer la température si le système ne peut échanger de chaleur avec l'extérieur? Comment s'effectue le transfert de chaleur si le système est maintenu à température constante?  
Pour un solide, $\Delta U_{Solide} = C_V \Delta T_{Solide}$. L'énergie interne étant extensive, on peut écrire: $\Delta U = \Delta U_A + \Delta U_B = C_{VA} \Delta T_{A} + C_{VB} \Delta T_{B}$ où les indices A et B renvoient à chaque solide. Comme ils sont en équilibre thermique entre eux, $T_A = T_B$ au début et à la fin de la transformation, donc: $\Delta U = (C_{VA} + C_{VB}) (T_{finale} - T_{initiale})$.

* _Cas isotherme:_ A température constante, il vient $\Delta U = 0$ donc $Q = - W < 0$: il y a nécessairement un échange thermique avec l'extérieur. Plus précisément, le système pers de l'énergie sous forme de chaleur vers l'éxterieur. __Ce cas montre bien que la constante de T ne correspond PAS à un transfert thermique nul.__  
* _Cas adiabatique:_ Si le système est isolé thermiquement $Q=0$ et $(C_{VA} + C_{VB}) \Delta T = W >0$ donc la température va nécessairement augmenter. __Ce cas montre bien que le caractère adiabatique n'implique que T ne varie pas.__  


````
