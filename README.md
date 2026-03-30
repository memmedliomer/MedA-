# SIIM-Melanoma-Classification

Currently, dermatologists evaluate every one of a patient's moles to identify outlier lesions or **“ugly ducklings”** that are most likely to be melanoma. Existing AI approaches have not adequately considered this clinical frame of reference. Dermatologists could enhance their diagnostic accuracy if detection algorithms consider “contextual” images within the same patient to determine which images represent a melanoma. If successful, classifiers would be more accurate and could better support dermatological clinic work.

## I. PROBLEM DESCRIPTION

The project aims to classify melanoma in images of skin lesions and create a model which predicts whether the lesion in the image is **malignant** or **benign**. 

For this specific purpose, two primary objectives were established:
1. **Data Extraction:** Extract information from metadata (patient information) and image data (images of melanoma) of the training dataset.
2. **Model Evaluation:** Use **Logistic Regression** and **SVM** to analyze the accuracy of the model on the test set, utilizing performance metrics such as accuracy score and confusion matrix.

> **Note:** Skin cancer is the most prevalent type of cancer. Melanoma, specifically, is responsible for **75% of skin cancer deaths**, despite being the least common skin cancer. The American Cancer Society estimates over 100,000 new melanoma cases will be diagnosed in 2020, with almost 7,000 projected deaths. Early and accurate detection—aided by data science—can make treatment significantly more effective.

---

## II. TECHNICAL APPROACH

### A. Datasets Used
This project utilizes the **SIIM-ISIC Melanoma Classification** dataset, composed of metadata and skin lesion images. The following files were specifically used:

* `train.csv` – Training dataset for patient information.
* `test.csv` – Test dataset for patient information.
* `jpeg/train` – Training image dataset.
* `jpeg/test` – Test image dataset.

*Additional file formats available in the dataset but not utilized in this specific project include DICOM images and TFRecord format.*

### B. List of Features
For the metadata (patient information), the following features were utilized:

| Feature | Description |
| :--- | :--- |
| **image_name** | Unique identifier, points to filename of related image |
| **patient_id** | Unique patient identifier |
| **sex** | The sex of the patient (blank when unknown) |
| **age_approx** | Approximate patient age at time of imaging |
| **anatom_site_general_challenge** | Location of the imaged site |
| **diagnosis** | Detailed diagnosis information |
| **benign_malignant** | Indicator of malignancy of imaged lesion |
| **target** | Binarized version of the target variable |
