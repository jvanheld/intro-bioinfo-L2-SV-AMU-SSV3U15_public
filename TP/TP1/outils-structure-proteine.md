# Création d'un fichier RMarkdown avec les informations fournies sous forme de tableau.
rmd_content = """
---
title: "Comparatif des outils Web pour l'analyse de la structure des protéines"
author: "TP Biologie, 2ème année Licence"
output: html_document
---

# Comparatif des outils Web pour l'analyse de la structure des protéines

Ce document compare différents outils Web pour l'analyse des structures de protéines, accessibles en ligne et adaptés à un usage pédagogique.

```{r}
library(knitr)
# Création du tableau comparatif
tools_comparison <- data.frame(
  Propriété = c("Accès sans login", 
                "Accès en ligne gratuit", 
                "Téléchargement de structures PDB via leur ID", 
                "Affichage du profil d'hydrophobicité", 
                "Alignement de structures", 
                "Sélection et marquage d'un résidu ou d'une région", 
                "Cartes de contact entre résidus", 
                "Lien avec les prédictions AlphaFold", 
                "Capacité de prédire une structure", 
                "Visualisation des liaisons hydrogène", 
                "Visualisation des interactions entre résidus", 
                "Personnalisation de l'apparence des structures", 
                "Capacité d'exporter des images ou animations", 
                "Capacité d'analyser des mutations et leurs effets structuraux", 
                "Accès aux annotations fonctionnelles", 
                "Calcul des distances entre atomes ou résidus"),
  
  Jmol_JSmol = c("Oui", "Oui", "Oui", "Non", "Oui", "Oui", "Oui (via scripts)", "Non", "Non", "Oui", "Oui", "Oui", "Oui", "Oui", "Oui", "Oui"),
  
  NGL_Viewer = c("Oui", "Oui", "Oui", "Non", "Oui", "Oui", "Non", "Non", "Non", "Oui", "Oui", "Oui", "Oui", "Oui", "Oui", "Oui"),
  
  iCn3D = c("Oui", "Oui", "Oui", "Oui", "Oui", "Oui", "Oui", "Oui", "Non", "Oui", "Oui", "Oui", "Oui", "Oui", "Oui", "Oui"),
  
  Mol_ = c("Oui", "Oui", "Oui", "Non", "Non", "Oui", "Non", "Oui (RCSB AlphaFold)", "Non", "Non", "Non", "Oui", "Non", "Non", "Oui", "Non"),
  
  PV = c("Oui", "Oui", "Oui", "Non", "Non", "Oui", "Non", "Non", "Non", "Non", "Non", "Non", "Non", "Non", "Non", "Non"),
  
  LiteMol = c("Oui", "Oui", "Oui", "Non", "Non", "Oui", "Non", "Non", "Non", "Oui", "Oui", "Oui", "Oui", "Non", "Oui", "Oui"),
  
  Swiss_Model = c("Non", "Oui", "Oui", "Non", "Oui", "Oui", "Non", "Oui", "Oui", "Oui", "Oui", "Oui", "Oui", "Oui", "Oui", "Oui")
)

# Affichage du tableau
kable(tools_comparison, format = "html", caption = "Comparatif des outils Web pour l'analyse des structures de protéines")
