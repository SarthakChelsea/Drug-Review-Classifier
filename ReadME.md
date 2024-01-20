# Disease Prediction from Drug Review

## Overview
This project aims to predict the medical condition of patients based on their drug reviews. The dataset used contains drug reviews from various customers, and the goal is to classify the reviews into specific medical conditions such as Birth Control, Depression, High Blood Pressure, and Diabetes Type 2.


![Medications](https://huenemefamily.com/wp-content/uploads/2016/06/medications-620x420_c.jpg)


## Dataset
The dataset used in this project is loaded from the 'drugsComTrain_raw.tsv' file, containing information about drug reviews, including the drug name, rating, date, useful count, and the condition for which the drug was taken.

## Exploratory Data Analysis (EDA)
- The dataset is explored to understand the distribution of medical conditions.
- Individual dataframes are created for analyzing each specific medical condition.
- Word clouds are generated to visualize the most frequent words in reviews for each condition.

## Data Preprocessing
The following steps are applied to preprocess the text data:
1. Removal of HTML links
2. Retaining only alphabets and numbers
3. Removal of stopwords (common words)
4. Lowercasing the text
5. Lemmatization of words (reducing words to their root form)

## Feature Extraction
Features are created using both Bag of Words (BoW) and Term Frequency-Inverse Document Frequency (TF-IDF) approaches. Three types of n-gram language models (unigram, bigram, and trigram) are utilized to capture different levels of context in the text.

## Machine Learning Models
Two classification models are implemented:
1. **Naive Bayes:** Utilized with both BoW and TF-IDF representations.
2. **Passive Aggressive Classifier:** Employed for BoW and TF-IDF with various n-gram models.

## Model Evaluation
Confusion matrices are plotted to visualize the performance of the models. Accuracy is used as the primary metric, and other metrics like precision, recall, and F1-score could be considered for a more comprehensive evaluation.

## Hyperparameter Tuning
For TF-IDF models with n-grams, hyperparameter tuning is performed by experimenting with different values for `max_df` and the n-gram range. The goal is to identify the combination that yields the highest accuracy.

## Conclusion
The project explores different text processing techniques and machine learning models for disease prediction based on drug reviews. The accuracy scores indicate that the TF-IDF model with bigrams performs the best among the tested configurations. Further optimization and experimentation with hyperparameters may enhance model performance.

---

*Note: The README provides an overview of the project structure and key steps. Additional details, visualizations, and explanations can be found in the Jupyter Notebook.*
