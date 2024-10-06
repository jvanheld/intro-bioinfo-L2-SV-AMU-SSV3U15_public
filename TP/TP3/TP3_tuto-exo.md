# TP 3 : Du gène au génome

## Table des matières

- [Introduction](#introduction)
- [Exemples traités](#exemples-traites)
- [Ressources bioinformatiques](#ressources-bioinformatiques) 
- [Exercice 1 - Annotations génomiques dans la région du gène humain PAX6](#exercice-1---annotations-génomiques-dans-la-région-du-gène-humain-pax6)
- [Exercice 2 - Conservation du gène PAX6 dans les génomes de vertébrés](#exercice-2---conservation-du-gène-pax6-dans-les-génomes-de-vertébrés)
- [Exercice 3 - Profil tissulaire de transcription de PAX6](#exercice-3---profil-tissulaire-de-transcription-de-pax6)
- [Exercice 4 - Annotation d’un fragment chromosomique bactérien](#exercice-4---annotation-dun-fragment-chromosomique-bactérien)
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

## Exercice 1 - Annotations génomiques dans la région du gène humain PAX6

Nous allons utiliser le navigateur de génomes [**UCSC genome browser**](https://genome.ucsc.edu/) pour consulter différents types d'annotations génomiques dans la région du gène humain PAX6. 

- Connectez-vous au [**UCSC genome browser**](https://genome.ucsc.edu/)
- Dans le menu **Genomes**, sélectionnez la version **hg38** du génome humain.
- Entrez le nom du gène d’intérêt (**PAX6**) dans la boîte de recherche et cliquez sur **Search**. 

La page de résultat affiche une série d’annotations de PAX6 dans différentes bases de données de référence pour le génome humain. Comment choisir ? En première instance, le mieux est de se fier aux annotations du consortium international HUGO, responsable de la nomenclature des gènes humains. 
- Sous le titre **HUGO Gene Nomenclature**, cliquez sur le lien  `PAX6 - chr11:31789026-31817960`. 

Le navigateur de génomes UCSC Genome Browser affiche un vaste choix de pistes d’annotation. La carte génomique en affiche un sous-ensemble, qui s’adaptent en fonction de vos consultations précédentes. 
Nous allons restreindre la visualisation aux pistes d’annotations utilisées pour ce TP. 


- Descendez sous la carte génomique pour afficher les choix de pistes d’annotations. 

- Entre la carte et les options, cliquez **Hide all** pour masquer les pistes génomiques par défaut.

- Dans la catégorie **Mapping and Sequencing**, sélectionnez le mode d’affichage **dense** pour la piste d’annotation **Base position**. 

- Dans la catégorie **Genes and Gene Prediction**, sélectionnez le mode **pack** pour les pistes **HGNC** et **GENCODE_V46**. HGNC indique les limites des gènes, tandis que GENCODE_V46 fournit des informations plus détaillées sur la structure des gènes (introns, exons, transcrits alternatifs, ...). 

- Cliquez **Refresh** à droite d’une des catégories. 

- Cliquez **Resize** sous la carte pour ajuster la largeur à celle de votre écran. 

Vous pouvez à tout moment reconfigurer le mode d’affichage d’une piste d’annotation, en cliquant droit (**contrôle-clic**) sur la figure. Ceci vous affichera un menu avec des modes d’affichages de plus en plus détaillés : hide, dense, squish, pack, full.


- Testez les différents niveaux de détail avec la piste GENCODE_V46, puis sélectionnez le mode **squish**, qui vous permet généralement de visualiser les transcrits alternatifs en occupant une place raisonnable. 

- Dans la catégorie **Repeats**, activez l’affichage de **Repeatmasker**” en format **dense** et cliquez **Refresh**. 

- Dézoomez (**Zoom out**) d’un facteur **x1.5** pour voir les environs du gène

- **Déplacez la piste HGCN** au-dessus de la piste GENCODE_V46 (en  positionnant la souris vers le coin supérieur gauche d’une piste, une flèche apparaît qui permet de la déplacer)

Observez la disposition du gène PAX6. Notez qu’il chevauche ses voisins de gauche (ELP4) et de droite (PAX6-AS1, où AS indique qu’il s’agit d’un gène antisens). 


### Questionnaire TP3 – Exercice 1

Sur Ametice, ouvrez le questionnaire du TP3 et répondez aux questions de l'Exercice 1 Annotations génomiques dans la région du gène humain PAX6.



## Exercice 2 - Conservation du gène PAX6 dans les génomes de vertébrés

- Dans la catégorie **Comparative genomics**, activez l’affichage pack de la piste **Conservation**. 

- A priori, cette piste s’affiche entre les annotations GENCODE_V46 et les régions répétitives. **Faites remonter la piste RepeatMasker** pour la placer entre les pistes GENCODE_V46 et Conservation. 

- Cliquez droit (**contrôle-clic**) sur l’image de conservation à la hauteur où s’affichent les espèces et sélectionnez **Configure MultiZ Align**. 

- Dans la fenêtre d’options qui apparaît, **cochez quelques espèces de votre choix**. 

    - **Veillez à panacher** (essayez d’avoir une ou deux espèces de chaque groupe plutôt qu’un tas d’espèces du même groupe).
    
    - Pour une raison technique, le génome du chien présente des lacunes à cet endroit du génome. **Désactivez l’affichage du chien** (dog) et activez celui d’un ou deux autres mammifères du même groupe.  
    
    - Dans la catéogrie **Mammal, cochez toutes les espèces**. Notez que les catégories précédentes contiennent également des mammifères (Primates, Euarchontoglires, Laurasiatheria). La catégorie Mammal présente des espèces plus éloignées (marsupiaux, monotrèmes), qui sont utiles pour visualiser les régions les plus conservées entre mammifères. 

- Cliquez **Apply**. 

- **Dézoomez d’un facteur 1.5** pour observer le contexte aux alentours du gène. 

Dans la figure qui apparaît, la carte de conservation génomique comporte deux parties. 

1. La partie supérieure affiche un **profil de conservation** calculé à partir de l’alignement de 100 génomes de vertébrés. La hauteur du profil indique le *pourcentage de positions identiques* (*PPI*) à chaque position du génome.  Notez que l'échelle verticale va de  50% à 100%, pour mieux faire ressortir les régions conservées. 

2. La partie inférieure indique, sous forme d’une échelle de gris, le pourcentage de conservation par position chez chacune des espèces que vous avez sélectionnées. 


### Questionnaire TP3 – Exercice 2

Sur Ametice, ouvrez le questionnaire du TP3 et répondez aux questions de l'Exercice 2 "*Conservation de la région génomique PAX6 chez les vertébrés*".

## Exercice 3 - Profil tissulaire de transcription de PAX6

Nous allons maintenant ajouter à notre carte génomique une piste d’annotation de la base de données GTEx (Genotype-Tissue Expression). GTEx contient des données de transcriptome (mesure quantitative de tous les transcrits produits par un génome) dans des échantillons de 54 tissus prélevés chez 948 personnes adultes. 



- Dans la catégorie **Expression**, activez l’affichage **pack** de **GTEX_Gene_V8**. 

- **Cliquez sur l’icône** du gène PAX6 sur la piste GTEX_Gene_V8, et examinez le profil d’expression tissulaire. 


**Interprétation du graphique**

Les profils sont affichés sous forme de "boîte à moustaches" (box plot en anglais) pour chaque tissu.
- L’axe horizontal indique les tissus échantillonnés dans GTEx. 
- L’axe vertical indique le taux de transcription. 
- La barre horizontale épaisse indique le niveau médian (50% des échantillons ont un niveau inférieur, et 50% un niveau supérieur)
- Le bas du rectangle indique le 1er quartile  (25% des échantillons ont un niveau inférieur)
- Le haut du rectangle indique le 3ème quartile (75% des échantillons ont un niveau supérieur)
- La barre verticale indique un intervalle de confiance
- Les points isolés sont des "outliers" (valeurs exceptionnellement hautes ou basses, non représentatives de l’ensemble des échantillons). 

### Questionnaire TP3 – Exercice 3

Sur Ametice, ouvrez le questionnaire du TP3 et répondez aux questions de l'Exercice 3 "*Profil d’expression tissulaire de PAX6*".

## Exercice 4 - Annotation d’un fragment chromosomique bactérien

Vous disposez d’un fragment chromosomique bactérien, que vous pouvez récupérer en cliquant ici. 

- [seq_bact_a-annoter.fasta.txt](sequences/seq_bact_a-annoter.fasta.txt)

Vous allez utiliser quelques outils bioinformatiques pour annoter ce fragment d’ADN chromosomique.
La première étape d’annotation consiste à localiser les gènes sur ce fragment d’ADN, puis il faudra essayer de trouver la fonction assurée par ces gènes.


Afin de localiser les gènes sur ce fragment d’ADN chromosomique, vous allez réaliser une recherche de cadres ouverts de lecture (*open reading frames*, *ORFs*). Pour cela, vous allez utiliser l’outil ORFinder du NCBI.

1.	Connectez-vous à ORFinder du NCBI.
2.	Collez la séquence du fragment chromosomique bactérien dans l’encadré "**Enter Query Sequence**".
3.	Dans la section, "**Choose Search Parameters**" :


    - Fixez la longueur minimale des ORFs recherchés à 300 pb ;
    - Choisissez le code génétique le plus approprié
    - Pour le codon start à utiliser pour la recherche, choisissez "**ATG only**"

4.	Cliquez **Submit**.


## Que retenir de ce TP ?

