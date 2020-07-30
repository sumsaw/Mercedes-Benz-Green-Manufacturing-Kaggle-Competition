# Mercedes-Benz-Green-Manufacturing-Kaggle-Competition
My process of trying out ensemble and stacking methodology

Kaggle note book : https://www.kaggle.com/sumeetsawant/mercedes-green-manufacturing-ensemble-and-stacking <br>
Medium post : https://medium.com/p/ba55ad553c75/edit <br>

As part of my continuing data analysis learning journey I thought of trying out past completed Kaggle competition in order to test my skills and knowledge so far . While going through the datasets I came across this Mercedes Green Manufacturing Kaggle competition conducted in sometime in 2017.
Coming from a automotive domain I though this could be a good dataset to apply by data analysis skills. On reading the competition description I could relate to this problem even more closely. The competition is asking, given a set of anonymous categorical and binary variable can you predict the time which the car will take to complete its testing.
As a engineer from this domain I can completely see the importance of such a model. I know how time consuming vehicle testing can be. The process consists of building a prototype car, instrumenting it and then running the required tests. The major bottle neck in car testing occurs during instrumentation phase which requires to de-assemble the car, fit the required recording instruments and then re-assemble the car.
Another bottle neck during testing is also the availability of testing equipment such as drive cells required to run the test.<br>

All this factors results in man-hours wastage and a increased development time in the vehicle development program. This adds unplanned over-head cost to the company. Hence a model which can predict how much time a car will take to complete a test will help better plan and manage cost and resources.
Here is a link to the competition page . <br>

The evaluation metric for this competition is R-square which is a statistical measure that represents the proportion of the variance for a dependent variable that’s
explained by an independent variable or variables in a regression model. __The winner of this competition 3 years back has a R-square value of 0.555__. 
My aim here was to come as much close to the above value in a week’s time.

# Running the file 
- The above notebook can be run by using the copy and edit option in my Kaggle notebook -https://www.kaggle.com/sumeetsawant/mercedes-green-manufacturing-ensemble-and-stacking

# Description of the dataset 

As with most Kaggle competition this dataset has its column names removed so cant discuss much on it .We needed to predict the time it will take to complete the test given a set 
of catergorical and binary data.

# Challenges Encountered 

- Time Constraint
Fist was the time constraint which I imposed on myself ( max a week timeframe ) <br>

- Curse of dimensionality 
The shape ( row ,columns) of the dataset where (4209,377). There where 8 categorical columns and 1 dependent variable and other where binary columns with just 1 or 0 as its values .
Even the 8 categorical columns had lot of unique values so using one hot encoding for categorical variables was going to be tough with so little data provided for training.

- Anonymous Data 
Difficult to create meaningful features in such a case. 

# Key Insights gained 
- I was able to try out stacking and ensemble of various linear and tree based models 
-Taking care of data-leakage so as to have tight control over CV as the data points provided where less . Was able to get close Public and Private LB scores 
-Successfully handle curse of dimensionality using Label encoder and spliting models who take only catergorical featues and who take only Binary features . 

# Final Submission 
My final submission score was 0.5440 vs 0.555 for the compition winner which I feel was a decent attempt taking into consideration my aim here was to gain experience points in generating a Kaggle working model with
a certain tight time constraints 

# Additional Improvements 
- We can try running the model with Target Encoding instead of Label encoding for catergorical variable .
- We Can try LGBM regressor . 
- More Feature Engineering 
