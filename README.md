# Report Baseball Players' Batting Metrics using R

This final project of the MATH158 Statistical Linear Models aims to predict a player's performance (measured by `isolated power percentage`).

## 1. Initial Assessment of Dataset: 
- How representative of our population is our dataset? Note strengths and limitations
- Graphing distributions of and correlations between select variables
- Conclusion: investigate outliers as well as skews and asymmetry in bell-shaped distributions of certain variables

## 2. Apply Simple Linear Regression (SLR)
- Check statistical assumptions for Student's T-test: linearity, independent variables, normally-distributed errors and homoscedasticity
- Test hypothesis that `isolated power percentage` is correlated with `launch angle average` with **Student's T-test**
- Conclude `launch angle average` can be used to predict `isolated power percentage`, but more variables need to be added to the regression model to explain more of the variance.

## 3. Apply Multiple Linear Regression (MLR)
- Checked for multicollinearity between predictor variables 
- Choose one predictor variable among groups of highly correlated variables
- Conduct **F-test** to check if interaction variables are necessary
- **Compare MLR models** with different combinations of borderline highly correlated variables
	- Manually selected variables compared using 3-fold cross validation on 2/3 of dataset
	- Separately, use **forward selection algorithm** on all predictor variables; F-statistic as selection criteria
	- Test significance of model coefficients through F-tests
	- Assess R^2 and RMSE of chosen model

## 4. Smooth model fit using LOESS
- This nonparametric model using k-nearest neighbour methods is more robust since it does not make statistical assumptions on the data