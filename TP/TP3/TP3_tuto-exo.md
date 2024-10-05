# TP 3 : Du gène au génme

## Table des matières

- [Introduction](#introduction)
- [Ressources bioinformatiques](#ressources-bioinformatiques) 
- [Exercice 1 - ](#)
- [Que retenir de ce TP ?](#que-retenir-de-ce-tp)

## Auteurs

1. Jacques van Helden
2. Bénédicte Wirth

## Introduction


### But du TP

Utiliser  des ressources bioinformatiques pour explorer les génomes d’organismes modèles, afin de comprendre la structuration et la composition de ces génomes. 

### Concepts


## Exemples traités

### Détermination de la formation de l'oeil des métazoaires (PAX6, aniridia, eyeless)

Le gène PAX6 humain (également appelé aniridia) code pour un facteur trnascriptionnel qui s'exprime dans certains tissus pendant l'embryogenèse, et contrôle la formation de l'oeil. Des mutations de PAX6 suscitent des malformations de l'oeil. On trouve des homologues du gène PAX6 dans les génomes des métazoaires (animaux pluricellulaires). 

### Notions mises en pratique dans ce TP

- Structuration des gènes (transcrits, introns, exons, régions codantes, régions non traduites)
- Organisation des génomes (éléments structurels des chromosomes, régions géniques et intergéniques, opérons bactériens). 
- Quelques éléments de génomique comparative (conservation / divergence, réarrangements chromosomiques, synténie)
- Les principaux types d’homologie : orthologie, paralogie
- Annotation fonctionnelle des gènes. 
- Transcriptomique : expression différentielle des gènes dans différents tissus
- Protéomique : analyse de l’ensemble des protéines codées par un génome


## Ressources bioinformatiques

| Ressource | Lien | Description |
|:--------------------|:-----------------|:-------------------------------------------------------|
| UCSC genome browser | [genome.ucsc.edu](https://genome.ucsc.edu/) | Navigateur génomique présentant un vaste choix de types d'annotations  |
| ECR Browser | [ecrbrowser.dcode.org](https://ecrbrowser.dcode.org/) | Outil de visualisation des régions génomiques conservées entre quelques espèces animales |

## Annotations génomiques dans la région du gène humain PAX6

Nous allons utiliser le navigateur de génomes [**UCSC genome browser**](https://genome.ucsc.edu/) pour consulter différents types d'annotations génomiques dans la région du gène humain PAX6. 

- Connectez-vous au [**UCSC genome browser**](https://genome.ucsc.edu/)
- Dans le menu **Genomes**, sélectionnez la version **hg38** du génome humain
- Entrez le nom du gène d’intérêt (**PAX6**) dans la boîte de recherche et cliquez sur **Search**. 

La page de résultat affiche une série d’annotations de PAX6 dans différentes bases de données de référence pour le génome humain. Comment choisir ? En première instance, le mieux est de se fier aux annotations du consortium international HUGO, responsable de la nomenclature des gènes humains. 
- Sous le titre **HUGO Gene Nomenclature**, cliquez sur le lien  `PAX6 - chr11:31789026-31817960`. 

Le navigateur de génomes UCSC Genome Browser affiche un vaste choix de pistes d’annotation. La carte génomique en affiche un sous-ensemble, qui s’adaptent en fonction de vos consultations précédentes. 
Nous allons restreindre la visualisation aux pistes d’annotations utilisées pour ce TP. 


- Descendez sous la carte génomique pour afficher les choix de pistes d’annotations. 

- Dans la catégorie "**Mapping and Sequencing**", sélectionnez le mode d’affichage "**dense**" pour la piste d’annotation "**Base position**". 

- Dans la catégorie "**Genes and Gene Prediction**", sélectionnez le mode "**pack**" pour la piste "**GENCODE_V46**". 

- Cliquez "**Refresh**" à droite d’une des catégories. 

- Cliquez "**Resize**" sous la carte pour ajuster la largeur à celle de votre écran. 

Vous pouvez à tout moment reconfigurer le mode d’affichage d’une piste d’annotation, en cliquant droit (contrôle-click) sur la barre grise à sa gauche. Ceci vous affichera un menu avec des modes d’affichages de plus en plus détaillés : hide, dense, squish, pack, full.


- Testez les différents niveaux de détail avec la piste GENCODE_V46, puis sélectionnez le mode **squish**, qui vous permet généralement de visualiser les transcrits alternatifs en occupant une place raisonnable. 

- Dans la catégorie "**Repeats**", activez l’affichage de "**Repeatmasker**” en format "**dense**" et cliquez "**Refresh**". 

- Modifiez l’affichage de la piste **GENCODE_V46** pour l’afficher en "**dense**". 

### Questionnaire TP3 – Exercice 1

Sur Ametice, ouvrez le questionnaire du TP3 et répondez aux questions de l'Exercice 1.



## Conservation du gène PAX6 chez les animaux




## Que retenir de ce TP ?

