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
# Analyse quantitative

## Fractions molaires et massiques. Théorème de moments

_Dans toutes cette partie, nous n'étudierons que la transition liquide-vapeur. La plupart des résultats donnés peuvent néanmoins se transposer facilement aux autres transitions._

_Notation: Dans la suite, on notera avec un indice l les grandeurs liées au liquide et avec un indice g les grandeurs liées au gaz._

### Fractions molaires et massiques

````{important} __Définition : Fraction massique et molaire__

Dans un système où deux phases liquide et gaz coexistent, on définit la fraction molaire $X_{ml}$ de la phase liquide par la grandeur: $X_{ml} = \frac{n_l}{n_T}$ où $n_l$ est la quantité de matière de la phase liquide et $n_T$ la quantité de matière totale.

Dans un système où deux phases liquide et gaz coexistent, on définit la fraction massique $x_l$ de la phase liquide par la grandeur: $x_l =\frac{m_l}{m_T}$ où $m_l$ est la masse de la phase liquide et $m_T$ la masse totale.

On définira bien entendu les mêmes grandeurs pour la phase gazeuse.

````

__Utilisation des grandeurs massiques et molaires__  

Soit une grandeur extensive Y du système diphasé. On a les relations suivantes:

\begin{align*}
y &= x_l y_l  + x_g y_g\\
Y_m &= X_{ml} Y_{ml} + X_{mg} Y_{mg} 
\end{align*}
où $y_l$ et $y_g$ sont respectivement les grandeurs massiques de la phase liquide et gazeuse seule aux mêmes conditions de pression et température et $Y_{ml}$ et $Y_{mg}$ les grandeurs molaires de la phase liquide et gazeuse seule aux mêmes conditions de pression et température.
 


__Démonstration__  
Prouvons pour la grandeur molaire:

\begin{align*}
Y_m &= \frac{Y}{n_T} = \frac{Y_l + Y_g}{n_T} + \frac{n_l Y_{ml} + n_g Y_{mg}}{n_T}\\
&= X_{ml} Y_{ml} + X_{mg} Y_{mg}
\end{align*}

### Théorème des moments

````{important} __Fondamental : Théorème des moments__

Soit, sur un diagramme de Clapeyron, un point M du palier à T et les points E et B du même palier placées respectivement sur la courbe d'ébullition et la courbe de rosée. On peut alors écrire: $x_l ME = x_g MB$ où ME et MB correspondent aux longueurs des deux segments.

```{figure} ./images/thermo_chap_6_diag_pv_liqvap.jpg
:name: fig_289
:align: center

```
````


__Démonstration__  
On a $n_T = n_l + n_g \Longrightarrow 1 = x_l + x_g$. De plus: $v = x_l v_l + x_g v_g$ par extensivité du volume. Soit:

\begin{align*}
v & = x_l (v_l - v_g) + v_g \Longrightarrow x_l = \frac{v_g - v}{v_g - v_l} = \frac{MB}{EB}\\
v & = x_g (v_g - v_l) + v_l \Longrightarrow x_g = \frac{v - v_l}{v_g - v_l} = \frac{ME}{EB}
\end{align*}
En divisant les deux expressions, on retrouve le théorème des moments.


On retiendra que cette preuve __permet aussi d'obtenir les fractions massiques__ en fonction des volumes massiques des différentes phases et du système.
 

````{dropdown} Remarque

__Diagramme P-h__  
Le même raisonnement peut-être réalisé sur le diagramme $(h-p)$. C'est ce qui permet de tracer les isotitre en vapeur comme on peut les voir sur le graphique.
````

## Bilans énergétiques et entropiques

### Bilans d'enthalpie


__Notation__  
Rappel: On appelle enthalpie massique de changement d'état, la variation d'enthalpie du corps pur au cours du changement d'état complet d'un kilogramme du corps pur considéré à température donnée.

Avec les notations précédentes, il vient que l'enthalpie massique de vaporisation s'écrit: $\Delta h_{vap} (T_{sat}) = h_{g}(T_{sat}) - h_g (T_{sat})$ et $\Delta h_{liq} (T_{sat}) = h_{l}(T_{sat}) - h_g (T_{sat})$. Il vient immédiatement que l'enthalpie massique de liquéfaction est l'opposé: $\Delta h_{vap} = - \Delta h_{liq}$.

Remarque: On pourrait aussi l'écrire en fonction de $P_{sat}$ puisque température et pression sont liées lors d'un changement d'état d'un corps pur.


__Bilan enthalpique lors d'un changement d'état__  

Soit un corps pur à la température $T_{sat}$ et à la pression $P_{sat}$ associée. La variation d'enthalpie massique correspondant à la formation de $\Delta x_g$ (soit une formation de liquide $\Delta x_l = - \Delta x_g$) de gaz à température et pression constante est: $\Delta h = \Delta x_g \Delta h_{vap} = \Delta x_l \Delta h_{liq}$
 

````{attention}

Il est important de ne pas se tromper sur l'enthalpie de changement d'état à choisir, elle correspond à la grandeur formée (en grandeur algébrique).

````


__Démonstration__  
A démontrer à titre d'exerice.


````{important} __Fondamental : Signe des enthalpies de changement d'état__

Observation: Expérimentalement on observe que, pour tous les corps, il faut fournir de l'énergie au système pour passer du solide au liquide, du solide au gaz et du liquide au gaz. Il vient donc que:

\begin{align*}
&\Delta h_{vap} >0; \Delta h_{fus} >0; \Delta h_{sub} >0;\\
&\Delta h_{liq} <0; \Delta h_{sol} <0; \Delta h_{cond} <0
````

### Bilans entropiques

````{important} __Définition : Entropie massique de changement d'état__

L'entropie massique de changement d'état à la température $T_{sat}$ est la variation d'entropie d'un kilogramme de corps pur lors du changement d'état complet.

````

````{admonition} Exemple : 
:class: tip, dropdown

Par exemple l'entropie massique de vaporisation est: $\Delta s_{vap}(T_{sat}) = s_{g}(T_{sat}) - s_{l}(T_{sat})$.
````

````{important} __Fondamental : Relation entropie-enthalpie__

Considérons un changement d'état monotherme à température T dont l'enthalpie massique de changement d'état est $\Delta h_{ch}$. L'entropie massique de changement d'état $\Delta s_{ch}$ est:

$$
\Delta s = \frac{\Delta h}{T}
$$
````


__Démonstration__  
Considérons le changement d'état complet et réversible. Le second principe s'écrit: $\Delta S = S_e + S_c = \frac{Q}{T}$. La transformation est isotherme sur un changement d'état, elle est donc aussi isobare\footnote{Cet argument est crucial lorsqu'on étudie des changements d'état, il sera très souvent utilisé.}. Le premier principe s'écrit donc: $Q = \Delta H$. Ramené aux grandeurs massiques, il vient:

$$
\Delta s = \frac{\Delta h}{T}
$$
Cette relation ne fait intervenir que des variables et fonctions d'état. __Elle ne dépend donc pas du chemin parcouru.__ On peut la généraliser à tout changement d'état monotherme complet.



__Réversibilité__  
Si le changement d'état est isotherme, c'est-à-dire qu'on reste toujours à température $T$ (isotherme), alors la transformation est réversible. En effet, l'entropie échangée s'écrit alors: $S_{e} = \frac{Q}{T} = \frac{\Delta H}{T} = \Delta S$. Donc $S_c = \Delta S - S_e = 0$.

Attention: Le chemin "palier" est réversible mais quand on met deux corps en contact et qu'il se produit un changement d'état, il est rare qu'on suive spontanément ce palier. En général, le système n'est PAS à l'équilibre durant la transformation: on ne peut même pas définir proprement la température et la pression du système! On peut par exemple voir la compression/dilatation par le mercure lors du TP: les fortes variations de pression montrent que le système est hors équilibre: ces transformations brutales ne suivent PAS le palier et ne sont PAS réversibles.


````{dropdown} Remarque

__Ordre et désordre__  
Les relations précédentes montrent que le signe de la variation d'entropie et la variation d'enthalpie sont identiques. Les observations expérimentales effectuées précédemment permettent d'écrire que:

\begin{align*}
&\Delta s_{vap} >0; \Delta s_{fus} >0; \Delta s_{sub} >0;\\
&\Delta s_{liq} <0; \Delta s_{sol} <0; \Delta s_{cond} <0
\end{align*}
Rappelons que l'entropie est une mesure du désordre. On retrouve donc que le gaz est l'état le plus désordonné devant le liquide, l'état solide étant au contraire l'état le plus ordonnée.
````

### Bilan complet

````{admonition} Exercice 
:class: attention

On s'intéresse au passage de la phase 1 à la température T à la limite de changement d'état seule à la phase 2 seule à la température T à la limite de changement d'état et on veut exprimer d'une manière général. Soit $\Delta h_{1 \rightarrow 2}$ l'enthalpie massique de changement d'état. On suppose l'évolution monotherme à température $T$.

1. Justifier que l'évolution est aussi monobare.
1. Déterminer les variations massiques d'entropie, d'énergie interne, d'énergie libre $F = U - TS$ et d'enthalpie libre $G = F + PV$.
1. Déterminer le transfert thermique $q$ et le travail mécanique massique reçu $w$.


````
````{dropdown} Démonstration

 

__Palier__  

__Durant toute la transformation, deux phases coexistent à la même température T__. La pression est alors imposée (pression de changement d'état à la température T) donc l'isotherme est aussi une isobare.
 


__Fonctions d'état__  
\begin{align*}
\Delta s &= \frac{\Delta h}{T}\\
\Delta u &= \Delta h - P_{ch} \Delta v\\
\Delta f &= - P_{ch} \Delta v\\
\Delta g &= 0
\end{align*}


__Transferts__  
\begin{align*}
q &= \Delta h\textrm{ car isobare }\\
w &= - P_{ch} \Delta v
\end{align*}
````

## Exemples

### Transformation de la glace en eau

````{admonition} Exercice 
:class: attention

On considère $m=1g$ de glace pris à la température de $T_1 = 250K$ sous pression extérieure constante $P_{atm}$ à 1bar. On supposera que la température de fusion de la glace est alors de $T_{fus} = 273K$. On chauffe la glace pour la transformer en eau liquide à $T_2 = 300K$. Calculer les variations d'enthalpie et d'entropie.

Données: $c_{glace} = 2,1 \rm{kJ.K^{-1}.kg^{-1}}, c_{liquide} = 4,2 \rm{kJ.K^{-1}.kg^{-1}}, \Delta h_f(T = 273 \rm{K}) = 335 \rm{kJ.kg^{-1}}$

````
````{dropdown} Démonstration

 

__Choix de la transformation__  

L'enthalpie est une fonction d'état, on peut donc choisir un chemin particulier pour calculer la variation $\Delta H$. Il est en de même pour la variation d'entropie $\Delta S$. Le chemin choisi se compose:

* d'un échauffement isobare de la glace jusqu'à 273K
* de la fonte totale de la glace à 273K
* d'un échauffement isobare de l'eau jusqu'à 300K

 

```{dropdown} Remarque

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

__Bilan entropique__  

Pour une phase condensée: $\Delta S = \int_{T_1}^{T_2} C\frac{dT}{T} = C \ln \left(\frac{T_2}{T_1}\right)$ d'où:

\begin{align*}
\Delta S_1 &= m c_{glace} \ln(\frac{T_{fus}}{T_1})\\
\Delta S_2 &= m \frac{\Delta h_{f}(T_{fus})}{T_{fus}}\\
\Delta S_3 &= m c_{liquide} \ln(\frac{T_2}{T_{fus}})\\
\Delta S &= m ( c_{glace} \ln(\frac{T_{fus}}{T_1}) + \frac{\Delta h_{f}(T_{fus})}{T_{fus}} + c_{liquide} \ln(\frac{T_2}{T_{fus}}))
\end{align*} 
````

### Mélange eau-glace

````{admonition} Exercice 
:class: attention

Un récipient contenant un mélange de 0,5kg de glace à 273K avec 0,5kg d'eau liquide est placé dans l'air ambiant à la température $T_0 = 293\rm{K}$ sous une pression extérieure de $p_0 = 1 \rm{bar}$. On constante qu'au bout d'une durée $\tau$, on isole le récipient et on observe que 0,2kg de glace a fondu. Faire un bilan entropique du système. Les données numériques sont les mêmes que dans l'exercice précédent.

````
````{dropdown} Démonstration

 

__Bilan entropique__  

La transformation est un changement d'état (partiel) à pression extérieure constante et à température extérieure constante. On suppose que la pression du système ne varie pas de sorte que sa température reste à 273K. On va considérer que les états initiaux et finaux sont des états d'équilibre (on a soustrait le système du contact du thermostat).

La variation d'entropie ne dépend pas du chemin. Elle s'écrit $\Delta S = m_{fondue} \frac{\Delta h_f(T_{fus})}{T_{fus}}$.

La transformation se fait au contact d'un thermostat à $T_0$, l'entropie échangée s'écrit donc $S_{ech} = \frac{Q}{T_0} = \frac{m_{fondue}\Delta h}{T_0}$ (la dernière expression vient de l'hypothèse d'une transformation monobare entre deux états d'équilibre).

Le second principe permet de calculer l'entropie crée:

\begin{align*}
S_c &= \Delta S - S_{ech}\\
&= \Delta h_{f}(T_{fus}) \left(\frac{1}{T_{fus}} - \frac{1}{T_0}\right) > 0
\end{align*}
L'évolution est irréversible à cause de l'inhomogénéité de température.
 
````

