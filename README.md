# Product Review Sentiment Analyzer

## Project Overview

This project focuses on building a Natural Language Processing (NLP) model that analyzes product reviews and classifies them into three sentiment categories: **Positive, Negative, and Neutral**.

The project was developed as part of an internship project using the **Amazon Alexa Reviews Dataset**.

## Objective

The main objective is to preprocess unstructured review text, convert text into numerical features using **TF-IDF**, and build a machine learning model that can automatically predict the sentiment of product reviews.

## Dataset

The project uses the **Amazon Alexa Reviews Dataset**.

The dataset contains **3,150 reviews** with the following information:

* Rating
* Date
* Product variation
* Verified review
* Feedback
* Sentiment

After removing the missing review entry, **3,149 reviews** were used for text classification.

## Technologies Used

* Python
* Pandas
* NLTK
* Scikit-learn
* Matplotlib
* Seaborn

## Project Workflow

1. Data loading and inspection
2. Handling missing values
3. Sentiment label creation
4. Text preprocessing
5. Stopword removal
6. Lemmatization
7. TF-IDF feature extraction
8. Train-test split
9. Naive Bayes classification
10. SVM classification with class balancing
11. Model evaluation
12. Confusion matrix visualization
13. Testing on new reviews

## Text Preprocessing

The review text was cleaned before applying machine learning techniques.

The preprocessing steps included:

* Converting text to lowercase
* Removing punctuation and unnecessary characters
* Removing stopwords
* Lemmatization

Example:

`Love my Echo!` → `love echo`

## TF-IDF Feature Extraction

**TF-IDF (Term Frequency-Inverse Document Frequency)** was used to convert the cleaned review text into numerical features.

The resulting TF-IDF matrix contained:

* **3,149 reviews**
* **3,834 features**

## Model Building

Two classification models were explored:

### Naive Bayes

Multinomial Naive Bayes was used as a baseline model.

The model achieved an accuracy of **87%**, but it struggled to identify the Negative and Neutral classes because the dataset was imbalanced.

### Support Vector Machine

A Linear SVM with `class_weight='balanced'` was then used to give more importance to minority classes.

The SVM performed better than the Naive Bayes baseline.

## Model Evaluation

The SVM model achieved:

* **Accuracy: 91%**
* **Macro F1-score: 0.67**
* **Weighted F1-score: 0.90**



## Conclusion

This project demonstrates a complete NLP sentiment classification workflow, from text preprocessing and TF-IDF feature extraction to machine learning classification and evaluation.

The balanced SVM model performed better than the Naive Bayes baseline, particularly in identifying the minority sentiment classes.

The project also highlights the importance of using metrics beyond accuracy when working with imbalanced datasets.

## Author

**Mahi Saxena**

This project was completed as part of an internship project.
