# Ski Resort Review Sentiment Analysis

## Overview
This project uses natural language processing and machine learning to analyze ski resort reviews and classify customer sentiment. The goal is to better understand what drives positive and negative guest experiences and how these insights can support data-driven decision-making.

## Objective
Build a classification model that predicts whether a review is positive or negative based on its text, and identify key factors that influence customer satisfaction.

## Dataset
The dataset consists of ski resort reviews from OnTheSnow.com, including review text and star ratings. Ratings were converted into binary sentiment labels:
- 0 = Negative (1–3 stars)
- 1 = Positive (4–5 stars)

## Tools & Technologies
- Python
- pandas
- scikit-learn
- NLP preprocessing (tokenization, stopword removal, lemmatization)
- TF-IDF vectorization
- Jupyter Notebook

## Methodology
- Cleaned and preprocessed raw review text
- Performed exploratory data analysis to understand sentiment distribution
- Converted text into numerical features using TF-IDF
- Trained a classification model (Logistic Regression)
- Evaluated performance using accuracy, precision, recall, and confusion matrix

## Results
- The model achieved strong performance in identifying positive vs negative reviews
- High recall for positive sentiment, with lower precision on negative sentiment (class imbalance impact)
- Identified key words and phrases associated with customer satisfaction and dissatisfaction

## Key Insights
- Positive reviews are strongly associated with factors like snow quality, terrain, and overall experience
- Negative reviews often highlight crowding, staff issues, and wait times
- Imbalanced data can significantly affect model performance, especially for minority classes

## Business Impact
This type of model can help ski resorts:
- Prioritize improvements based on customer feedback
- Detect recurring issues at scale
- Make more informed investment and operational decisions

## Project Structure
ski-resort-review-sentiment-analysis/
│
├── sentiment_analysis.ipynb
├── text_preprocessing.ipynb
├── data/
│   └── ski_reviews.csv
├── README.md
