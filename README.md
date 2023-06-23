# Typhoon-Data-Analysis
Typhoon: - It is intense circular storm that originates over warm tropical oceans and is characterized by 
low atmospheric pressure, high winds, and heavy rain. Drawing energy from the sea surface and maintaining its 
strength as long as it remains over warm water, a tropical cyclone generates winds that exceed 119 km (74 miles) per hour

This is a list of the deadliest tropical cyclones, including all known storms that caused at least 1,000 direct deaths. 
There were at least 74 tropical cyclones in the 20th century with a death toll of 1,000 or more, including the deadliest tropical cyclone in recorded history. 
In October 1970, the Bhola cyclone struck what is now Bangladesh and killed at least 300,000 people. There have been 13 tropical cyclones in the 21st century 
so far with a death toll of at least 1,000, of which the deadliest was Cyclone Nargis, with at least 138,373 deaths when it struck Myanmar. In recent years, 
the deadliest Atlantic hurricane was Hurricane Mitch of 1998, with at least 11,374 deaths attributed to it, while the deadliest Atlantic hurricane was 
the Great Hurricane of 1780, which resulted in at least 22,000 fatalities. The most recent tropical cyclone with at least 1,000 fatalities was Cyclone 
Idai in 2019, which killed 1,303 people. (as according to 'WIKIPEDIA)

In this project I have done a complete analysis of typhoon and I also predict central Pressure and Grade of Typhoo.

## Analysis Process steps
In this Project I have done the analysis on Typhoon data set where I have done: - 

pre-process the data

perform the features selction

Taking sample

Pre-Process the sample

Perform Visualization

Load Machine Learning Model

and deploy Machine learning model on data set.

So when I was starting pre-processing of the dataset, there are lot of null value is available inside the dataset. I just refined it.
the Date of the typhoon is in wrong format so, I convert it into right format. Taking the sample form the entire population and start
pre-processing of it. After ensuring that Pre-Processing state of sample data is done successfully than we took sample data in further
stage which is data correlation.

## Terms and their Meaning
Before starting the data correlation portion few thinds to understand

'Lac' == 'Latitude of the Center'

'Loc' == 'Longitude of the Center'

'cp' == 'Central Pressure'


'MSWS' == 'Maximum Sustained Wind Speed'

'DLR' == 'Direction of the longest radius of 50kt winds or greater'

'tlr' == 'The longeast radius of 50kt winds or greater'

'tsr' == 'The shortest radius of 50kt winds or greater'

'DLR30' == 'Direction of the longest radius of 30kt winds or greater'

'tlr30' == 'The longeast radius of 30kt winds or greater'

'tsr30' == 'The shortest radius of 30kt winds or greater'
 
 ## Data Correlation Unit

We Done correlation and find relationship inbetween the elements of the sample dataset
 the Correlation was in the following :-
 
 'MSWS - tlr' = 0.83 (highly possitively correlated and having 83% of directly proportion correlation with each other)

'MSWS - tsr' = 0.80 (highly possitively correlated and having 80% of directly proportion correlation with each other)

'MSWS - tlr30' = 0.37 (Not highly possitively correlated but have some 37% of directly  proportion correlation with each other)

'MSWS - tsr30' = 0.40 (Not highly possitively correlated but have some 40% of directly  proportion correlation with each other)

'cp - tlr' = -0.70 (highly negatively correlated and having 70% of inversly  proportion correlation with each other)

'cp - MSWS' = -0.90 (highly negatively correlated and having 90% of inversly  proportion correlation with each other)

'cp - tsr' = -0.67 (highly negatively correlated and having 67% of inversly  proportion correlation with each other)

'cp - tlr30' = -0.41 (Not highly negatively correlated but have some 41% of inversly  proportion correlation with each other)

'cp - tsr30' = -0.43 (Not highly negatively correlated but have some 43% of inversly  proportion correlation with each other)


So this the overall correlation chart of the sample dataset. After checking the relationship between each element let's visualized it.

## Visualization Unit
In Visualization section of the project I use multiple Visualizaition chart to understand more clearly what the correlation is saying?

I use statistically Visualization modules well known as Seaborn and performing various operation among all I use Matplotlib

seaborn :- Seaborn is an amazing visualization library for statistical graphics plotting in Python. It provides beautiful default 
styles and color palettes to make statistical plots more attractive. It is built on the top of matplotlib library and also closely 
integrated to the data structures from pandas.Seaborn aims to make visualization the central part of exploring and understanding data. 
It provides dataset-oriented APIs, so that we can switch between different visual representations for same variables for better 
understanding of dataset.

Matplotlib :- Matplotlib is an amazing visualization library in Python for 2D plots of arrays. Matplotlib is a multi-platform data 
visualization library built on NumPy arrays and designed to work with the broader SciPy stack. It was introduced by John Hunter in the year 2002.

So with the help of Visualiztion we Visualize and express the Quantiative Numeric data into Graphical representation bars. 

In seaborn we use the Lineplot and barplot to visualize the things and atlast we use Vilonplot to understand more clearly.


This all about of data Visualization unit.

## Machine Learning Unit
At the end we perform some machine learning algorithm for the prediction,

So in machine Learning Deployment unit we use scikit Learn Module to perform the ML operations

Scikit Learn :-scikit-learn (formerly scikits.learn and also known as sklearn) is a free software machine learning library 
for the Python programming language.It features various classification, regression and clustering algorithms including 
support-vector machines, random forests, gradient boosting, k-means and DBSCAN, and is designed to interoperate with the 
Python numerical and scientific libraries NumPy and SciPy. Scikit-learn is a NumFOCUS fiscally sponsored project.

With help of sklearn we load Decision tree classifier and train_test_split model from sklearn.tree and sklearn.model_selection
The Train_test_split model is used to divide the data into 4 different categories such are X_train, Y_train and X_test, Y_test
were in general it is used to divide the whole data set into two or three parts train, test and some times vaidation.

After chunks the data with the help of train_test_split model we have make some prediction and for the prediciton we have to first 
train our data and this trained data we have to fit on the Mahine Learning model after then we test it.

So to load the model we use DecisionTreeClassifier, and then we fit the data inside it Train data as well as test data and start making 
prediction with them.

## Prediction Unit
So we perform two type of prediction with the help of model

1. we predict the central pressure of Typhoon by giving the three attribute to ML model which are the following

a) by giving the Latitude of the Center

b) by giving the Longitude of the Center

c) by giving Maximum Sustained wind speed

The Model generates the Prediction as according to training data.

2. We predict the Grade(type of Typhoon) of Typhoon by giving some parameter to the model and parameters are :-

a) by giving the Latitude of the Center

b) by giving the Longitude of the Center

c) by giving Maximum Sustained wind speed

d) by giving the value of tlr30 (to understand tlr30 refer to the Correlation unit)

e)by giving the value of tsr30 (to understand tsr30 refere to the Correlation Unit) 

The Model generates the Prediction as according to training data.

After then I just check the accuracy of my model.

Hence Project is END


Thanking You.
