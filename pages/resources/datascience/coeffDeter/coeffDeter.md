---
layout: article
key: page-resources-datascience-coeffDeter
permalink: /resources/datascience/coeffDeter/
---

Let's say we have a distribution of values, maybe something like this: <img align="right" src="/pages/resources/datascience/coeffDeter/plot.png">

How well does your model fit the observed data? Can differences in observed values be explained by

$\Large R^2 = 1 - \frac{ \sum_i(y_i - p_i)^2 }{ \sum_i(y_i - \bar{y} )^2 }$


$\bar{y}$ serves as a baseline model to compare with a model containing additional explanatory variables 
since the mean is the central point of a distribution, and outcomes have a tendency to take values near the mean, it is not a bad baseline or control to compare models that introduce additional variables.

The interpretation of $R^2$ is the propportion of the variability in y (since $\sum_i(y_i - \bar{y} )^2$ is the variability) explained by the new explanatory variables introduced in the model.

This values comes up very frequently in data analysis.

