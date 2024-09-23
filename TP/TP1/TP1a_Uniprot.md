# TP 1a. Exploration de la base de connaissances Uniprot

Auteurs: Jacques van Helden

## Table des matières

- [Requête naïve](#requête-naïve)
- [Requête avancée](#requête-avancée)
- [Protéome de référence](#protéome-de-référence)
- [Annotations fonctionnelles](#annotations-fonctionnelles)
- [Exercices](#exercices)


[Retour au TP 1](README.md)



----------------------------------------------------------------


## Introduction

Ce TP vise à se familiariser avec l'interface de la base de données et de connaissances Uniprot. 

Durant le TP, vous apprendrez à :

- effectuer une requête avancée (structurée) pour sélectionner des protéines sur base d'un ou plusieurs critères combinés 
- sélectionner un protéome de référence
- explorer les annotations fonctionnelles basées sur la Gene Ontology

## Ressources

| Ressource | Description | URL |
|:---------------|:-------------------------------------------|:--------------------------------|
| Uniprot | principale base de données mondiale de séquences protéiques et d'informations fonctionnelles | [https://www.uniprot.org/](https://www.uniprot.org/) |


## Requête naïve

Dans un premier temps nous allons faire une requête "naïve" en entrant "Human" dans la boîte de recherche. 

1. Ouvrez une connexion à Uniprot ([uniprot.org](https://uniprot.org))

2. Cliquez **Search** en veillant à laisser la boîte de recherche vide. Ceci sélectionnera l'ensemble des entrées la base de données. 

Connectez-vous à Ametice et répondez à la première section questionnaire du TP1: **Requêtes naïves sur UniprotKB**. 

3. Dans la boîte de recherche, tapez "Human" et cliquez "Search"

Connectez-vous à Ametice et répondez à la deuxième section questionnaire du TP1: **Requêtes naïves sur UniprotKB**. 

4. Dans la section "Popular organisms", cliquez "Human". 

Connectez-vous à Ametice et répondez à la troisième section questionnaire du TP1: **Requêtes naïves sur UniprotKB**. 

## Requête avancée

Nous avons vu ci-dessus qu'une requête naïve peut s'avérer trompeuse, car elle retourne toutes les entrées d'Uniprot qui contiennent les termes de la boîte de recherche, sans tenir compte de l'endroit où ces termes apparaissent dans les annotations. On peut donc se retrouver avec des tas de protéines non-humaines, qui sont sélectionnées parce que le mot "Human" apparaît dans l'un ou l'autre champ (par exemple "similar to Human ...").

Nous recommandons donc fortement d'éviter cela, et de recourir systématiquement aux requêtes avancées. 

1. Revenez à la page d'accueil d'Uniprot en cliquant sur l'icône "Uniprot" en haut à gauche. 
2. Dans la boîte "Find your protein", cliquez le lien "Advanced"
3. Les boîtes bleues vous permettent de restreindre votre recherche à un ou plusieurs champs particulier. Cliquez sur la première boîte bleue, et sélectionnez "Organism [OS]", puis tapez "Homo sapiens" dans la boîte de recherche. Un menu déroulant apparaît avec les différentes possibilités pour Homo sapiens, choisissez la première option ("Homo sapiens (Human/Man) [9606]")


| Requête avancée | Nombre de résultats |
|:------------------------------------:|:------------------------------------|
| ![img>](images/requete-avancee-OS-Homo-sapiens.png) | ![image](images/requete-avancee-OS-Homo-sapiens_result.png) |

**Info:** 9606 est l'identifiant taxonomique de l'espèce *Homo sapiens* dans la base de données taxonomique de référence, qui est gérée par le NCBI. Vous pouvez consulter les informations associées en cherchant "Homo sapiens" sur [www.ncbi.nlm.nih.gov/Taxonomy/](https://www.ncbi.nlm.nih.gov/Taxonomy/)

Voici le lien direct: 
- [www.ncbi.nlm.nih.gov/Taxonomy/Browser/wwwtax.cgi?id=9606](https://www.ncbi.nlm.nih.gov/Taxonomy/Browser/wwwtax.cgi?id=9606)

On notera que ce taxon *inclut* deux variétés fossiles 
- [Homo sapiens neanderthalensis](https://www.ncbi.nlm.nih.gov/Taxonomy/Browser/wwwtax.cgi?id=63221)
- [Homo sapiens subsp. 'Denisova'](https://www.ncbi.nlm.nih.gov/Taxonomy/Browser/wwwtax.cgi?mode=Info&id=741158)



## Annotations fonctionnelles

Nous avons maintenant sélectionné le protéome de référence de l'espèce *Homo sapiens* dans Uniprot. 

Le panneau de gauche permet d'explorer de façon interactive différentes propriétés de ce protéome. 

1. Nous effectuerons cette exploration en nous limitant au sous-ensemble des protéines révisées. Pour cela, cliquez sur "Reviewed (Swiss-Prot)" dans le panneau de gauche.  Ceci restreindra les analyses suivantes aux 20.420 protéines les mieux documentées pour l'humain. 

2. Dans la section "Group by" du panneau de gauche, cliquez "Gene Ontology". Ceci vous affiche le nombre de protéines (parmi les 20.420) pour lesquelles on dispose d'annotation dans chacune des trois catégories de la Gene Ontology: 

    - 17.517 biological_process
    - 18.801 cellular_component
    - 16.049 molecular_function
    
3. Les triangles à gauche de chaque nombre permettent de déployer le niveau suivant de la classification hiérarchique des termes de l'ontologie. Cliquez sur le triangle à gauche de "biological process" pour afficher ses sous-catégories. 

![Nombre de protéines humaines dans Swiss-prot (révisées) par classe de l'ontologie "biological process"](images/GO_biological-processes-Homo-sapiens.png)

Notez que la somme des nombres des sous-catégories dépasse de loin la taille de la catégorie parente (biological process. Ceci est logique, car une même protéine peut appartenir à plusieurs classes simultanément. Par exemple, une protéine pourrait être impliquée dans la régulation biologique (12.123 protéines) positive (6.193 protéines) d'un processus de développement (5.698 protéines). Cette protéine sera donc comptée 3 fois à ce niveau de la classification. 


## Deuxième partie du TP: visualisation et analyse des structures tridimensionnelles de protéines

Nous avons fini la première partie du TP1, qui consistait à se familiariser avec les requêtes Uniprot pour sélectionner l'ensemble des protéines d'un organisme considéré. 

Nous avons prévu ci-dessous quelques exercices facultatifs pour les personnes qui désireraient pousser plus loin les analyses. 
Cependant, pendant la séance de TP nous vous suggérons d'attaquer d'emblée la deuxième partie, consacrée aux relations séquence ) structures - fonction. 

***Voici le lien vers cette deuxième partie du TP1: [TP PDB](TP1b_PDB.md)***


il vous sera loisible de terminer les exercices facultatifs ultérieurement. 


## Facultatif (à faire chez soi) : protéome de référence

Le protéome d'un organisme consiste en l'ensemble de ses protéines. Dans Uniprot, les séquences protéiques proviennent de la traduction automatique de séquences génomiques. Avec la multiplication des projets de séquençages individuels d'humains, le nombre de séquences différentes a augmenté, avec une certaine redondance. 

Pour faciliter le travail, l'équipe d'Uniprot a défini le concept de "Protéome de référence". 

Après avoir effectué une requête avancée en cherchant *Homo sapiens* dans le nom d'organisme, le titre de la page de résultat inclut un lien vers le protéome de référence de l'humain. 


> UniProtKB 204,411 results or expand search to "9606" to include lower taxonomic ranks or restrict to reference proteome [UP000005640](https://www.uniprot.org/?query=(organism_id:9606)%20AND%20(proteome:UP000005640))

En cliquant sur le lien  [UP000005640](https://www.uniprot.org/?query=(organism_id:9606)%20AND%20(proteome:UP000005640)), on obtient un protéome totalisant 82.861 protéines dont 20.420 révisée par des annotateurs (Swiss-prot) et 62.441 non-révisées (TrEMBL). 

Notez que la boîte de requête affiche maintenant le texte structuré suivant:

```(organism_id:9606) AND (proteome:UP000005640)```

Vous pouvez construire des requêtes plus complexes avec l'outil "Advanced", qui vous permettra de combiner plusieurs critères de sélection avec différents opérateurs logiques (AND, OR). 

Pour consulter la liste des protéomes de référence, en revenant à la page d'accueil d'Uniprot, et en sélectionnant, à gauche de la boîte de recherche, la section "Proteomes"

![Sélection de la section protéome d'Uniprot](images/proteome_query.png)

Ceci remplace la boîte "Find your protein" par "Find your proteome"

![Boîte de recherche de protéomes](images/proteome_query_2.png)

Vous pouvez ensuite effectuer une requête avancée pour sélectionner le protéome de référence (Proteome type) de l'organisme modèle de votre choix (par exemple "Escherichia coli (strain K12) (E.coli) [83333]")

![Recherche avancée dans les protéomes](images/proteome_query_4.png)

### Exercices

1. Formulez une requête avancée sur l'ensemble des protéines du protéome de référence humain en sélectionnant les enzymes annotées dans Swiss-Prot, qui ont une localisation cytoplasmique et sont impliquées dans la voie canonique de la glycolyse. Combien de protéines obtenez-vous ?

    - *Coup de pouce : utilisez les classes de la Gene Ontology [GO] dans la requête avancée*
        - `canonical glycolysis (GO:0061621) [0061621]`
        - `cytoplasm (GO:0005737) [0005737]`

2. Sélectionnez le protéome de référence de l'un des organismes modèles suivants, et analysez la répartition de ses gènes aux deux premiers niveaux des processus biologiques de la gene ontology. 

    - Escherichia coli (strain K12) (E. coli) [83333]
    - Drosophila melanogaster (Fruit fly/D. melanogaster) [7227]
    - Bacillus subtilis (strain 168) (B. subtilis) [224308]
    - Saccharomyces cerevisiae (strain ATCC 204508 / S288c) (Baker’s yeast/Baker's yeast/Brewer’s yeast/S. cerevisiae) [559292]
    - Mus musculus (Mouse/House mouse/Laboratory mouse) [10090]
    - Rattus norvegicus (Laboratory rat/Buffalo rat/R. norvegicus/Rat/Norway rat/Brown rat) [10116]
    - Arabidopsis thaliana (Mouse-ear cress/Arabidopsis/A. Thaliana/Thale cress) [3702]
    - Oryza sativa subsp. japonica (Japanese rice/O. sativa/Japonica rice/Rice) [39947]
    - Macaca mulatta (Rhesus monkey/M. mulatta/Rhesus macaque) [9544]
    - Mycoplasma genitalium (strain ATCC 33530 / DSM 19775 / NCTC 10195 / G37)


    Pour l'organisme de votre choix, quels sont les valeurs suivantes ?
    
    - Nombre de protéines dans Uniprot
    - Nombre de protéines révisées
    - Nombre de protéines non-révisées
    - Pourcentage de protéines révisées
    
3. Dans Uniprot, ouvrez la fiche de la sous-unité alpha de l'hémoglobine humaine (Hemoglobin subunit alpha)

...

4. Dans le protéome de la levure du boulanger (Saccharomyces cerevisiae (strain ATCC 204508 / S288c) (Baker’s yeast/Baker's yeast/Brewer’s yeast/S. cerevisiae) [559292]), comptez le nombre de protéines appartenant aux classes suivantes : 

    - facteur transcripitionel se liant à l'ADN
    - transporteur
    - protéine cytoplasmique
    - protéine transmembranaire
    - protéine impliquée dans la voie métabolique de la glycolyse

5. Dans le protéome de référence de l'humain, combien y a-t-il de récepteurs olfactifs?

    - 12
    - 120
    - 1200
    - 12000
    - 120000


----------------------------------------------------------------

[Retour au TP 1](README.md)

----------------------------------------------------------------
