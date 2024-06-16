
# Healthcare Resource Demand Prediction and Patient Segmentation

This Python project utilizes the insurance.csv dataset to analyze resource data and predict resource demand i.e charges and segment patients based on several factors like age, sex, bmi, children, smoker status, and region. The project leverages various machine learning techniques, including K-means clustering, Random Forest, Gradient Boosting, Neural Networks, and Linear Regression to provide insights and improve predictions of resource demand i.e charges. We also used healthcare_dataset.csv to predict the patient health outcome and resource demand but this dataset shows very minimum accuracy.


## Work Flow/ Module BreakDown 
### Data Consumption
1) #### Load Data: 
Import the insurance.csv dataset and healthcare_dataset.csv

2) #### Data Inspection: 
Perform initial explorations to understand the data structure.

### Data Cleaning and Preprocessing
1) #### Handling Missing Values: 
Identify and impute or remove missing values.

2) #### Detecting and Handling Outliers: 
Use IQR scores to detect and filter out outliers from the dataset.

3) #### Categorical Encoding: 
Convert categorical data into numerical format using label encoding.
### Data Analysis
1) #### Exploratory Data Analysis: 
Generate summary statistics and visualizations to identify trends and outliers.

2) #### Correlation Analysis: 
Assess how various features correlate with charges which is our target variable.

#### insurance.csv
![alt text](17.jpeg)

#### healthcare_dataset.csv
![alt text](21.jpeg)





### Patient Segmentation
Patient are segmented based on K-means clustering for both datasets. We first implemented Elbow method and found the number of clusters. Based on the number of clusters patients are segmented in to different categories.

#### insurance.csv
![alt text](10.jpeg)

#### healthcare_data.csv
![alt text](22.jpeg)





### Model Building
1) #### Model Selection: 
Evaluate different models like Random Forest, Gradient Boosting, and Neural Networks, Linear Regression and  choosing the best among them.

2) #### Model Training: 
Train the models using the preprocessed dataset.

3) #### Model Evaluation: 
Use metrics like RMSE , RÂ², f1 score, accuracy, and precision, recall to evaluate model performance.


### Visualization
1) #### Result Visualization: 
Create plots to visualize the accuracy of predictions and the importance of different features.

#### insurance.csv
![alt text](17.jpeg)

#### healthcare_dataset.csv
![alt text](21.jpeg)

### Linear Regression for Resource Demand Prediction

By applying linear regression on the first dataset, we get Mean Absolute Error equals to 0.5737 which is good as the less it is the better the prediction will be. R squared is negative for the second dataset which shows that the data is not fitted well on the regression model. 

![alt text](20.jpeg)

#### healthcare_dataset.csv
![alt text](23.jpeg)


### Linear Regression for Patient health outcome
By applying linear regression on the first dataset, as we keep the charges as target variable as there was not any other appropriate field the MAE is same as above. On the other hand, for the second dataset the R square is negative which tells us that the data is not fitted well on the regression model

#### healthcare_dataset.csv
![alt text](24.jpeg)

## Dataset
This dataset contains information on the relationship between personal attributes (age, gender, BMI, family size, smoking habits), geographic factors, and their impact on medical insurance charges. It can be used to study how these features influence insurance costs and develop predictive models for estimating healthcare expenses.
Age: The insured person's age.

Sex: Gender (male or female) of the insured.

BMI (Body Mass Index): A measure of body fat based on height and weight.

Children: The number of dependents covered.

Smoker: Whether the insured is a smoker (yes or no).

Region: The geographic area of coverage.

Charges: The medical insurance costs incurred by the insured person.

#### insurance.csv
![alt text](1.jpeg)

![alt text](2.jpeg)

![alt text](3.jpeg)

![alt text](4.jpeg)

![alt text](5.jpeg)

In the second dataset each column provides specific information about the patient, their admission, and the healthcare services provided, making this dataset suitable for various data analysis and modeling tasks in the healthcare domain. Here's a brief explanation of each column in the dataset -

Name: This column represents the name of the patient associated with the healthcare record.

Age: The age of the patient at the time of admission, expressed in years.

Gender: Indicates the gender of the patient, either "Male" or "Female."

Blood Type: The patient's blood type, which can be one of the common blood types (e.g., "A+", "O-", etc.).

Medical Condition: This column specifies the primary medical condition or diagnosis associated with the patient, such as "Diabetes," "Hypertension," "Asthma," and more.

Date of Admission: The date on which the patient was admitted to the healthcare facility.

Doctor: The name of the doctor responsible for the patient's care during their admission.

Hospital: Identifies the healthcare facility or hospital where the patient was admitted.

Insurance Provider: This column indicates the patient's insurance provider, which can be one of several options, including "Aetna," "Blue Cross," "Cigna," "UnitedHealthcare," and "Medicare."

Billing Amount: The amount of money billed for the patient's healthcare services during their admission. This is expressed as a floating-point number.

Room Number: The room number where the patient was accommodated during their admission.

Admission Type: Specifies the type of admission, which can be "Emergency," "Elective," or "Urgent," reflecting the circumstances of the admission.

Discharge Date: The date on which the patient was discharged from the healthcare facility, based on the admission date and a random number of days within a realistic range.

Medication: Identifies a medication prescribed or administered to the patient during their admission. Examples include "Aspirin," "Ibuprofen," "Penicillin," "Paracetamol," and "Lipitor."

Test Results: Describes the results of a medical test conducted during the patient's admission. Possible values include "Normal," "Abnormal," or "Inconclusive," indicating the outcome of the test.

#### healthcare_dataset.csv
![alt text](34.jpeg)
![alt text](35.jpeg)
![alt text](36.jpeg)
![alt text](37.jpeg)
![alt text](38.jpeg)
![alt text](39.jpeg)
![alt text](40.jpeg)
![alt text](41.jpeg)



## Methodologies
### Data Preprocessing
1) #### Missing Data Handling: 
There was no missing data in both dataset

2) #### Outlier Detection and Handling: 
Outliers are identified using statistical methods like IQR and handled appropriately to prevent skewing of model predictions but in our case the outliers only existed in the charges which was the target variable and hence we did not remove it.

#### insurance.csv
![alt text](6.jpeg)

![alt text](7.jpeg)

![alt text](8.jpeg)

![alt text](9.jpeg)

#### healthcare_dataset.csv
![alt text](31.jpeg)
![alt text](32.jpeg)
![alt text](33.jpeg)

3) #### Feature Engineering: 
Derivation of new features that might affect charges, such as interaction terms between features.

![alt text](17.jpeg)



 
## Approaches

### Data Cleaning and Preprocessing
#### Approach: 
Robust preprocessing steps including outlier detection, missing data handling, and categorical encoding to prepare the data for modeling.

#### Reason: 
Ensuring data quality is critical for building accurate and reliable predictive models.

### Model Selection and Evaluation
#### Approach: 
Use of multiple machine learning models to predict resource demand i.e charges, with a focus on comparing their performances to select the best model.
#### Reason: 
Different models provide varying degrees of accuracy and are suitable for different types of data distributions and complexities.

### Visualization
#### Graphical Representations: 
Use of scatter plots, bar charts, and line graphs to visually represent the data analysis and results.

#### insurance.csv

![alt text](10.jpeg)
![alt text](18.jpeg)
![alt text](19.jpeg)
![alt text](56.jpeg)
![alt text](17.jpeg)


#### healthcare_dataset.csv
![alt text](25.jpeg)
![alt text](26.jpeg)
![alt text](27.jpeg)
![alt text](28.jpeg)
![alt text](29.jpeg)
![alt text](30.jpeg)


## Results
#### Model Comparison: 
We are using 3 classifier models which are Random Forest, Gradient Boosing, Neural Network. Before scaling random forest provides best accuracy among these 3 which is 83% and gradient boosting 81% and Neural Network 66%. After scaling only Neural Network accuracy increased to 85% as scaling only improves Neural Network model.

#### insurance.csv
![alt text](11.jpeg)
![alt text](12.jpeg)
![alt text](13.jpeg)
![alt text](14.jpeg)
![alt text](15.jpeg)
![alt text](16.jpeg)

For the second dataset, we did the same procedure and the accuracy with random forest before scaling was 34% for patient health outcome and 10% for resource demand prediction. For gradient boosting we get 36% accuracy for patient health outcome and 10% for resource demand prediction. Using Neural Network accuracy was 32% for patient health outcome and 9% for resource demand prediction. After scaling all were same but Neural Network gave 33% for patient health outcome and 11% for resource demand prediction.  

#### healtcare_dataset.csv
![alt text](42.jpeg)
![alt text](43.jpeg)
![alt text](44.jpeg)
![alt text](45.jpeg)
![alt text](46.jpeg)
![alt text](47.jpeg)
![alt text](48.jpeg)
![alt text](49.jpeg)
![alt text](50.jpeg)
![alt text](51.jpeg)
![alt text](52.jpeg)
![alt text](53.jpeg)
#### Insights Derived: 
Important features influencing resource demand were identified, such as smoker status and age, which were significant predictors of higher charges.




## Unique Approaches and Comparison with Current Available Methods

#### Unique Approaches: 
Implementation of advanced machine learning algorithms like Gradient Boosting and Neural Networks. For the second dataset to improve the accuracy from 10% we did data preprocessing to handle imbalance data, we use a technique called smote and the accuracy increased to 17% for Random forest healthcare_dataset. We also did hyperparameter tuning on resampled Random Forest but the accuracy remain the same.
![alt text](54.jpeg)

After hyperparameter tuning
![alt text](55.jpeg)


#### Comparison: 
This project's approaches are compared with traditional statistical methods, showcasing significant improvements in prediction accuracy and insights generation.


## Challenges Faced
#### Data Quality Issues: 
The first dataset has no field related to predicting patient health outcome so we used charges as target variable for the patient health outcome prediction. For the second dataset the data was distributed very badly and there was very minimal correlation of columns with the target variables hence it was giving very low accuracy for both predicting the resource demand and patient health outcome which is 17% and 35% which is not helpful. 

#### Model Selection and Tuning: 
The challenge of selecting and tuning the right model to balance accuracy and computational efficiency.


## References
https://www.kaggle.com/datasets/prasad22/healthcare-dataset

https://www.kaggle.com/datasets/willianoliveiragibin/healthcare-insurance

https://youtu.be/8klqIM9UvAc?si=xgzTk2aAjy65mDpD

https://youtu.be/iNlZ3IU5Ffw?si=gyV6o_4_vWwfLhOC

https://youtu.be/EItlUEPCIzM?si=PnpsusaKTwca753R

https://youtu.be/rzR_cKnkD18?si=KRpApCb4RBenfgmX

https://youtu.be/pYVScuY-GPk?si=j5aBhaUPZyBxOtSy

https://youtu.be/7eh4d6sabA0?si=OiZkFh8ptq1N8vYX

https://youtu.be/x08AN87G0mg?si=udjntdyk-ayy-5US

https://youtu.be/UoYO-MjqiVQ?si=5JP0Vi-bRlK6Ts0c

https://youtu.be/Xsp6rxPJ0Nk?si=pGB0hfxIfOdaXkyI

