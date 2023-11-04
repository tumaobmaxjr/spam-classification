# CSci 144 - Intelligent Systems | Coursework 1
# Spam Classification

## Project Overview
<a id="project-overview"></a>
This coursework is designed to classify text messages as either "spam" or "ham" (non-spam). It utilizes a Multinomial Naive Bayes model for text classification. The model is trained on a dataset of SMS messages and is capable of predicting whether a given message is spam or not.

## Table of Contents
- [Project Overview](#project-overview)
- [Data Source](#data-source)
- [Dependencies](#dependencies)
- [Installation](#installation)
- [Usage](#usage)
- [Results](#results)
- [Example Usage](#example-usage)

## Data Source
<a id="data-source"></a>
The dataset used for this coursework is the "SMS Spam Collection Dataset," available on [Kaggle](https://www.kaggle.com/datasets/uciml/sms-spam-collection-dataset). The dataset has been preprocessed to include two columns: "label" (ham/spam) and "message" (text content of the SMS).

## Dependencies
<a id="dependencies"></a>
The following Python libraries are required to run:
- pandas
- seaborn
- scikit-learn
- matplotlib

## Installation
<a id="installation"></a>
To install the necessary dependencies, you can use pip. Open a command prompt and run the following commands:
```
pip install pandas
pip install numpy
pip install seaborn
pip install scikit-learn
pip install matplotlib
```

## Usage
<a id="usage"></a>
1. Clone or download the project repository from GitHub.
2. Navigate to the project directory in your terminal.
3. Run the Python script containing the code for spam classification.
```
python spam_classification.py
```
The script will perform the following steps:
  - Read the dataset from 'spam.csv.'
  - Clean the data by removing unnecessary columns and renaming them.
  - Convert text messages to vectors using CountVectorizer.
  - Split the data into training and testing sets.
  - Train a Multinomial Naive Bayes model on the training data.
  - Display the training and testing accuracy.
  - Visualize the confusion matrix.


## Results
<a id="results"></a>
The model's performance can be evaluated using the following metrics:
- Training Accuracy: 0.9937177473636976
- Testing Accuracy: 0.9838565022421525

**Confusion Matrix:**

<table>
  <tr>
    <th></th>
    <th>Predicted ham</th>
    <th>Predicted spam</th>
  </tr>
  <tr>
    <th>Actual ham</th>
    <td>[953]</td>
    <td>[12]</td>
  </tr>
  <tr>
    <th>Actual spam</th>
    <td>[6]</td>
    <td>[144]</td>
  </tr>
</table>

