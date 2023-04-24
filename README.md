# Using Machine Learning to predict Coronary Heart Disease Risk using the Framingham Data Set
## About the dataset:
The dataset is publically available on the Kaggle website. **The classification goal is to predict whether the patient has 10-year risk of future coronary heart disease (CHD).** The dataset provides the patients’ information and includes over 4,240 records and 15 attributes.


## Attributes:
1. sex: male(0) or female(1);(Nominal)
2. age: age of the patient;(Continuous)
3. currentSmoker: whether or not the patient is a current smoker (Nominal)
4. cigsPerDay: the number of cigarettes that the person smoked on average in one day.(can be considered continuous as one can have any number of cigarretts, even half a cigarette.)
5. BPMeds: whether or not the patient was on blood pressure medication (Nominal)
6. prevalentStroke: whether or not the patient had previously had a stroke (Nominal)
7. prevalentHyp: whether or not the patient was hypertensive (Nominal)
8. diabetes: whether or not the patient had diabetes (Nominal)
9. totChol: total cholesterol level (Continuous)
10. sysBP: systolic blood pressure (Continuous)
11. diaBP: diastolic blood pressure (Continuous)
12. BMI: Body Mass Index (Continuous)
13. heartRate: heart rate (Continuous)
14. glucose: glucose level (Continuous)
15. 10 year risk of coronary heart disease CHD (binary: “1”, means “Yes”, “0” means “No”) - **Target Variable**


## Objective: Build a classification model that predicts wheher a patient has 10-year risk of future coronary heart disease
*(note the target column to predict is 'TenYearCHD' where CHD = Coronary heart disease)


In this project I will do the following:
- Read the file and display columns.
- Handle missing values
- Calculate basic statistics of the data (count, mean, std, etc) and exploratory analysts and describe your observations.
- Create training and testing sets, using 3 sample sets of (50,50 | 70,30 | 80,30)
- Build multiple machine learning models to predict TenYearCHD
- Evaluate the models (f1 score, Acuuracy, Precision ,Recall and Confusion Matrix)
- Conclude my findings (Model which is giving best f1 score and why)


## Conclusion:

Best Model - The overall best model was SVM with an RBF kernel

Overall conclusion - The overall outcome of this project was very low F1 scores - most likely due to the target class imbalance, and overall poor performance. When training the models, due to the imbalanced dataset, the modelel become biased and overfit towards the majority class, which resulted in poor performance on the minority class. This is because the models learned to predict the majority class more frequently, leading to a higher accuracy on the majority class and a lower accuracy on the minority class and overall poor performance and ability to generalize. 


**In a medical context, false positives can lead to unnecessary treatments or tests, while false negatives can result in missed diagnoses and delayed treatment, so it is important to strive for a balance between precision and recall, and to achieve a high F1 score, in order to minimize the risk of misdiagnosis or mistreatment.**


## Additional Steps:
Due to class imbalance in the dataset, several techniques were done additionaly in an attempt to address this issue including: Feature selection and various sampling techniques including oversampling, undersampling, SMOTE, and ASYDM. The code ML_Sampling will showcase the results of the additional steps. 


---
Link to dataset:
https://www.kaggle.com/datasets/aasheesh200/framingham-heart-study-dataset
