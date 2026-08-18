# Spam_Email_Dissertation-

# Author : Amruth Sai Guggilla 
# Enrollment Id : 34033769

### Project Title

Evaluating an Email Spam Classification Prototype Using Machine Learning
and Deep Learning Models with Cross-Validation

### Project Overview

This project develops and evaluates a binary email spam classification
system that distinguishes between spam and non-spam emails. The workflow
includes dataset inspection, text preprocessing, exploratory data
analysis, class balancing, TF-IDF feature extraction, machine learning,
deep learning, cross-validation, hyperparameter tuning and prototype
development.

The project also includes human evaluation of the developed prototype.
Users can enter email content, receive a spam or non-spam prediction
with confidence information, and provide feedback about the prediction
and their experience using the prototype.

### Aim

The main aim is to evaluate machine learning and deep learning models
for email spam classification using multiple performance metrics,
cross-validation and hyperparameter tuning, and to develop a functional
classification prototype assessed through human feedback.

### Objectives

1.  Examine and preprocess the selected email spam dataset.
2.  Implement and evaluate Logistic Regression, KNN, Random Forest, ANN
    and DNN.
3.  Evaluate models using accuracy, precision, recall, F1-score and
    ROC-AUC.
4.  Apply cross-validation to examine model consistency.
5.  Apply Grid Search hyperparameter tuning.
6.  Identify the best-performing model using F1-score.
7.  Develop a functional email spam classification prototype.
8.  Collect human feedback concerning ease of use, prediction clarity,
    usefulness, satisfaction and overall user experience.

### Dataset

The project uses the publicly available Email Spam Classification
Dataset CSV from Kaggle.

Dataset source:

https://www.kaggle.com/datasets/balaka18/email-spam-classification-dataset-csv

The working dataset contains the following main variables:

- text: email message content
- spam: binary target variable

The implementation dataset used in the dissertation contains 5,728
observations and two columns.

The target classes are:

- 0: Non-Spam
- 1: Spam

### Technologies

The project was implemented using Python and the following main
technologies:

- Python
- Pandas
- NumPy
- Scikit-learn
- TensorFlow
- Keras
- NLTK
- Matplotlib
- Imbalanced-learn
- Tkinter
- Joblib
- Regular Expressions

### Project Workflow

The overall workflow is:

1.  Dataset collection
2.  Dataset inspection
3.  Text preprocessing
4.  Exploratory Data Analysis
5.  Class imbalance analysis
6.  SMOTE
7.  TF-IDF feature extraction
8.  Train-test splitting
9.  Default model development
10. Baseline evaluation
11. Cross-validation
12. Grid Search hyperparameter tuning
13. Tuned model evaluation
14. Best-model selection
15. Prototype development
16. Human evaluation
17. Results analysis
18. Dissertation reporting

### Text Preprocessing

The raw email text was processed before model development. The
preprocessing included:

- Lowercase conversion
- URL removal
- Email address removal
- Number removal
- Punctuation and special-character removal
- Word splitting
- English stop-word removal
- WordNet lemmatisation

The purpose was to reduce unnecessary textual variation and create a
consistent representation of the email content.

### TF-IDF Feature Extraction

TF-IDF was used to transform cleaned email text into numerical features.

The maximum number of features was set to 5,000.

The resulting feature matrix was:

5,728 observations x 5,000 features

The first extracted features included terms such as aa, ab, ab html,
ability, able, absence, absolutely, abstract, academic, access and
accepted.

### Train-Test Split

The data was divided using an 80:20 training and testing split.

Training features:

4,582 x 5,000

Testing features:

1,146 x 5,000

Training labels:

4,582

Testing labels:

1,146

The training data was used for model development, cross-validation and
hyperparameter tuning. The test data was retained for final evaluation.

### Exploratory Data Analysis

EDA was used to examine the structure, target distribution and email
length characteristics.

The original class distribution was approximately:

- Non-Spam: 76.1 percent
- Spam: 23.9 percent

The analysis also identified substantial variation in email length, with
most messages being relatively short and several messages being
considerably longer.

### SMOTE

SMOTE was applied to the training data to address the identified class
imbalance.

The testing data was not oversampled.

After SMOTE, the two training classes were approximately balanced, with
around 3,500 observations in each class.

### Machine Learning Models

### Logistic Regression

Logistic Regression was selected because the project is a binary
classification problem and because it provides a suitable baseline for
high-dimensional TF-IDF text features.

### K-Nearest Neighbours

KNN was selected as a similarity-based method. It provides a different
classification approach by using nearby observations in the feature
space.

### Random Forest

Random Forest was selected as an ensemble method combining multiple
decision trees. It provides a different learning approach from Logistic
Regression and KNN.

### Deep Learning Models

### Artificial Neural Network

ANN was included to provide a neural-network-based classification
approach for the TF-IDF features.

The ANN achieved the strongest tuned F1-score and was selected as the
model for prototype development.

### Deep Neural Network

DNN was included to investigate whether a deeper neural architecture
could learn useful relationships from the high-dimensional TF-IDF
representation.

### Evaluation Metrics

The project uses five main evaluation metrics:

### Accuracy

Measures the proportion of correctly classified emails.

### Precision

Measures the proportion of emails predicted as spam that were actually
spam.

### Recall

Measures the proportion of actual spam emails that were correctly
identified.

### F1-Score

Combines precision and recall and provides a balanced measure of
classification performance.

### ROC-AUC

Measures the ability of the model to distinguish between spam and
non-spam classes across classification thresholds.

Multiple metrics are used because high recall alone does not necessarily
indicate strong overall classification performance.

### Cross-Validation

Cross-validation was applied to examine model consistency across
different subsets of the training data.

It was used to:

- Assess consistency
- Support overfitting analysis
- Reduce dependence on one data split
- Support model selection
- Support hyperparameter tuning

The principal models maintained strong validation performance and no
obvious overfitting was identified from the cross-validation analysis.

### Hyperparameter Tuning

Grid Search was used to systematically test predefined hyperparameter
combinations.

The tuning process was:

1.  Define candidate parameters.
2.  Generate parameter combinations.
3.  Evaluate combinations using cross-validation.
4.  Identify the strongest configuration.
5.  Train the tuned model.
6.  Evaluate the tuned model using the selected metrics.

The tuned models were then considered alongside the default and
cross-validation results.

### Best-Performing Model

The Artificial Neural Network was selected as the best-performing model
based on F1-score.

The selection considered:

- Precision and recall balance
- F1-score
- Cross-validation behaviour
- Tuned performance
- Suitability for prototype development

### Prototype

The project includes a graphical Email Spam Classification Prototype.

The interface provides:

- Email input area
- Predict button
- Clear button
- Prediction output
- Confidence output
- Human Evaluation section
- Prediction is Correct option
- Prediction is Incorrect option
- Exit option

The prototype processes new email input using the project preprocessing
and feature-extraction workflow before generating the classification.

### Prototype Testing

The prototype was tested using different types of email content.

A promotional-style email was classified as Spam with a displayed
confidence of 99.98 percent.

A meeting-related email was classified as Non-Spam with a displayed
confidence of 100.00 percent.

These examples demonstrate the prototype’s ability to accept different
email inputs and provide a classification result.

### Human Evaluation

Human evaluation was incorporated into the prototype to obtain practical
feedback.

The evaluation considers:

- Ease of use
- Prediction clarity
- Perceived usefulness
- Satisfaction
- Overall user experience

The prototype also allows participants to indicate whether an individual
prediction is correct or incorrect.

### Results Summary

The main experimental findings are:

- Logistic Regression achieved strong baseline performance.
- Random Forest achieved strong and consistent classification
  performance.
- ANN and DNN performed strongly across the experimental stages.
- KNN produced strong recall but weaker precision and F1-score.
- Cross-validation showed strong consistency for the principal models.
- No obvious overfitting was identified through the cross-validation
  analysis.
- Hyperparameter tuning affected the models differently.
- ANN achieved the strongest tuned F1-score.
- ANN was selected for prototype development.
- The prototype successfully generated spam and non-spam predictions
  with confidence information.
- Human evaluation was incorporated to assess practical interaction with
  the prototype.

### Installation

Create a Python environment and install the main dependencies:

``` bash
pip install pandas numpy scikit-learn tensorflow nltk matplotlib imbalanced-learn joblib
```

NLTK resources required by the preprocessing stage should also be
downloaded before running the text-processing workflow.



### Running the Project

Run the workflow in the following order:

1.  Load the dataset.
2.  Inspect the data.
3.  Clean the email text.
4.  Perform EDA.
5.  Split the dataset.
6.  Apply SMOTE to training data.
7.  Generate TF-IDF features.
8.  Train default models.
9.  Calculate evaluation metrics.
10. Perform cross-validation.
11. Run Grid Search.
12. Evaluate tuned models.
13. Select the best-performing model.
14. Save the required model and preprocessing objects.
15. Run the prototype.
16. Conduct human evaluation.
17. Analyse the results.

### Reproducibility

Random states should be controlled where supported by the selected
algorithms and data-splitting procedures.

The main controlled stages include:

- Train-test splitting
- SMOTE
- Model training
- Cross-validation
- Hyperparameter tuning

The same preprocessing and TF-IDF transformation should be applied to
new email input before classification.

### Ethical and Data Considerations

The project uses a publicly available dataset for model development.

Human evaluation should be voluntary and participants should be informed
about the purpose of the evaluation and the type of feedback being
collected. Only information necessary for the evaluation should be
collected.

The prototype is intended as a dissertation-level classification system
and should not be treated as a replacement for human judgement in
situations where an incorrect classification could have important
consequences.

### Limitations

The main technical limitations are:

- Use of one selected email spam dataset
- Dependence on TF-IDF representation
- Fixed feature selection settings
- Use of SMOTE for training-data balancing
- Predefined Grid Search parameter ranges
- Lack of testing on multiple independent external datasets
- Potential changes in spam patterns over time

### Future Work

Future technical development could investigate:

- Transformer-based text representations
- Context-aware email classification
- Ensemble and stacking methods
- Bayesian hyperparameter optimisation
- Evolutionary optimisation
- Temporal validation
- Adversarial spam testing
- Incremental or online learning
- Larger independent datasets
- Additional prototype testing

### Dissertation Structure

### Chapter 1: Introduction

Presents the background, research problem, motivation, research
question, aim and objectives, scope, deliverables, assumptions, benefits
and dissertation overview.

### Chapter 2: Literature Review

Reviews email spam classification, detection approaches, machine
learning and deep learning models, datasets, cross-validation,
hyperparameter tuning and research gaps.

### Chapter 3: Methodology

Explains the research methodology, research onion, system design,
dataset, preprocessing, EDA, SMOTE, TF-IDF, model development,
evaluation metrics, cross-validation, hyperparameter tuning, prototype
development, human evaluation, planning and ethical considerations.

### Chapter 4: Results, Discussion and Evaluation

Presents default model results, cross-validation and overfitting
analysis, tuned results, analysis of experimental conditions, best-model
selection, prototype results, human evaluation, existing-study
comparison and key findings.

### Chapter 5: Conclusion, Limitations and Future Work

Summarises achievement of the aim and objectives, presents the
conclusion, discusses limitations and identifies future technical
development.

### Main Contribution

The main contribution of the project is a structured email spam
classification workflow that combines:

- Text preprocessing
- TF-IDF feature extraction
- SMOTE
- Machine learning
- Deep learning
- Multiple evaluation metrics
- Cross-validation
- Hyperparameter tuning
- Best-model selection
- Prototype development
- Human evaluation

The workflow provides both technical model evaluation and practical
prototype assessment within one dissertation project.

### Academic Context

This repository supports the dissertation:

Evaluating an Email Spam Classification Prototype Using Machine Learning
and Deep Learning Models with Cross-Validation

The code, experimental results, prototype and dissertation should be
considered together when interpreting the project findings.
