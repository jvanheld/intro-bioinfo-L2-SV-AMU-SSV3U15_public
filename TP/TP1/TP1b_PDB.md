## Analyse de la structure tridimensionnelle des protéines

Auteurs: Jacques van Helden

## Table des matières

- [Introduction](#introduction)
- [Ressources](#ressources)
- [Exploration de PDB](#exploration-de-pdb)
- [Transporteur de glucose](#transporteur-de-glucose)


[Retour au TP 1](TP1_tuto-exo.md)

----------------------------------------------------------------

## Introduction

Nous allons combiner les informations de Swiss-prot et de la Protein Data Bank (PDB) pour étudier quelques cas illustratifs de relations entre la séquence, la structure et fonction des protéines. 



----------------------------------------------------------------


## Ressources

| Ressource | Description | URL |
|:---------------|:-------------------------------------------|:--------------------------------|
| Uniprot | principale base de données mondiale de séquences protéiques et d'informations fonctionnelles | [https://www.uniprot.org/](https://www.uniprot.org/) |
| PDB | Protein Databank, base de données de sructures protéiques | [https://www.rcsb.org/](https://www.rcsb.org/) |
| icn3D | Outil de visualisation et d'analyse des structures protéiques (NCBI) | [https://www.ncbi.nlm.nih.gov/Structure/icn3d/](https://www.ncbi.nlm.nih.gov/Structure/icn3d/) |


----------------------------------------------------------------


## Exploration de PDB

Nous commençons ce TP par explirerexpl orer sommairement l'interface usager de Protein Data Bank, la base de données de référence pour les structures tridimensionnelle des protéines. 

1. Ouvrez une connexion à PDB ([www.rcsb.org](https://www.rcsb.org))
2. Notez le nombre de protéines présentes dans PDB
3. Sous la boîte de recherche, cliquez "[Browse"Annotations](https://www.rcsb.org/search/browse)". 
4. 


### Questions

- Combien de structures (expérimentales) contient PDB ?
- Combien PDB contient-elle de modèles de structures "calculés" (structures rpédites) ?


### Réponses

PDB contient actuellement (22 septembre 2024) 
- 225.158 structures expérimentales
- 1.068.577 Modèles de structure calculés


----------------------------------------------------------------

## Transporteur de glucose

1. Dans [Uniprot](https://www.uniprot.org/), ouvrez la fiche de la protéine dénommée "Solute carrier family 2, facilitated glucose transporter member 1" (identifiant [GTR1_HUMAN](https://www.uniprot.org/uniprotkb/P11166))

2. Consultez la section "[Subcellular location](https://www.uniprot.org/uniprotkb/P11166/entry#subcellular_location)". 

    - quelle est la localisation sous-cellulaire principale de cette protéine ?
    - combien y a--til de domaines transmembranaires annotés dans la section "Features" ?
    - quel est le type de reploiement de ces domaines transmembranaires ?
    - combien y a--t-il d'autres domaines topologiques annotés dans la sous-section "Features" de "Subcellular location" ?
    - combien y a--t-il de domaines cytoplasmiques ?
    - combien y a--t-il de domaines intracellulaires ?

3. Consultez la section "[Diseases and variants](https://www.uniprot.org/uniprotkb/P11166/entry#disease_variants)"

    - quels sont les types de pathologies associés aux mutations de cette protéine ?

4. Dans un onglet séparé, connectez-vous au portail GTEx ([gtexportal.org/](https://gtexportal.org/)) et consultez le profil transcriptomique du gène qui code pour cette protéine (vous trouverez son nom dans la section "[Names and taxonomy](https://www.uniprot.org/uniprotkb/P11166/entry#names_and_taxonomy)" de la fiche Uniprot)

    - dans quels tissus ce gène est-il principalement exprimé ?
    - voyez-vous un lien avec les pathologies suscitées par des mutations de ce gène ?

5. Revenez à la page de cette protéine dans Uniprot et consultez la section "[Structure](https://www.uniprot.org/uniprotkb/P11166/entry#structure)". 

    - Combien y a-t-il de structures disponibles ? 
    - Combien y a-t-il de structures caractérisées expérimentalement ? 
    - Par quelles méthodes expérimentales ont-elles été caractérisées ?
    - Quelle est la meilleure résolution (en Angstroms) ?
    

6. CLiquez sur le lien "[RCSC-PDB](https://www.rcsb.org/structure/6THA)" de la structure 6HTA et consultez rapidement les annotations pour identifier les types d'informations disponibles. Vous constaterez que les annotations de PDB sont à première vue moins détaillées que celles d'Uniprot (ce qui est normal, puisque PDB se concentre sur la structure protéique). 

7. Dans la section "Explore 3D" sous l'image de la structure, cliquez "[Sequence annotations](https://www.rcsb.org/3d-sequence/6THA?assemblyId=1)". Ceci ouvre un onglet qui vous permet de positionner les segments annotés de la protéine (panneau de gauche) avec la structure tridimensionnelle (panneau de droite). Cliquez successive=ment sur les segments de la piste d'annotation "Membrane topology" et identifiez les éléments structurels (hélices alpha, feuillets beta) correspondants. 

    - Quel est le type d'élément structurel associé aux segments transmembranaires ?
    - Quel est le type d'élément structurel associé plus grand segment intracellulaire ?
    - Quel est le type d'élément structurel associé plus grand segment extracellulaire ?


    

    - 


    

----------------------------------------------------------------

## Exercices

----------------------------------------------------------------

[Retour au TP 1](TP1_tuto-exo.md)

----------------------------------------------------------------
