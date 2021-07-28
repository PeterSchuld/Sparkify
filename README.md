# Capstone project in the Udacity Data Scientist nanodegree program (Project No.4) 
by Peter Hermann Schuld

### Project Description
The imaginary start-up company Sparkify offers music streaming service to many users in the USA. Sparkify keeps a Log file with 18 fields for every user interaction (e.g., userId, name of song played, length of song played, name of artist). Soon the data volume of the log file has exceeded the available memory space on standard desktop computers, and the company has opted for using the distributed file system Apache Spark. Udacity provides the full dataset with 12GB on AWS S3, and you can run a Spark cluster on the cloud using AWS or IBM Cloud to analyse the large amount of data. 

In this project, we use Spark SQL and Spark Dataframes to analyse a small subset of the user data on Sparkify's Log file. We use PySpark's Machine Learning Library (MLlib) to predict churn of Sparkify's users. After examining the subset of the Log file, we identify features in the user data that can help to identify pending churn. We create a list of features for every user in the subset to train ML models, and we compare the performance of four MLlib classification models for churn prediction (Logistic regression, Random Forest classifier, Gradient-boosted tree classifier, Linear Support Vector Machine). We determine our winning model Gradient-boosted tree classifier based on test accuracy and F-score results on the validation set. However, a tuned version of the Logistic Regression model performs almost as good as the winning model, and it needs much less time to train compared to the Gradient-boosted tree model. Since the churned users are a small subset, we use F1 score as the metric to optimize. We use cross-validation to improve usage of the available data, and because it gives us more information about the algorithm performance. The Gradient-boosted tree model achieves a F1 score of 0.71 on the validation set, and the tuned Logistic Regression Model achieves a F1 score of 0.70 . In comparisson, the Random Forest classifier and Linear Support Vector Machine models achieve F1 scores of 0.67 and 0.69, respectively. 

Our churn prediction model should help Sparkify to identify users for special promotions or other measures to prevent them from cancelling the service. However, the model should avoid falsely classifying loyal users as vulnerable to churn, because offering discounts or other promotions is expensive and should be targeted to users we would otherwise loose as customers.    

### Motivation
Predicting churn rates is a challenging and common problem that data scientists and analysts regularly encounter in any customer-facing business. Additionally, the ability to efficiently manipulate large datasets with Spark is one of the highest-demand skills in the field of data. 

Essential Skills
- Load large datasets into Spark and manipulate them using Spark SQL and Spark Dataframes
- Use the machine learning APIs within Spark ML to build and tune models
- Integrate the skills learned in the Spark course and the Data Scientist Nanodegree program



#### What do you need to run the code
- Spark v2.4.3
- Python 3.7

#### The following packages (libraries) need to be installed #### 
- PySpark's Machine Learning Library (MLlib)
- Pyspark SQL Module
- Pandas, NumPy, matplotlib, seaborn

### Data Source ####
The data is provided by Udacity.

mini_sparkify_event_data.json





