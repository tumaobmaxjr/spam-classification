# CSci 144 - Intelligent Systems | Coursework 1
# Spam Classification

## Coursework Overview
<a id="coursework-overview"></a>
This coursework is designed to classify text messages as either "spam" or "ham" (non-spam). It utilizes a Multinomial Naive Bayes model for text classification. The model is trained on a dataset of SMS messages and is capable of predicting whether a given message is spam or not.

## Table of Contents
- [Project Overview](#coursework-overview)
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
    <th>Actual spam</th>
    <th>Actual ham</th>
  </tr>
  <tr>
    <th>Prediction spam</th>
    <td>953</td>
    <td>12</td>
  </tr>
  <tr>
    <th>Predicted ham</th>
    <td>6</td>
    <td>144</td>
  </tr>
</table>

- Correctly classified values: 953 + 144 = 1097
- Total number of values: 1115
- Overall accuracy: 1097 / 1115 = 0.9838565022421

## Example Usage
<a id="example-usage"></a>
You can use the trained model to classify text messages. Here's an example of how to do it:

```python
while True:
    msg = input("Type the message: ")
    msg = cv.transform([msg])
    prediction = model.predict(msg)
    print("This is a", prediction[0], "message")
```
Simply input a message, and the model will predict whether it's "spam" or "ham."



