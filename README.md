# MedA-AI-Powered Skin Cancer Detection System
SIIM-Melanoma-Classification
Currently, dermatologists evaluate every one of a patient's moles to identify outlier lesions or “ugly ducklings” that are most likely to be melanoma. Existing AI approaches have not adequately considered this clinical frame of reference. Dermatologists could enhance their diagnostic accuracy if detection algorithms consider “contextual” images within the same patient to determine which images represent a melanoma. If successful, classifiers would be more accurate and could better support dermatological clinic work.

I. PROBLEM DESCRIPTION
The project aims to classify melanoma in images of skin lesions and create a model which predicts the whether the lesion in the image is malignant or benign. For this specific purpose, two things needed to be done:

Extract information from metadata (patient information) and image data (images of melanoma) of training dataset.
Use logistic regression and SVM to see the accuracy of our model on test set (performance metrics – accuracy score and confusion matrix). Skin cancer is the most prevalent type of cancer. Melanoma, specifically, is responsible for 75% of skin cancer deaths, despite being the least common skin cancer. The American Cancer Society estimates over 100,000 new melanoma cases will be diagnosed in 2020. It is also expected that almost 7,000 people will die from the disease. As with other cancers, early and accurate detection—potentially aided by data science—can make treatment more effective.
II. TECHNICAL APPROACH
A. Datasets used This project uses SIIM-ISIC Melanoma Classification dataset which is composed of metadata (patient information) and skin lesion images. Particularly only given files were used in this project: • train.csv – training dataset for patient information • test.csv – test dataset for patient information • jpeg/train – training image dataset • jpeg/test – test image dataset Additionally, in this dataset there are additional file formats that were not utilized in this project: • DICOM training/test images - Commonly used medical imaging data format that combines patient information and image data in one file. • TFRecord format B. List of Features For metadata (patient information), the given features were:

image_name - unique identifier, points to filename of related DICOM image
patient_id - unique patient identifier
sex - the sex of the patient (when unknown, will be blank)
age_approx - approximate patient age at time of imaging
anatom_site_general_challenge - location of imaged site
diagnosis - detailed diagnosis information
benign_malignant - indicator of malignancy of imaged lesion
target - binarized version of the target variable
