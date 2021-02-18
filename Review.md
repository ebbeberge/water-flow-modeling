# Review for the MA8701 Data Analysis Project "Water Flow Modeling"

Authors: Group 7 (Eirik Berge, Camilla Idina Jensen Elvebakken, Martin Ludvigsen)

Reviewers: Group 5 (Helene Minge Olsen, Florian Beiser, Yaolin Ge)

## General Comments

The group provides an introduction to their data analysis repository in the README.md what is well appreciated by the reviewers. Therein and the Introduction, the authors highlight the relevance of their prediction models for safety as well as energy production and mention the current operational HBV modelling. This gives a clear motivation for their data-driven predition modelling in the subsequent report. 

(Sentences to Models)

(Sentences to Shrinkage)

### Introduction

The report provides a fundation for the understanding of the practical problem setting and the provided data. The preprocessing of the data base is cleary comprehensible. 

- In the figure for missing data the y-axis could be transformed to a scala with years. 
- Are the orange lines linear regression results?
- Calling the relation between `snødekningsgrad` and `snøvannekvivalent` "somewhat of linear" is more somewhat than linear.
- We cannot see any information in the `dato` versus `vannføring` plot and hence recommend to delete it - the later plots are much more illustrative and significant.
- Mention quantile value in boxplot description. 
- Honesty about the loss function is appreciated.


### Linear Models

Already in this section whose principal purpose is mainly to produce reference results, the authors already show impressively the potential of shrinkage methods. The section helps to understand the characteristics of the data set. As the rest of the work, this section has a high technical quality.

- If you compare in the text with HBV, please include the HBV in the summary for better comparison (with MSE at least). 
- It is a bit confusing confusing that you show that your `data$train` has 54 variables including `vannstand`, `dato` and `modellertvannføring` despite those are not considered, but this is personal preference. Please indicate this when printing `dim(train)`. 
- Do you have an idea why already linear regression is better than HBV? Is it the chosen loss function? If you have an educated guess, it would be nice to include. 
- The visualisation of the predicion is very illustrative. Please always use the same time range for those plots. 

- @5: what are BIC and Cp? What is forward and backward selection?




### Shrinkage



## Conclusion

The authors perform a statistically sound analysis of the given data and develop interpretable prediction models, where they deliberately respect the time-dependence of the variables. The methods are more than appropriate for the scope of the project and the results are clearly presented. The report is very well written. It stands out that the authors implement, interpret and compare five different approaches!

We suggest the following minor amendments:
- ...
- ...