# HeartGuard ML: Detect risk before heart failure appear

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
**Objectives**: Develop machine learning models to identify important predictors of heart disease. **Methods**: Use the Heart Failure Prediction Dataset (918 observations) with preprocessing steps, exploratory data analyses, and models like Logistic Regression, Random Forest, and/or XGBoost. **Expected Outcomes**: Deliver a validated predictive model with a high performace that highlights influential features. **Significance**: The model will inform relevant stakeholders such as medical technology companies to design targeted interventions and improve heart disease prevention strategies.<br>

Keywords: heart failure, machine learning, classification<br>

## Overview
* [Business Case](#business-case)
* [Objectives](#objectives)
* [Project Roadmap](#project-roadmap)
* [Methods](#methods)
* [Results](#results)
* [Conclusion](#conclusion)
* [Reflection Videos](#reflection-videos)

## Business Case
We are a machine learning team working on heart disease prevention. We support healthcare organizations, including hospitals, government agencies, and private companies developing heart disease prevention solutions, by identifying the key factors that predict heart failure, enabling them to design more effective interventions and products.<br>

### Stakeholders: 
* Medical Technology Companies<br>
* Hospitals<br>
* Government agencies<br>
* Pharmaceutical companies<br>

### Risks and uncertainties:
One major risk is overfitting, where models trained on such a small and specific dataset perform well on internal tests but fail on new, unseen data. Closely related is the risk of poor generalization, as the merged dataset may not represent all patient populations equally. There is also a bias risk if certain demographic groups, such as older adults, women, or underrepresented ethnicities, are not adequately represented, leading to unfair or inaccurate predictions for those groups.<br>

## Objectives
* Build a predictive classification model to identify the most significant demographic, clinical, and exercise-related features contributing to heart disease.<br> 
* Deliver a robust heart disease predictive model that enables stakeholders to develop products that drive profit, improve health management, support preventive medicine, enable screening of high-risk populations, and promote healthier diets within the food industry.<br>

## Project Roadmap
<img src="images/Project Roadmap.png" width="800"/>

## Methods
### Dataset, features, and target 
We will use the Heart Failure Prediction Dataset from Kaggle to build machine learning models. This dataset contains 918 observations, 11 features (5 continuous and 6 categorical), and one target variable (categorical). The column names, types, descriptions, and values are detailed in the table below.

| Column Name     | Type        | Description                                           | Values / Units                                      | Risk Direction*         |
|-----------------|-------------|-------------------------------------------------------|-----------------------------------------------------|------------------------|
| HeartDisease    | Target: Categorical      | Diagnosis outcome                                     | 1 = heart disease,<br> 0 = normal                       | —                      |
| Age             | Feature: Continuous  | Patient’s age                                         | Years                                               | Age ↑                  |
| Sex             | Feature: Categorical | Biological sex                                        | M = male,<br> F = female                                | Male                   |
| ChestPainType   | Feature: Categorical | Type of chest pain                                    | TA = typical angina,<br> ATA = atypical angina,<br> NAP = non-anginal pain,<br> ASY = asymptomatic | TA or ATA        |
| RestingBP       | Feature: Continuous  | Resting blood pressure                                | mm Hg                                               | Higher values          |
| Cholesterol     | Feature: Continuous  | Serum cholesterol level                               | mg/dL                                               | Higher values          |
| FastingBS       | Feature: Categorical | Fasting blood sugar status                            | 1 = >120 mg/dL,<br> 0 = ≤120 mg/dL                      | 1                      |
| RestingECG      | Feature: Categorical | Resting electrocardiogram findings                    | Normal,<br> ST = ST-T wave abnormality,<br> LVH = left ventricular hypertrophy | ST or LVH              |
| MaxHR           | Feature: Continuous  | Maximum heart rate achieved                           | bpm (beats per minute)                              | Lower values           |
| ExerciseAngina  | Feature: Categorical | Presence of exercise-induced angina                   | Y = yes,<br> N = no                                     | Y                      |
| Oldpeak         | Feature: Continuous  | ST depression induced by exercise relative to rest    | mV (millivolts)                                     | Higher values          |
| ST_Slope        | Feature: Categorical | Slope of the peak exercise ST segment                 | Up = upsloping,<br> Flat = flat,<br> Down = downsloping     | Flat or Down           |

*This column indicates how each feature (direction) is theoretically associated with a greater likelihood of heart disease.<br>

Source: fedesoriano. (September 2021). Heart Failure Prediction Dataset. Retrieved [Date Retrieved] from https://www.kaggle.com/fedesoriano/heart-failure-prediction.<br>

### Environment & Dependencies
* Environment: Python (3.9.19), Jupyter Notebook (VS Code Integration)<br> 
* Python Libraries: pandas, numpy, random, sklearn, matplotlib, seaborn<br> 
* Version Control: Git/GitHub<br>

### Preprocessing
The dataset will be reviewed starting with data loading and inspection to understand its structure and identify inconsistencies. For handling missing values, the .isnull().sum() function will be used to locate gaps in the data. Outlier detection will be conducted using boxplots, z-scores, and the IQR method to identify and address extreme values. Finally, data normalization and scaling will be performed to bring all numerical features to a similar scale.<br>

### EDA
Exploratory data analysis will identify patterns, relationships, and trends in the dataset. It will begin with univariate analysis using summary statistics, histograms, and boxplots to understand individual variables. Bivariate analysis will then explore relationships between predictors and the target variable (HeartDisease) using bar charts, scatter plots, and boxplots. A correlation heatmap will measure linear relationships and detect multicollinearity, while pair plots will visualize feature interactions and reveal potential patterns or clusters.<br>

### Models

#### Model building
We aim to predict the presence of heart disease, which frames this as a supervised classification problem. We will establish a baseline using Logistic Regression before implementing more advanced models like Random Forest or XGBoost. A comparison of the model results will determine the necessity of exploring additional models. GridSearchCV will also be employed for optimization, as described in the model optimization section.<br>

#### Model Optimization & Cross-validation
In the later stages of development, the project will optimize both the baseline and advanced models through hyperparameter tuning. Model evaluation will be conducted using cross-validation techniques, specifically GridSearchCV.<br>

#### Model Testing & Performance Evaluation
During the testing phase, unseen data will be used for prediction. The final performance of both the baseline and advanced models will be assessed using key metrics, including accuracy, precision, recall, F1 score, and the ROC/AUC curve.<br>

#### Model comparison
At the conclusion of the testing phase, we will compare the performance of the baseline and advanced models across various evaluation metrics. Based on this comparison, the most effective model will be recommended to the client.<br>

#### Feature Importance
After model comparison (baseline vs. advanced), To analyze and determine the features for the model with better performance, we will use SHAP (SHapley Additive exPlanations) values to assess feature importance.<br>

### Limitations
The Heart Failure Prediction Dataset's dependability and generalizability are impacted by a number of limitations. With just 918 samples and 11 features, the model's complexity is limited and overfitting may result. Due to the fact that it combines data from five distinct sources, there can be inconsistencies as a result of numerous methods of collecting. Additionally, its limited ethnic variety and possible imbalances make it less typical of larger communities.<br>

## Results
### Preprocessing
Pending

### EDA
Pending

### Baseline model
Pending

### Advanced model
Pending

### Model comparison
(Baseline model vs. Advanced model)<br>
Pending

### Feature importance
Pending

## Conclusion
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

