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

## Variables d'état
````{admonition} Utilisation des grandeurs intensives 
:class: attention

1. On considère un gaz parfait dont l'équation d'état est $PV = nRT$. Réexprimer cette équation avec uniquement des grandeurs intensives en introduisant le volume massique et la masse molaire puis en introduisant le volume molaire.
1. On considère maintenant l'équation d'état d'un gaz de Van der Waals donnée comme $(P - \frac{a^2}{V_m^2})(V_m - b) = RT$ où $V_m$ est le volume molaire. Etablir l'équation de Van der Waals pour un volume V et un nombre de mole n.
````

````{topic} Correction
>
>__1. De l'extensif vers l'intensif.__  
>
>Pour obtenir des grandeurs massiques, il faut diviser par la masse. Il vient $P v = \frac{n}{m}RT$ soit $Pv = \frac{RT}{M}$.
>
>Pour obtenir des grandeurs molaires, il faut divier par le nombre de moles. Il vient $PV_m = RT$.
> 
>
>__2. De l'intensif vers l'extensif.__  
>
>On va remplacer le volume molaire $V_m$ par $V/n$ soit:
>
>\begin{align*}
(P - \frac{n^2 a^2}{V})(\frac{V}{n} - b) &= RT\\
(P - \frac{n^2 a^2}{V})(V - nb) &= nRT
\end{align*} 
````

````{admonition} Energie interne 
:class: attention

On considère un gaz non modélisable par le modèle du gaz parfait car les interactions à longue distance entre les particules du gaz ne sont pas négligeable. L'énergie totale se décompose en la partie macroscopique définie comme en mécanique et l'énergie interne. Un modélisation possible dite de Van der Waals consiste à écrire l'énergie interne du gaz à partir de celle du gaz parfait sous la forme $U = U_{GP} - \frac{n^2 a}{V} + U_0$ où $U_0$ est l'énergie interne aux conditions $(T_0,V_0)$ et $U_{GP}$ l'énergie interne d'un gaz s'il suivait le modèle du gaz parfait dans les mêmes conditions.

Préciser physiquement quel signe attend-on pour a.
````

````{topic} Correction
>
>Les interactions dans un gaz de Van der Waals sont des interactions entre molécules neutres donc de ...  Van der Waals. Elles sont donc attractives. L'énergie potentielle d'interaction doit donc être croissante avec la distance entre particules et l'énergie potentielle d'interaction totale sera donc aussi croissante avec le volume V (qui augmente la distance moyenne entre particules). La différence proposée ici entre les deux modèles est qu'on tient compte des interactions. On attend donc un terme correction croissant avec le volume donc un coefficient a positif.
````

````{admonition} Entropie: Analyse qualitative 
:class: attention

On se propose ici de retrouver la monotonie de l'entropie d'un gaz parfait par un raisonnement qualitatif. On considère n moles d'un gaz parfait. _On rappelle que l'entropie est une mesure du désordre._

* Justifier que l'entropie du gaz va augmenter si l'on augmente la température à volume constant.
* Justifier que l'entropie du gaz va augmenter si l'on augmente le volume à température constante.
* Peut-on prévoir qualitativement l'évolution de l'entropie de l'entropie si l'on augmente le volume et qu'on diminue la température?

On considère un corps pur à une pression P et une température T de changement d'état (ici vaporisation). Il peut alors exister sous sa forme gazeuse ou liquide (P,T). 
* Dans quelle phase l'entropie sera la plus grande?
* Reprendre la question précédente pour les phases solides et liquides d'un corps pur à un couple (P,T) de solidification.

````
````{topic} Correction
>__Cas d'un gaz parfait__  
>Si l'on augmente la température, cela signifie qu'on augmente l'énergie cinétique des molécules. On peut donc considérer qualitativement qu'on augmente le désordre (on augmente la gamme de vitesses accessibles) et donc l'entropie. C'est ce qu'on observe avec l'expression de S(T,V).
>
>Si l'on augmente le volume, on augmente la place accessible et donc les positions possibles pour les particules: le désordre augmente donc l'entropie aussi. C'est aussi ce qu'on observe avec l'expression de S(T,V)
>
>Si le volume augmente tandis que la température diminue, on ne peut déterminer si l'entropie va augmenter ou diminuer. En effet, il y a plus de place accessible mais l''énergie cinétique moyenne va diminuer. L'expression de S nous permettra de remarquer qu'effectivement suivant les cas l'entropie va augmenter ou diminuer.
>
>__Cas d'un changement de phase__  
>Dans une phase gazeuse, les molécules peuvent se mouvoir sur de plus grandes distances avec peu d'interactions avec les autres particules: il naît donc un chaos plus important. L'entropie de la phase gazeuse sera donc plus grand (cela suppose évidemment qu'on compare la même quantité de matière).
>
>De même l'entropie de la phase liquide, plus désordonnée, sera plus grande que l'entropie de la phase solide.
````

````{admonition} Calculer une pression 
:class: attention

On considère un gaz contenu dans une enceinte fermée sur un côté par un piston de section S et de masse M glissant sans frottement sur les paroi de l'enceinte. De l'autre côté du piston se trouve une atmosphère à pression $P_0$.

1. Déterminer la pression du gaz à l'équilibre en fonction de M,g, S et $P_0$ suivant que le piston se trouve sur une face latérale ou sur la face supérieure de l'enceinte.
1. Déterminer le volume de l'enceinte à l'équilibre en supposant que la température du gaz est maintenue à $T_0$ et que le gaz suit le modèle du gaz parfait.


````
````{topic} Utilisation d'un équilibre mécanique

>Un équilibre mécanique est traduit par un théorême de la résultante dynamique à l'équilibre sur la paroi mobile - ici le piston. On travaille dans le référentiel de l'enceinte supposée galliléen.
>
>On note Ox l'axe vertical ascendant et Oy un axe horizontal.
>
>Les actions qui s'exercent sur le piston sont:
>
>* l'action de la paroi. Elle n'a pas de composante suivant le déplacement du piston puisqu'il n'y a pas de frottements.
>* l'action de __l'atmosphère extérieure.__  
>* l'action du gaz
>* l'action de la pesanteur.
>
>
>Cas horizontal. On projette suivant Ox (dirigé du gaz vers l'extérieur):
>
>\begin{align*}
0 &= PS - P_0 S\\
P &= P_0
\end{align*}
>Cas vertical. On projette suivant Oz:
>
>\begin{align*}
0 &= PS - P_0 S - Mg\\
P &= P_0 + \frac{Mg}{S}
\end{align*} 

```{attention}

Plusieurs erreurs fréquentes sont rencontrées lors de l'établissement de l'équilibre mécanique.

* Très souvent, l'étudiant écrit directement $P = P_0$ sans tenir compte des autre action.
* De nombreuses erreurs de signe peuvent se produire.


```


_Calcul des forces de pression :_ En thermodynamique, on sera souvent amené à étudier des forces de pressions uniformes sur des surfaces planes. Il n'est pas nécessaire dans ce cas de passer par un calcul intégrale: la force de pression est directement la pression multipliée par la surface (reste à l'orienter correctement).

````

````{admonition} Etude d'un gaz 
:class: attention

Considérons une mole d'argon ($M = 39,9 \rm{g.mol^{-1}}$) considérée comme un gaz parfait contenu dans un récipient de volume $V=22.4\rm{L}$ et à une température $T=273,15\rm{K}$.

1. Déterminer la pression du gaz.
1. Déterminer le nombre de particules et la distance moyenne entre deux particules proches.
1. Déterminer l'énergie cinétique moyenne et la vitesse quadratique moyenne des particules.
1. En déduire un estimation du temps entre deux chocs sur une paroi. Commenter le principe de calculer une force "moyenne" pour étudier une force de pression.
1. On définit le __libre parcours moyen__ d'une particule comme la distance moyenne que parcourt la particule entre deux chocs. On peut montrer qu'il vaut $l=\frac{1}{\sqrt{2}n^* \pi d^2}$ où d est le diamètre des particules et $n^*$ la concentration en particule.
    1. Reexprimer le libre parcours moyen en fonction de la pression, de la température et de d.
    1. A température ambiante et pression ambiante, le libre parcours moyen est d'environ 100nm. Représenter qualitativement la trajectoire d'une particule. Commenter.
    1. Estimer le diamètre des particules. Commenter.


````
````{topic} Résolution

>__Pression__  
>$P = \frac{nRT}{V} = 10^5 \rm{Pa}$.
>
>
>
>__Distance inter atomique__  
>$N = n N_A = 6 \times 10^{23} \rm{particules}$
>
>On peut estimer le volume moyen libre entourant une particules par $V^* = \frac{V}{nN_A}$. En assimilant ce volume à un cube, la distance moyenne entre deux particules proches se de l'ordre de $d \sim {\left( \frac{V}{nN_A}\right)}^{1/3} = 3 \times 10^{-9} \rm{m}$.
>
>On remarque que cette distance est grande devant la taille des atomes. Dans une modélisation en terme d'interaction entre dipôle électrostatique, on pourrait considérer que cette distance suffit à négliger les interactions à distance entre particules.
>
>
>
>__Vitesse quadratique moyenne__  
>On utilise l'interprétation cinétique de la température $\overline{E_c} = \frac{3}{2}k_B T = 5 \times 10^{-21} J$ (on pourra remarquer que cette énergie est faible devant 1eV).
>
>Pour calculer la vitesse quadratique moyenne, on a besoin de la masse d'un atome d'argon qu'on va déterminer à partir de sa masse molaire: $m = \frac{M}{N_A}$
>
>Il vient une vitesse quadratique moyenne $v = \sqrt{\frac{2 \overline{E_c}N_A}{M}} = 1.2 \times 10^2 \rm{m.s^{-1}}$
>
>On remarquera qu'il s'agit de vitesses très importantes. Ce déplacement n'est pas "visible" car il se fait dans toutes les directions de sorte que la vitesse moyenne de déplacement reste faible.
>
>
>
>__Fréquence des chocs__  
>Pour un volume V, on peut considérer que la taille caractéristique de l'enceinte est $L = V^{1/3}$. La distance parcouru entre deux chocs sur une même paroi par une particule est de l'ordre de 2L et donc le temps deux chocs sur une paroi pour une particule est de l'ordre de $\frac{2L}{v}$. Avec N particules, la fréquence des chocs est donc de l'ordre de $f_{choc} \sim \frac{Nv}{2L} \sim 1.2 * 10^{26} \rm{Hz}$.
>
>On observe qu'il y a donc un très grand nombre de chocs. Pendant une durée infinitésimale (mais associée à une échelle mésoscopique) dt, on pourra considérer que ce nombre reste grand et motive une étude statistique. On travaillera ainsi avec des forces moyennes exercées par les particules.
>
>On pourra remarquer aussi que les fréquences des chocs est bien plus grandes que la fréquence de mesures que peut prendre un capteur de pression. Ce dernier mesure donc aussi une force __moyenne.__  
>
>
>
>__Libre parcours moyen__  
>De l'équation d'état des gaz parfait, il vient que $n^* = \frac{N}{V} = \frac{PN_A}{RT} = \frac{P}{k_B T}$ (on retiendra que $R = N_A k_B$). Il vient $l = \frac{k_B T}{\sqrt{2}\pi d^2 P}$.
>
>Il s'agit donc d'une trajectoire erratique, on parlera de chaos moléculaire. On peut par contre remarquer que cette distance est grande devant la taille des atomes.
>
>$d = \sqrt{\frac{k_B T}{\sqrt{2}\pi P l}} \sim 3 \times 10^{-10} \rm{m}$. Il s'agit donc à peu près de la taille d'un atome. Elle est légèrement plus grande du fait qu'on tient compte de la portée de l'interaction entre particules.

````

