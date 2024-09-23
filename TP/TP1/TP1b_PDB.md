## Analyse de la structure tridimensionnelle des protéines

Auteurs: Jacques van Helden

## Table des matières

- [Introduction](#introduction)
- [Ressources](#ressources)
- [Exploration de PDB](#exploration-de-pdb)
- [Transporteur de glucose](#transporteur-de-glucose)


[Retour au TP 1](README.md)

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

Nous commençons ce TP par explorer sommairement l'interface usager de Protein Data Bank, la base de données de référence pour les structures tridimensionnelles des protéines. 

1. Ouvrez une connexion à PDB ([www.rcsb.org](https://www.rcsb.org))
2. Notez le nombre de protéines présentes dans PDB

3. En cliquant sur le nombre de structures (expérimentales) affiché en haut de la page d'accueil, vous pourrez observer la répartition de ces structures. Observez le nombre de structures expérimentales caractérisées par organisme, groupe taxonomique, méthode expérimentale, ...

3. Sous la boîte de recherche, cliquez sur "[Browse Annotations](https://www.rcsb.org/search/browse)" pour parcourir la base de données en fonction des propriétés des structures. 

    - Combien de structures (expérimentales) contient PDB ?
    - Quel est l'organisme le plus représenté pour les structures expérimentales ?
    - Quelle est la méthode la plus utilisée pour caractériser les structures expérimentales ?
    - PDB contient d'autres types de macromolécules que les protéines. Lesquels ? 
    - Combien PDB contient-elle de modèles de structures rpédites (computed structure models)) ?
    - Quel est la méthode la plus utilisée pour les structures prédites ?
    - Quel est l'organisme le plus représenté pour les structures prédites ?



----------------------------------------------------------------

## Transporteur de glucose


### Annotations du transporteur de glucose dans Uniprot

1. Dans [Uniprot](https://www.uniprot.org/), ouvrez la fiche de la protéine dénommée "Solute carrier family 2, facilitated glucose transporter member 1" (identifiant [GTR1_HUMAN](https://www.uniprot.org/uniprotkb/P11166))

2. Consultez la section "[Subcellular location](https://www.uniprot.org/uniprotkb/P11166/entry#subcellular_location)". 

    - quelle est la localisation sous-cellulaire principale de cette protéine ?
    - combien y a-t-il de domaines transmembranaires annotés dans la section "Features" ?
    - quel est le type de reploiement de ces domaines transmembranaires ?
    - combien y a-t-il d'autres domaines topologiques annotés dans la sous-section "Features" de "Subcellular location" ?
    - combien y a-t-il de domaines cytoplasmiques ?
    - combien y a-t-il de domaines intracellulaires ?

3. Consultez la section "[Diseases and variants](https://www.uniprot.org/uniprotkb/P11166/entry#disease_variants)"

    - quels sont les types de pathologies associés aux mutations de cette protéine ?

### Profils transcriptomiques tissulaires (sur GTEx)

4. Dans un onglet séparé, connectez-vous au portail GTEx ([gtexportal.org/](https://gtexportal.org/)) et consultez le profil transcriptomique du gène qui code pour cette protéine (vous trouverez son nom dans la section "[Names and taxonomy](https://www.uniprot.org/uniprotkb/P11166/entry#names_and_taxonomy)" de la fiche Uniprot)

    - dans quels tissus ce gène est-il principalement exprimé ?
    - voyez-vous un lien avec les pathologies suscitées par des mutations de ce gène ?

### Structure du transporteur de glucose sur PDB

5. Revenez à la page de cette protéine dans Uniprot et consultez la section "[Structure](https://www.uniprot.org/uniprotkb/P11166/entry#structure)". 

    - Combien y a-t-il de structures disponibles ? 
    - Combien y a-t-il de structures caractérisées expérimentalement ? 
    - Par quelle(s) méthode(s) expérimentale(s) ont-elles été caractérisées ?
    - Quelle est la meilleure résolution (en Angstroms) ?
    

6. Cliquez sur le lien "[RCSC-PDB](https://www.rcsb.org/structure/6THA)" de la structure 6THA et consultez rapidement les annotations pour identifier les types d'informations disponibles. Vous constaterez que les annotations de PDB sont à première vue moins détaillées que celles d'Uniprot (ce qui est normal, puisque PDB se concentre sur la structure protéique). 

7. Dans la section "Explore 3D" sous l'image de la structure, cliquez "[Sequence annotations](https://www.rcsb.org/3d-sequence/6THA?assemblyId=1)". Ceci ouvre un onglet qui vous permet de positionner les segments annotés de la protéine (panneau de gauche) avec la structure tridimensionnelle (panneau de droite). Cliquez successivement sur les segments de la piste d'annotation "Membrane topology" et identifiez les éléments structurels (hélices alpha, feuillets beta) correspondants. 

    - Quel est le type d'élément structurel associé aux segments transmembranaires ?
    - Quel est le type d'élément structurel associé plus grand segment intracellulaire ?
    - Quel est le type d'élément structurel associé plus grand segment extracellulaire ?

### Analyse de la structure avec icn3D
    
Dans un onglet séparé, connectez-vous au serveur [icn3D](https://www.ncbi.nlm.nih.gov/Structure/icn3d/), et entrez l'identifiant de la structure PDB (6THA) dans la boîte de requête, et pressez la touche "Entrée". Vérifiez que vous avez bien chargé la bonne structure : "PDB ID 6THA: Crystal structure of human sugar transporter GLUT1 (SLC2A1) in the inward conformation".

1. Choisissez une coloration en arc-en-ciel pour repérer la position des différents éléments de structure par rapport aux extrémités de la chaîne polypeptidique (*Color -> Rainbow -> For selection*). 


2. Testez les différents modes d'affichage de la protéine en explorant les options du menu *Styles -> Proteins* et tentez d'identifier l'intérêt des différents modes de représentation. En particulier, assurez-vous de comprendre les options d'affichage suivantes : 

    - C Alpha trace
    - Balls and stick
    - Sphere
    - Backbone
    - Ribbon

(la réponse à cette question peut faire l'objet d'un debriefing en séance)

3. Revenz à la représentation Ribbon, que nous utiliserons principalement pour la suite. 

4. Faites tourner la structure et localisez les molécules qui ne font pas partie de la protéine. Sélectionnez ces molécules (*Select -> Defined sets*, puis cliquez *chemicals* dans la boîte qui apparaît à droite de la fenêtre). Affichez-les en style "Balls and stick" (*Style -> Chemicals -> Balls and sticks*), et colorez-les en fonction des atomes (*Color -> Atom*). Désélectionnez ensuite ces molécules (*Select -> Clear Selection*). 

5. Sélectionnez la protéine (*Select -> Defined sets* puis *protein*) et colorez-la en fonction de la charge des résidus (*Color -> Charge*). Défaites la sélection pour mieux voir le résultat. 

    - estimez le nombre de résidues chargés positivement
    - estimez le nombre de résidues chargés négativement
    - estimez la proportion de ces résidus par rapport à la taille de la protéine

6. Analysez la localisation de ces résidus chargés, et interprétez le résultat dans le contexte des annotations d'Uniprot. 

    - quelle est la localisation majoritaire pour les résidus chargés ?
    - il y a-t-il des résidus chargés localisés dans les parties transmembranaires ?
    - si oui, sont-ils localisés du côté extérieur (membrane) ou intérieur (canal) du transporteur ?

 
    


----------------------------------------------------------------

[Retour au TP 1](README.md)

----------------------------------------------------------------
