# 🐦 Twitter Sentiment Analysis Using Decision Tree Classifier

This documentation provides a detailed explanation of the Twitter Sentiment Analysis project implemented using a Decision Tree classifier with TF-IDF vectorization in Python. The goal of this system is to analyze and predict sentiment from Twitter text data using machine learning techniques.

## Overview
The project employs textual data from Twitter, preprocessing it to remove noise, then uses TF-IDF vectorization to transform texts into features for classification. The model achieves an accuracy of approximately 90% in predicting sentiment labels from tweets.

## Libraries Used
The following Python libraries were used to implement the model:
- **NumPy:** For numerical operations
- **Pandas:** For data manipulation and analysis
- **Matplotlib & Seaborn:** For data visualization
- **Regular Expressions (re):** For text cleaning
- **Scikit-learn:** For ML modeling, preprocessing, and evaluation metrics

## Project Structure

### 1. Data Loading and Preprocessing:
- Dataset is loaded from Twitter training and validation CSV files
- Columns are renamed and unnecessary ones are dropped
- Text data is cleaned using a custom function that:
  - Removes URLs, mentions, and hashtags
  - Removes special characters and digits
  - Converts text to lowercase
  - Removes extra whitespace
- Empty texts and duplicates are removed from the dataset

### 2. Feature Engineering:
- Text data is vectorized using TF-IDF (Term Frequency-Inverse Document Frequency)
- Labels are encoded using LabelEncoder

### 3. Model Architecture:
- A Decision Tree Classifier is trained on the TF-IDF transformed data
- Random state is set to 42 for reproducibility

### 4. Model Evaluation:
- The model's accuracy is calculated on the test dataset
- A classification report shows precision, recall, and F1-score for each class
- A confusion matrix visualizes the performance across different classes

### 5. Sentiment Prediction Function:
- A function `predict_text_dt` is implemented to:
  - Take new text input
  - Clean and preprocess it
  - Transform it using the trained TF-IDF vectorizer
  - Predict sentiment using the trained model

## Evaluation Results
- **Test Accuracy:** Approximately 90%
- The confusion matrix helps visualize where the model performs well and where it might need improvement
- The classification report provides detailed metrics for each sentiment class

## Conclusion
The Twitter sentiment analysis system built with a Decision Tree classifier and TF-IDF vectorization demonstrates effective performance in predicting sentiment from tweet text. This model can be valuable for social media monitoring, brand sentiment analysis, and public opinion research.

## Future Improvements
- Experiment with other classifiers like Random Forest or SVM
- Implement more advanced text preprocessing techniques
- Consider using word embeddings or transformer-based models
- Add more features like tweet length, hashtag count, etc.
