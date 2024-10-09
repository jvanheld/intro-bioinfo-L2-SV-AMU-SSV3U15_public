# TP 3 : Du gène au génome

## Table des matières

- [Introduction](#introduction)
- [Exemples traités](#exemples-traites)
- [Ressources bioinformatiques](#ressources-bioinformatiques) 
- [Exercice 1 - Annotations génomiques dans la région du gène humain PAX6](#exercice-1---annotations-génomiques-dans-la-région-du-gène-humain-pax6)
- [Exercice 2 - Conservation du gène PAX6 dans les génomes de vertébrés](#exercice-2---conservation-du-gène-pax6-dans-les-génomes-de-vertébrés)
- [Exercice 3 - Profil tissulaire de transcription de PAX6](#exercice-3---profil-tissulaire-de-transcription-de-pax6)
- [Exercice 4 - Annotation d'un fragment chromosomique bactérien](#exercice-4---annotation-dun-fragment-chromosomique-bactérien)
- [Qu'avez-vous acquis au terme de ce TP ?](#quavez-vous-acquis-au-terme-de-ce-tp)

## Auteurs

1. Jacques van Helden
2. Bénédicte Wirth

----------------------------------------------------------------

## Introduction


### But du TP

Utiliser  des ressources bioinformatiques pour explorer les génomes d'organismes modèles, afin de comprendre la structuration et la composition de ces génomes. 

### Concepts


## Exemples traités

### Détermination de la formation de l'oeil des métazoaires (PAX6, aniridia, eyeless)

Le gène PAX6 humain (également appelé aniridia) code pour un facteur transcriptionnel qui s'exprime dans certains tissus pendant l'embryogenèse, et contrôle la formation de l'œil. Des mutations de PAX6 suscitent des malformations de l'oeil. On trouve des homologues du gène PAX6 dans les génomes des métazoaires (animaux pluricellulaires). 

### Notions mises en pratique dans ce TP

- Structuration des gènes (transcrits, introns, exons, régions codantes, régions non traduites).
- Organisation des génomes (éléments structurels des chromosomes, régions géniques et intergéniques, opérons bactériens). 
- Quelques éléments de génomique comparative (conservation / divergence, réarrangements chromosomiques, synténie).
- Les principaux types d'homologie : orthologie, paralogie.
- Annotation fonctionnelle des gènes.
- Transcriptomique : expression différentielle des gènes dans différents tissus.
- Protéomique : analyse de l'ensemble des protéines codées par un génome.

----------------------------------------------------------------


## Ressources bioinformatiques

| Ressource | Lien | Description |
|:--------------------|:-----------------|:-------------------------------------------------------|
| UCSC genome browser | [genome.ucsc.edu](https://genome.ucsc.edu/) | Navigateur génomique présentant un vaste choix de types d'annotations  |
| NCBI ORFfinder | [www.ncbi.nlm.nih.gov/orffinder](https://www.ncbi.nlm.nih.gov/orffinder/) | Détection de cadre ouverts de lecture (ORFs)  dans des séquences nucléiques |
| RegulonDB | [regulondb.ccg.unam.mx/](https://regulondb.ccg.unam.mx/) | base de connaissance sur la régulation transcriptionnelle chez la bactérie *Escherichia coli*: facteurs transcriptionnels, sites de liaison, régulons, opérons |

## Exercice 1 - Annotations génomiques dans la région du gène humain PAX6

Nous allons utiliser le navigateur de génomes [**UCSC genome browser**](https://genome.ucsc.edu/) pour consulter différents types d'annotations génomiques dans la région du gène humain PAX6. 

- Connectez-vous au [**UCSC genome browser**](https://genome.ucsc.edu/).
- Dans le menu **Genomes**, sélectionnez la version **hg38** du génome humain.
- Entrez le nom du gène d'intérêt (**PAX6**) dans la boîte de recherche et cliquez sur **Search**. 

La page de résultat affiche une série d'annotations de PAX6 dans différentes bases de données de référence pour le génome humain. Comment choisir ? En première instance, le mieux est de se fier aux annotations du consortium international HUGO, responsable de la nomenclature des gènes humains. 
- Sous le titre **HUGO Gene Nomenclature**, cliquez sur le lien  `PAX6 - chr11:31789026-31817960`. 

Le navigateur de génomes UCSC Genome Browser affiche un vaste choix de pistes d'annotation. La carte génomique en affiche un sous-ensemble, qui s'adaptent en fonction de vos consultations précédentes. 
Nous allons restreindre la visualisation aux pistes d'annotations utilisées pour ce TP. 


- Descendez sous la carte génomique pour afficher les choix de pistes d'annotations. 

- Entre la carte et les options, cliquez **Hide all** pour masquer les pistes génomiques par défaut.

- Dans la catégorie **Mapping and Sequencing**, sélectionnez le mode d'affichage **dense** pour la piste d'annotation **Base position**. 

- Dans la catégorie **Genes and Gene Prediction**, sélectionnez le mode **pack** pour les pistes **HGNC** et **GENCODE_V46**. HGNC indique les limites des gènes, tandis que GENCODE_V46 fournit des informations plus détaillées sur la structure des gènes (introns, exons, transcrits alternatifs, ...). 

- Cliquez **Refresh** à droite d'une des catégories. 

- Cliquez **Resize** sous la carte pour ajuster la largeur à celle de votre écran. 

Vous pouvez à tout moment reconfigurer le mode d'affichage d'une piste d'annotation, en cliquant droit (**contrôle-clic**) sur la figure. Ceci vous affichera un menu avec des modes d'affichages de plus en plus détaillés : hide, dense, squish, pack, full.


- Testez les différents niveaux de détail avec la piste GENCODE_V46, puis sélectionnez le mode **pack**, qui vous permet généralement de visualiser les transcrits alternatifs en occupant une place raisonnable. 

- Dans la catégorie **Repeats**, activez l'affichage de **Repeatmasker** en format **dense** et cliquez **Refresh**. 

- Dézoomez (**Zoom out**) d'un facteur **x1.5** pour voir les environs du gène

- **Déplacez la piste HGCN** au-dessus de la piste GENCODE_V46 (en  positionnant la souris vers le coin supérieur gauche d'une piste, une flèche apparaît qui permet de la déplacer)

Observez la disposition du gène PAX6. Notez qu'il chevauche ses voisins de gauche (ELP4) et de droite (PAX6-AS1, où AS indique qu'il s'agit d'un gène antisens). 


### Questionnaire TP3 – Exercice 1

Sur Ametice, ouvrez le questionnaire du TP3 et répondez aux questions de l'Exercice 1 "*Annotations génomiques dans la région du gène humain PAX6*".


----------------------------------------------------------------

## Exercice 2 - Conservation du gène PAX6 dans les génomes de vertébrés

- Dans la catégorie **Comparative genomics**, activez l'affichage **pack** de la piste **Conservation**. 

- A priori, cette piste s'affiche entre les annotations GENCODE_V46 et les régions répétitives. **Faites remonter la piste RepeatMasker** pour la placer entre les pistes GENCODE_V46 et Conservation. 

- Cliquez droit (**contrôle-clic**) sur l'image de conservation à la hauteur où s'affichent les espèces et sélectionnez **Configure MultiZ Align**. 

- Dans la fenêtre d'options qui apparaît, **cochez quelques espèces de votre choix**. 

    - **Veillez à panacher** (essayez d'avoir une ou deux espèces de chaque groupe plutôt qu'un tas d'espèces du même groupe).
    
    - Pour une raison technique, le génome du chien présente des lacunes à cet endroit du génome. **Désactivez l'affichage du chien** (dog) et activez celui d'un ou deux autres mammifères du même groupe.  
    
    - Dans la catéogrie **Mammal, cochez toutes les espèces**. Notez que les catégories précédentes contiennent également des mammifères (Primates, Euarchontoglires, Laurasiatheria). La catégorie Mammal présente des espèces plus éloignées (marsupiaux, monotrèmes), qui sont utiles pour visualiser les régions les plus conservées entre mammifères. 

- Cliquez **Apply**. 

- **Dézoomez d'un facteur 1.5** pour observer le contexte aux alentours du gène. 

Dans la figure qui apparaît, la carte de conservation génomique comporte deux parties. 

1. La partie supérieure affiche un **profil de conservation** calculé à partir de l'alignement de 100 génomes de vertébrés. La hauteur du profil indique le *pourcentage de positions identiques* (*PPI*) à chaque position du génome.  Notez que l'échelle verticale va de  50% à 100%, pour mieux faire ressortir les régions conservées. 

2. La partie inférieure indique, sous forme d'une échelle de gris, le pourcentage de conservation par position chez chacune des espèces que vous avez sélectionnées. 


### Questionnaire TP3 – Exercice 2

Sur Ametice, ouvrez le questionnaire du TP3 et répondez aux questions de l'Exercice 2 "*Conservation de la région génomique PAX6 chez les vertébrés*".


----------------------------------------------------------------

## Exercice 3 - Profil tissulaire de transcription de PAX6

Nous allons maintenant ajouter à notre carte génomique une piste d'annotation de la base de données GTEx (Genotype-Tissue Expression). GTEx contient des données de transcriptome (mesure quantitative de tous les transcrits produits par un génome) dans des échantillons de 54 tissus prélevés chez 948 personnes adultes. 



- Dans la catégorie **Expression**, activez l'affichage **pack** de **GTEX_Gene_V8**. 

- **Cliquez sur l'icône** du gène PAX6 sur la piste GTEX_Gene_V8, et examinez le profil d'expression tissulaire. 


**Interprétation du graphique**

Les profils sont affichés sous forme de "boîte à moustaches" (box plot en anglais) pour chaque tissu.
- L'axe horizontal indique les tissus échantillonnés dans GTEx. 
- L'axe vertical indique le taux de transcription. 
- La barre horizontale épaisse indique le niveau médian (50% des échantillons ont un niveau inférieur, et 50% un niveau supérieur)
- Le bas du rectangle indique le 1er quartile  (25% des échantillons ont un niveau inférieur)
- Le haut du rectangle indique le 3ème quartile (75% des échantillons ont un niveau inférieur)
- La barre verticale indique un intervalle de confiance
- Les points isolés sont des "outliers" (valeurs exceptionnellement hautes ou basses, non représentatives de l'ensemble des échantillons). 

### Questionnaire TP3 – Exercice 3

Sur Ametice, ouvrez le questionnaire du TP3 et répondez aux questions de l'Exercice 3 "*Profil d'expression tissulaire de PAX6*".

----------------------------------------------------------------

## Annotation d'un fragment chromosomique bactérien

----------------------------------------------------------------
Nous disposons d'un fragment chromosomique bactérien, qu'on peut récupérer en cliquant ici. 

- [seq_bact_a-annoter.fasta.txt](sequences/seq_bact_a-annoter.fasta.txt)

Ouvrez ce fichier dans un onglet séparé. Pour l'étape suivante, vous pourrez soit le copier à partir de cet onglet, soit le sauvegarder sur votre ordinateur et l'ouvrir avec un éditeur de texte de votre choix. 

Nous allons utiliser quelques outils bioinformatiques pour annoter ce fragment d'ADN chromosomique. La première étape  consiste à localiser les gènes sur ce fragment d'ADN. Il faudra ensuite essayer de trouver la fonction assurée par ces gènes.

### Exercice 4-5 - Recherche des cadres ouverts de lecture

Afin de localiser les gènes sur ce fragment d'ADN chromosomique, nous allons effectuer une recherche de cadres ouverts de lecture (*open reading frames*, *ORFs*), en utilisant l'outil ORFinder du NCBI.

1.	Connectez-vous à l'outil **[ORFinder du NCBI](https://www.ncbi.nlm.nih.gov/orffinder/)**.
2.	Collez la séquence du fragment chromosomique bactérien dans l'encadré "**Enter Query Sequence**".
3.	Dans la section, "**Choose Search Parameters**" :

    - Fixez la longueur minimale des ORFs recherchés à 300 pb.
    - Choisissez le code génétique le plus approprié. 
    - Pour le codon start à utiliser pour la recherche, choisissez "**ATG only**".
    -	Cliquez **Submit**.

4. Sur la fenêtre de résultats de la recherche d'ORFs, cliquez sur "**Six-frame translation**", puis sur "**Display six-frame translation**".

#### Questionnaire TP3 – Exercice 4: Annotation d'une séquence bactérienne  - traduction sur 6 phases

Qu'observez-vous dans la fenêtre qui s'affiche ?  En particulier
- à quoi correspondent les lettres rouges?

- à quoi correspondent les astérisques ?

- pourquoi y a-t-il 3 lignes de lettres décalées au dessus de la séquence d'ADN, et 3 en-dessous ?

- à quoi correspondent les lettres bleues (descendez dans la fenêtre pour les voir)

  

Fermez la fenêtre "Six frame translation", puis relancez la traduction sur 6 phases  avec une option alternative, en cliquant sur **Six-frame translation** puis sur **Add six-frame translation track**. Qu'observez-vous dans la fenêtre qui s'affiche ?

**Astuce :** pour répondre aux questions 2 et 3, zoomez sur la carte jusqu'à faire apparaître l'enchaînement des résidus (acides aminés et nucléotides).

#### Questionnaire TP3 – Exercice 5: Pistes de traduction sur les 6 phases de lecture

- à quoi correspondent les pistes marquées +1, +2, +3, -1, -2, -3 ? 
- à  quoi correspondent les traits verticaux verts ? 
- à quoi correspondent les traits verticaux rouges ? 
- à quoi correspondent les plages grises ?
- y a-t-il le même nombre de plages grises que d'ORFs détectés en rouge dans la piste ORFinder ? D'où vient la différence ? 

### Exercice 6 - Tailles des régions intergéniques

Vous allez maintenant déterminer la taille des régions intergéniques (RI) entre ces ORFs.

***Astuce:**  sous la carte des ORF, ORFfinder affiche un tableau indiquant les coordonnées génomiques et la taille des ORFs détectés. Vous pouvez récupérer les valeurs de ce tableau pour calculer la taille des régions intergéniques. *


- **Dézoomez** complètement.
- **Refermez la piste six-frame translation** en cliquant sur la petite croix rouge en haut à droite (attention, ne fermez pas la piste des ORFs produits par ORFfinder).
- Sur le tableau de coordonnées des ORFs, cliquez sur l'en-tête de colonne **Start** pour **trier les ORFs par position**. 
- **Notez les positions** de fin de l'ORF1 et de début de l'ORF6. 
- **Calculez la taille de la RI** entre ORF1 et ORF6. 
- **Zoomez** sur la région intergénique entre ORF1 et ORF6 et **vérifiez** si la taille calculée correspond à ce que vous voyez, au nucléotide près.
- Faites de même pour les autres ORFs, pour déterminer la taille des RI qui les séparent.



#### Questionnaire TP3 – Exercice 6: Tailles des régions intergéniques

- Quelle est la taille de la RI entre ORF1 et ORF6 ?
- Quelle est la taille de la RI entre ORF6 et ORF4 ? 
- Quelle est la taille de la RI entre ORF4 et ORF2 ? 
- Quelle est la taille de la RI entre ORF2 et ORF7 ? 
- Quelle est la taille de la RI entre ORF7 et ORF5 ? 
- Quelle est la taille de la RI entre ORF5 et ORF3 ? 
- Quelle est la taille de la RI entre ORF3 et ORF8 ? 
- Quelle est la taille de la RI entre ORF8 et ORF9 ? 

Quelles  conclusions  peut-on tirer à partir des tailles de ces RI ?

- Quelle structure serait présente sur ce fragment d'ADN chromosomique ? 

    Une seule réponse: UTR, intron, exon, opéron, site d'épissage

- Quels ORFs seraient inclus dans cette structure ? 

    Une ou plusieurs réponses:  ORF1, ORF6, ORF4, ORF5, ORF8, ORF10 

- Quels éléments vous permettent de conclure sur le nombre d'ORFs inclus dans cette structure ? (une ou plusieurs réponses)
    - Distances intergéniques courtes ou nulles
    - Chevauchements entre ORFs
    - Orientation des ORFs
    - Longueur des ORFs



### Exercice 7 - Assignation de fonction par recherche de similarité

Vous allez maintenant vous intéresser à l'annotation fonctionnelle de ces ORFs détectés dans le fragment d'ADN chromosomique étudié.  Pour cela, le plus simple est de faire une recherche par similarité dans une base de données (outil BLAST), afin de comparer les ORFs identifiés aux séquences déjà connues et répertoriées dans les bases de données.

Vous allez ainsi vérifier à quel gène pourraient correspondre les ORF1 et 10. 

- Cliquez sur l'ORF1. La traduction de l'ORF en protéine s'affiche dans l'encadré du dessous.
- Cliquez sur le bouton BLAST. Vous lancez ainsi une recherche de similarité en comparant la séquence protéique traduite de l'ORF1 avec chacune des séquences d'une base de données.
- A partir de la page de résultats du BLAST, répondez aux questions suivantes.

#### Questionnaire TP3 – Exercice 7: Assignation de fonction par recherche de similarité

- Quelle est la modalité de BLAST utilisée ?  (une seule réponse): blastn, blastp, blastx, tblastn
- En quoi consiste une recherche par BLASTP ?

    - Requête protéine versus base de données de protéines
    - Requête nucléique versus base de données de protéines
    - Requête protéine versus base de données nucléique

- Quelle est la base de données interrogée lors de cette requête ? (une seule réponse) UniprotKB TREMBL, UniprotKB complet, Swiss-prot

- Combien de résultats obtenez-vous ? (Réponse numérique)

- Pour la séquence cible la plus similaire à la requête soumise, quel est le pourcentage d'identité obtenu ? (Réponse numérique)

- Quel est son pourcentage de couverture par rapport à la séquence requête ? (Réponse numérique)

- Quelle est la E-value obtenue ? (réponse numérique)

- Que signifie une e-value de 0.0 ? (plusieurs choix possibles)

    - Similarité non significative
    - Ressemblance nulle
    - Similarité extrêmement significative

- Est-ce que ces deux séquences alignées sont vraisemblablement homologues ? (Oui / Non)

- Quelle est la fonction que l'on peut ainsi associer à l'ORF1 ?

    - ATP phosphoribosyltaransferase
    - Aspartate kinase
    - ATP-PRT
    - Homoserine dehydrogenase

### Identification du gène correspondant à ORF1

Vous allez maintenant rechercher le nom du gène correspondant à l'ORF1.

- Dans la dernière colonne du tableau de résultats de BLAST, cliquez sur le "numéro d'accession" de la séquence la plus similaire à l'ORF1.  Ceci ouvre dans un nouvel onglet la fiche de la séquence protéique correspondante.
- Dans la section "FEATURES" (annotations de la séquence), trouvez le premier objet de type gène, et consultez son nom (attribut “/gene” de l'objet "gene".

**Question** (Hors questionnaire)

- Quel est le nom du gène correspondant à l'ORF1 ? (une seule réponse)

    - HIS1_ECOK1
    - A1ACN1
    - Glycosyltransferase,
    - hisG
    - HisG
    - ATP-PRT
    - ATP-PRTase
    - ATP phosphoribosyltransferase

### Fonction et identification de l'ORF10

L'ORF10 chevauche étonnamment l'ORF8 de manière importante, sur une grande partie de sa longueur. Afin de tenter de déterminer à quel gène pourrait correspondre cet ORF10, vous allez donc faire, pour l'ORF10, la même manipulation que celle faite pour l'ORF1.

- Sur la page de résultat de la recherche d'ORF, commencez par trouver la taille en nucléotides de l'ORF10, ainsi que la taille en acides aminés de la protéine potentielle codée par cet ORF10. Pour cela, vous avez deux possibilités :
- Trouver ces informations dans l'encadré qui récapitule les ORFs trouvés sur le fragment d'ADN. 
- Placer le curseur sur l'ORF10 (sans cliquer) : la fenêtre qui s'ouvre contient les caractéristiques de l'ORF10.
- Cliquez ensuite sur l'ORF10, afin de le sélectionner. La traduction de l'ORF en protéine s'affiche dans l'encadré du dessous.
- Cliquez sur le bouton BLAST pour lancer la recherche par similarité de séquences avec cette séquence protéique.

**Questions** (Hors questionnaire)

- Combien de résultats obtenez-vous ?
- Quelle fonction pouvez-vous assigner à l'ORF10 sur base du résultat ? (une ou plusieurs réponses possibles)

    - 4-hydroxy-3-methylbut-2-en-1-yl diphosphate synthase (flavodoxin)
    - Dynein axonemal heavy chain 1
    - Splicing factor U2af large subunit A
    - Uncharacterized protein YuaQ
    - Aucune: les 6 résultats obtenus ne sont pas significatifs, car les e-values obtenues sont trop élevées (toutes > 1).
    - Aucune : ces 6 séquences cibles ne sont vraisemblablement pas homologues de l'ORF10.
    - Aucune: l'ORF10 est probablement un faux positif, une fausse prédiction d'ORFfinder. 


### Exercice 8 - Recherche d'information sur RegulonDB


- Connectez-vous à la base de connaissances [RegulonDB](https://regulondb.ccg.unam.mx/).
- Sur ce site, effectuez une recherche avec le nom de gène que vous avez trouvé précédemment pour l'ORF1. Pour cela, entrez simplement le nom de gène dans la barre de recherche.
- Cliquez sur l'unique résultat qui apparaît dans la section **Gene**. 
- Dézoomez et recadrez la carte avec les flèches.

#### Questionnaire TP3 – Exercice 8: Consultation de RegulonDB

- D'après cette carte, le gène étudié se trouve-t-il bien dans la structure supposée précédemment ? (oui / non)
- Dans les informations qui apparaissent sous la carte, trouvez le nom de l'opéron. Cliquez sur le nom de l'opéron, puis répondez aux questions suivantes.
- Sur quel brin ce trouve cet opéron ? (forward / reverse)
- Combien y-a-t'il de gènes dans cet opéron ? 0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12
- Combien y-a-t'il de promoteurs dans cet opéron ? 0, 1, 2, 3
- Quel est le type de terminateur de la transcription présent dans cette unité de transcription ?
- Quelle est la fonction de cet opéron ? 



Comparez votre prédiction d'ORFs avec ORFinder à la carte de l'opéron sur RegulonDB. 

- Avez-vous détecté l'ensemble des gènes de l'opéron avec ORFinder ? (oui / non)
- Quel est le gène manquant dans votre résultat d'ORFinder ? (une seule réponse) 

    - yeM
    - hisLp
    - hisL
    - wzzB
    - hisA
    
- Cliquez sur ce gène, puis trouvez sa taille. (Réponse numérique)

- Pourquoi ce gène n'est-il pas détecté lors de la recherche avec ORFinder ?  (une ou plusieurs réponses)

    - Ce gène n'est pas codant
    - La taille minimale d'ORFfinder était de 75bp
    - La taille minimale d'ORFfinder était de 300bp
    - Ce gène est situé sur le brin complémentaire

- D'après la carte de l'opéron, à quel gène correspondrait l'ORF 9 détecté avec ORFinder ? (une seule réponse)

    - yeeZ
    - hisI
    - wzzB
    - ugd
    
- Comment s'appelle le gène directement en amont de l'opéron ?  (une seule réponse)

    - wzzB
    - ugd
    - hisL
    - hisLp
    - yefM

- Pourquoi ce gène n'est-il pas détecté lors de la recherche avec ORFinder ?

    - Il n'est pas codant
    - Il est situé sur le brin complémentaire
    - Il est en amont de la séquence fournie en début d'exercice. 
    - La taille minimale d'ORFfinder était de 300bp


## Qu'avez-vous acquis au terme de ce TP ?

Au cours de ce TP, vous avez utilisé des outils de navigation génomique et d'analyse de séquences pour explorer les régions génomiques humaines (autour du gène humain PAX6) et bactériennes (opéron his chez *Escherichia coli*). 

Ceci vous a amenés à mettre en pratique une série de concepts biologiques en manipulant des séquences et annotations génomiques avec deux des navigateurs génomiques les plus utilisés en biologie : UCSC Genome Browser et NCBI (que vous aviez commencé à utiliser au TP2). 

L'exploration des annotations génomiques de PAX6 vous a permis d'acquérir les compétences suivantes

- maîtrise de l'affichage des pistes d'annotation : sélection de pistes, niveau de détail
- affichage progressif de pistes d'annotations apportant un éclairage complémentaire sur une région génomique : structure des gènes annotés, éléments répétitifs, conservation génomique, profils transcriptomiques
- interprétation de la carte génomique en intégrant ces différentes informations

L'analyse de la séquence génomique vous a placés dans la situation des biologistes qui disposent de nouvelles séquences génomiques bactériennes. Vous avez appris à manipuler une série d'outils en ligne qui permettent de réaliser facilement les premières étapes de cette démarche d'annotation :

- localisation des gènes codants en détectant les phases ouverts de lecture (par traduction de l'ADN génomique sur les 6 phases de lecture)
- recherche de similarités entre les séquences protéiques potentiellement produites par ces ORFs et la  base de connaissance Swiss-prot
- analyse de l'organisation des ORFs : positions, distances intergéniques
- prédiction d'un opéron sur base de l'orientation des gènes et du calcul des distances intergéniques

