# HOUSE-PRICE-PREDICTIONS-
STEPS INVOLVED -
1. DATA EXPLORATION
2. DATA VISUALIZATION ( WITH THE HELP OF CHARTS )
3. DATA PRE-PROCESSING (CLEANING OF DATA- We check the datasets and handle the missing data, outliers and categorical variables.)
4. CONVERTING THE DATA INTO A NUMERIC FORM 
5. CREATING ML MODELS

Understand the problem : We look at each variable and do a philosophical analysis about their meaning and importance for this problem.
Univriable Study : We focus on the dependent variable SalePrice.

STEP 1 - DATA EXPLORATION 
1. Shape of the datasets
2. Structure of the datasets 
3. Unique and null values 
4. Dropping columns with more than 95% null values 


STEP 2 - DATA VISUALIZATION INSIGHTS 
1. SalePrice has a positive skewness.
2. Reject most of the categorical & continuous variables as they are not correlated with our predictive variable.
3. GrLivArea and TotalBsmtSF seem to be linearly related with 'SalePrice'. Both relationships are positive, 
    which means that as one variable increases, the other also increases. In the case of 'TotalBsmtSF', we can see that 
    the slope of the linear relationship is particularly high.
4. OverallQual also seem to be related with 'SalePrice'. The relationship seems to be stronger in the case of 'OverallQual',
   where the box plot shows how sales prices increase with the overall quality.
5. GarageCars and GarageArea are also some of the most strongly correlated variables.
6. YearBuilt id slightly correlated with SalePrice 


STEP 3 - DATA PRE-PROCESSING
1. Dropping all the unwanted rejected categorical and continuous columns from the datasets (after visualizing the variable one by one )
2. For example- variables like 'PoolQC', 'MiscFeature' and 'FireplaceQu' have too many outliers, so we delete them.
3. MasVnrArea and MasVnrType, we can consider that these variables are not essential. Furthermore, they have a strong correlation with 
   YearBuilt and OverallQual which are already considered. Thus, we will not lose information if we delete MasVnrArea and MasVnrType.
4. Filling all the null values with 'None'.
5. Outlier treatment for SalePrice, GrLivArea and TotalBsmtSF :
   - SalePrice showed 'peakedness', positive skewness and does not follow the diagonal line, which is corrected by a minor change.
   - Similiar outlier treatment is done for GrLivArea and TotalBsmtSF.
   
   
STEP 5 - ML MODELLING 
1. Splitting the data into train and test samples in the ratio of 70:30 ratio. (70 % training data & 30% test data)
2. Evaluating with the help of Mean squared error, Mean absolute error and median absolute error.
3. Models used are Linear Regression, Decision tree, Random forest, Gradient boosting regression.
4. Accuracy rates of different models are predicted.
5. The best predicted model among the four are is the Gradient boosting regression with the accuracy rate of 86 %.

THANKYOU
