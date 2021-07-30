---
title: Statistical Analysis
author: Tao He
date: 2021-07-06
category: Jekyll
layout: post
---

## Code Description: 
Under the Statistical Analysis tab the user is asked what percent of genes they want to be filtered. On the server side, the genes get filtered based on the percent that the user had entered, the genes below the indicated percentile being removed from the data. However the annotated data is getting filtered. Prior to the genes being filtered, the data went through annotation in which the duplicates, NA, and duplicate gene symbols were removed. After the user sees that the genes were filtered, the user will determine how the samples will be grouped for limma analysis. The user can choose to group the samples using the metadata feature. Then the user is asked to select which features they want to compare specifically. The code then generates a data frame with the differentially expressed genes using the topTable() function. On the server side the first step was to determine the type of data that was being used, the filtered data or the non filtered data. Then in the metadata, a new column is created for the manual group. If the grouping was based on metadata then the new column is not needed. Once that is complete, it is important to make sure that the expression data only includes the data that the user had selected. Then it is time to create the top table by first creating a design matrix, and then going through limma analysis. Using model.matrix() a matrix was made, which will then be used for the limma analysis. For the limma analysis, lmfit() and eBays() were used. Limma analysis is really important because it helps with the analysis of gene expression data. From the limma analysis, the top table could be created for the DEG with the user inputting the cutoff p-value and the percent of DEGs to display with the topTable(). After the top table is generated, a volcano plot is used to visualize the DEGs. The user gets to distinguish the LogFC and the adjusted p-value cutoff for the volcano plot. 

## Significance of Output: 
The final input is the volcano plot which represents a lot of important components. One of the important parts was the top DEGs which are filtered, annotated, and had undergone the limma analysis. The DEG analysis also represents how the data has changed through the processes of limma analysis and filtering. 

## Important Functions: 
The dataTableProxy() is used so that it can manipulate the existing data table created to select or add rows/columns. This was an important function because it allowed the server code to be flexible depending on what the user inputs. The lmfit() was also crucial for the limma analysis which allowed the data to fit a linear model for the genes and allowed the analysis of the data. The toptable() was also important because it calculated the DEGs and put it into a table. The EnhancedVolcano() is also crucial for creating the volcano plot that is used to visualize the top table with the DEGs. 
