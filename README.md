# Predict-Customer-Churn-using-PySpark-
Predicting customer churn is a challenging and common problem that data scientists encounter these days. The ability to predict that a particular customer is at a high risk of churning, while there is still time to do something about it, represents a huge additional potential revenue source for every customer-facing business. This solution will be realized with Apache Spark. Apache Spark is a popular distributed data processing engine which provides a stack of libraries including Spark SQL, Spark Streaming, MLlib for machine learning and GraphX for graph processing. For this project, we will focus on the machine learning library MLlib. We will use the Python API for Spark known as PySpark.

# Introduction:
The users stream their favorite songs every day either using the free tier that places advertisements between the songs or using the premium subscription model where they stream music as free but pay a monthly flat rate. The users can upgrade, downgrade and cancel the service at any time. Every time the user interacts with the service like playing songs, logging out or liking a song with a thumbs-up, it generates data. All this data contains the key insights for keeping the users happy and helping the business thrive. It’s our job on the data team to predict which users are at risk to cancel their accounts. If we can accurately identify these users before they leave, our business can offer them discount and incentives, potentially saving our business millions in revenue.

# DATASET DESCPRITION:
•	Use of data from a fictitious music streaming service called Sparkify to try to predict customer churn. 
When working with any type of data it's important to understand the structure of the data and other complexities in the data that may influence a model's predictive power and robustness.

# Data preprocessing:
•	The next step is to investigate missing values. 
•	In theory there should not be any missing values, since most of the data is system generated, but we did that some of the users had missing values for First Name, Surname, Registration date and Gender. 
•	These entries belong to users who didn't log in or register. 
•	These users also didn't have user ids assigned to them, so we drop them altogether.

# Exploratory Data Analysis:
Churn: Once we've done some preliminary analysis, create a column Churn to use as the label for your model. Using the Cancellation Confirmation events to define churn, which happens for both paid and free users. As a bonus task, we can also look into the Downgrade events.

# Feature Engineering:
•	The next step was to generate some additional features and transform existing features into more useable features.
•	The first feature we created is the number of months the customer has been registered on the platform till the end of the observation date — the date before he churned or the 1st of December 2018 for those who didn't churn.

# Modeling:
Spark makes it exceptionally easy to build data pipelines and models, since it's closely modelled on the Sci-kit learn framework. We made use of Random Forest, Gradient Boosting and Linear Support vector machine algorithm to see which model performs best.

# Conclusion:
Using a gradient boosting classifier, I was able to achieve a reasonably accurate model with a recall of 0.83 and precision of 0.77. These are however based on cut-off values of 0.5. By ranking the raw probabilities the company can focus on the top x percent of customers at risk of churning and thereby maximize returns and minimize costs.
