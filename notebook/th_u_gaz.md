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
# Etude des gaz

## Etude empirique des gaz

_En général l'étude empirique des gaz se fait par le contrôle de deux paramètres (température et volume par exemple) et par la mesure du troisième. On cherche alors à modéliser la relation (P,V,T) par une équation d'état et à l'interprêter physique (notamment à l'échelle microscopique)._

### Gaz parfait


__Gaz parfait: Approche empirique__  
Un gaz parfait n'a aujourd'hui de définition rigoureuse que si l'on considère ses aspects cinétiques et donc microscopiques. A l'échelle macroscopique, on ne peut définir un gaz parfait que par son comportement: il suit la loi de Boyle-Mariote qu'on peut réécrire, la définition de la température absolue aidant: $PV = nRT$


````{dropdown} Remarque

__Comportement à basse pression__  
Du point de vue macroscopique, un gaz suit cette loi __si sa pression est relativement faible__ (cf. expérience de Boyle-Mariotte). Le seuil de pression à partir duquel on peut considérer que le gaz suit le modèle du gaz parfait dépend du gaz et de la précision exigée.

D'un point de vue microscopique, la nécessité d'une basse pression peut être reliée à la nécessité de négliger les interactions à longue distance.
````

### Mélange de gaz et pression partielle

````{admonition} Définition : Pression partielle
:class: tip

Quand plusieurs gaz parfaits sont mélangés et à l'équilibre, on définit la pression partielle des gaz comme la pression qu'il auraient s'ils étaient seuls dans l'enceinte.

````

````{admonition} Fondamental : Pression partielle et équation d'état
:class: attention

Dans un mélange de gaz parfaits, la pression partielle $P_r$ du gaz est reliée à la température et au volume du système par l'équation d'état des gaz parfait $P_r V = nRT$.
````

````{admonition} Fondamental : Pression totale
:class: attention

La pression totale est la somme des pressions partielles de chaque gaz.
````

### Ecart au gaz parfait. Gaz réel


Si l'on réalise une mesure du produit PV en faisant varier P,V pour une température donnée, on s'aperçoit qu'il apparaît un écart entre le produit PV et le produit nRT au fur et à mesure que P grandit. Cet écart au modèle du gaz parfait est d'autant plus important qu'on s'approche de la pression de vapeur saturante, c'est-à-dire la pression pour laquelle, pour une température donnée, le gaz se condense et forme un liquide.

Rappelons nous que le modèle du gaz parfait correspond à des particules dont l'interaction à distance est négligeable. Si l'on augmente la pression, ces interactions deviennent importantes et la réalité s'écarte du modèle. Comme on l'a vu en chimie, les interactions entre molécules ou atomes sont des interactions dites de Van der Waals. On peut se baser sur ces interactions pour trouver une équation d'état.



__Equation d'état de Van der Waals__  
Pour décrire le comportement réels des gaz, on dispose notamment d'un modèle: le gaz de Van der Waals. On propose comme équation d'état des gaz:

\begin{equation}
(P + \frac{n^2 a}{V^2})(V - nb) = nRT
\end{equation}
où a et b sont des constantes positives. Les termes correctifs $\frac{n^2 a}{V^2}$ et nb sont, en général, faibles devant respectivement P et V aux basses pressions. On appelle le terme $\frac{n^2 a}{V^2}$ __pression moléculaire__ et b le __covolume molaire__.


### Interprétation de l'équation d'état de Van der Waals

````{admonition} Exercice 
:class: attention

On considère un gaz suivant le modèle de Van der Waals.

1. Vers quoi tend le volume quand P tend vers l'infini à température fixée? En déduire une interprétation de b.
1. On suppose le covolume négligeable. Exprimer la pression $P$ d'un gaz de Van der Waals. La comparer à celle d'un gaz parfait dans les mêmes conditions. Cette correction est-elle cohérente avec des interactions attractives.

````

````{dropdown} Démonstration

 


__Interprétation du covolume.__  
Quand P tend vers l'infini, le terme $V-nb$ tend vers 0, c'est-à-dire que le volume tend vers $nb$. Cela correspond à un cas limite où toute les molécules se touchent. Le terme $nb$, homogène à un volume, correspond au volume minimal occupé par les particules du gaz. Il s'agit d'une correction due à la dimension non négligeable des particules.

Le terme $\frac{n^2 a}{V^2}$ est homogène à une pression (c'est-à-dire une force par unité de volume). Si l'on se place dans le cas relativement courant où le covolume est négligeable devant le volume V, l'équation d'état devient: $P = \frac{nRT}{V} - \frac{n^2 a}{V^2}$.

Autrement dit, pour une température et un volume donné, la pression moléculaire va avoir tendance à diminuer la pression par rapport au modèle du gaz parfait. La pression moléculaire représente en effet les forces d'interaction entre particules, c'est-à-dire les force de Van der Waals (le terme en $n^2/V^2$ représentent bien la distance moyenne entre particule élevée à la puissance 6). Ces forces sont attractives: elles vont avoir tendance à diminuer la "poussée'' du gaz sur la paroi (puisque les particules sont attirées ``vers" le gaz).

````

## Etude des gaz: Approche microscopique

### Théorie cinétique des gaz


Nous allons étudier les gaz par leur comportement à l'échelle microscopique. Cela permettra d'expliquer par des phénomènes microscopiques l'équation d'état des gaz parfait. Pour faire cette étude, nous devons distinguer deux types d'hypothèses: les premières sont générales à la théorie cinétique des gaz et les secondes sont propres à l'étude d'un gaz parfait.


````{admonition} Fondamental : Hypothèse de la théorie cinétique des gaz.
:class: attention

* Le gaz est à l'équilibre thermodynamique: la répartition des grandeurs macroscopiques extensives est donc homogène et constante dans tout le gaz.
* Il y a à l'échelle microscopique un chaos moléculaire c'est-à-dire que les molécules ont un mouvement incessant et désordonné: il est sans cesse modifié par des chocs avec d'autres molécules. Les vitesses et positions sont alors distribuées aléatoirement.

````


__Interprétation__  
Ces hypothèses ont quelques conséquences sur l'étude des gaz. On rappelle qu'à l'échelle microscopique, on ne peut connaître les caractéristiques de chaque particules mais on peut s'intéresser à la __statistique des différentes grandeurs, notamment des vitesses__.

* l'équilibre thermodynamique impose que la répartition statistique des vitesses $\overrightarrow{v}$ est la même à tout instant: on pourra noter $n(\overrightarrow{v})$ sans se soucier de l'instant $t$.
* l'homogénéité des grandeurs impose aussi que la distribution $n(\overrightarrow{v})$ est la même quelque soit la portion  considérée tout comme la concentration en particule.
* l'hypothèse du chaos moléculaire et le fait que que le gaz soit au repos impose aussi qu'il y a __isotropie de l'espace__, c'est-à-dire que toutes les directions de l'espace sont équivalente.On rappelle quelques conséquences sur la distribution des composantes des vitesses
* la moyenne d'ensemble d'une composantes est nulle.
* la statistique des composantes de vitesse est la même quelque soit la direction. Il vient notamment que la moyenne du carré de chaque composante est identique.
* une conséquence du dernier point est que le carré de la vitesse quadratique moyenne vaut 3 fois la moyenne du carré de chaque composante $u^2 = 3 \left\langle v_x^2 \right\rangle= 3 \left\langle v_y^2 \right\rangle= 3 \left\langle v_z^2 \right\rangle$




### Modèle du gaz parfait monoatomique


A l'échelle microscopique, le modèle du gaz parfait monoatomique est décrit par trois hypothèses.


````{admonition} Définition : Modèle du gaz parfait monoatomique
:class: tip

* Dans un gaz parfait, __les seuls interactions qui existent sont des forces de contact au moment des chocs__, soit entre particules, soit entre une particule et la paroi. Les interactions à longues distances, notamment entre particules sont négligées.
* On suppose de plus que __les chocs sont tous élastiques__, c'est-à-dire que l'énergie cinétique des deux particules qui s'entrechoquent ou du système {particule+paroi} est conservée au cours du mouvement.
* Dans le cadre d'un gaz parfait monoatomique, les particules peuvent être assimilées à des __particules ponctuelles__.


````

````{dropdown} Remarque

__Sur les hypothèses__  
La troisième hypothèse est propre aux gaz parfait monoatomiques. Son implication directe est que l'énergie cinétique microscopique se réduit à l'énergie cinétique de translation. Pour déterminer l'équation d'état du gaz, cette conséquence a peu d'importance mais elle en aura quand il s'agira de déterminer l'énergie interne du gaz. Pour un gaz parfait composé de molécules, l'hypothèse d'une taille négligeable reste importante pour négliger le covolume.

L'assimilation à des particules ponctuelles a une conséquences gênantes. En effet, si les particules sont ponctuelles, la probabilité qu'elles s'entrechoquent est...  nulle! Or les chocs sont nécessaires pour atteindre le chaos moléculaire (l'isotropie notamment). Il faut donc comprendre pour cette hypothèse: "particules de dimensions négligeables" devant la distance entre particules. Cela revient à dire que __le libre parcours moyen des particules est très grand devant la taille des particules__. Pour un gaz parfait dans les conditions ambiantes, le libre parcours moyen se situe entre 10nm et $1 \rm{\mu m}$.

La première hypothèse est cruciale. On a vu que macroscopiquement, l'existence d'interactions à distances non négligeables impliquaient une déviance du comportement réel du gaz par rapport au modèle du gaz parfait.

On peut s'attarder sur l'hypothèse de l'élasticité des chocs. Dans le cas d'un gaz parfait monoatomique, la seule possibilité de transfert d'énergie est de l'énergie cinétique vers l'énergie de l'atome (du gaz ou de la paroi) qui conduit à une excitation de l'atome: les électrons peuvent passer à un niveau d'énergie supérieure. Or cela implique un échange d'énergie de l'ordre de l'électron-volt et donc une énergie cinétique du même ordre au moins. Pour cela, il faudrait une température d'au moins 11000K! Les systèmes étudiées n'atteindrons jamais cette température. L'hypothèse du choc élastique est donc pleinement justifiée.
````

### Calcul de la pression cinétique


Ce calcul est à savoir faire par coeur.


````{admonition} Exercice 
:class: attention

On s'intéresse à un élément de surface orienté vers l'extérieur de l'enceinte. Pour plus de simplicité, nous définissons un repère cartésien où l'axe Ox est suivant la normale à la paroi orienté vers l'extérieur ($\overrightarrow{dS} = dS \overrightarrow{e_x} = dy dz \overrightarrow{e_x}$).

On va travailler sous le modèle du choc simplifié (modèle de Krönig, 1856). Dans ce cadre, on suppose que:

* toutes les particules (identiques) ont en module la même vitesse v.
* chaque particule ne peut se déplacer que suivant une seule des trois directions Ox, Oy, Oz (dans les deux sens).


On peut obtenir l'expression de la pression cinétique sans ces hypothèses mais une telle démonstration n'est plus dans le cadre du programme.

1. Que vaut la vitesse quadratique?
1. Déduire des hypothèses précédentes le nombre de particules par unité de volume qui possèdent la vitesse $+v \overrightarrow{e_x}$.
1. On considère une particule heurtant la paroi entre t et t+dt. Relier la variation $\overrightarrow{\rm{d} p_1}$de quantité de mouvement de la particule entre t et t+dt à la force moyenne exercée par la particule sur la paroi entre t et t+dt. En déduire l'expression de la pression cinétique en fonction de $\overrightarrow{\rm{d} p_1}$, du nombre $dN_{choc}$ de particules qui heurtent la paroi dS entre t et t+dt et de la surface dS.
1. Exprimer $\overrightarrow{\rm{d} p_1}$ en fonction de la masse de la particule et de sa vitesse v.
1. Déterminer le volume dans lequel doivent se trouver les particules à l'instant t pour qu'elles heurtent la paroi dS entre t et t+dt. En déduire $dN_{choc}$.
1. En déduire que la pression cinétique s'exprime comme $P = \frac{N}{3V}mu^2$


````
````{dropdown} Démonstration

 


__Pression et force moyenne__  
Le principe fondamentale de la dynamique appliqué à la particule dans le référentiel de la paroi supposé galiléen s'écrit: $\frac{\rm{d}\overrightarrow{p}}{\rm{dt}} = \overrightarrow{F_{paroi \to particule}} = - \overrightarrow{F_{particule \to paroi}}$. Il vient le calcul de la force moyenne:

\begin{align*}
\left\langle F_{particule \to paroi} \right\rangle &= \frac{1}{\rm{d}t} \int_{t}^{t+\rm{d}t}F_{particule \to paroi}(t) \rm{d}t\\
&= - \frac{1}{\rm{d}t} \int_{t}^{t+\rm{d}t}\frac{\rm{d}\overrightarrow{p}}{\rm{\rm{d}t}} \rm{d}t\\
&= - \frac{1}{\rm{d}t} \int_{\overrightarrow{p}(t)}^{\overrightarrow{p}(t+\rm{d}t)} \rm{d}\overrightarrow{p}\\
&= - \frac{1}{\rm{d}t} \overrightarrow{\rm{d} p_1}
\end{align*}
La force exercée par l'ensemble du gaz s'écrit évidemment $\left\langle \overrightarrow{dF_{gaz \to paroi}} \right\rangle = dN_{choc} \left\langle \overrightarrow{F_{gaz \to particule}} \right\rangle$ soit une pression cinétique:

\begin{align*}
P &= \frac{\left\langle \overrightarrow{\rm{d}F_{gaz\to paroi}} \right\rangle \cdot \overrightarrow{e_x}}{\rm{d}S}\\
&= - \frac{dN_{choc}}{\rm{d}t \rm{d}S} \overrightarrow{\rm{d} p_1}\cdot \overrightarrow{e_x}
\end{align*}


__Variation de quantité de mouvement__  
Remarquons que pour heurter la paroi, la particule doit nécessairement se diriger suivant $+ \overrightarrow{e_x}$. Avec les hypothèses simplifiées, elle aura donc une vitesse $+ v \overrightarrow{e_x}$ avant le choc et une vitesse $- v\overrightarrow{e_x}$ après le choc.

\begin{align*}
\overrightarrow{d p_{1}} &= \overrightarrow{p(t+dt)} - \overrightarrow{p(t)}\\
&= - 2m v \overrightarrow{e_x}
\end{align*}


__Dénombrement des particules__  
On veut déterminer $dN_{choc}$. Pour venir taper la surface $dS$ entre $t$ et $t+dt$, les particules, sous l'hypothèse du choc simplifié doivent satisfaire les conditions suivantes:

* avoir à l'instant $t$ la vitesse $\overrightarrow{v} = + v \overrightarrow{e_x}$
* se trouver dans le cylindre de base $dS$ (sinon elle taperait à côté)
* être à une distance de la paroi inférieure à $vdt$ (sinon, elle n'atteindrait pas la paroi avant $t+dt$)


Les deux dernières conditions impliquent toutes les particules qui se situent dans le cylindre de hauteur $vdt$ appuyé sur la base $dS$ et seulement ces particules viendront heurter la paroi entre $t$ et $t+dt$. A l'équilibre, les grandeurs sont homogènes, et le nombre total de particules contenues dans ce volume s'obtient par une règle de trois (on note $N_V$ le nombre de particules par unités de volume du gaz): $dN_{cylindre} = N_V d \tau_{cylindre} = \frac{N}{V} vdt dS$

La première condition, associée à l'isotropie implique que seules $1/6$ de ces particules vont venir heurter la paroi: $dN_{choc} = \frac{N}{6V} v dt dS = \frac{N}{6V} u dt dS$



__Calcul de la pression cinétique:__  
Il vient: $P = \frac{N}{6V} u dt dS \frac{2mu}{dt dS} = \frac{N}{3V} m u^2$

````

### Approche microscopique: Equation d'état des gaz parfait

````{admonition} Fondamental : Pression cinétique
:class: attention

Sous les hypothèses de la théorie cinétique et du gaz parfait, la pression cinétique est reliée à la vitesse quadratique moyenne:

\begin{equation}
P = \frac{N}{3V} mu^2
````

_Rappel : Température cinétique_  
On rappelle que la vitesse quadratique moyenne est reliée à la température par $\frac{3}{2}k_B T = \frac{1}{2}m u^2$.


````{admonition} Fondamental : Equation d'état des gaz parfait.
:class: attention

L'équation d'état d'un gaz parfait monoatomique est: $PV = Nk_B T = nRT$. Elle se démontre à partir de l'expression de la pression cinétique et de la température cinétique.
````

## Etude des gaz: Equation énergétique

### Energie interne des gaz parfaits: Première loi de Joule

_Rappel :_  
L'énergie interne est une fonction d'état. Elle peut donc se définir comme une fonction de variables d'état indépendantes par exemple U(T,V,n) (en pratique on écrira en physique U(T,V) car on travaille avec des systèmes fermés où n peut être considéré comme un paramètre).

On rappelle que le comportement de l'énergie interne vis-à-vis d'une des variables est caractérisée par une dérivée partielle. On définit en particulier la capacité thermique à volume constante $C_V = {\left ( \frac{\partial U}{\partial T}\right )}_V$.

La différentielle de l'énergie interne peut alors s'écrire:

\begin{equation}
dU(T,V) = C_V(T,V) dT + {\left(\frac{\partial U}{\partial V}\right)}(T,V)_T dV
\end{equation}


On a choisi ici d'exprimer U comme une fonction de T et V. Ce sera souvent le cas dans les premiers temps mais il faut savoir qu'on peut aussi exprimer U comme une fonction de S et V. Les dérivées partielles sont alors différentes (on pourra remarquer qu'il s'agit alors de la température et de la pression).


````{admonition} Fondamental : Première loi de Joule
:class: attention

L'énergie interne d'un gaz parfait __ne dépend que de la température__: $U(T,V) = U(T)$. Sa différentielle s'écrit: $dU = C_V(T) dT$.

Dans la majorité des cas étudiés, on peut considérer que la capacité thermique à volume constant ne dépend pas de T sur de grandes gammes de températures, de sorte que la variation d'énergie interne sur une transformation finie s'écrit $\Delta U = C_V \Delta T$.
````

````{admonition} Exemple : 
:class: tip, dropdown

La capacité thermique molaire à volume constant du Néon dans les gammes de températures ambiantes (et jusqu'à plus de 600K) est de l'ordre de $12.4 J.\rm{mol^{-1}.K^{-1}}$. Elle est à peu près égale à $\frac{3}{2}R$.

La capacité thermique molaire à volume constant du dihydrogène dans les gammes de températures ambiantes (et jusqu'à plus de 600K) est de l'ordre de $20.8 J.\rm{mol^{-1}.K^{-1}}$. Elle est à peu près égale à $\frac{5}{2}R$.

Nous verrons par la suite que ces valeurs ont un sens particuliers.
````

### Enthalpie des gaz parfaits: Deuxième loi de Joule

_Rappel : L'enthalpie est une fonction d'état. Elle peut donc se définir comme une fonction de variables d'état indépendantes par exemple U(T,P,n) (en pratique on écrira en physique U(T,P) car on travaille avec des systèmes fermés où n peut être considéré comme un paramètre)._

On rappelle que le comportement de l'enthalpie vis-à-vis d'une des variables est caractérisée par une dérivée partielle. On définit en particulier la capacité thermique à pression constante $C_P = {\left ( \frac{\partial H}{\partial T}\right )}_P$.

La différentielle de l'enthalpie peut alors s'écrire:

\begin{equation}
dH(T,P) = C_P(T,P) dT + {\left(\frac{\partial H}{\partial P}\right)}(T,P)_T dP
\end{equation}


On a choisi ici d'exprimer H comme une fonction de T et P alors qu'on a exprimé U comme une fonction de T et V. On aurait très bien pu exprimer H comme une fonction de T et V mais comme on le verra par la suite, il est préférable d'exprimer H(T,P) plutôt que H(T,V) à cause de l'utilisation faite de H. De même, il arrive qu'on préfère écrire H(S,P) mais nous nous servirons peu de cette vision de l'enthalpie.


````{admonition} Fondamental : Deuxième loi de Joule
:class: attention

L'enthalpie d'un gaz parfait __ne dépend que de la température__: $H(T,P) = H(T)$. Sa différentielle s'écrit: $dH = C_P(T) dT$.

Dans la majorité des cas étudiés, on peut considérer que la capacité thermique à pression constante ne dépend pas de T sur de grandes gammes de températures, de sorte que la variation d'énergie interne sur une transformation finie s'écrit $\Delta H = C_P \Delta T$.
````

````{admonition} Exemple : 
:class: tip, dropdown

La capacité thermique molaire à pression constante du Néon dans les gammes de températures ambiantes (et jusqu'à plus de 600K) est de l'ordre de $20.8 J.\rm{mol^{-1}.K^{-1}}$. Elle est à peu près égale à $\frac{5}{2}R$.

La capacité thermique molaire à pression constante du dihydrogène dans les gammes de températures ambiantes (et jusqu'à plus de 600K) est de l'ordre de $29.0 J.\rm{mol^{-1}.K^{-1}}$. Elle est à peu près égale à $\frac{7}{2}R$.

Nous verrons par la suite que ces valeurs ont un sens particuliers.
````

### Relation de Mayer et coefficient gamma

````{admonition} Fondamental : Relation de Mayer
:class: attention

Pour un gaz parfait: $C_P - C_V = nR$
````


__Démonstration__  
La première loi de Joule donne l'expression de $\Delta U = C_V \Delta T$. La variation d'enthalpie s'écrit donc: $\Delta H = \Delta (U + PV) = \Delta U + \Delta (nRT) = (C_V + nR) \Delta T$ donc $C_P = C_V + nR$



__Interprétation__  
On rappelle que la capacité thermique à volume constant donne l'énergie à fournir pour augmenter la température de 1K à volume constant et la capacité thermique à pression constante l'énergie à fournir pour augmenter la température de 1K à pression constante. La relation de Mayer montre que $C_P > C_V$: il est donc plus coûteux (en énergie) d'augmenter la température à pression constante que de l'augmenter à volume constante. On pourra en comprendre la raison par la suite.


````{admonition} Définition : Coefficient gamma.
:class: tip

On définit le coefficient gamma $\gamma$ d'un gaz parfait par le rapport $\gamma = \frac{C_P}{C_V}$. Il dépend du type de gaz mais pas de la quantité de gaz. Il est nécessairement supérieur à 1.

````

````{admonition} Fondamental : Coefficient gamma et capacités thermiques
:class: attention

En général, la seule donnée du coefficient gamma suffit à caractériser un gaz parfait (en plus de préciser qu'il s'agit d'un gaz parfait) d'un point de vue énergétique. En effet, avec la relation de Mayer, on a deux relations, faisant intervenir les capacités thermiques, on peut donc les exprimer en fonction du coefficient gamma et du nombre de mole.

__On s'entraînera à montrer les expressions suivantes (utilisables directement):__  

\begin{align*}
C_V &= \frac{nR}{\gamma-1}\\
C_p &= \frac{\gamma nR}{\gamma - 1}
\end{align*}
````

### Cas du gaz parfait monoatomique

````{admonition} Fondamental : Energie interne d'un gaz parfait monoatomique
:class: attention

L'énergie interne d'un gaz parfait monoatomique est $U = \frac{3}{2}n R T$. Sa capacité thermique à volume constant est donc $C_V = \frac{3}{2}nR$ et sa capacité thermique à pression constante est $\frac{5}{2}nR$.

Le coefficient gamma d'un gaz parfait monoatomique est donc $\gamma = \frac{5}{3}$.
````


__Justification__  
On rappelle que l'énergie interne est la somme de toutes les composantes "microscopiques" de l'énergie. On distingue l'énergie associée à la translation des molécules, à leur vibration, à leur rotation et enfin l'énergie potentielle d'interaction.

Dans le cas d'un gaz parfait, l'énergie potentielle d'interaction est nulle puisqu'on néglige les interactions à longues distances.

De plus, il n'y a ni vibration, ni rotation pour des atomes (assimilables à des points matériels). La seule compose restante est donc l'énergie cinétique de translation.

On a vu que cette dernière valait en moyenne $\overline{E_C}=\frac{3}{2}k_B T$ soit une énergie cinétique totale pour N particule: $E_C = \frac{3}{2}Nk_B T = \frac{3}{2}n R T$.


### Cas des gaz parfaits polyatomiques

_Rappel : On rappelle que pour tout gaz parfait, l'énergie interne ne dépend que de la température._


````{admonition} Compléments : Loi d'équipartition (admis)
:class: hint, dropdown

On peut montrer que chaque terme énergétique "quadratique'' (c'est-à-dire proportionnel au carré de la position ou de la vitesse) __peut contribuer__ à l'énergie interne pour une valeur $\frac{1}{2}k_B T$. On appelle ces termes des ``degrés de liberté" du système.
````

````{admonition} Exemple : Cas de l'énergie cinétique de translation.
:class: tip, dropdown

Pour une particule l'énergie cinétique de translation s'écrit $\frac{1}{2}m v_x^2 + \frac{1}{2}m v_y^2 + \frac{1}{2}m v_z^2$. Il y a donc trois termes quadratiques qui contribuent donc pour $\frac{3}{2}k_B T = \frac{3}{2}nR T$. Pour un gaz composé de N particules, on retrouve une énergie interne de $\frac{3}{2}Nk_B T$.
````

````{admonition} Exemple : Cas d'une molécule diatomique. Energie interne maximale.
:class: tip, dropdown

Pour une molécule diatomique, outre l'énergie cinétique de translation, il va aussi y avoir une énergie cinétique de vibration ($\frac{1}{2}m \dot \Delta l^2$) et une énergie potentielle de vibration ($\frac{1}{2}k \Delta l^2$) qui peuvent contribuer à l'énergie interne  soit un terme supplémentaire $nRT$.

De plus il y a aussi l'énergie cinétique de rotation qui peut être complètement décrite par deux rotations (de vitesses angulaires notés $\dot \phi$ et $\dot \theta$ associées à des énergies cinétiques $\frac{1}{2}J_{\phi}\dot \phi^2$ et $\frac{1}{2}J_{\theta}\dot \theta^2$) soit un terme supplémentaire $nRT$.

Il vient qu'on attend une énergie interne maximale égale à $U = \frac{7}{2}nRT$ soit $C_V = \frac{7}{2}nR$.
````

````{admonition} Compléments : Gel des degrés de liberté.
:class: hint, dropdown

En pratique, l'énergie interne des gaz parfaits diatomiques n'est que très rarement égale à sa valeur maximale. Par exemple, à température ambiante (pour beaucoup de gaz parfait diatomique et de gaz parfaits en général), elle est égale à $\frac{5}{2}nR T$.

En effet, suivant la température, certains "degrés" de liberté sont "gelés", c'est-à-dire que les mouvements associées se ne se produisent. On observe ainsi que pour de nombreux gaz parfait diatomiques à température ambiante, les molécules ne vibrent pas de sorte que les degrés de liberté associés ne participent par à l'énergie interne.D'où une énergie interne $U = \frac{5}{2}nRT$.

On peut montrer que lorsque la température augmente, le degré de liberté se dégèle pour la quasi-totalité de molécule très rapidement de sorte que la capacité thermique change assez rapidement de valeur avec la température avant de rester constante sur un large palier de température.

```{figure} ./images/thermo_cv_temperture.jpg
:name: fig_271
:align: center

```
````

### Energie interne des gaz réels

````{admonition} Exemple : Cas du gaz de Van der Waals (pas à connaître)
:class: tip, dropdown

De manière générale, l'énergie interne d'un gaz qui ne suit pas la première loi Joule: elle dépend à la fois de la température et du volume.

Par exemple, on associe au modèle de Van der Waals, une énergie interne $U = U_{GP} - \frac{n^2 a}{V^2}$. Le terme correctif est associé à l'énergie potentielle d'interaction. Elle est négative car l'interaction est attractive (Van der Waals).
````

