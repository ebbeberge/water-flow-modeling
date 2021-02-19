# Review for the MA8701 Data Analysis Project "Water Flow Modeling"

Authors: Group 7 (Eirik Berge, Camilla Idina Jensen Elvebakken, Martin Ludvigsen)

Reviewers: Group 5 (Helene Minge Olsen, Florian Beiser, Yaolin Ge)

## General Comments

The group provides an introduction to their data analysis repository in the README.md what is well appreciated by the reviewers. Therein and the Introduction, the authors highlight the relevance of their prediction models for safety as well as energy production and mention the current operational HBV modelling. This gives a clear motivation for their data-driven predition modelling in the subsequent report. 

(Sentences to Models)

(Sentences to Shrinkage)
It seems that many different methods have been applied. It is so nice to see the implementation on different methods. In general, it worked as expected to reduce the variance of the predicted model. 

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
So nice to see muliple implementation on lasso, elastic net and fused lasso. It is so interesting to see the effect from fused lasso on the predicted water level, it achieves the goal of reducing variance as a shrinkage method even though it might hamper the capability for the fused lasso model to have higher accuracy. It is great to see the comparison in terms of the test MSE to dig out which one performs the best. Although linear regression works pretty perfect, 50 numbers of covariates are certainly not easy to interpret. Therefore, you did a great job by applying different lassos for proving its ability of shrinking. But we had a small confusion on the lasso section, why lambda is so small to reduce the number of the covariates dramatically. Also, in the plot showing the seasonability variation comparing different effects from multiple methods. It seems that the variances in those significant months are shrinked, but not in other months, so it is nice that you can have a discussion on why this happened. But in general, it is a very comprehensive part to read and understand.

## Conclusion

The authors perform a statistically sound analysis of the given data and develop interpretable prediction models, where they deliberately respect the time-dependence of the variables. The methods are more than appropriate for the scope of the project and the results are clearly presented. The report is very well written. It stands out that the authors implement, interpret and compare five different approaches!

We suggest the following minor amendments:
- ...
- ...