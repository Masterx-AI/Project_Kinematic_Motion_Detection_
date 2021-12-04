# AI/ML Project - Breast Cancer Diagnosis

<p align="center"><img src="https://user-images.githubusercontent.com/54996245/144494628-74d4abb9-9f26-4c12-b499-f6fa79a56864.jpg" style="width: 1000px;"/></p>

### Description:

Smartphones are getting intelligent day by day to assist Human's to aid in their day to day activites. A new feature has emerged popular in the fitness comunity that keeps an account of one's daily footsteps. 

More advanced versions include differentiating between detecting the difference between walking & run. This is achieved with the help of Sensors. Several such Sensorory data is recorded with IOS device & labelled as walking or running as 0 or 1. 

Currently, the dataset contains a single file which represents 88588 sensor data samples collected from accelerometer and gyroscope from iPhone 5c in 10 seconds interval and ~5.4/second frequency. This data is represented by following columns (each column contains sensor data for one of the sensor's axes):

* acceleration_x
* acceleration_y
* acceleration_z
* gyro_x
* gyro_y
* gyro_z

There is an activity type represented by "activity" column which acts as label and reflects following activities:
* "0": walking
* "1": running

Apart of that, the dataset contains "wrist" column which represents the wrist where the device was placed to collect a sample on:
* "0": left wrist
* "1": right wrist

Additionally, the dataset contains "date", "time" and "username" columns which provide information about the exact date, time and user which collected these measurements.

Can you build a strong classifier model to detect these so that it can be incorporated in the IOS device?

### Acknowledgements:
This dataset complements https://github.com/vmalyi/run-or-walk project which aims to detect whether the person is running or walking based on deep neural network and sensor data collected from iOS device.

This dataset has been accumulated with help of "Data Collection" iOS app specially developed for this purpose: https://github.com/vmalyi/run-or-walk/tree/master/ios_app_data_collection.

### Objective:
- Understand the Dataset & cleanup (if required).
- Build classification model to predict the type of Kinematic Motion.
- Also fine-tune the hyperparameters & compare the evaluation metrics of vaious classification algorithms.

### Stractegic Plan of Action:
**We aim to solve the problem statement by creating a plan of action, Here are some of the necessary steps:**
1. Data Exploration
2. Exploratory Data Analysis (EDA)
3. Data Pre-processing
4. Data Manipulation
5. Feature Selection/Extraction
6. Predictive Modelling
7. Project Outcomes & Conclusion

### Some Visuals of the Project:

**1. Target Variable Distribution**
  
<p align="left"><img src="https://user-images.githubusercontent.com/54996245/144722371-0980896b-554a-4bdb-98d7-310461066928.png" /></p>

**2. Categorical Feature-set Distribution**

![image](https://user-images.githubusercontent.com/54996245/144722377-ad089451-3988-4482-8bc0-8c1a1bba2f3d.png)

**3. Numerical Feature-set Distribution**

![image](https://user-images.githubusercontent.com/54996245/144722411-af1fdabc-a9fc-45bc-9aa3-61cddd642bbf.png)
![image](https://user-images.githubusercontent.com/54996245/144722415-e09f9c8a-d46c-4c3e-a2c4-f61807c59a4f.png)

**4. Relationship between the Feature-set**

![image](https://user-images.githubusercontent.com/54996245/144722420-7a5aee36-dc35-4e5d-891c-c7ac09749152.png)

**5. Data Retention after preforming preprocessing step**

![image](https://user-images.githubusercontent.com/54996245/144722429-6c303087-051e-4a2e-a612-b8a8c5009784.png)

**6. Correlation plot for features**

![image](https://user-images.githubusercontent.com/54996245/144722435-51ca59ea-08db-45f0-8c55-d5b7893b8ea2.png)

**7. VIF & RFE Scores & PCA Decomposition**
  
![image](https://user-images.githubusercontent.com/54996245/144495198-230994ed-c7c8-4843-9c7a-f77f2e7f374c.png)
![image](https://user-images.githubusercontent.com/54996245/144722448-cae84032-9e51-430b-bddf-560252b7ddee.png)
<!--![image](https://user-images.githubusercontent.com/54996245/144495291-7eb061b9-e3a7-42e5-873f-cb942a36bdd9.png)-->

**8. ROC Plots**

![image](https://user-images.githubusercontent.com/54996245/144722468-8c811595-f9ca-46e0-bde3-ad20d4048ac4.png)

**9. Tree Plot & Feature Importance in Random Forest
  
![image](https://user-images.githubusercontent.com/54996245/144722471-ed5c0470-0d10-4825-8e75-31b0d47bda7c.png)
![image](https://user-images.githubusercontent.com/54996245/144722478-f6b936ff-8992-4e46-a8b0-3ee75a245b8a.png)


**10. ML Algorithm's Scores for the Dataset**
  
![image](https://user-images.githubusercontent.com/54996245/144495382-21862d14-a6cb-4b90-a32f-2a0d29b78c1c.png)
![image](https://user-images.githubusercontent.com/54996245/144495393-16c7bee4-7cc3-4b8b-a48f-9ee25a9635c2.png)

  
### Here are some of the key outcomes of the project:
- The Dataset was small totally around 569 samples & after preprocessing 8.3% of the datasamples were dropped. 
- The samples were highly imbalanced, hence SMOTE Technique was applied on the data to  balance the classes, adding 21.3% more samples to the dataset.
- Visualising the distribution of data & their relationships, helped us to get some insights on the relationship between the featureset.
- Feature Selection/Eliminination was carried out and appropriate features were shortlisted.
- Testing multiple algorithms with fine-tuning hyperparamters gave us some understanding on the model performance for various algorithms on this specific dataset.
- The Support Vector algorithm perform the best on the current dataset, considering Recall as the key-metric, as is relatively ok to falsely classify any patient as False Positive, but can be quiet dangerous if classified as False Negative.
- Yet it wise to also consider simpler model like Logistic Regression as it is more generalisable & is computationally less expensive.

