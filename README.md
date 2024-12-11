Kaggle Tabular Data Analysis Project

Overview

* This project demonstrates a complete pipeline for training and evaluating machine learning models on a Kaggle tabular dataset. The workflow includes preprocessing, model training, validation, and generating predictions for the test dataset. The objective is to achieve meaningful predictions for classification tasks while adhering to Kaggle’s submission requirements.

Features

* Data preprocessing
* Handling missing values
* Feature normalization using MinMaxScaler
* One-hot encoding for target variable
* Histograms for feature distribution
* Logarithmic scale visualizations for skewed data
* Class-wise feature comparison
* Machine Learning model training and validation


| Feature          | Description                                        |
|:-----------------|:---------------------------------------------------|
| loc              | McCabe's line count of code                        |
| v(g)             | McCabe's cyclomatic complexity                     |
| ev(g)            | McCabe's essential complexity                      |
| iv(g)            | McCabe's design complexity                         |
| n                | Halstead total operators + operands                |
| v                | Halstead volume                                    |
| l                | Halstead program length                            |
| d                | Halstead difficulty                                |
| i                | Halstead intelligence                              |
| e                | Halstead effort                                    |
| b                | Halstead bugs                                      |
| t                | Halstead's time estimator                          |
| lOCode           | Halstead's line count                              |
| lOComment        | Halstead's count of lines of comments              |
| lOBlank          | Halstead's count of blank lines                    |
| lOCodeAndComment | Combination of Code and Comments                   |
| uniq_Op          | Unique operators                                   |
| uniq_Opnd        | Unique operands                                    |
| total_Op         | Total operators                                    |
| total_Opnd       | Total operands                                     |
| branchCount      | Flow graph                                         |
| defects          | Defects Y/N                                        |

Model Training:
* A Random Forest Classifier was used as the primary model.

Evaluation:
* Metrics like Accuracy, Precision, Recall, F1-Score, and ROC-AUC were computed to assess model performance on the validation dataset.

Test Dataset:
* The trained model was applied to the preprocessed test dataset.

* Predictions were saved to a CSV file in the required format for Kaggle submission.

Key Results

* Validation Accuracy: Achieved 80.6% accuracy on the validation dataset using the Random Forest Classifier.

* ROC-AUC: Measured as a secondary performance metric to evaluate classification quality.

Prerequisites
* Python 3.7+

Required Python packages:
* pandas
* numpy
* matplotlib
* scikit-learn

License
* This project is licensed under the MIT License. See the LICENSE file for more details.

Acknowledgements
* Kaggle for providing the dataset.
* Scikit-learn for enabling efficient machine learning development.

Contact
* For any inquiries or contributions, feel free to contact me at [riverpengelly@gmail.com].
