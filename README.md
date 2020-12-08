# IMDB-Ratings

## File Description
1. Case Study.txt: Problem Statement
2. IMDB Ratings.html: HTML version of already executed Jupyter Notebook
3. IMDB Ratings.ipynb: Jupyter Notebook
4. movie_review_data.csv: CSV Data File

## Steps 
1. Importing Data
2. Cleaning Data
3. Feature Engineering
    -  Keep only top 5 most frequent classes for all categorical variables
    -  Split Genre between different columns
    -  Generate new variable success_flag which indicates whether movie is successful or not
        - Assumption: Top 25% movies are assumed to be successful 
    -  Get Dummy Variables   
4. EDA
    - Visualization
    - Hypothesis testing
    - Determine statistically significant variables wrt success flag and imdb_score
    
5. Modelling
    - Drop insignificant variable
    - Choose AUC-ROC too be main metric
    - Split data in training and test set
    - Start with base tree, KNN, SVM and logistic model
    - Will notice that RF is slightly better than others
    - Try random hyperparameter grid search along with cross validation
    - Will notice significant increase in AUC-ROC ~0.9
    - Choose the model with maximum AUC-ROC on validation data
    - Plot ROC curve for all the models on test set
    - Display confusion matrix along with precision and recall
    
6. What to do after this?
    - Thorough analysis for each class
    - More efficient encoding techniques
    - Stacked Ensemble
    - PCA to further reduce dimension of continous variable without information loss (after standardization)
