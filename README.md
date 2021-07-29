# Capstone project in the Udacity Data Scientist nanodegree program (Project No.4) 

### Project Description
The imaginary start-up company Sparkify offers music streaming service to users in the USA. Many users stream their favourite songs to our service every day either using the free tier that places advertisements between the songs, or using the premium subscription model, where they stream the music for free but pay a monthly flat rate. Users can upgrade, downgrade, or cancel their service at any time. So, it is crucial to make sure the users love the service. Every time a user interacts with the service such as playing songs, logging out, liking a song with a thumps-up, hearing an ad, or downgrading their service, it generates data. All this data contains key insides for keeping the users happy and helping Sparkify’s business thrive.  It is our job on the data team to predict which users are at risk to churn either downgrade from premium to free tier or cancelling their service altogether.  If we can accurately identify these users before they leave, Sparkify can offer them discounts and incentives, potentially saving the business millions in revenue. 

Sparkify keeps a Log file with 18 fields for every user interaction (e.g., userId, name of song played, length of song played, name of artist). Soon the data volume of the log file has exceeded the available memory space on standard desktop computers, and the company has opted for using the distributed file system Apache Spark™. Udacity™ provides the full dataset with 12GB on AWS™ S3, and you can run a Spark cluster on the cloud using AWS or IBM™ Cloud to analyse the large amount of data. 

### Blogpot 

In this article on medium.com  I describe the project in greater detail with a focus on technical questions.
https://peterschuld.medium.com/sparkify-project-45d8941fa995

### Project Steps
- Load data into Spark
- Explore and Clean Data
- Create Features
- Build Models 
- Predict Churn
 
In this project, we use Spark SQL and Spark Dataframes to analyse a small subset of the user data on Sparkify's Log file. We use PySpark's Machine Learning Library (MLlib) to predict churn of Sparkify's users. After examining the subset of the Log file, we identify 37 features in the user data that can help to detect pending churn. We create a list of features for every user in the subset to train ML models, and we compare the performance of four MLlib classification models for churn prediction (Logistic regression, Random Forest classifier, Gradient-boosted tree classifier, Linear Support Vector Machine). 

We determine our winning model, a tuned version of the Logistic Regression model. Since the churned users are a small subset, we use F1 score as the metric to optimize. We use cross-validation to improve usage of the available data, and because it gives us more information about the algorithm performance. 


### Results
The winning model for churn prediction is a tuned Logistic Regression Model that achieves an Accuracy of 0.8 and a F1 score of 0.73 on the validation set. 

for comparison 

Accuracy / F1-Score on the validation set
- 0.80 / 0.73	Best Logistic Regression Model
- 0.73 / 0.69 	Random Forest classifier		 
- 0.73 / 0.71	Gradient-boosted Tree classifier		
- 0.73 / 0.69	Linear Support Vector Machine 		

Our churn prediction model should help Sparkify to identify users for special promotions or other measures to prevent them from cancelling the service. However, the model should avoid falsely classifying loyal users as vulnerable to churn, because offering discounts or other promotions is expensive and should be targeted to users we would otherwise lose as customers.    

### Motivation
Predicting churn rates is a challenging and common problem that data scientists and analysts regularly encounter in any customer-facing business. Additionally, the ability to efficiently manipulate large datasets with Spark is one of the highest-demand skills in the field of data. 

Essential Skills
- Load large datasets into Spark and manipulate them using Spark SQL and Spark Dataframes
- Use the machine learning APIs within Spark ML to build and tune models
- Integrate the skills learned in the Spark course and the Data Scientist Nanodegree program


### All the project code is contained in the Jupyter notebook: ###
Sparkify_small_PeterSchuld 

### All the project data is contained in the json-file: ###
mini_sparkify_event_data.json

#### What do you need to run the code
- Spark v2.4.3
- Python 3.7

#### The following packages (libraries) need to be installed #### 
- PySpark's Machine Learning Library (MLlib)
- Pyspark SQL Module
- Pandas, NumPy, matplotlib, seaborn

### Data Source ####
The data is provided by Udacity.

### Acknowledgements
I would like to express my sincere gratitude to Udacity for providing the data and to IBM Watson for cooperating with Udacity and providing free cloud services essential for this project.  

 

![grafik](https://user-images.githubusercontent.com/59873708/127336175-2dfef549-206b-48f4-9327-482a62f764cb.png)

![grafik](https://user-images.githubusercontent.com/59873708/127336861-d1829fa4-2a2e-4d33-b12f-08f4fcf000f1.png)

