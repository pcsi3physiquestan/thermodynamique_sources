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
# Introduction

_On dit que le second principe est historiquement antérieur au premier. L'idée sur laquelle il repose est en effet plus ancienne. En effet, le second principe permet de déterminer si une transformation peut se réaliser dans les deux sens (elle sera donc réversible) ou au contraire si elle ne peut se dérouler que dans un sens (elle sera donc irréversible). Par exemple, la détente de Joule Gay-Lussac est irréversible. Au contraire, l'affaissement d'un piston par ajout successif de toutes petites masses est réversible si on néglige les frottements._

## Insuffisance du premier principe (en ligne)


````{topic} Mise en situation
Si l'on considère deux corps de températures différentes isolés de l'extérieur. Le premier principe peut s'appliquer mais il ne donne pas d'information complète sur l'état final. En effet, la conservation de l'énergie permet de lier les températures des deux solides mais on ne peut les calculer sans une donnée/hypothèse supplémentaire.

Le "bon sens" nous permet de dire que dans l'état final, les deux corps auront la même température mais du point de vue du seul premier principe, on pourrait tout autant supposer que le corps chaud s'est réchauffé et le corps froid s'est refroidi.

On trouve bien d'autres transformations dont l'__irréversibilité__ ne peut être expliquée par le premier principe. Ainsi:

* deux gaz mis en contact vont se mélanger
* de nombreux réactions chimiques sont irréversibles.


C'est le rôle du second principe de permettre de distinguer le sens d'évolution possible des transformations.

On parlera de principe d'évolution.
````


## Causes d'irréversibilité


__Causes d'irréversibilité__  
On sera amené à montrer qu'une transformation est irréversible. Il est important de pouvoir déterminer une cause d'irréversibilité. Les principales causes sont: 
* la présence de forces de frottement (visqueux ou solide).
* la non uniformité des grandeurs intensives: elles entraîne en général des phénomènes de diffusion (thermiques ou de particules) qui sont irréversibles.
* les réactions chimiques (qui correspond en réalité à la non uniformité d'une grandeur intensive particulière, le potentiel chimique)


On pourra noter qu'il peut y avoir plusieurs causes simultanées. En général, en trouver une suffit.


