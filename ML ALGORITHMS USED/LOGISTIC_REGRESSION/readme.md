# LOGISTIC REGRESSION

In statistics, the logistic model (or logit model) is used to model the probability of a certain class or event existing such as pass/fail, win/lose, alive/dead or healthy/sick. 

This can be extended to model several classes of events such as determining whether an image contains a cat, dog, lion, etc. Each object being detected in the image would be assigned a probability between 0 and 1 and the sum adding to one.

Logistic regression is a statistical model that in its basic form uses a logistic function to model a binary dependent variable, although many more complex extensions exist. 

In regression analysis, logistic regression​ (or logit regression) is estimating the parameters of a logistic
model (a form of binary regression). 

Mathematically, a binary logistic model has a dependent
variable with two possible values, such as pass/fail which is represented by an indicator variable, where the two values are labeled "0" and "1".

![linear regression](https://github.com/Valdermaut/HOT-METAL-SILICON-REDUCTION-USING-ML/blob/master/IMAGES/logistic1.jpeg)


## LOGISTIC REGRESSION ASSUMPTIONS
    1.Binary logistic regression requires the dependent variable to be binary.
    
    2.For a binary regression, the factor level 1 of the dependent variable should represent the desired outcome.
    
    3.Only the meaningful variables should be included.
    
    4.The independent variables should be independent of each other. That is, the model should have little or no multicollinearity.
    
    5.The independent variables are linearly related to the log odds. 6.Logistic regression requires quite large sample sizes.


## STEPS INVOLVED IN TRAINING THE MODEL :
    Step 1 : import all the required libraries required.

    Step 2 : Read the dataset.

    Step 3 : Define X and y

    Step 4 : Use train test split from sklearn

    Step 5 : Lets train our model and fit the dataset.

    Step 6 : Now check the accuracy of the model

    Step 7 : Now lets you test how well your model fits the data set.
    
    Step 8 : Finding the confusion matrix


## CONFUSION MATRIX
 

 The confusion matrix is a handy presentation of the accuracy of a model with two or more classes.
The table presents predictions on the x-axis and accuracy outcomes on the y-axis. The cells of the table are the number of predictions made by a machine learning algorithm.

For example, a machine learning algorithm can predict 0 or 1 and each prediction may actually have been a 0 or 1. Predictions for 0 that were actually 0 appear in the cell for prediction=0 and actual=0, whereas predictions for 0 that were actually 1 appear in the cell for prediction = 0 and actual=1. And so on.
from sklearn.metrics import confusion_matrix confusion_matrix = confusion_matrix(y_test, y_pred) print(confusion_matrix)

    Step 9 : Finally get a full summary of your model
    model_1 = sm.Logit(y, X) result_1 = model_1.fit() result_1.summary()
    



## LOGISTIC REGRESSION TRUTH VS PREDICTED

![linear regression](https://github.com/Valdermaut/HOT-METAL-SILICON-REDUCTION-USING-ML/blob/master/IMAGES/logistic.png)

    
    
## MODEL SUMMARY    
   

![linear regression](https://github.com/Valdermaut/HOT-METAL-SILICON-REDUCTION-USING-ML/blob/master/IMAGES/logistic2.png)

![linear regression](https://github.com/Valdermaut/HOT-METAL-SILICON-REDUCTION-USING-ML/blob/master/IMAGES/logistic3.png)

## LOGISTIC RESULTS

![linear regression](https://github.com/Valdermaut/HOT-METAL-SILICON-REDUCTION-USING-ML/blob/master/IMAGES/logistic4.png)


![linear regression](https://github.com/Valdermaut/HOT-METAL-SILICON-REDUCTION-USING-ML/blob/master/IMAGES/logistic5.png)


![linear regression](https://github.com/Valdermaut/HOT-METAL-SILICON-REDUCTION-USING-ML/blob/master/IMAGES/logistic6.png)

## LOGISTIC REGRESSION (IMPORTANT PARAMETERS)

![linear regression](https://github.com/Valdermaut/HOT-METAL-SILICON-REDUCTION-USING-ML/blob/master/IMAGES/logistic7.png)
