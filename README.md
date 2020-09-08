# HOT-METAL-SILICON-REDUCTION-USING-ML

# DATA MINING PHASES/ TYPES
![Image of data mining](https://github.com/Valdermaut/HOT-METAL-SILICON-REDUCTION-USING-ML/blob/master/IMAGES/datamining.png)

## INTRODUCTION

Iron ores​ ​ are ​rocks​ and ​minerals​ from which ​metallic​ ​iron​ can be economically extracted.
The ​ores​ are usually rich in ​iron oxides​ and vary in color from dark grey, bright yellow, or deep
purple to rusty red.
The iron is usually found in the form of ​magnetite​ (​Fe3O4​, 72.4% Fe), ​hematite​ (​Fe2O3​, 69.9%
Fe), ​goethite​ (​FeO(OH)​, 62.9% Fe), ​limonite​ (​FeO(OH)·n(H​ O)​, 55% Fe) or ​siderite​ (​FeCO​ ,
48.2% Fe).


Ores containing very high quantities of hematite or magnetite (greater than about 60% iron) are known as "natural ore" or "direct shipping ore", 
meaning they can be fed directly into iron-making blast furnaces. Iron ore is the raw material used to make pig iron, which is one of the main raw materials 
to make steel—98% of the mined iron ore is used to make steel.

​ In 2011 the Financial Times has speculated that iron ore is "more integral to the global economy than any other commodity, except perhaps oil".

### EXTRACTING IRON FROM IRON ORE USING A BLAST FURNACE

The common ores of iron are both iron oxides, and these can be reduced to iron by heating them with carbon in the form of coke. Coke is produced by heating coal in the absence of air. Coke is cheap and provides both the ​reducing agent​ for the reaction and also the heat source. 


## DEFINE THE PROBLEM

So the problem which we will dealing is to reduce hot metal silicon at GBF . So to go about this we use the data mining technique.

            a) Business Case

         - Silicon directly impacts the quality as well as the production rate of the hot metal. For e.g. It has a direct impact on the slag viscosity which is a transport property that relates to the reaction kinetics and the degree of reduction of the final slag. It also determines the slag– metal separation efficiency, and subsequently the metal yield and impurity removal capacity. In operation, the slag viscosity is indicative of the ease with which slag could be tapped from the furnace, and therefore relates to the energy requirement and profitability of the process.
         Slag also plays a major role in determining the quality of hot metal obtained which, in turn is dependent on the formation of the slag and its mineralogical transformations. A good quality slag is necessary for a quality hot metal. Slag is a mixture of low melting chemical compounds formed by the chemical reaction of the gangue of the iron bearing burden and coke ash with the flux materials in the charge. All unreduced compounds such as silicates, aluminosilicates, and calcium alumino silicate etc. also join the slag. It is well known that the components of slag namely silica (SiO2) and alumina (Al2O3) increase the viscosity whereas the presence of calcium oxide reduces the viscosity. The melting zone of slag determines the cohesive zone of blast furnace and hence the fluidity and melting characteristics of slag play a major role in determining the blast furnace productivity.


         Currently, Silicon levels are controlled through experience and some primary data analysis. An example can be that of Hot Metal temperature which shows a direct correlation with Si.

            b) Problems in the existing process

         - Following are the issues faced :-

         i) Does not leverage the historical data to full extent.

         ii) Action is based on experience rather than the actual data.

         iii) Difficult to arrive at new parameters beyond what is already known.

            Why Si?

         ■ Directly impacts the quality and the production rate of hot metal

         ■ e.g. affects slag viscosity

         ■ transport property related to the reaction kinetics and the degree of reduction of the final slag -> impurity removal capacity

         ■ the slag–metal separation efficiency -> metal yield


             c) Overall objective
         - Hence, it is an important factor that needs to be controlled. A data mining model needs to be developed which can help arrive at a set of predominant factors and their relationships for the purpose of reducing the mean value of Silicon. Output of this model will then be verified with the existing data and operating ranges of the final select process parameters need to be determined.



## IDENTIFY AND PREPARE THE DATA

   #### a) Data Source and collection
         - Relevant data was collected from iMonitor system. Data is primarily of 4 types which are process parameters, hot metal chemistry, input coke data and input sinter data. Frequency is date wise. Period under consideration is between 1 Jan 2014 to 15 Oct 2017. As data was extracted from different screens/reports, parameters were arranged as per the date. Also, effort was put in for data preparation as data is not ready for analysis. A total of 112 parameters were captured initially and all were numerical data except the date field.

   #### b) Assumptions
         - Following are the assumptions made :-
         i) Si value>=0.70 is to be considered as High Silicon.

         ii) Days with Availability > 95% are assumed to be days with stable operation.

         iii) A ratio 1:2 for Low-High cases is good enough for prediction of Low cases.

         iv) Data is relevant and accurate.

         v) Conditions for high Silicon may not be entirely conversely true for conditions for low Silicon
         Shortlist parameters which have to be considered

         a. Domain knowledge

         i. Direct controllers

         ii. Indirect controllers (Indicators)

   #### c.Extract relevant data
          a. Availability>=95% 
          b. 17 months

   #### d. Data Sanitization
          a. Remove outliers – manual
          b. Address missing values/nulls – 0/Average
          c. Address class imbalance problem
          d. Remove inter-correlated data
          e. Categorization
          f. Low <=0.70(L)
          g. High>0.70(H
## AVAILABILITY AND SI TREND

![si trend](https://github.com/Valdermaut/HOT-METAL-SILICON-REDUCTION-USING-ML/blob/master/IMAGES/ava.png)





The given data is the availability of silicon in the iron ore found after it undergoes extraction process.




![si trend](https://github.com/Valdermaut/HOT-METAL-SILICON-REDUCTION-USING-ML/blob/master/IMAGES/ava1.png)

   ### GR95DAYS - No of days with Availability>=95 Data from 1 Jan 2014 to 31 Mar 2017

## PREPARE AND PROCESS THE DATA
[PREPARE AND PROCESS](https://github.com/Valdermaut/HOT-METAL-SILICON-REDUCTION-USING-ML/blob/master/SELECT_REL_DATA/readme.md)
    
## MODEL THE DATA

### Metrics To Evaluate Machine Learning Algorithms

The metrics that you choose to evaluate your machine learning algorithms are very important.

Choice of metrics influences how the performance of machine learning algorithms is measured and compared. They influence how you weight the importance of different characteristics in the results and your ultimate choice of which algorithm to choose.

### Classification Metrics

Classification problems are perhaps the most common type of machine learning problem and as such there are a myriad of metrics that can be used to evaluate predictions for these problems.

In this section we will review how to use the following metrics:

            #### 1. Classification Accuracy.

            #### 2. Log Loss.

            #### 3. Area Under ROC Curve.

            ####  4. Confusion Matrix.

            #### 5. Classification Report.

#### 1. Classification Accuracy

Classification accuracy is the number of correct predictions made as a ratio of all predictions made.
This is the most common evaluation metric for classification problems, it is also the most misused. It is really only suitable when there are an equal number of observations in each class (which is rarely the case) and that all predictions and prediction errors are equally important, which is often not the case.

#### 2. Log Loss

Logistic loss​ (or log loss) is a performance metric for evaluating the predictions of probabilities of membership to a given class.

The scalar probability between 0 and 1 can be seen as a measure of confidence for a prediction by an algorithm. Predictions that are correct or incorrect are rewarded or punished proportionally to the confidence of the prediction.
Smaller log loss is better with 0 representing a perfect log loss. As mentioned above, the measure is inverted to be ascending when using the ​cross_val_score()​ function.

#### 3. Area Under ROC Curve

Area Under ROC Curve (or ROC AUC for short) is a performance metric for binary classification problems.
The AUC represents a model’s ability to discriminate between positive and negative classes. An area of 1.0 represents a model that made all predictions perfectly. An area of 0.5 represents a model as good as random.
A ROC Curve is a plot of the true positive rate and the false positive rate for a given set of probability predictions at different thresholds used to map the probabilities to class labels. The area under the curve is then the approximate integral under the ROC Curve.
You can see the the AUC is relatively close to 1 and greater than 0.5, suggesting some skill in the predictions.

#### 4. Confusion Matrix

The confusion matrix is a handy presentation of the accuracy of a model with two or more classes.
The table presents predictions on the x-axis and accuracy outcomes on the y-axis. The cells of the table are the number of predictions made by a machine learning algorithm.

For example, a machine learning algorithm can predict 0 or 1 and each prediction may actually have been a 0 or 1. Predictions for 0 that were actually 0 appear in the cell forprediction=0 and actual=0, whereas predictions for 0 that were actually 1 appear in the cell for prediction = 0 and actual=1. And so on.
Although the array is printed without headings, you can see that the majority of the predictions fall on the diagonal line of the matrix (which are correct predictions).

#### 5. Classification Report

Scikit-learn does provide a convenience report when working on classification problems to give you a quick idea of the accuracy of a model using a number of measures.

The ​classification_report()​ function displays the precision, recall, f1-score and support for each class.
Regression Metrics

In this section will review 3 of the most common metrics for evaluating predictions on regression machine learning problems:

            1. Mean Absolute Error.

            2. Mean Squared Error.

            3. R^2.

#### 1. Mean Absolute Error

The Mean Absolute Error (or MAE) is the average of the absolute differences between predictions and actual values. It gives an idea of how wrong the predictions were.
The measure gives an idea of the magnitude of the error, but no idea of the direction (e.g. over or under predicting).
A value of 0 indicates no error or perfect predictions. Like logloss, this metric is inverted by the ​cross_val_score()​ function.


#### 2. Mean Squared Error

The Mean Squared Error (or MSE) is much like the mean absolute error in that it provides a gross idea of the magnitude of error.
Taking the square root of the mean squared error converts the units back to the original units of the output variable and can be meaningful for description and presentation. This is called the Root Mean Squared Error (or RMSE).

#### 3. R^2 Metric

The R^2 (or R Squared) metric provides an indication of the goodness of fit of a set of predictions to the actual values. In statistical literature, this measure is called the coefficient of determination.
This is a value between 0 and 1 for no-fit and perfect fit respectively.
You can see that the predictions have a poor fit to the actual values with a value close to zero and less than 0.5.

#### Summary

#### You learned about 3 classification metrics:

      ● Accuracy.

      ● Log Loss.

      ● Area Under ROC Curve.

#### Convenience methods for classification prediction results:

      ● Confusion Matrix. 

      ● Classification Report.


####  And 3 regression metrics:

      ● Mean Absolute Error.

      ● Mean Squared Error. 

      ● R^2.
      
## TRAIN AND TEST 
1. [LINEAR REGRESSION](https://github.com/Valdermaut/HOT-METAL-SILICON-REDUCTION-USING-ML/tree/master/ML%20ALGORITHMS%20USED/LINEAR_REGRESSION)

2. [LOGISTIC REGRESSSION](https://github.com/Valdermaut/HOT-METAL-SILICON-REDUCTION-USING-ML/tree/master/ML%20ALGORITHMS%20USED/LOGISTIC_REGRESSION)

3. [DECISION TREE](https://github.com/Valdermaut/HOT-METAL-SILICON-REDUCTION-USING-ML/tree/master/ML%20ALGORITHMS%20USED/DECISION_TREE)

## VERFIY AND DEPLOY
[MODEL WISE IMPORTANT PARAMETERS](https://github.com/Valdermaut/HOT-METAL-SILICON-REDUCTION-USING-ML/tree/master/ML%20ALGORITHMS%20USED)

## CONCLUSION

### Out of the three models , model on decision tree was accepted to control Hot metal Silicon

### The reasons are :

      - It has the most reasonable accuracy.

      - The relevance of it parameters in terms of impact and the number.

      -It gives the least controlling levers and is actionable

      -It gives branching at each value and thus helping us obtain which parameter needs to be tweaked so that we can control silicon.

      -The outcome is easily communicable with the line manager as well as the operator.
       
    

    
