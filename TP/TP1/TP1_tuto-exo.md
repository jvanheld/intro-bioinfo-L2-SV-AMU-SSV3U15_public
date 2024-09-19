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


## Protéomes de référence

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


- *Quel est le nombre total de protéines?* : 245.896.766
- *Quel est le nombre de protéines révisées par un annotateur?* Reviewed (Swiss-Prot) (571.864)
- *Comment s'appelle la base de connaissances des protéines révisées par des annotateurs?* : Swiss-Prot
- *Quel est le nombre de protéines non révisées?* : Unreviewed (TrEMBL) (245,324,902)
- *Comment s'appelle la base de données des protéines non révisées par des annotateurs?* : TrEMBL
- *Swiss-Prot est (a) une base de données; (b) une base de connaissances* : une base de connaissances
- *TrEMBL est (a) une base de données; (b) une base de connaissances* : une base de données




- *combien de résultats au total obtenez-vous?* : 6.201.771
- *combien de résultats obtenez-vous dans Swiss-Prot?* : 52.187
- *combien de résultats obtenez-vous dans TrEMBL?* : 6.149.584
- dans la section "Popular organisms" du panneau de gauche, combien de protéines sont associées à l'humain ? : 204.411
- quels sont les autres "organismes populaires" ? : Zebrafish, Mouse, Rat, Bovine
- pourquoi la recherche avec le mot "human" retourne-t-elle des protéines appartenant à d'autres organismes ?
        - parce qu'elle retourne toutes les protéines pour lesquelles les annotations contiennent le mot "Human", quel que soit l'endroit où c'est mentionné. Par exemple, si dans les annotations on indique que la protéine est homologue à une protéin humaine, cette protéine sera  sélectionnée par la recherche. 


### Requête avancée (structurée)

Nous avons vu ci-dessus qu'une requête naïve peut s'avérer trompeuse, car elle retourne toutes les entrées d'Uniprot qui contiennent les termes de la boîte de recherche, sans tenir compte de l'endroit où ces termes apparaissent dans les annotations. Nous recommandons donc fortement d'éviter cela, et de recourir systématiquement aux requêtes avancées. 

1. Revenez à la page d'accueil d'Uniprot en cliquant sur l'icône "Uniprot" en haut à gauche. 
2. Dans la boîte "Find your protein", cliquez le lien "Advanced"
3. Les boîtes bleues vous permettent de restreindre votre recherche à un ou plusieurs champs particulier. Cliquez sur la première boîte bleue, et sélectionnez "Organism [OS]", puis tapes "Homo sapiens" dans la boîte de recherche. Un menu déroulant apparaît avec les différentes possibilités pour Homo sapiens, choisissez la première option 

| Requête avancée | Nombre de résultats |
|:------------------------------------:|:------------------------------------|
| ![<img src="https://github.com/user-attachments/assets/15129ba3-c422-41cc-8754-5d25438b5ac8/" width="100">](https://github.com/user-attachments/assets/15129ba3-c422-41cc-8754-5d25438b5ac8) | ![image](https://github.com/user-attachments/assets/49043a3e-aeb2-4510-9940-500174764173) |



4. 
5. 


## Annotations fonctionnelles

### Tutoriel : exploration de la base de connaissances Swiss-Prot et de la base de données Uniprot/TREMBL


### Exercice : 



## Analyse de structure

