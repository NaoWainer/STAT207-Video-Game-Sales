# Video Game Sales & Commercial Success Analysis

## Overview

This project analyzes the factors associated with video game sales and commercial success using a dataset of over 1,700 video games released between 2004 and 2010. The dataset was originally compiled and curated by Dr. Joe Cox and includes information such as US sales, platform, genre, critic review scores, sequel status, used price, and online multiplayer availability.

The project uses **linear regression** and **logistic regression** to investigate relationships between game characteristics and commercial performance.

## Research Questions

### Linear Regression

What is the relationship between a game's critic review score and its US sales after controlling for sequel status, used price, and platform? How well does the model predict sales for new, unseen games?

### Logistic Regression

How do critic review score, sequel status, and online multiplayer availability relate to whether a game becomes a blockbuster, defined as selling more than 1 million copies? How well does the resulting classifier perform on new data?

## Methods

### Linear Regression

A multiple linear regression model was used to predict US video game sales, measured in millions of units.

Predictors included:

* Critic review score
* Sequel status
* Used price
* Platform

The model was evaluated using:

* Regression coefficients
* 95% confidence intervals
* Residual diagnostics
* R²
* RMSE
* Training and test data performance

### Logistic Regression

A logistic regression model was used to predict whether a game was a blockbuster.

A blockbuster was defined as a game selling more than 1 million copies.

Predictors included:

* Critic review score
* Sequel status
* Online multiplayer availability

The classifier was evaluated using:

* Logistic regression coefficients
* Pseudo-R²
* AUC
* Accuracy
* Sensitivity
* Specificity

## Key Findings

* Critic review score had a statistically significant positive relationship with US sales.
* A one-point increase in critic review score was associated with approximately **0.019 million (19,000) additional copies sold**, controlling for the other variables in the linear regression model.
* The linear regression model had an **R² of 0.117**, meaning it explained approximately 11.7% of the variability in US sales.
* The linear regression model had a test RMSE of approximately **0.987 million units**, indicating limited precision when predicting individual game sales.
* The logistic regression model achieved an **AUC of 0.801**, indicating that the model was able to distinguish between blockbuster and non-blockbuster games reasonably well.
* The classifier achieved approximately **84.3% sensitivity** and **55.3% specificity** on the test data.

## Limitations

The dataset only includes games released between 2004 and 2010, so the findings may not fully represent the modern video game industry.

The linear regression model also showed violations of equal variance and normality, largely due to a small number of games with exceptionally high sales. Additionally, important factors such as marketing spending, franchise popularity, social media attention, and release timing were not included in the dataset.

Because of these limitations, the models provide useful insights into the relationships in the dataset but should not be treated as definitive predictors of video game success.

## Tools & Libraries

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Statsmodels
* Scikit-learn
* Jupyter Notebook

## Project Files

* `project_03_template(1).ipynb`: Jupyter Notebook containing the data cleaning, statistical analysis, regression models, visualizations, and conclusions.
* `video_games copy.csv`: Dataset used for the analysis.

## Future Work

Future analysis could incorporate additional predictors such as marketing spending, social media buzz, genre, publisher size, and pre-release hype. More recent video game data could also be used to examine whether the factors associated with commercial success have changed with the growth of digital distribution, downloadable content, streaming, and mobile gaming.
