 
# Loan Prediction using Decision Tree and Support Vector Machine
 
The repository contains a loan eligibility prediction based on a [Kaggle dataset](https://www.kaggle.com/ninzaami/loan-predication). 
The primary goal of this project was to use Decision Tree and Support Vector Machines for predicting loan approval.  

### Quick Start: 
[Check out](https://nbviewer.jupyter.org/github/alicevillar/Loan_Eligibility_Prediction/blob/main/loan_prediction.ipynb
) a static version of the notebook with Jupyter NBViewer from the comfort of your web browser.


## Dependencies:
 
* [Numpy](https://numpy.org/)
* [Pandas](https://pandas.pydata.org/)
* [SciKit-Learn](https://scikit-learn.org/)
* [Matplotlib](https://matplotlib.org/)
* [Seaborn](https://seaborn.pydata.org/)
 
## Approach:

This project is organized in three parts:

    PART 1: Data Handling -> Importing Data with Pandas, Cleaning Data, Data description.  
    PART 2: Data Analysis -> Supervised Machine learning Techniques: + Decision Tree Model + Support Vector Machine (SVM).  
    PART 3: Valuation of the Analysis -> K-folds cross validation to evaluate results locally.  
    

## Results

The dataset consisted of 614 rows and 13 columns, with Y being defined as Loan_Status. First, I had to find out the number of missing values in each column. To see how many missing values existed in the collection I used .sum() chained on the function isnull(). Then, I used dropna() function to remove the empty fields from the data. After this, I used the replace method I replaced all Y values with boolean values. 

In Part 2, I found the following accuracy score for the Decision Tree and SVM models : 

* Decision Tree  => Accuracy score = 0.7916666666666666
* Suport Vector Machine => Accuracy score = 0.7708333333333334

In Part 3 I applied kfold (model validation technique): 

* Applying Kfold to the Decision Tree result => 0.8
* Applying Kfold to the Support Vector Machine result  => 0.7854166666666667
 
Note that the result found with Kfold is very close to the result from the Decision Tree and SVM models, which demonstrates that both the Decision Tree and SVM models are not overfitting and therefore valid.
