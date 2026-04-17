# Homework 1 Task 3

------------------------------------------------------------------------

Answer the following questions based on exercises from *An Introduction to Statistical Learning with Applications in Python*.

## Chapter 2.4 Exercises

------------------------------------------------------------------------

### Exercise 1 (ISLP exercise 2)

Explain whether each scenario is a **classification or regression** problem, and indicate whether we are most interested in **inference or prediction**. Finally, provide **n** (size of observation dataset) and **p** (number of predictors).

**(a)** We collect data on 200 protected marine reserves worldwide. For each reserve we record species richness, reserve size, years since establishment, enforcement budget, and proximity to human settlements. We are interested in understanding which factors affect species richness.

> **Your Answer:**
>
> This is a *regression* scenario because richness is a continuous numerical value. We are most interested in *inferring* the relationship between each factor and species richness. n = 200, p = 4.

------------------------------------------------------------------------

**(b)** A conservation agency wants to know whether a proposed habitat corridor will successfully support wildlife movement or fail to do so. They collect data on 30 previously established corridors. For each corridor they have recorded whether wildlife movement was successful or unsuccessful, corridor width, length, surrounding land use type, and eight other variables.

> **Your Answer:**
>
> This would be a *classification* scenario because each corridor falls into a category of being successful or unsuccessful. We are interested in *predicting* the outcome of a proposed corridor. n = 30, p = 11.

------------------------------------------------------------------------

**(c)** We are interested in predicting weekly average ground-level ozone concentration in a coastal city. We collect weekly data for all of 2019. For each week we record average ozone concentration, sea surface temperature, wind speed, solar radiation, and atmospheric

> **Your Answer:**
>
> This would be a *regression scenario* because we are *predicting* a continuous numerical variable. n = 52 weeks, p = 4.

------------------------------------------------------------------------

### Exercise 2 (ISLP exercise 5)

What are the advantages and disadvantages of a very flexible (versus a a less flexible) approach for regression? Under what circumstances might a more flexible approach be preferred to a less flexible approach? When might a less flexible approach be preferred?

> **Your Answer:**
>
> A more flexible approach (more predictors) will have higher variance (disadvantage) resulting in a less accurate prediction but lower bias (advantage) resulting in a more confidence in the predictor effect. A more flexible approach is preferred when the real-life problem has many factors so you need to make more assumptions to approximate the true shape of F. A less flexible approach would be preferred when your confident there aren't as many predictors so your not worried about bias and want an accurate prediction. Ultimately, to minimize the test MSE you want to find a method that minimizes both variance and bias.
>
> For inference, a less flexible approach is preferred because it provides clear, interpretable relationships between predictors. For prediction, a more flexible approach is better because it can capture complex patterns to minimize error, as long as it doesn't overfit.
>
> A flexible approach can lead to better predictions by reducing bias, but it risks being less accurate if high variance causes more noise. The goal is to balance these to minimize the overall test MSE.
>
> A large training set allows for a more flexible approach because there is enough data to support complex shapes. Conversely, a small training set requires a less flexible approach to prevent the model from overfitting to a limited number of points.

------------------------------------------------------------------------

### Exercise 3 (ISLP exercise 6)

Describe the differences between a **parametric** and a **non-parametric** statistical learning approach. What are the **advantages** of a parametric approach to regression or classification (as opposed to a non-parametric approach)? What are its **disadvantages**?

> **Your Answer:**
>
> A parametric approach has a functional form for how variables are related and a non-parametric approach does not. The parametric approach advantages are that it can be used with small training sets and is computationally easier to estimate. Since you are only estimating a few fixed parameters, the model is simpler to interpret and requires less data to reach a good conclusion. The disadvantage is that your predictions will not be as good if your assumptions are wrong. If the functional form you pick is far from the true $f$, the model will suffer from high bias and will be too rigid to capture the actual patterns in the data. This mismatch leads to underfitting, where the model ignores the complexities of the real-world problem because it is forced to follow a pre-defined shape.