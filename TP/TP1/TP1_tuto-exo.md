# TP 1 : Séquence - structure - fonction

## Table des matières

- [Auteurs](#auteurs)
- [Introduction](#introduction)
- [Ressources informatiques](#ressources-informatiques) 
- [Annotations fonctionnelles](#annotations-fonctionnelles) 
- [Analyse de structure](#analyse-de-structure)


## Auteurs

- Jacques van Helden

## Introduction

### But du TP

Durant cette séance de TP, nous analyserons le lien entre séquence, structure tridimensionnelle et fonction des protéines. 

### Exemples traités


### Notions abordées

Ce TP mobilisera les notions suivantes abordées au cours

- Annotation des séquences protéiques
- Eléments structurels (hélice alpha, chapine bêta)

### Compétences acquises au cours de ce TP

- Effectuer une recherche structurée dans une base de connaissances (Swissprot) ou de données (Uniprot)
- Interpréter les annotations fonctionnelles d'une protéine
- Etablir le lien entre annotations fonctionnelles et éléments structurels
- Utiliser des modes de visualisation appropriés pour mettre en évidence différentes propriétés des protéines

## Ressources informatiques

| Ressource | Description | URL |
|:---------------|:-------------------------------------------|:--------------------------------|
| Uniprot | principale base de données mondiale de séquences protéiques et d'informations fonctionnelles | https://www.uniprot.org/ |
| PDB | Protein Databank, base de données de sructures protéiques | https://www.rcsb.org/ |


## Annotations fonctionnelles des protéines dans Uniprot

### Requête naïve

Dans un premier temps nous allons faire une requête "naïve" en entrant "Human" dans la boîte de recherche. 

1. Ouvrez une connexion à Uniprot ([uniprot.org](https://uniprot.org))
2. Cliquez **Search** en veillant à laisser la boîte de recherche vide. Ceci sélectionnera l'ensemble des entrées la base de données. 

    - *Quel est le nombre total de protéines?*
    - *Quel est le nombre de protéines révisées par un annotateur?*
    - *Comment s'appelle la base de connaissances des protéines révisées par des annotateurs?*
    - *Quel est le nombre de protéines non révisées?*
    - *Comment s'appelle la base de données des protéines non révisées par des annotateurs?*
    - *Swiss-Prot est (a) une base de données; (b) une base de connaissances*
    - *TrEMBL est (a) une base de données; (b) une base de connaissances*

3. Dans la boîte de recherche, tapez "Human" et cliquez "Search"

    - *combien de résultats au total obtenez-vous?*
    - *combien de résultats obtenez-vous dans Swiss-Prot?*
    - *combien de résultats obtenez-vous dans TrEMBL?*
    - dans la section "Popular organisms" du panneau de gauche, combien de protéines sont associées à l'humain ?
    - quels sont les autres "organismes populaires" ?
    - pourquoi la recherche avec le mot "human" retourne-t-elle des protéines appartenant à d'autres organismes ?

4. Dans la section "Popular organisms", cliquez "Human". 

    - *combien de résultats obtenez-vous dans Swiss-Prot?*
    - *combien de résultats obtenez-vous dans TrEMBL?*


#### Réponses

Résultats de la requête le 19 septembre 2024. 


| Toutes les protéines d'Uniprot  | Requête non structurée "Human" | Après avoir cliqué sur "Homo sapiens" sous "Popular organisms" |
|:-------------------------------:|:-------------------------------:|:-------------------------------:|
| ![image](https://github.com/user-attachments/assets/a98671f1-b7cc-4242-8941-34cb4f144cfa) | ![image](https://github.com/user-attachments/assets/713ab344-feaa-4d9f-a95a-224f87b02ef0) | ![image](https://github.com/user-attachments/assets/31aa616c-ed01-46af-969a-23f3ea0fc534) |


#### Toutes les protéines d'Uniprot

- *Quel est le nombre total de protéines?* : 245.896.766
- *Quel est le nombre de protéines révisées par un annotateur?* Reviewed (Swiss-Prot) (571.864)
- *Comment s'appelle la base de connaissances des protéines révisées par des annotateurs?* : Swiss-Prot
- *Quel est le nombre de protéines non révisées?* : Unreviewed (TrEMBL) (245,324,902)
- *Comment s'appelle la base de données des protéines non révisées par des annotateurs?* : TrEMBL
- *Swiss-Prot est (a) une base de données; (b) une base de connaissances* : une base de connaissances
- *TrEMBL est (a) une base de données; (b) une base de connaissances* : une base de données


#### Requête non structurée "Human"

- *combien de résultats au total obtenez-vous?* : 6.201.771
- *combien de résultats obtenez-vous dans Swiss-Prot?* : 52.187
- *combien de résultats obtenez-vous dans TrEMBL?* : 6.149.584
- dans la section "Popular organisms" du panneau de gauche, combien de protéines sont associées à l'humain ? : 204.411
- quels sont les autres "organismes populaires" ? : Zebrafish, Mouse, Rat, Bovine
- pourquoi la recherche avec le mot "human" retourne-t-elle des protéines appartenant à d'autres organismes ?
        - parce qu'elle retourne toutes les protéines pour lesquelles les annotations contiennent le mot "Human", quel que soit l'endroit où c'est mentionné. Par exemple, si dans les annotations on indique que la protéine est homologue à une protéin humaine, cette protéine sera  sélectionnée par la recherche. 

#### Après avoir cliqué sur "Homo sapiens" sous "Popular organisms"

(voir capture d'écran ci-dessus)

## Requête avancée (structurée)

Nous avons vu ci-dessus qu'une requête naïve peut s'avérer trompeuse, car elle retourne toutes les entrées d'Uniprot qui contiennent les termes de la boîte de recherche, sans tenir compte de l'endroit où ces termes apparaissent dans les annotations. Nous recommandons donc fortement d'éviter cela, et de recourir systématiquement aux requêtes avancées. 

1. Revenez à la page d'accueil d'Uniprot en cliquant sur l'icône "Uniprot" en haut à gauche. 
2. Dans la boîte "Find your protein", cliquez le lien "Advanced"
3. Les boîtes bleues vous permettent de restreindre votre recherche à un ou plusieurs champs particulier. Cliquez sur la première boîte bleue, et sélectionnez "Organism [OS]", puis tapez "Homo sapiens" dans la boîte de recherche. Un menu déroulant apparaît avec les différentes possibilités pour Homo sapiens, choisissez la première option ("Homo sapiens (Human/Man) [9606]")


| Requête avancée | Nombre de résultats |
|:------------------------------------:|:------------------------------------|
| ![img>](https://github.com/user-attachments/assets/15129ba3-c422-41cc-8754-5d25438b5ac8) | ![image](https://github.com/user-attachments/assets/49043a3e-aeb2-4510-9940-500174764173) |

**Info:** 9606 es l'identifiant taaxonomique de l'espèce *Homo sapiens* dans la base de données taxonomique de référence, qui est gérée par le NCBI. Vous pouvez consulter les informations associées en cherchant "Homo sapiens" sur [www.ncbi.nlm.nih.gov/Taxonomy/](https://www.ncbi.nlm.nih.gov/Taxonomy/)

Voici le lien direct: 
- [www.ncbi.nlm.nih.gov/Taxonomy/Browser/wwwtax.cgi?id=9606](https://www.ncbi.nlm.nih.gov/Taxonomy/Browser/wwwtax.cgi?id=9606)

On notera que ce taxon *inclut* deux variétés fossiles 
- [Homo sapiens neanderthalensis](https://www.ncbi.nlm.nih.gov/Taxonomy/Browser/wwwtax.cgi?id=63221)
- [Homo sapiens subsp. 'Denisova'](https://www.ncbi.nlm.nih.gov/Taxonomy/Browser/wwwtax.cgi?mode=Info&id=741158)

## Protéome de référence

Le protéome d'un organisme consiste en l'ensemble de ses protéines. Dans Uniprot, les séquences protéiques proviennent de la traduction automatique de séquences génomiques. Avec la multiplication des projets de séquençages individuels d'humains, le nombre de séquences différentes a augmenté, avec une certaine redondance. 

Pour faciliter le travail, l'équipe d'Uniprot a défini le concept de "Protéome de référence". 

Après avoir effectué une requête avancée en cherchant Homo sapiens dans le nom d'organisme, le titre de la page de résultat inclut un lien vers le protéome de référence de l'humain. 


> UniProtKB 204,411 results or expand search to "9606" to include lower taxonomic ranks or restrict to reference proteome [UP000005640](https://www.uniprot.org/?query=(organism_id:9606)%20AND%20(proteome:UP000005640))

En cliquant sur le lien  [UP000005640](https://www.uniprot.org/?query=(organism_id:9606)%20AND%20(proteome:UP000005640)), on obtient un protéome totalisant 82.861 protéines dont 20.420 révisée par des annotateurs (Swiss-prot) et 62.441 non-révisées (TrEMBL). 

Notez que la boîte de requête affiche maintenant le texte structuré suivant:

```(organism_id:9606) AND (proteome:UP000005640)```

Vous pouvez construire des requêtes plus complexes avec l'outil "Advanced", qui vous permettra de combiner plusieurs critères de sélection avec différents opérateurs logiques (AND, OR). 


## Annotations fonctionnelles




### Exercice



## Analyse de structure

