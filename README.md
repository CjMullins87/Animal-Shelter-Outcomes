
# Classification Tasks:  Predicting Outcomes of Shelter Animals

### Overview

In this project I will be looking at the [*Austin Animal Center Shelter Intakes and Outcomes*](https://www.kaggle.com/aaronschlegel/austin-animal-center-shelter-intakes-and-outcomes) dataset made publicly available on Kaggle to try and predict animal outcomes. After a brief review of the data and the meaning of its columns, I remove data that can't be used to make a prediction - such as data which details the outcome event - and then create two new features to better clarify information in the dataset.

After cleaning and modifying the data, I attempt several modeling methods including 1) simple decision tree, 2) random forest classifier, 3) adaboost classifier, 4) gradient boosting classifier, and 5) xgboost classifier to compare performance.

### Contents

1. [EDA and Feature Engineering](/EDA.ipynb)
2. [Model Fitting and Review](/Model%20Fitting%20and%20Review.ipynb)

### Supplementary Materials

1. [Executive Summary](/Executive%20Summary.pdf)

### Results

After first fitting a simple decision tree, I find that both of the features I engineered were listed in the top 5 features - suggesting that they could reliably impact what happened to the animal.

![.](/1.PNG)

Using this simple decision tree model as a baseline, I took its 78% as a minimum result for the next sets of classifiers. After testing multiple models, the best performing one was found using XG Boost, with an accuracy of 82%; the next best performing model was a random forest which scored 81% accuracy.

While the random forest was initially overfit, gridsearch was used to fine tune and select optimal paramaters to successfully yield that level of accuracy.

In exploring the efficacy of our most accurate model, it was found that the model was less successful at predicting whether the animal would die or go missing, but overall the model was able to broadly and accurately anticipate an outcome.

![.](/3.png)
