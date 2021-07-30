---
title: Functional Analysis
author: Tao He
date: 2021-07-07
category: Jekyll
layout: post
---

## Code Description: 
In the Functional Analysis page, there were three major factors: gene set enrichment analysis, KEGG analysis, and gene ontology. The first step is to generate a DEG vector with a given threshold value. Additionally the gene symbols in the data had to be converted to ENTREZIDs using the select(). (ENTREZIDs are an alternative way to identify genes with databases.) Once the DEG vector is made, the GSEA() is used for the gene set enrichment analysis. Then to visualize the output of the GSEA() the gseaplot2() function is used. The next part of the functional analysis is the enriched KEGG analysis. To get the KEGG pathways, the function used was the enrichKEGG(), and for the visualization the dotplot() was optimized. Additionally the barplot() was used to create a barplot visualization for the KEGG analysis. The number of categories that were shown for the KEGG analysis was determined by the user. Then the setReadable() was used so that the gene concept network for the significant KEGG pathways could be presented as well. Additionally, the user can choose which barplot it wants to visualize for the gene ontology. There are three different aspects the viewer can view: Biological Processes, Cellular Components, and Molecular Functions. Depending on which aspect the user decides to view the gene ontology, the enrichGO() was used. The results were boxplots with the colors representing the p-value. 

## Significance of Output: 
The significance of the different plots that were plotted have an immense importance as they represent the top DEGs from the data and with the ENTREZIDs there is additional information to more biological concepts. 

## Important Functions: 
A crucial function in the functional analysis was the select() so that the data could be converted to the Entrenzids. The select function allowed the users data to identify genes from a NIH database. 
