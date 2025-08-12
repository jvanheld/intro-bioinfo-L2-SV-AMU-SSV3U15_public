# Glossaire des termes utilisés

Cours d'**Introduction à la bioinformatique** (SSV3U15)

[Retour à la page d'accueil du cours](../)


[]{#contenu}

## Table des matières

- [Séquence, structure, fonction](#sequence_structure_fonction)

  - [Base de données versus base de connaissance](#db_vs_kb)

- [Matrices de substitution](#matrices_substitutions)

- [Alignements par paires](#pairwise_align)

- [Alignement global versus local](#global_local)

- [BLAST: une famille d'outils pour la recherche de séquences par similarités](#blast)

   - [Modalités de BLAST](#blast_modes)

- [Phylogénie moléculaire](#phylogénie-moléculaire)

   - [Homologie](#homologie)
   - [Orthologie](#orthologie)
   - [Paralogie](#paralogie)
   - [Xénologie](#xénologie)
   - [Analogie](#analogie)
   - [Taxonomie (ou taxinomie)](#taxonomie-ou-taxinomie)
   - [Arbre vrai ou inféré](#arbre-vrai-ou-inféré)
   - [Arbre des espèces](#arbre-des-espèces)
   - [Arbre des molécules](#arbre-des-molécules)
   - [Unité taxonomique opérationnelle (operational taxonomic unit, OTU)](#unité-taxonomique-opérationnelle-operational-taxonomic-unit-otu)
   - [Unité taxonomique hypothétique (hypothetical taxonomic unit, HTU)](#unité-taxonomique-hypothétique-hypothetical-taxonomic-unit-htu)
   - [Spéciation](#spéciation)
   - [Duplication](#duplication)
   - [Phylogramme](#phylogramme)
   - [Groupe monophylétique / Clade](#groupe-monophylétique-clade)
   - [Groupe paraphylétique](#groupe-paraphylétique)
   - [Groupe polyphylétique](#groupe-polyphylétique)
   - [Cénancêtre](#cénancêtre)
   - [Groupe basal (ou lignée basale)](#groupe-basal-ou-lignée-basale)
   - [Groupes frères](#groupes-frères)
   - [Robustesse](#robustesse)
   - [Bootstrap](#bootstrap)
   - [Phylogénomique](#phylogénomique)

[]{#sequence_structure_fonction}

## Séquence, structure, fonction

[]{#db_vs_kb}

### Base de données versus base de connaissance

**Base de données** : ressource logicielle permettant de stocker et d’interroger des ensembles de données structurées, généralement homogènes par leur nature. Elle peut être alimentée automatiquement, sans intervention humaine directe. C’est le cas de TrEMBL, qui regroupe toutes les séquences protéiques obtenues par traduction de séquences nucléotidiques, avec des annotations générées automatiquement.

**Base de connaissances** :  base de données qui intègre, en plus des données brutes, des informations interprétées, organisées et validées par des experts du domaine. Ces annotations peuvent concerner la fonction biologique, la structure tridimensionnelle ou d’autres propriétés pertinentes. C’est le cas de Swiss-Prot, dont chaque entrée est enrichie par un travail manuel de curateurs spécialisés.

Toute base de connaissances est donc une base de données, mais la réciproque n’est pas vraie.


[]{#matrices_substitutions}

## Matrices de substitution

**[A REDIGER]**

[]{#pairwise_align} [Retour à la table des matières](#contenu)

## Alignements par paires

Un [alignement par paire]{.concept} indique les régions similaires entre
deux séquences biologiques (nucléiques ou peptidiques).

[]{#gaps}

### Les gaps

Afin d'aligner au mieux les résidus identiques ou similaires (scores
positifs dans les [matrices de substitutions](#matrices_substitutions)),
les programmes d'alignement peuvent insérer des espacements
([gaps]{.concept}) au sein des séquences alignées. Les gaps sont
représentés par des traits d'union \"-\".

          R  L  A  S  V  E  T  D  M  P   -  -  -  -  -  L  T  L  R  Q  H
          T  L  T  S  L  Q  T  T  L  K   N  L  K  E  M  A  H  L  G  T  H

Les gaps peuvent être interprétés selon deux scénarios évolutifs
alternatifs:

1.  perte des résidus par délétion dans la séquence présentant le gap;
2.  gain de résidus par insertion dans l'autre séquence.

L'alignement d'une paire de séquences ne permet pas de départager ces
deux possibilités. On définit le terme [indel]{.concept} (*in extenso*:
insertion ou délétion) pour indiquer cet événement évolutif de nature
indéterminé qui est à l'origine du gap.

[]{#score_alignement}

### Comment calculer le score brut d'un alignement ?

Pour calculer le score brut ([raw score]{.en}) d'un alignement, on
associe à chaque paire de résidus alignés le score correspondant dans la
[matrice de substitutions](#matrices_substitutions).

Dans l'exemple ci-dessous, nous avons calculé le score de l'alignement
suivant avec la matrice [BLOSUM62](images/BLOSUM62_colored.png){target="_blank"}.

          R  L  A  S  V  E  T  D  M  P   -  -  -  -  -  L  T  L  R  Q  H
          T  L  T  S  L  Q  T  T  L  K   N  L  K  E  M  A  H  L  G  T  H
         -1 +4 +0 +4 +1 +2 +5 -1 +2 -1                 -1 -2 +4 -2 -1 +8

On applique un traitement particulier pour assigner un score aux gaps: on définit (de façon quelque peu arbitraire) deux pénalités.

1.  Pour la première position de chaque gap, on applique la [pénalité d'ouverture de gap]{.concept} (ci-dessous: -10).
2.  Pour les résidus suivants du gap, on applique la [pénalité d'extension de gap]{.concept} (ci-dessous: -1).
3.  **Note:** on peut, de façon optionnelle, décider d'assigner ou non une pénalité aux gaps terminaux (en début et en fin d'alignement).

On peut dès lors calculer le [score brut]{.concept} ([raw score]{.concept}) en additionnant, tout au long de l'alignement, des scores d'identité, de substitution, d'ouverture et d'extension de
gap.

          R  L  A  S  V  E  T  D  M  P   -  -  -  -  -  L  T  L  R  Q  H
          T  L  T  S  L  Q  T  T  L  K   N  L  K  E  M  A  H  L  G  T  H
         -1 +4 +0 +4 +1 +2 +5 -1 +2 -1 -10 -1 -1 -1 -1 -1 -2 +4 -2 -1 +8 = 7

Enfin, pour faciliter la lecture de l'alignement, on insère entre les deux séquences alignées un ligne de symboles.

  ---- ---------------------------------------------------------------------------------------------------------------
  \|   identités  
  :    substitutions conservatives (celles qui ont un score positif dans la matrice de substitution)
  .    substitutions non-conservatives (celles qui ont un score strictement négatif dans la matrice de substitution)
  \-   gaps
  ---- ---------------------------------------------------------------------------------------------------------------

          R  L  A  S  V  E  T  D  M  P   -  -  -  -  -  L  T  L  R  Q  H
          .  |  .  |  :  :  |  .  :  .                  .  .  |  .  .  |
          T  L  T  S  L  Q  T  T  L  K   N  L  K  E  M  A  H  L  G  T  H
          -1 +4 +0 +4 +1 +2 +5 -1 +2 -1 -10 -1 -1 -1 -1 -1 -2 +4 -2 -1 +8 = 7 

[]{#scores_derives}

### Scores dérivés d'un alignement  par paires

Au-delà du score brut, on peut dériver une série de scores qui
fournissent des informations complémentaires concernant la qualité de
l'alignement.

+---------------------------+-------------------------------------------+
| Longueur de l'alignement  |  Nombre de colonnes de  l'alignement.     |
|                           | Attention, la longueur de l'alignement    |
|                           | diffère généralement de celle des         |
|                           | séquences alignées, pour différente       |
|                           | raisons:                                  |
|                           |                                           |
|                           | - Dans un **alignement global**, la       |
|                           |   présence de gaps alternés  dans les     |
|                           |   deux séquences peut générer un          |
|                           |   alignement plus long que chacune des    |
|                           |    séquences alignées.                    |
|                           |                                           |
|                           | - En cas d'**alignement local**,          |
|                           |             l'alignement peut se limiter  |
|                           |             à un fragment des protéines   |
|                           |             alignées, et peut donc être   |
|                           |             plus court que chacune des    |
|                           |             séquences alignées. Notons    |
|                           |             que ceci n'est pas forcé:     |
|                           |             selon les cas, un algorithme  |
|                           |             d'alignement local peut       |
|                           |             éventuellement arriver à un   |
|                           |             alignement qui recouvre les   |
|                           |             séquences alignées sur toute  |
|                           |             leur longeur, et, s'il y a    |
|                           |             des gaps, ce alignement sera  |
|                           |             plus long que les protéines   |
|                           |             alignées.                     |
+---------------------------+-------------------------------------------+
| Nombre d'identités        | Nombre de positions où sont               |
|                           |         alignés deux résidus identiques   |
+---------------------------+-------------------------------------------+
| Pourcentage d'identités   | Nombre d'identités divisé par la          |
|                           |         longueur totale de l'alignement.  |
+---------------------------+-------------------------------------------+
| Nombre de positifs        | Nombre de positions de                    |
|                           |         l'alignement caractérisées par    |
|                           |         un score positif dans la matrice  |
|                           |         de substitution (identités et     |
|                           |         substitutions \"conservatives\"). |
+---------------------------+-------------------------------------------+
| Pourcentage de positifs   | Nombre de positifs divisé par             |
|                           |         la longueur totale de             |
|                           |         l'alignement, fois $100$          |
+---------------------------+-------------------------------------------+

[Retour à la table des matières](#contenu)

------------------------------------------------------------------------

[]{#global_local}

## Alignement global versus local

Un [alignement global]{.concept} recouvre les séquences alignées sur
l'ensemble de leur longueur, tandis qu'un [alignement local]{.concept}
peut se limiter à un fragment de chaque séquence.

L'intérêt de l'alignement global est de révéler les événements
évolutifs (délétions, insertions, substitutions) sur l'ensemble de la
longueur des séquences d'intérêt. On recourt par exemple aux
alignements globaux quand on veut étudier l'évolution d'une famille de
protéines dans son ensemble.

Les alignements locaux révèlent les segments conservés entre deux ou
plusieurs séquences. On les utilise par exemple pour extraire un domaine
conservé à partir d'une famille de séquences homologues.

[Retour à la table des matières](#contenu)

------------------------------------------------------------------------

[]{#blast}

## BLAST: une famille d'outils pour la recherche de séquences par similarités

BLAST est une méthode de recherche de séquences par similarité qui
effectue des alignements locaux entre une [séquence requête]{.concept}
([query sequence]{.concept}) et chacune des séquences d'une base de
données (par exemple UniprotKB, qui recouvre 40 millions de séquences
protéiques).

Pour pouvoir effectuer cette tâche énorme dans un temps raisonnable,
BLAST se base sur une approche heuristique: les séquences de la base de
données sont préalablement indexées dans un \"dictionnaire de mots\",
qui dresse la liste des séquences de la base de données contenant chaque
oligomère (oligopeptide pour les bases de données de protéines,
oligonucléotides pour les séquences nucléiques) d'une taille donnée.

Quand on lance une recherche, BLAST commence par analyser la séquence
requête en dressant la liste des oligomères présents. Il consulte
ensuite le dictionnaire pour extraire la liste des séquences de la base
de données qui contiennent ces mots, et lance un alignement par paire
avec ce sous-ensemble des séquences.

Cette heuristique est plus rapide que les méthodes d'alignement par
paire par programmation dynamique (Needleman-Wunsch en alignement
global, Smith-Waterman en alignement local), mais elle présente un
certain risque de louper des similarités.

[]{#blast_modes}

#### Les modalités de BLAST

BLAST permet non seulement de comparer des séquences de même type
(protéine versus protéine, acide nucléique versus acide nucléique), mais
également d'effectuer des recherches avec une séquence requête d'un
type (peptidiques ou nucléiques) dans une base de donnée de l'autre
type. Pour ces recherches croisées, les séquences nucléiques sont
traduites dans les 6 cadres de lectures (3 cadres de lecture par brin),
et le résultat est analysé avec l'algorithme blastp.

  -----------------------------------------------------------------------------------------
  Requête           Base de données   Outil         Exemples d'applications
  ----------------- ----------------- ------------- ---------------------------------------
  séquence          séquence          **blastp**    En partant d'une
  peptidique        peptidique                              protéine de
                                                            fonction connue,
                                                            collecter les
                                                            protéines
                                                            similaires dans
                                                            la base de
                                                            données Uniprot
                                                            afin de
                                                            constituer la
                                                            famille de
                                                            protéine
                                                            supposées
                                                            homologues.

  séquence          séquence          **blastn**    Comparer les
  nucléique         nucléique                               séquences d'ARNm
                                                            aux séquences
                                                            génomiques.
                                                            
                                                            Aligner un ARN
                                                            d'interférence
                                                            (ARNi) sur un
                                                            génome pour
                                                            détecter ses
                                                            cibles
                                                            potentielles.

  séquence          séquence          **blastx**     Après avoir
  nucléique         peptidique                              séquencé un
  (traduite dans                                            morceau d'ADN,
  les 6 cadres)                                             chercher des
                                                            fragments
                                                            potentiellement
                                                            codants
                                                            (susceptibles de
                                                            produire un
                                                            polypeptide
                                                            similaire à des
                                                            protéines
                                                            connues) dans
                                                            cette séquence
                                                            même si on ne
                                                            connaît pas la
                                                            position des
                                                            gènes.

  séquence          séquence          **tblastn**    Identifier une
  peptidique        nucléique                               région génomique
                    (traduite dans                          susceptible de
                    les 6 cadres)                           coder pour un
                                                            homologue d'une
                                                            protéine
                                                            d'intérêt.
                                                            
                                                            Identifier dans
                                                            un génome les
                                                            pseudo-gènes
                                                            (gènes défectifs,
                                                            qui peuvent
                                                            contenir un ou
                                                            plusieurs codons
                                                            stop)
                                                            correspondant à
                                                            une protéine
                                                            d'intérêt.

  séquence          séquence          **tblastx**   A partir d'une séquence d'ADN,  
  nucléique         nucléique                       identifier des segments de régions 
  (traduite dans    (traduite dans                  codantes ayant une contrepartie dans 
  les 6 cadres)     les 6 cadres)                   un génome ou une base de données de 
                                                    référence
  -----------------------------------------------------------------------------------------

[Retour à la table des matières](#contenu)

----------------------------------------------------------------

## Phylogénie moléculaire 

### Homologie

Ressemblance de caractères phénotypiques ou génétiques qui s'explique par le fait que ces caractères résultent d'une origine ancestrale commune. Les différences entre les deux caractères homologues résultent de l’accumulation de mutations à partir de l’ancêtre commun. Il s’agit donc d’une évolution par *divergence évolutive*. 

### Orthologie

Relation entre deux séquences dont le dernier ancêtre commun précède immédiatement un événement de spéciation.

### Paralogie

Relation entre deux séquences dont le dernier ancêtre commun précède immédiatement un événement de duplication. 

### Xénologie

Relation entre deux caractères dont l’histoire, depuis leur dernier ancêtre commun, inclut un transfert entre espèces (horizontal) du matériel génétique pour au moins l’un de ces caractères.


### Analogie

Ressemblance entre deux traits (organes, séquence) qui ne résulte pas d'une origine ancestrale commune. Les traits similaires sont apparus de façon indépendante. Leur ressemblance peut éventuellement manifester l’effet d’une pression évolutive qui a sélectionné les mêmes propriétés. Dans ce cas, on parle de *convergence évolutive*.


### Taxonomie (ou taxinomie)

1. Science de la classification
2. Classification des éléments d’un domaine, en particulier les espèces biologiques


### Arbre vrai ou inféré 

Un arbre phylogénétique qui reflète exactement les relations de parenté entre groupes d'êtres vivants est qualifié d’arbre vrai. En réalité, l’arbre vrai n’est jamais connu. L’idée de l’inférence phylogénétique est de construire des arbres à partir des données à disposition (arbre inféré) qui s’approchent le plus possible de l’arbre vrai.

### Arbre des espèces

Arbre qui indique les relations de parenté entre des espèces d’êtres vivants – ou par extension d’autres niveaux taxonomiques.

### Arbre des molécules

Arbre phylogénétique inféré à partir des séquences biologiques, et qui reflète l’évolution vraisemblable des séquences.

### Unité taxonomique opérationnelle (operational taxonomic unit, OTU)

Unité taxonomique d'un arbre phylogénétique pour laquelle on dispose de données. Les OTU correspondent aux noeuds externes (feuilles) de l'arbre phylogénétique. Note : les OTU peuvent correspondre à des organismes existants ou éteints (dont les données proviennent d'études paléontologiques ou paléogénomiques). 

### Unité taxonomique hypothétique (hypothetical taxonomic unit, HTU)

Unité taxonomique inférée, pour laquelle on ne dispose pas de données. Les HTU constitue les noeuds internes des arbres phylogénétiques.

### Spéciation

Processus évolutif qui résulte en la formation d’espèces distinctes à partir d’une espèce unique. Suite à une spéciation, chaque molécule ancestrale se retrouve dans chacune des espèces dérivées.

### Duplication

Mutation qui génère un dédoublement d'une partie de l'ADN génomique. La duplication peut recouvrir l'ensemble du génome (formation d'organismes polyploïdes), un chromosome entier, ou un fragment de chromosome de taille plus ou moins grande. 

Les duplications peuvent éventuellement entraîner l’apparition de copies multiples d'un ou plusieurs gènes, provoquant ainsi une certaine redondance de l'information génétique.  Dans certains cas, l'une des copies dupliquées du gène acquiert, par accumulation de mutations, de nouvelles caractéristiques qui lui permettent d'assumer une nouvelle fonction. Ce mécanisme, appelé *duplication-divergence*, est en grande partie à l'origine de la diversification des fonctions biologiques. 


### Phylogramme

Arbre phylogénétique dont la longueur des branches représente les distances évolutives. Les branches ont donc des longueurs variables, et les feuilles ne sont pas forcément alignées)

### Chronogramme

Arbre phylogénétique dont la longueur des branches représente le temps de divergence entre unités taxonomiques mère et fille. Les branches ont donc des longueurs variables. Les feuilles sont alignées si les OTU sont des organismes actuels, mais elles peuvent éventuellement être décalées si les OTU incluent des espèces éteintes (données paléontologiques ou paléogénomiques). 

### Cladogramme

Arbre phylogénétique dont les branchements représentent les événements de divergence (spéciations, duplications) sans tenir compte de la distance évolutive (nombre de caractères morphologiques ou moléculaires distincts) ni du temps de divergence. 


### Groupe monophylétique / Clade 

Groupe comportant un organisme ancestral et tous les organismes en descendant, et uniquement eux. Exemple : les Hominidae incluent gibon, orang-outang, gorille, chimpanzé, bonobo (absent du dessins) et humain. 

### Groupe paraphylétique

Groupe qui inclut un organisme ancestral et ses descendant, mais en excluant certains d’entre eux. Exemples : les singes incluent les primates sauf l’humain: les poissons incluent les gnathostomes sauf les tétrapodes

### Groupe polyphylétique

Assemblage d’organismes n’incluant pas leur ancêtre commun le plus récent. Exemples : mammifères marins, animaux cavernicoles.

### Cénancêtre

Dernier ancêtre commun entre deux ou plusieurs groupes taxonomiques ; espèce la plus récente que ces taxons ont pour ancêtre commun. 


### Groupe basal (ou lignée basale)

Groupe taxonomique qui se détache des autres à proximité de la racine d’un arbre phylogénétique. Le concept de groupe basal est questionnable car il dépend du choix des échantillons ayant servi à établir l’arbre phylogénétique.

### Groupes frères

Groupes taxonomiques qui descendent immédiatement d'un ancêtre commun sur un arbre phylogénétique  (les branches sont directement rattachées au même nœud).

### Robustesse

Estimation de la mesure dont chaque nœud d’un arbre inféré est soutenu par le jeu de données.  La méthode la plus connue est le bootstrap.

### Bootstrap

Méthode d’estimation de la robustesse de chaque nœud d’un arbre. Cette méthode consiste à échantillonner les positions de l'alignement pour relancer la construction phylogénétique de façon itérative puis de comparer les arbres obtenus après de nombreuses répétitions. La valeur de bootstrap d’un nœud représente la proportion des arbres dans lequel le nœud a été retrouvé.

### Phylogénomique 

Reconstruction phylogénétique sur base de génomes ou de protéomes complets ou, à défaut, d'un grand nombre de séquences de gènes ou de protéines.

----------------------------------------------------------------

[]{#pairwise_align} [Retour à la table des matières](#contenu)
