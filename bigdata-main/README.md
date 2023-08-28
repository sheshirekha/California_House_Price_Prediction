# California House Price Prediction
# Big-Data-Group-8
This project is a part of the ITCS 6100 - Big Data Analytics for Competitive Advantage course from the University of North Carolina at Charlotte.
# Deliverable 1

## Team Members
* Kousik Varma Dandu
* Dinesh Reddy Chinnamallaiahgari
* Reddy Sai Krishna Sanda
* Sheshi Rekha Guntuka

## Communication plan
Zoom meetings, Atkins Library, Slack. 
We plan to communicate 3 times per week through zoom or in-person meetings based on the availability of the group members. The meetings will last for 2-3 hrs each. 

## Dataset
Canvas-sample-housing.csv: In this dataset, we will find data about the characteristics associated with a particular housing price. We can use this dataset to predict housing prices. With this dataset, use the Numeric prediction model type. The link to the dataset can be found here. https://www.kaggle.com/datasets/camnugent/california-housing-prices

## Selection of Data
California Housing Prices Data

https://www.kaggle.com/datasets/camnugent/california-housing-prices

Description:  ```California housing prices Dataset```

Resource type: 
```S3 Bucket```

Amazon Resource Name (ARN): 
```arn:aws:s3:::housee```

AWS Region: 
```US East (N. Virginia) us-east-1```

## Business Problem or Opportunity, Domain Knowledge 
As the population increases day-by-day the demand for houses increases side by side. Predicting housing prices based on the characteristics of a locality is the task at hand. During the COVID-19 pandemic era, the demand for houses has increased rapidly. During this process, we should identify the most significant features in the California Housing Dataset. The real Estate domain is the most earning field in the world. Most realtors may not be able to provide a good house to the customers. We will be using machine learning techniques to predict California housing prices.

## Research Objectives and Questions
We are trying to predict the house price in the California area by using a few machine learning techniques and representing the data visually by using different types of graphs. This helps people to find houses according to their flexibility. 

What is the actual value of the price and predicted value of the price of the house?

Find the location where the highest total rooms are located?  

What is the median house value in accordance with median house age in different ocean proximities? 

How median house value can be compared with median income?

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------

# Deliverable 2

## Data Understanding

a) Exploratory Data Analysis

Through AWS Sagemaker, exploratory data analysis was carried out. The related file can be seen here.: [Exploratory Data Analysis](https://github.com/saikrishnasanda/bigdata/blob/main/Project%20Files/AWS%20Sagemaker/Exploratory%20Data%20Analysis.ipynb)

b) Dashboard

AWS Quicksight was used to construct dashboard instances, which were then displayed as PDF documents. The PDF file can be found below. These dashboards are also examined in the Results section as a tool for addressing the goals and issues of the research.

[Click Here For Dashboards](https://github.com/saikrishnasanda/bigdata/blob/main/Project%20Files/AWS%20Quicksight/AWS%20Quicksight.pdf)



## Data Preparation
At every stage of the project, data preparation was done, including an initial study of the dataset structures listed in the Open Dataset Registry. Data preparation tasks include reading column data correctly based on the tool being used, taking into account anomalous data, erroneous values, manipulating the data, and more.  We found some null values in total_bed_rooms column in the dataset and filled that with the median of the values from the same column.

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------

# Deliverable 3  

## Analytics, Machine Learning
Using Amazon SageMaker, we performed Machine learning and analytics for predicting the results. We used different types of barcharts, scatter plots, Heatmaps to view the results. The dataset was train and tested with random forest and CatBoost algorithms and printed the root mean square(RMSE) and R-square. These two gave the best results. So, we combined the two models to get final prediction. 

[Click Here to View the results](https://github.com/saikrishnasanda/bigdata/blob/main/Project%20Files/AWS%20Sagemaker/house%20price%20prediction.ipynb)

## Evaluation and Optimization
Performing machine learning on AWS will boosts the running computations. The machine learning model like Random forest which helps to find the predicted median house value in the data, along with random forest we used Catboost which adds best solutions with out parameter tuning that reduces time spent on parameter tuning because CatBoost provides effective results with default parameters. Using Scatter plot for visualizing the predicted house values, based on the positive correlations of the plot helps the data scientist to analyse the stats for better understanding. By optimizing the models for the best fit, a scatter chat can help in setting up models

## Results
### What is the actual value of the price and predicted value of the price of the house?
Here the main aim to display the results by showing the comparision between the actual median_house_price vs predicted median_house_price. The scatter plot explains all the comparison between the values. The results are displayed below.

The nodes represents in the scatter plot are in the high positive corelation with 85 percentage of root squared values where the plots are present in one cluster displays the best accuracy of the median_house_price.
![alt text](https://github.com/saikrishnasanda/bigdata/blob/main/Project%20Files/Results/prediction.png)


### Find the location where the highest total rooms are located?
Using this visualization box we can understand at what area of location have the highest number of total rooms. We can see from below bar chart that "<1H Ocean" from ocean proximity column (location of houses located with respect to ocean) area has the highest number of total rooms. 

There are a total number of 9,034 bedrooms in total in that area. So we can make assumption that this area contains the big houses or many houses.
![alt text](https://github.com/saikrishnasanda/bigdata/blob/main/Project%20Files/Results/Highest%20rooms%20located.jpg)

### What is the median house value in accordance with median house age in different ocean proximities?
Presenting the visualization for the house value against the  house age in all different ocean proximity locations. This helps us to understand how old the house age is and it tell the house value and it helps people to understand wheather the house value is suitable for that particular house age. Many people will see in a particular way that how old the house is and the value will be increased or decreased according to the market values. 

We can see that the median value of house in Inland location for the house age of 2 is 164,400. Simillarly we can observe the different value of median houses at different locations for different house ages.

![alt text](https://github.com/saikrishnasanda/bigdata/blob/main/Project%20Files/Results/Median%20House%20price%20vs%20Median%20house%20age.jpg)

### How median house value can be compared with median income?
We can compare the values of median house value and median income using scatter plot. This gives the easy understanding about the what level of income people are purchasing the what value of median house value.

Suppose, for example we can see the people median income with 0 to 5 million are purchasing the house value worth range between 75,000 to 200,000. We can understand like this many people with that income range are looking to buy houses with in the above mentioned house value range.

![alt text](https://github.com/saikrishnasanda/bigdata/blob/main/Project%20Files/Results/Analysis%20between%20median%20house%20value%20and%20median%20income.png)

## Future Work, Comments

### What was unique about the data? Did you have to deal with imbalance? What data cleaning did you do? Outlier treatment? Imputation?
The median income which provides individual income of the location that can help to suggest the quality of the house according to income. 
Resampling with different ratios of the data according to particular location for better outputs.
Filling the empty values in columns Total_bedrooms, Total_rooms with mean values of the respective columns to full fill the data that missing.
Finding the outlier of the column median_house_price by Z-score method which gives outliers of the column and equalizing with the mean of the column to fit the data.
Filling the empty values with mean of the respective column and removing the unwanted data from the data. The duplicate values will conflict while running the model.

### Did you create any new additional features / variables?
The new column bed_per_room that added by dividing total_bed_rooms/total_rooms which gives the individual bed rooms per house so that will helps us to get find the ratio of the bed rooms present is the total rooms.

### What was the process you used for evaluation?  What was the best result?
Finding the best solutions for the know data is challenging, for evaluation of the model comes under the accuracy provided by the model. The results that evaluated helps to find the good affordable house in specific location.

### Is there Bias in your work? What were the problems you faced? How did you solve them?
No, We didn’t find any bias among ourselves.  We helped each other while doing this project. The main problem is working with AWS for developing machine learning with tools its challenging to work but it helps us a lot by providing all required tools at one place and provides good performance. Getting access for the tool and the credits pays more while developing a model in aws for using tools.

### What future work would you like to do? 
Gathering more data source and performing better models to evaluate good results that users can get. Deploying this model into user interface so that it can help users to find best location with good houses that they can afford.

## Presentation Video
https://github.com/saikrishnasanda/bigdata/blob/main/Project%20Files/videos/Big%20data%20project%20recording.mp4
[Presentation Video](https://github.com/saikrishnasanda/bigdata/blob/main/Project%20Files/videos/Big%20data%20project%20recording.mp4)
