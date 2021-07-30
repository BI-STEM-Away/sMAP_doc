---
title: Batch Correction
author: Tao He
date: 2021-07-03
category: Jekyll
layout: post
---

### Code Description: 
Before batch correction occurs there is a drop down menu in the UI to ask the user to select which metadata column provides the batch assignment for each of the samples. Then the user selects the button Perform Batch Correction and the process of batch correction takes place in the Server using the ComBat() function. Once the server code runs and batch correction is complete, the user will see a text output saying “Batch Correction is Complete”. 

### Significance of Output: 
Batch Correction is important and useful when using various numbers of batches. This is because it makes the two batches comparable to one another by correcting for differences in equipment and experimentation. As a result, after batch correction, the two batches can be used for the same analysis. 

### Advanced Functions: 
We used the ComBat() which allows users to adjust their data for batch correction. The imputed object is the normalized data and the returned value is an expression matrix that was corrected for batch effects. 
