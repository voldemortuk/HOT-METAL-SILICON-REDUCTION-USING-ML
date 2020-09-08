## PREPARE & PROCESS THE DATA

![prepare and process](https://github.com/Valdermaut/HOT-METAL-SILICON-REDUCTION-USING-ML/blob/master/IMAGES/ava2.png)


##### Due to high bias, data from 2016 onwards was considered

#### (Trial also done with Training data from 2015 onwards but resulted in drop in accuracy of models)

#### We can also see the cum % in Reverse and for 2016 onwards the data is more appropriate
#### and practical.




### CORRELATION COEFFICIENT
      The correlation coefficient (sometimes referred to as Pearson's correlation coefficient,
      Pearson's product-moment correlation, or simply ​r​) measures the strength of the linear relationship between two variables. 
      It is indisputably one of the most commonly used metrics in both science and industry. 
      In science, it is typically used to test for a linear association between two dependent variables, or measurements. 
      In industry, specifically in a machine-learning context, it is used to discover collinearity between features, 
      which may undermine the quality of a model.

### STEPS INVOLVED IN FINDING THE CORRELATION MATRIX
      STEP 1 :importing libraries


      STEP 2 : Read the dataset using pandas
      df = pd.read_csv("base_data2.csv") 
      df.drop(['CLASS','DT','YEAR','HML_SI_CAT'],axis=1,inplace=True) 

      Step 3 :Define X and y


      STEP 4 : Define the correlation between each parameter. df.corr().round(2)

      #The correlation matrix for the following dataset

      STEP 5 : Plot the correlation matrix.

      STEP 6 : Finding the important features #Correlation with output variable
      #Selecting highly correlated features
      relevant_features = cor_target[cor_target>0.7] 
      relevant_features
      
      
![correlation](https://github.com/Valdermaut/HOT-METAL-SILICON-REDUCTION-USING-ML/blob/master/IMAGES/correlation1.png)



#### Final data set to be used for model construction had 33 parameters (excluding Si and Availability) and sample set = 419



![correlation](https://github.com/Valdermaut/HOT-METAL-SILICON-REDUCTION-USING-ML/blob/master/IMAGES/correlation.png)


![correlation](https://github.com/Valdermaut/HOT-METAL-SILICON-REDUCTION-USING-ML/blob/master/IMAGES/correlation2.png)




### Exclusions with rationale

- 1) From a set of 112 parameters, a set of 38 parameters were shortlisted on the basis of domain knowledge of the business users. If all the parameters are considered for the subsequent model development, they will lead to the following problems :-

      i) Resultant model may give importance to parameters which actually do not play any role in the actual process to control Si.
      ii) Since the model development considers the entire data set to determine the important parameters, the non-impacting parameters will
      also affect the final set.
      iii) The base data is loaded using pandas and we drop the parameters 'CLASS','DT','YEAR','HML_SI_CAT to obtain the our final dataset which 
      we will use the train our modelss.
  
    df.drop(['CLASS','DT','YEAR','HML_SI_CAT'],axis=1,inplace=True)
    df.head(3)
 
 
 ### List of parameters considered for final set is provided below

![correlation](https://github.com/Valdermaut/HOT-METAL-SILICON-REDUCTION-USING-ML/blob/master/IMAGES/correlation4.png)

### Missing data recover in python


  Pandas series is a One-dimensional ndarray with axis labels. 
  The labels need not be unique but must be a hashable type. The object supports both integer- and label-based indexing and provides a host of methods for performing operations involving the index.

Pandas​ Series.fillna()​ function is used to fill NA/NaN values using the specified method.

Syntax: Series.fillna(value=None, method=None, axis=None, inplace=False, limit=None, downcast=None, **kwargs)

Parameter : value : Value to use to fill holes

method : Method to use for filling holes in reindexed Series pad / ffill axis : {0 or ‘index’}
inplace : If True, fill in place.
limit : If method is specified, this is the maximum number of consecutive NaN values to forward/backward fill
downcast : dict, default is None Returns : filled : Series


      Step 1: Read the data

      Step 2: Find the median of each column and fill it in column using the fillna().
 
As we can see in the output, the ​Series.fillna()​ function has successfully filled out the missing values in the given series object.

