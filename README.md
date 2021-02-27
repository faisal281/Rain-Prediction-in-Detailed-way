This dataset contains about 10 years of daily weather observations from many locations across Australia.

AIM: RainTomorrow is the target variable to predict. It means -- did it rain the next day, Yes or No? This column is Yes if the rain for that day was 1mm or more

ABOUT DATASET: This data set contain an huge amount of data which has to be processed in  many different ways for building an model. This data contain many NAN values in it and there are many outliers and categorical data as well. The data has total of 145460 rows and 23 columns where the job has to be done for analysing the data.

Jobs Done on Data: 
1. Analysing The Data
2. Exploratory Data Analysis
3. Data Preprocessing
4. Removing of Outliers
5. Removing of NAN values IN Categorical and Numerical features
6. Conversion of Categorical feature to Numerical Feature
7. Building a LogisticRegression model

Analysing The Data: After performing of many analysing techniques found that data is humongous. Every coulmn has nan values in it. The describe section gives an idea of 25%, 75% of what the data contains and maximum and minimum values as well.

Exploratory Data Analysis: By using of seaborn,plotting of correlation haetmap, I understood that how well the features are correlated with eachother. By use of Boxplot it very much clear and found that there are much outliers in it which I will describe in below sections.

Data Preprocessing: This part is the most imortant part of any building model because it is mandatory that Data has to be cleaned completely so that model doesn't get affected by many factors.

Removing of Outliers: By drwaing the boxplot the outliers were presnet in columns['Rainfall', 'Evaporation', 'WindGustSpeed', 'Windspeed9am', Windspeed3pm']. These outliers will affect the accuracy of model. By use IQR(INter Quantile Range). By calcualting the difference between Quantiles and giving the upper and lower boundaries for every feature mentioned above I made sure that every value above and below of that is outlier and which has to be removed/excluded from the dataset.

Removing of NAN values in categorical and numerical features: Removing of nan values is in numerical features has to be done using the filling it by use of median because we cannot use mean,the reason for it is it might get affected by any outliers present in the dataset. The filling of nan values in categorical  data  is by use of mode(which occured most of the times). BY this part the dataset is completely cleaned by outliers and nan values, So that I can move ahead by remaining part of building a model.

Conversion of Categorical feature to Numerical: This has to be done compulsory if any categorical data is present because machines can only understand numerical data. If any objects are present in the dataset  then the machinen cant understand it. By use of Labelbinazie, Label encoder and Onehotencoding, This job can be done perfectly. First we will use labelencoder so that the object be converted to an array and then we use onehotencoding to change the array in 0 and 1 for each seperate feature prefixx so that it will be easier to read it. The date format is also changed by using the pandas.

Building a LogisticRegression model: Before building a model,the target feature has to be dropped from the data so that the prediction should be done on that. The data is split into train and test data. I have used minmaxscaler to normalize and strandadise the data.I used logisticregression for building the model.The accuracy of the model is 83%.
