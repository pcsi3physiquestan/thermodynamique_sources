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
# Comprendre le contexte

Les machines thermiques sont la base de la révolution industrielle et d'une partie du fonctionnement industriel actuel. Leur but: effectuer une conversion d'énergie (ou de puissance) incluant un transfert thermique.

Leur fonctionnement général se base sur le principe simple d'équivalence entre travail et échange thermique (ou chaleur) --- c'est-à-dire le premier principe tel que l'a énoncé Joule. On peut donc voir une machine thermique comme un système, en général un fluide passant pour différentes transformation pour soit:

* prendre et donner de la chaleur à des corps pour fournir un travail mécanique: on parlera de __moteur__.
* à partir d'un travail mécanique reçu, effectuer un échange de chaleur qui ne peut se faire naturellement (refroidir en été, chauffer une pièce en hiver... ). On distinguera deux types de machines suivant leur utilité:
* les réfrigérateurs, servant à refroidir une source froide
* les pompes à chaleur qui fonctionnement sur le même principe thermodynamique mais qui servent à maintenir une pièce à une température chaude.
