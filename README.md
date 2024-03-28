# BioML Project: Dementia Prediction Dataset Analysis

## Overview

This project aims to analyze a dataset containing longitudinal records of MRI scans from patients with dementia. The dataset consists of 373 records with 15 features, including subject ID, MRI ID, group classification, visit number, demographic information, and clinical assessments.

## Dataset Description
- **Subject ID:** Unique identifier for individual subjects.
- **MRI ID:** Unique identifier for each MRI scan.
- **Group:** Classification label indicating dementia status.
- **Visit:** Number of times a subject visited for a scan.
- **MR Delay:** Delay of visit by a subject since the last visit (in days).
- **M/F:** Gender of the subject (Male/Female).
- **Hand:** Handedness of the subject.
- **Age:** Age of the subject.
- **EDUC:** Years of education.
- **SES:** Socio-Economic Status assessed by the Hollingshead index of social position.
- **MMSE:** Mini-Mental State Examination score.
- **CDR:** Clinical Dementia Rating.
- **eTIV:** Estimated total intracranial volume.
- **nWBV:** Normalized whole-brain volume.
- **ASF:** Atlas Scale Factor; volume scaling factor for brain size.

## Analysis Steps
### Preprocessing

1. **Labels Uniformization**: Converted patients were adjusted to reflect their nondemented status at the initial visit and demented status at the last visit.
2. **Feature Selection**: Features irrelevant for analysis, such as MRI ID, Visit, MR Delay, and Hand, were removed.
3. **Handling Missing Values**: Rows with NaN values in the SES feature were removed.
4. **Exploratory Data Analysis**: Various visualizations were created to understand data distributions and relationships between features. examples:

   ![image](https://github.com/yeela8g/Dementia-Prediction-Dataset-Analysis/assets/118124478/c7414148-10e3-49be-bc7e-5949c806cb3d)


### ML Algorithms

### K-Nearest Neighbors (KNN):
Min-max normalization was applied to the data.KNN algorithm was trained on features EDUC, MMSE, and nWBV, achieving high precision and recall.
In the optimization process, K value of 15 yielded the best results.
![image](https://github.com/yeela8g/Dementia-Prediction-Dataset-Analysis/assets/118124478/ea92c858-6b6b-4460-9a70-d5b57aad1895)


### Random Forest
- **Feature Importance**: Random forest model identified the most important features.
- **Training**: The algorithm was trained, achieving high accuracy in predicting dementia.

### Support Vector Machine (SVM)
- **Training**: SVM model was trained, yielding high accuracy in dementia prediction.


## Conclusions
- All models achieved high accuracy in classifying dementia status, indicating the suitability of the dataset for classification tasks.
- Education years were found to play a significant role in reducing the risk of dementia.
- As for key features - CDR, MMSE, nWBV, and ASF were identified as significant predictors of dementia.
- PCA and K-means clustering aided in visualizing data clusters, revealing distinct groups of dementia and healthy patients.


Overall, the project demonstrates the effectiveness of machine learning algorithms in predicting dementia and provides insights into relevant features for early detection.
