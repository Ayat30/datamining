
churn prediction customer

Churn Prediction for Telephone Customers Classification

Abstract:
            Customer churn is a major problem and one of the most important concerns for large companies. Due to the direct effect on the revenues of the companies, especially in the telecom field, companies are seeking to develop means to predict potential customer to churn. Therefore, finding factors that increase customer churn is important to take necessary actions to reduce this churn. The main contribution of our work is to develop a churn prediction model which assists telecom operators to predict customers who are most likely subject to churn. The model developed in this work uses machine learning techniques on Data set and builds a new way of features’ engineering and selection. In order to measure the performance of the model .
Introduction:
    Consumers are considered as main significant assets in any type of sector or industry because they are recognized as major source for profit .The telecommunications sector has become one of the main industries in developed countries. For Telco companies it is key to attract new customers and at the same time avoid contract terminations (=churn) to grow their revenue generating base. Looking at churn, different reasons trigger customers to terminate their contracts, for example better price offers, more interesting packages, bad service experiences or change of customers’ personal situations.
The technical progress and the increasing number of operators raised the level of competition .Companies are working hard to survive in this competitive market depending on multiple strategies. Three main strategies have been proposed to generate more revenues: (1) acquire new customers, (2) upsell the existing customers, and (3) increase the retention period of customers. However, comparing these strategies taking the value of return on investment (RoI) of each into account has shown that the third strategy is the most profitable strategy, proves that retaining an existing customer costs much lower than acquiring a new one, in addition to being considered much easier than the upselling strategy. To apply the third strategy, companies have to decrease the potential of customer’s churn, known as “the customer movement from one provider to another”.
Customers’ churn is a considerable concern in service sectors with high competitive services. On the other hand, predicting the customers who are likely to leave the company will represent potentially large additional revenue source if it is done in the early phase .
To reduce customer churn, telecom companies need to predict which customers are at high risk of churn:
    Many research confirmed that machine learning technology is highly efficient to predict this situation. This technique is applied through learning from previous data.
The model also was evaluated using a new dataset and the impact of this system to the decision to churn was tested. Churn analytics provides valuable capabilities to predict customer churn and also define the underlying reasons that drive it. The churn metric is mostly shown as the percentage of customers that cancel a product or service within a given period (mostly months). The Churn analytics  model gave good results and was deployed to production.
Customers  play  a  vital  role  in  telecom  industry.  Nowadays,  customers  do  not  wait  to  change  the company  if  they  are not  satisfied  with their  services  and hence  to  retain  the  customers  in  the  telecom  industry  companies  must  concentrate  on  identifying  the  reasons  behind  consumer  churn  so  that  they  could  make appropriate  changes  in  the  industry.  The  main  intention  of  the  research  is  to  study  about  customer  churn prediction in telecom using machine learning in big data platform. Machine learning approaches play a vital role in  predicting the  consumer  churn.  This research makes use Machine learning approaches for  predicting  the  consumer churn in  the telecom  industry.
Objectives:
I will explore the data and try to answer some questions like:
What's the % of Churn Customers and customers that keep in with the active services?
Is there any patterns in Churn Customers based on the gender?
Is there any patterns/preference in Churn Customers based on the type of service provided?
What's the most profitable service types?
Which features and services are most profitable?
Many more questions that will arise during the analysis 

The data set includes information about:
Customers who left within the last month – the column is called Churn
Services that each customer has signed up for – phone, multiple lines, internet, online security, online backup, device protection, tech support, and streaming TV and movies
Customer account information - how long they’ve been a customer, contract, payment method, paperless billing, monthly charges, and total charges
Demographic info about customers – gender, age range, and if they have partners and dependents

a sample data set is build and performance of different model types is compared. In steps below:
Step 1: Problem Definition
Step 2: Data Collection
Step 3: Exploratory Data Analysis (EDA)
Step 4: Feature Engineering
Step 5: Train/Test Split
Step 6: Model Evaluation Metrics Definition
Step 7: Model Selection, Training, Prediction and Assessment

Step 1: Problem Definition
          Based on the introduction the key challenge is to predict if an individual customer will churn or not. To accomplish that, machine learning models are trained based on 80% of the sample data. The remaining 20% are used to apply the trained models and assess their predictive power with regards to “churn / not churn”. A side question will be, which features actually drive customer churn. That information can be used to identify customer “pain points” and resolve them by providing goodies to make customers stay.
To compare models and select the best for this task, the accuracy is measured. Based on other characteristics of the data, for example the balance between classes (number of “churners” vs. “non-churners” in data set) .


Step 2: Data Collection
          The data set for this classification problem in link: (),is started with imports of some basic libraries that are needed throughout the case. This includes Pandas and Numpy for data handling and processing as well as Matplotlib and Seaborn for visualization.
Step 3: Exploratory Data Analysis
          After data collection, several steps are carried out to explore the data. Goal of this step is to get an understanding of the data structure, conduct initial preprocessing, clean the data, identify patterns and inconsistencies in the data (i.e. outliers, missing values) and build and validate hypotheses..
Understanding
         The goals of this step are to get a general understanding for the data set, check domain knowledge and get first ideas on topics to investigate. In this step some standard Pandas functions are used.
Meaning of Features
           By inspecting the columns and their unique values, a general understanding about the features can be build. The features can also be clustered into different categories:
Classification labels:
Churn — Whether the customer churned or not (Yes or No)
Customer services booked:
Phone Service — Whether the customer has a phone service (Yes, No)
Multiple Lines — Whether the customer has multiple lines (Yes, No, No phone service)
Internet Service — Customer’s internet service provider (DSL, Fiber optic, No)
Online Security — Whether the customer has online security (Yes, No, No internet service)
Online Backup — Whether the customer has online backup (Yes, No, No internet service)
Device Protection — Whether the customer has device protection (Yes, No, No internet service)
Tech Support — Whether the customer has tech support (Yes, No, No internet service)
Streaming TV — Whether the customer has streaming TV (Yes, No, No internet service)
Streaming Movies — Whether the customer has streaming movies (Yes, No, No internet service)
Customer account information:
Tenure — Number of months the customer has stayed with the company
Contract — The contract term of the customer (Month-to-month, One year, Two year)
Paperless Billing — Whether the customer has paperless billing (Yes, No)
Payment Method — The customer’s payment method (Electronic check, Mailed check, Bank transfer (automatic), Credit card (automatic))
Monthly Charges — The amount charged to the customer monthly
Total Charges — The total amount charged to the customer
Customers demographic info:
Customer ID — Customer ID
Gender — Whether the customer is a male or a female
Partner — Whether the customer has a partner or not (Yes, No)
Hypothesis Building:
Looking at the features included in data and connecting them to their potential influence on customer churn, the following hypotheses can be made:
The longer the contract duration the less likely it is that the customer will churn as he/she is less frequently confronted with the termination/prolongation decision and potentially values contracts with reduced effort.
Customers are willing to cancel simple contracts with few associated product components quicker and more often than complexer product bundles — for bundles customers value the reduced administrative complexity. 
     They might also be hesitant to cancel a contract, when they depend on the                                            additional service components (e.g. security packages).
Customers with spouses and children might churn less to keep the services running for their family.
Tenure, contract duration terms and number of additional services are assumed to be among the most important drivers of churn.
More expensive contracts lead to increased churn as the chances to save money by changing providers might be higher.
Feature Engineering Actions:
          Based on the data types and the values, following actions are defined to preprocess/engineer the features for machine readibility and further analysis:
Columns removed
CustomerID: not relevant
Label encoding The following features are categorical and each take on 2 values (mostly yes/no) — therefore are transformed to binary integers
gender
Partner
Churn
PhoneService
PaperlessBilling
One-Hot Encoding The following features are categorical, yet not ordinal (no ranking) but take on more than 2 values. For each value, a new variable is created with a binary integer indicating if the value occured in a data entry or not (1 or 0).
MultipleLines
InternetService
OnlineSecurity
OnlineBackup
DeviceProtection
TechSupport
StreamingTV
StreamingMovies
Contract
PaymentMethod
Min-Max Scaling Values of numerical features are rescaled between a range of 0 and 1. Min-max scaler is the standard approach for scaling. For normally distributed features standard scaler could be used, which scales values around a mean of 0 and a standard deviation of 1. For simplicity we use min-max scaler for all numerical features.
tenure
TotalCharges
MonthlyCharges

Step 4: Feature Engineering
          In feature engineering , a new feature is generated from extisting features and a correlation analysis is conducted after all features have been transformed to numerical.
Step 5: Train-Test-Split
          For conduction of model training and testing steps, the data set is split into 80% training data and 20% test data. The “Churn” column is defined as the class (the “y”), the remaining columns as the features (the “X”).
Step 6: Model Evaluation Metrics
          For performance assessment of the chosen models, various metrics are used:
       Accuracy score: Shows the overall accuracy of the model for training set and test set.
Step 7: Model Selection, Training, Prediction and Assessment
          In the beginning we will test out several models and measure their performance by several metrics. Those models will be optimized later .The models used include:
K Nearest Neighbors — fast, simple and instance-based.
Support Vector Machines — slower but accurate model used here in the non-linear form.


Summary:
Model Summary:
            Looking at model results, the best accuracy on the test set is achieved by the …….. with ………. Given the high imbalance of the data towards non-churners.
Hypotheses Check:
         Looking at the evaluation results ,the hypotheses can be directionally supported or refused:
Contract duration: Contract duration month-to-month is the second biggest driver of churn → supported
Number of additional services: This feature does not rank among the top features → refused
Partners and children: Having children ranks as the fourth feature that drives not churning, but strength is relatively low → partially supported
Tenure: High tenure ranks as the strongest factor for not churning and the strongest feature overall.. → supported
Monthly payment: Total payments, which is the product of tenure and monthly payment ranks as the strongest factor for churn. Indirectly, high monthly payments lead to churn. However, tenure is the highest driver of not churning → refused
Outlook:
           Telcos typically have much more data available that could be included in the analysis, like extended customer and transaction data and operational data around network services provided. Also they typically have much larger amounts of churn/non-churn events . With those, could be properly trained to detect more complex patterns in data and achieve higher accuracies. A high accuracy is needed to be able to identify promising customer cases where churn can be avoided as, eventually, the customer returns protected need to outweigh the costs of related retention campaigns.
