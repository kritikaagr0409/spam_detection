# Spam Detection Model Using Naive Bayes

## Project Overview
This project involves building a spam detection model using the Naive Bayes algorithm. The dataset used is a collection of SMS messages labeled as "ham" (non-spam) or "spam".

## Dataset
The dataset contains 5,572 rows with the following columns:
- v1: Label (ham or spam)
- v2: Message content
- Unnamed: 2, Unnamed: 3, Unnamed: 4: Additional columns that were dropped as they contained insignificant data.

## Preprocessing Steps
1. *Data Cleaning*:
   - Dropped unnecessary columns.
   - Renamed columns: v1 to result, v2 to content.

2. *Label Encoding*:
   - Encoded labels: "ham" as 0 and "spam" as 1 using LabelEncoder.

3. *Removing Duplicates*:
   - Removed duplicate rows, reducing the data size to 5,169 rows.

4. *Text Transformation*:
   - Converted text to lowercase.
   - Tokenized and removed non-alphanumeric characters.
   - Removed stopwords and punctuation.
   - Applied lemmatization for better word representation.

5. *Feature Engineering*:
   - Added character and word count columns for better understanding of message length characteristics.

## Visualizations
- Created a pie chart to show the proportion of spam and ham messages.

## Common Words Analysis
- Extracted and visualized the most common words in both ham and spam messages using the Counter module from the collections library.

## Model Building
- *Vectorization*: Used TfidfVectorizer to convert text data into numerical format.
- *Model*: Trained a MultinomialNB classifier.
- *Splitting Data*: 80% training data, 20% testing data using train_test_split.

## Model Performance
- Achieved an accuracy of *96.03%* on the test data.
- *Classification Report*:
  ```plaintext
              precision    recall  f1-score   support

          0       0.96      1.00      0.98       889
          1       1.00      0.72      0.84       145

      accuracy                           0.96      1034
     macro avg       0.98      0.86      0.91      1034
  weighted avg       0.96      0.96      0.96      1034
