Kaggle Tabular Data Analysis Project

Overview

* This project demonstrates a complete pipeline for training and evaluating machine learning models on a Kaggle tabular dataset. The workflow includes preprocessing, feature engineering, model training, validation, and generating predictions for the test dataset. The objective is to achieve meaningful predictions for classification tasks while adhering to Kaggle’s submission requirements.

Features

* Comprehensive data preprocessing pipeline
* Handling missing values
* Feature normalization using MinMaxScaler
* One-hot encoding for categorical features (if applicable)
* Histograms and boxplots for feature distribution
* Logarithmic scale visualizations for skewed data
* Class-wise feature comparison
* Machine Learning model training and validation

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
