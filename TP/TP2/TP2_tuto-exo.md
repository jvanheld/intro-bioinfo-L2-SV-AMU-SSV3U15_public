# TP 2 : Du gène à la protéine

## Table des matières

- [Auteurs](#auteurs)
- [Introduction](#introduction)
- [Ressources informatiques](#ressources-informatiques) 
- [Tutoriels et exercices](#tutoriels-et-exercices) 
- [Eléments de synthèse](#eléments-de-synthèse)


## Auteurs

- Emese Meglécz
- Bénédicte Wirth
- Aitor Gonzalez
  
## Introduction

### But du TP

Dans ce TP vous apprendrez à effectuer une recherche dans une base de données, et à réaliser les alignements par paires de séquences.

### Concepts

Dans un gène eucaryote, les exons et les introns sont alternés. Après transcription du gène en ARN primaire, la maturation de ce transcrit inclut généralement une étape d’épissage, qui consiste à éliminer les introns et à rabouter les exons. Au terme de ce processus, seuls les exons seront présents dans l’ARN mature. Quand on aligne l’ADN d’un gène avec son ARN mature, on devrait donc trouver des régions parfaitement alignées et identiques entre elles à 100% (les exons) séparées par de longs gaps de l’alignement, qui correspondent aux introns (présents dans le gène, mais absents de l’ARN mature). Il faut noter que ce processus d’épissage peut se produire dans les gènes codants ou non codants (ARN de transfert ou ribosomique). 

Pour les gènes codants, l’ARN “messager” (ARNm) comporte une région codante, des régions non traduites en amont (5’ UTR), en aval (3’ UTR). La région codante sert de modèle pour synthétiser une protéine en polymérisant des acides aminés (traduction). Similairement, en alignant la traduction de l’ARN avec la protéine codée par le gène, la protéine devrait s’aligner avec les régions codantes des exons, mais pas avec les régions UTR.


### Exemples traités

Nous nous baserons sur le cas d’étude suivant. 

**Comparaison des séquences de gène de phosducine (PDC) sa transcription (l’ARNm) et la protéine codée par le gène.** La phosphoducine est une phosphoprotéine située dans les  bâtonnets de la rétine. Elle module la cascade de phototransduction en interagissant avec la protéine G rétinienne. Le gène est un gène candidat pour la rétinite pigmentaire et le syndrome d'Usher de type II. Des variantes de transcription à épissage alternatif codant pour différentes isoformes ont été identifiées.


### Notions abordées

- Gène, exon, intron, UTR
- Alignment par paire
- Complémentarité des nucléotides, et séquences réverse complémentaires
- Traduction
- Cadre ouvert de lecture

### Compétences acquises au cours de ce TP

A l’issue de ce TP, vous devriez avoir acquis les compétences suivantes. 

- Recherche avancée dans une base de donnée de séquences
- Téléchargement des séquences
- Alignement par paire (alignement exact et BLAST)
- Interprétation des alignements et leurs divers représentations graphique

## Ressources informatiques

| Ressource | Lien | Description |
|:---------|:--------------------------|:-------------------------------------------|
| NCBI gene | https://www.ncbi.nlm.nih.gov/gene/ | Base de données des gène hébergée par NCBI |
| Sequence Manipulation Suite (**SMS**) | http://www.bioinformatics.org/sms2/ |  Large gammes d’outils pour la manipulation des séquences biologiques (traduction, reverse complement, ORFfinder...) |
| needle | https://www.ebi.ac.uk/jdispatcher/psa/emboss_needle  |  Algorithme d’alignement par paire (méthode de Needleman-Wunsch, exacte, produisant des alignements globaux) |
| NCBI BLAST|  https://blast.ncbi.nlm.nih.gov/Blast.cgi  |  Recherche par similarité: comparaison d’une séquence à une base de données  |


## Tutoriels et exercices

### Tutoriel 1 : 


### Exercice 1 : 


### Tutoriel 2 : 


### Exercice 2 : 


## Eléments de synthèse
