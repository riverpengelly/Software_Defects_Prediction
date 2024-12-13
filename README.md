![image](https://github.com/user-attachments/assets/3a423be7-8899-4e84-8cfa-eafdd602dcd4)
Kaggle Tabular Project: Software Defect Prediction

Project Overview
* Challenge Link: https://www.kaggle.com/competitions/playground-series-s3e23/data

**Description:**
* The goal of this competition is to predict whether a software module will be defective based on the provided dataset of software metrics. The dataset includes both static code attributes and defect indicators, offering a real-world challenge for identifying bugs before software deployment. The target variable is a binary classification (Defective: Yes/No). When tested on a split test dataset the model returned an accuracy of **80.84%**
* This is higher than the current top leaderboard submission of 79.42% accuracy (all Kaggle submissions are tested against 80% of the test dataset.)

**Dataset Description**
* The dataset includes 22 software metrics (featured below) collected from modules of a larger system. These metrics measure code by its complexity, coupling, cohesion, and size which are correlated with software quality.

      | **Feature Name**      | **Description**                     |
      |-----------------------|-------------------------------------|
      | loc                   | Lines of Code                       |
      | v(g)                  | Cyclomatic Complexity               |
      | ev(g)                 | Essential Complexity                |
      | iv(g)                 | Module Design Complexity            |
      | n                     | Operands                            |
      | v                     | Halstead Volume                     |
      | l                     | Halstead Level                      |
      | d                     | Halstead Difficulty                 |
      | i                     | Halstead Intelligence               |
      | e                     | Halstead Effort                     |
      | b                     | Halstead Bugs                       |
      | t                     | Halstead Time                       |
      | IOCode                | Code Lines                          |
      | IOComment             | Comment Lines                       |
      | IOBlank               | Blank Lines                         |
      | locCodeAndComment     | Lines of Code and Comment           |
      | uniq_Op               | Unique Operators                    |
      | uniq_Opnd             | Unique Operands                     |
      | total_Op              | Total Operators                     |
      | total_Opnd            | Total Operands                      |
      | branchCount           | Branch Count                        |
      | defects               | Defect Presence (Target)            |


**Files Provided:**

* train.csv – Training dataset with feature and target columns.
* test.csv – Test dataset for predictions.
* sample_submission.csv – Example of the required submission format.

**Data Download and Extraction:**
* Performed on Windows 10 OS, powershell commands may need personal tweaking to fit linux or mac OS kernels.

**Data Summary:**

* Number of Rows: 101,763
* Number of Features: float64(17), int64(5), and (bool(1) target [defects] column)


**Data Cleaning and Preparation**
* Dropped Unncesssary columns:
  * [id]
  * [defects]
    
* Missing Value Handling:
  * Extensive missing value methods were used but none were found. 

* Feature Rescaling:
  * Normalized all numeric features using Min-Max scaling for consistency.

* Feature Encoding:
  * One-hot encoded the categorical column [Defects]

**Data Understanding:**
* All 22 features were plotted against the target [defects] column to determine highly correlated features and negatively correlated features:
* Logarithmic scaling was used to discern better analysis of key features.

![image](https://github.com/user-attachments/assets/812023a8-8e47-4d9a-aacf-7d1baa1afeb0)

**Machine Learning**
* Problem Formulation:
  * Binary classification problem (`True`/`False`)
* Data Splits:
  * Training Data: 70%
  * Validation Data: 15%
  * Test Data: 15%
* Algorithm:
  * Model Used: Random Forest Classifier

#### *Performance metrics on the model:*
      | **Metric**        | **Value**      |
      |--------------------|---------------|
      | **Accuracy**       | 0.8084        |
      | **ROC-AUC Score**  | 0.7710        |

#### *Classification Report*
    | **Class** | **Precision** | **Recall** | **F1-Score** | **Support** |
    |-----------|---------------|------------|--------------|-------------|
    | 0         | 0.83          | 0.94       | 0.88         | 11,805      |
    | 1         | 0.64          | 0.36       | 0.46         | 3,460       |
    
    | **Metric**       | **Accuracy** | **Macro Avg** | **Weighted Avg** |
    |-------------------|--------------|---------------|------------------|
    | Precision         | -            | 0.74          | 0.79             |
    | Recall            | -            | 0.65          | 0.81             |
    | F1-Score          | -            | 0.67          | 0.79             |
    | Support           | 15,265       | 15,265        | 15,265           |


**Observations:**
* The model performed extremely well without any excessive usage of hyperparameters or fine tuning. Other models were tested; yet, random forest returned the best results and did so in a suprisingly short amount of time. Official Kaggle submission has not been done yet, but I will attempt to get my model tested as it performed quite well against the validation and test split.

 **Additional Information**
  *  15% test submission dataset: `testsubmission.csv`
  * Kaggle test submission dataset: `submission.csv`

**Prerequisites**
* Python 3.7+

**Required Python packages:**
* pandas
* numpy
* matplotlib
* scikit-learn

**Acknowledgements**
* Kaggle for providing the dataset.
* Scikit-learn for enabling efficient machine learning development.

**Contact**
* For any inquiries or contributions, feel free to contact me at [riverpengelly@gmail.com].
