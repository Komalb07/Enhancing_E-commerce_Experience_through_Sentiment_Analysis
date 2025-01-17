# Enhancing E-commerce Experience through Sentiment Analysis

This repository contains the implementation of a **Sentiment Analysis Tool** designed to enhance e-commerce platforms by categorizing customer feedback into **positive**, **negative**, and **neutral** sentiments. The project leverages machine learning models and advanced data balancing techniques to improve user experience and provide actionable insights for e-commerce stakeholders.

## Project Overview

Customer feedback plays a crucial role in e-commerce, offering insights into user satisfaction and product performance. However, analyzing vast amounts of textual data manually is time-consuming and error-prone. This project automates sentiment analysis by:

- Preprocessing and analyzing customer reviews.
- Employing robust sampling techniques to handle imbalanced data.
- Using machine learning models to classify sentiments with high accuracy.
- Providing a user-friendly interface for real-time sentiment predictions.

By automating sentiment analysis, the project enhances decision-making and user satisfaction on e-commerce platforms.

## Key Features

1. **Data Preprocessing**:
   - Cleaned and tokenized textual data from the Flipkart Customer Reviews dataset.
   - Transformed text into numerical vectors using the **TF-IDF Vectorizer**.

2. **Data Balancing**:
   - Addressed data imbalance using:
     - Random Under-Sampling (RUS)
     - Tomek Links
     - SMOTE (Synthetic Minority Oversampling Technique)

3. **Machine Learning Models**:
   - Implemented the following classifiers:
     - Support Vector Machine (SVM)
     - Random Forest
     - Gradient Boosting Machine
   - Evaluated models using F1 Score and Recall Score for accuracy on imbalanced datasets.

4. **Interactive User Interface**:
   - Users can input text reviews and receive real-time sentiment predictions.
   - Integrated actions based on predictions:
     - Redirecting negative reviews to email support.
     - Encouraging surveys for neutral feedback.
     - Sending a thank-you note for positive reviews.

## Methodology

### 1. Dataset
- **Source**: Flipkart Product Customer Reviews Dataset (Kaggle)
- **Details**:
  - Total Rows: 205,052
  - Features: `product_name`, `product_price`, `Rate`, `Review`, `Summary`, and `Sentiment`
  - Target: `Sentiment` (Positive, Negative, Neutral)

### 2. Sampling Techniques
- Addressed the dataset's imbalance:
  - Positive Sentiments: 147,171
  - Negative Sentiments: 24,401
  - Neutral Sentiments: 8,807

- Applied Random Under-Sampling, Tomek Links, and SMOTE to ensure unbiased model training.

### 3. Modeling
- Preprocessed data was split into training and testing sets (75% train, 25% test).
- Implemented SVM, Random Forest, and Gradient Boosting Classifiers.
- Evaluated models using:
  - **F1 Score**: Balances precision and recall.
  - **Recall Score**: Ensures effective identification of relevant sentiments.

### 4. Visualization
- Visualized sentiment distribution before and after sampling using bar plots.

### 5. Real-Time Sentiment Analysis
- Developed an interactive system:
  - Input: Customer review
  - Output: Sentiment classification (Positive, Negative, Neutral)
  - Actions: Email redirection, survey invitation, or acknowledgment.

## Results

For Random Under Sampling: 

| Model                  | F1 Score | Recall Score |
|------------------------|----------|--------------|
| Support Vector Machine | *0.9175*  | *0.9134*      |
| Random Forest          | *0.9043*  | *0.8988*      |
| Gradient Boosting      | *0.9118*  | *0.9068*      |

For Tomek Links Sampling: 

| Model                  | F1 Score | Recall Score |
|------------------------|----------|--------------|
| Support Vector Machine | *0.9359*  | *0.9416*      |
| Random Forest          | *0.9315*  | *0.9370*      |
| Gradient Boosting      | *0.9291*  | *0.9346*      |

For RUS + SMOTE Sampling: 

| Model                  | F1 Score | Recall Score |
|------------------------|----------|--------------|
| Support Vector Machine | *0.9087*  | *0.9006*      |
| Random Forest          | *0.8936*  | *0.8818*      |
| Gradient Boosting      | *0.9020*  | *0.8859*      |

## Repository Structure

```
Ecommerce-Sentiment-Analysis/
├── data/                     # Dataset and preprocessed files
├── notebooks/                # Jupyter notebooks for analysis
├── scripts/                  # Python scripts for preprocessing, sampling, and modeling
├── requirements.txt          # Python dependencies
├── README.md                 # Project documentation
└── sentiment_analysis.py     # Main script for running sentiment analysis
```

## Future Enhancements

- **Cross-Language Support**: Expand sentiment analysis to handle multiple languages.
- **Real-Time Analysis**: Integrate real-time processing for streaming customer reviews.
- **Feature Expansion**: Incorporate contextual features like user demographics and product categories.
