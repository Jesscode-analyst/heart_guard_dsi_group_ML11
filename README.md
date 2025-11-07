# HeartGuard ML: Detect risk before heart failure appear.

## Data Sciences Institute, University of Toronto - Cohort 7 - ML Team 11

### Members (alphabetical)
* [Amy Li](https://github.com/lsmamy)
* [Chun-Yuan Chen](https://github.com/Chun-YuanChen) 
* [Isra Khan](https://github.com/Issy90)
* [Jaskirat Kaur](https://github.com/Jesscode-analyst)
* [Uma Deshpande](https://github.com/aniruma3012)
* [Yi-Chen Hsiao](https://github.com/yichen-hsiao)

### Collaboration
Please see [taskboard](taskboard)

## Abstract
(Objectives, Methods, Results, Conclusions, Keywords)<br>
Pending

## Overview
* [Business Case](#business-case)
* [Objectives](#objectives)
* [Project Roadmap](#project-roadmap)
* [Methods](#methods)
* [Results](#results)
* [Conclusion](#conclusion)
* [Requirements](#requirements)
* [Reflection Videos](#reflection-videos)

## Business Case
We are a machine learning team working on heart disease prevention. Our job is to support companies working on solutions to prevent heart disease on which factors significantly predict the occurence of heart failures so companies know which factors to target in their solutions/products.

## Objectives
Pending

## Project Roadmap
<img src="images/Project Roadmap.png" width="800"/>

## Methods
### Dataset, features, and target 
We will use the Heart Failure Prediction Dataset from Kaggle to build machine learning models. This dataset contains 918 observations, 11 features (5 continuous and 6 categorical), and one target variable (categorical). The column names, types, descriptions, and values are detailed in the table below.

| Column Name     | Type        | Description                                           | Values / Units                                      | Risk Direction         |
|-----------------|-------------|-------------------------------------------------------|-----------------------------------------------------|------------------------|
| HeartDisease    | Target      | Diagnosis outcome                                     | 1 = heart disease, 0 = normal                       | —                      |
| Age             | Continuous  | Patient’s age                                         | Years                                               | Age ↑                  |
| Sex             | Categorical | Biological sex                                        | M = male, F = female                                | Male                   |
| ChestPainType   | Categorical | Type of chest pain                                    | TA = typical angina, ATA = atypical angina, NAP = non-anginal pain, ASY = asymptomatic | TA or ATA        |
| RestingBP       | Continuous  | Resting blood pressure                                | mm Hg                                               | Higher values          |
| Cholesterol     | Continuous  | Serum cholesterol level                               | mg/dL                                               | Higher values          |
| FastingBS       | Categorical | Fasting blood sugar status                            | 1 = >120 mg/dL, 0 = ≤120 mg/dL                      | 1                      |
| RestingECG      | Categorical | Resting electrocardiogram findings                    | Normal, ST = ST-T wave abnormality, LVH = left ventricular hypertrophy | ST or LVH              |
| MaxHR           | Continuous  | Maximum heart rate achieved                           | bpm (beats per minute)                              | Lower values           |
| ExerciseAngina  | Categorical | Presence of exercise-induced angina                   | Y = yes, N = no                                     | Y                      |
| Oldpeak         | Continuous  | ST depression induced by exercise relative to rest    | mV (millivolts)                                     | Higher values          |
| ST_Slope        | Categorical | Slope of the peak exercise ST segment                 | Up = upsloping, Flat = flat, Down = downsloping     | Flat or Down           |

*This column indicates how each feature (direction) is theoretically associated with a greater likelihood of heart disease.

Source: fedesoriano. (September 2021). Heart Failure Prediction Dataset. Retrieved [Date Retrieved] from https://www.kaggle.com/fedesoriano/heart-failure-prediction.

### Preprocessing
Pending

### EDA
Pending

### Baseline model
Pending

### Advanced model
Pending

### Model Optimization & Cross-validation
 
In the later stages of development, the project will optimize both the baseline and advanced models through hyperparameter tuning. Model evaluation will be conducted using cross-validation techniques, specifically GridSearchCV.
 
### Model Testing & Performance Evaluation
 
During the testing phase, unseen data will be used for prediction. The final performance of both the baseline and advanced models will be assessed using key metrics, including accuracy, precision, recall, F1 score, and the ROC/AUC curve.
 
### Model comparison
At the conclusion of the testing phase, we will compare the performance of the baseline and advanced models across various evaluation metrics. Based on this comparison, the most effective model will be recommended to the client.




## Results
### Preprocessing
Pending

### EDA
Pending

### Baseline model
Pending

### Advanced model
Pending

### Comparison
(Baseline model vs. Advanced model)<br>
Pending

## Conclusion
Pending

## Requirements
(This section outlines the required tool and library versions for running our models.)<br>
Pending

## Reflection Videos
The links currently point to YouTube as placeholders; please replace them with your own 3-5 minute video links once ready.

* [Amy Li](https://www.youtube.com/)
* [Chun-Yuan Chen](https://www.youtube.com/) 
* [Isra Khan](https://www.youtube.com/)
* [Jaskirat Kaur](https://www.youtube.com/)
* [Uma Deshpande](https://www.youtube.com/)
* [Yi-Chen Hsiao](https://www.youtube.com/)

## Folder Structure

```markdown
.
├── data
├── images
├── models
├── presentation
├── taskboard
├── LICENSE
└── README.md
```

* **data**: Raw, processed, and finalized datasets.
* **documentation**: Project timeline, action items, and related notes.
* **images**: Contains any images generated from EDA to modeling.
* **models**: Baseline and machine learning models for comparison.
* **presentation**: Slides and materials for project showcase. 
* **LICENSE**: Repository license information.
* **README.md**: Project overview and documentation.

