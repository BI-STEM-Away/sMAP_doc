---
title: 
author: Tao He
date: 2021-07-08
category: Jekyll
layout: post
---

## PCA
In the QC visualization, the user could choose to visualize the boxplot or the PCA plot. The PCA plot was constructed using the prcomp() and the ggplot(). The prcomp() was crucial for calculating the pca for all the genes. Then to visualize the PCA data, Group B1 used the ggplot(). In our app, in the UI, the user can choose the two features that the user wanted to analyze more. 

## Volcano Plot
The Volcano Plot is utilized in the Statistical Analysis for visualizing the top DEGs. The User specifies the LogFC and adjusted P-Values for the Volcano plot. The function used for generating the Volcano Plot is EnhancedVolcano which takes in the user input and the final result for the top table. The Volcano Plot allows the user to visualize how various processes have changed their data. 

## Boxplot
The Box plot was used to visualize the quality control in the aspect of normalization. The user can choose if they want to visualize the normalized data in a BoxPlot or PCA. If the user chooses BoxPlot then the boxplot() is used to generate the plot with the x axis representing the sample number and the y axis representing the gene expression values. The boxplot visualizes how the data changed from being normalized.
