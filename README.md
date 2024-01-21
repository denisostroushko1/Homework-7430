# Homework-7430

Homework for Fall 2023 PUBH 7430 at the University of Minnesota. I found a lot of cool ways to present tables with summary statistics, as well as test and models output. I also 
found a lot of useful packages that interact with `ggplot` mainly. 

Also, textbook and lecture materials cover way more intro-level regression methods and theory, and I wish to use this file as a table of  contents. 

By default, I use `kable`, `kableExtra`, `tidyverse`, and `ggplot2` a lot, so I will only be making notes of new packages 
I find and use for the analysis. 

# HW2

* Statistical Concepts: 
  + Review of GLMs and link functions for a variety of exponential family distributions. 
  + Comparison of how interpretation of model coefficients changes as we vary distributional and link function assumptions. 
  + Estimating variance from a linear model using varying link functions 
  + Review of residual diagnostics for a regression model. A new way of Poisson regression diagnostic for overdispersion parameter using fitted and observed values of the outcome 
  
* Implementation via R code
  + basic R code for `glm` functions 
  
# HW3

* Statistical Concepts: 
  + First examples in GEE GLM models. Compassion of varying correlation structure assumption on the final model estimates 
  + Showing the impact of imbalanced cluster size on the final model coefficients for varying correlation structure assumptions 
  + Review of hypothesis testing if coefficients are equal to zero. Several examples of hypothesis testing multiple coefficients at the same time. 
    - no implementation was done in this assignment, but an `anova` fucntion should be able to handle comparison of GEE models 
  
* Implementation via R code
  + Estimation of expected response level for a given set of covariate values using `emmeans`. This implementation works with 
    robust standard errors produced by the sandwich estimator of variance and gives a 95% confidence interval either for an 
    individual observation or an average response level in the population 
  
* Packages: 
  + `geepack`: fitting GLM models with robust variance estimators. Specifying cluster other than "~1" allows to wort with the 
    analysis of correlated outcomes, such as longitudinal data, or correlation within a certain cluster. 
  
# HW4

* Statistical Concepts: 
  + Mixed Effect Regression model/General Linear Mixed Models (GLMM)
  + Testing if mixed effects help explain observed variation in the outcomes. Testing is performed using a mixture $\large \chi^2$ distribution 
  + Interpretation of GLMM coefficients. Poisson regression used as an example. 
  
* Implementation via R code
  + use of `lmer` function to fit Gaussian Linear Mixed Effect models. 
  + calculation of the test statistic and a p-value for the mixture $\large \chi^2$ test using base R code and several `lmer` models
  + use of `glmer` function to fit GLMM models for other families of distribution for the outcome variable 
  
* Packages: 
  + `lme4`: all purpose package for fitting `lmer` and `glmer` models. 
    - Specifying `glmer` with Gaussian family and identity link function yields the same results as `lmer` 
  
# Final Project 

* Final Project focuses on the analysis of the data using methods covered in HW2-4. The purpose of the project was to: 
  + be able to develop a hypothesis from the exploratory data analysis (or data documentation like in the case of my project)
  + make proper modeling choices and assumptions 
  + make Statistical Analysis Plan (SAP) 
  + deliver the results as a report 
* Working folder covers all parts of the process, with the model development steps captured in the final report `.qmd` file 
* I am working on review of existing R function and packages to use LASSO shrinkage for variable selection in the GEE and GLMM models. 
