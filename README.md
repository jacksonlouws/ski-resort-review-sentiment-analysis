# Ski Resort Review Sentiment Analysis

## Project Overview

This project builds an end-to-end sentiment analysis pipeline for ski resort reviews, transforming unstructured customer feedback into structured, actionable insights.

The workflow includes:
- text preprocessing and cleaning  
- feature engineering using TF-IDF  
- training a Logistic Regression classification model  
- evaluating model performance  
- improving results through threshold tuning  
- interpreting key drivers of sentiment  

The goal is to classify reviews as positive or negative and demonstrate how customer feedback can be used to support data-driven decision-making.

---

## Dataset Overview

**Source:** OnTheSnow Ski Area Reviews (Kaggle)  
**Total Reviews:** ~18,000  
**Format:** CSV  

The dataset contains ski resort reviews across North America, including:
- written review text  
- star ratings (1–5)  
- basic metadata  

For this project, star ratings are converted into binary sentiment labels:

- `1` = positive (ratings ≥ 3)  
- `0` = negative (ratings < 3)  

---

## Project Structure

├── text_preprocessing.ipynb # Data cleaning and preprocessing pipeline
├── text_classification.ipynb # Model training, evaluation, and prediction
├── ski_reviews_binary.csv # Final cleaned dataset
└── README.md


---

## Methodology

### 1. Text Preprocessing
- Removed noise (punctuation, special characters, URLs)
- Tokenized and lemmatized text
- Removed stopwords
- Filtered out extreme review lengths
- Generated cleaned text for modeling

---

### 2. Feature Engineering
- Applied **TF-IDF vectorization**
- Used **unigrams and bigrams** to capture context
- Limited vocabulary size to control dimensionality

---

### 3. Model Training
- Used **Logistic Regression** as a baseline classifier  
- Applied `class_weight="balanced"` to address class imbalance  
- Trained on TF-IDF feature vectors  

---

### 4. Model Evaluation
- Evaluated using:
  - Accuracy  
  - Precision  
  - Recall  
  - F1-score  
- Visualized results using a confusion matrix  

**Key Insight:**  
The model performed strongly on positive sentiment but showed lower recall for negative reviews due to class imbalance.

---

### 5. Threshold Tuning (Key Improvement)

To improve detection of negative sentiment, the classification threshold was increased from **0.50 → 0.60**.

**Impact:**
- Reduced false positives  
- Improved identification of negative reviews  
- Made the model more aligned with business needs  

This highlights an important real-world consideration:  
> model performance should be optimized based on business objectives, not just default metrics.

---

### 6. Model Interpretation
- Extracted top positive and negative features using model coefficients  
- Identified key words associated with satisfaction and dissatisfaction  

---

## Business Application

Although this dataset does not include Batawa Ski Hill reviews, the pipeline demonstrates how a similar model could be applied to real customer feedback.

Potential applications include:
- tracking customer satisfaction trends  
- identifying recurring service issues  
- flagging negative reviews for follow-up  
- supporting operational and marketing decisions  

---

## Key Takeaways

- TF-IDF + Logistic Regression provides a strong baseline for text classification  
- Class imbalance can significantly impact model behavior  
- Threshold tuning is a simple but effective way to improve practical performance  
- Model success should be measured based on business relevance, not just accuracy  

---

## Technologies Used

- Python  
- pandas, numpy  
- scikit-learn  
- matplotlib, seaborn  

---

## Future Improvements

- Test additional models (e.g., XGBoost, neural networks)  
- Optimize threshold using validation data  
- Apply model to real Batawa Ski Hill reviews  
- Extend to multi-class sentiment classification  

---

## Author

Jackson Louws  
Queen’s University — Commerce & Computer Science
