---
title: Quality Control
author: Tao He
date: 2019-04-27
category: Jekyll
layout: post
---

## QC

### Code Description: 
In the beginning of the UI for the Quality Control page, the user has to choose the type of QC visualization desired before the normalization process. The two choices the user gets is NUSE and RLE. If the user chooses the NUSE method for quality control then in the server end, depending on the file that was imported, the quality control is completed using the NUSE() function. If the user chooses the RLE method, then in the server end the RLE() function is used for quality control using different methods depending on the file type. Once that is complete, the user can see the visualization of the data before the normalization and batch correction. The user also has the option to choose to visualize the data after the normalization with either a Boxplot or a PCA plot. On the server side, if the user chose Boxplot then the boxplot () is used to generate the plot with the x axis representing the sample number and the y axis representing the gene expression values. However if the user chose to visualize the data using a PCA plot the prcomp() is used to calculate the pca values. Then the user will choose the components for plotting the pca and the feature the pca plot will represent. The user will receive input from the server side if the user enters more or less than 2 components and if the user did not specify a feature. Then on the server side, the ggplot() is used to plot the PCA plot. 

### Significance of Output: 
Quality control is important because it helps check if the data is reliable. The QC visualizations before and after normalization helps see the quality control reports, but it also shows how normalization can change the data. 

### Advanced Functions: 
The ggplot() is very useful when not only plotting the PCA plot but also for various other types of plots and visualizations. Importation functions for QC were RLE() and NUSE(). The rle and nuse functions can produce a boxplot for arrays from a dataframe. 
