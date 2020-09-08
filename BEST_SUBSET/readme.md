# LINEAR REGRESSION(BEST SUBSET)

The problem of selecting the best subset or subsets of independent variables in a multiple linear regression analysis is two-fold. The first, and most important problem is the development of criterion for choosing between two contending subsets. Applying these criteria to all possible subsets, if the number of independent variables is large, may not be economically feasible and so the second problem is concerned with decreasing the computational effort. This paper is concerned with the second question using the Cp-statistic of Mallows as the basic criterion for comparing two regressions. A procedure is developed which will indicate 'good' regressions with a minimum of computation.

## Best subset selection
Best subset selection is an algorithm that will help you select the best linear model.


The algorithm is the following:
![Image of best subset](https://github.com/Valdermaut/HOT-METAL-SILICON-REDUCTION-USING-ML/blob/master/IMAGES/best_subset4.png)





### STEPS INVOLVED IN FINDING THE BEST SUBSET :
      Step 1  : Import all the required libraries required :

      Step 2  : Read the dataset.

      Step 3  : Define X and y

      Step 4  : Use train test split from sklearn

      Step 5  : Here we are using OLS model which stands for “Ordinary Least Squares”. This model is used for performing linear regression.
                     #Adding constant column of ones, mandatory for sm.OLS model
                     #Fitting sm.OLS model

      Step 6 : Using the backward elimination process.

      Hence we will remove this feature and build the model once again. This is an iterative process and can be performed at once with the help of loop​.
                   #Backward Elimination

       Step 7 : The Recursive Feature Elimination (RFE) method works by recursively removing attributes and building a model on those attributes that remain.

      #Initializing RFE model

      Step 8  : Now we need to find the optimum number of features, for which the accuracy is the highest. 
              We do that by using loop starting with 1 feature and going up to 13. 
              We then take the one for which the accuracy is highest.


      Step 9 : As seen from above code, the optimum number of features is 10. 
               We now feed 10 as number of features to RFE and 
               get the final set of features given by RFE method,
               as follows:
                            cols = ​list​(X.columns) model = LinearRegression() #Initializing RFE model
                            model.fit(X_rfe,y)
                            temp = pd.Series(rfe.support_,index = cols) selected_features_rfe = temp[temp==​True​].index print​(selected_features_rfe)


      Step 10 : Here we will do feature selection using Lasso regularization. 
               If the feature is irrelevant, lasso penalizes it’s coefficient and make it 0. 
               Hence 

      Step 11 :
                print​(​"Lasso picked "​ + ​str​(​sum​(coef != ​0​)) + ​" variables and eliminated the other "​ + ​str​(​sum​(coef == ​0​)) + ​" variables"​)

      Step 12 : Plot the best subset

 ## BEST SUBSET PLOTTING
 
 ![BEST SUBSET](https://github.com/Valdermaut/HOT-METAL-SILICON-REDUCTION-USING-ML/blob/master/IMAGES/best_subset.png)

      Step 13: Finally get a full summary of your model
 
 
 ![BEST SUBSET](https://github.com/Valdermaut/HOT-METAL-SILICON-REDUCTION-USING-ML/blob/master/IMAGES/bestsubset11.png)
 
 ![BEST SUBSET](https://github.com/Valdermaut/HOT-METAL-SILICON-REDUCTION-USING-ML/blob/master/IMAGES/bestsubset12.png)
 
 ![BEST SUBSET](https://github.com/Valdermaut/HOT-METAL-SILICON-REDUCTION-USING-ML/blob/master/IMAGES/bestsubset13.png)
 
 ![BEST SUBSET](https://github.com/Valdermaut/HOT-METAL-SILICON-REDUCTION-USING-ML/blob/master/IMAGES/bestsubset14.png)
      
      
