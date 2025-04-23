# Understanding Social Sentiment Through AI
### *A Machine Learning Approach to Sentiment Classification of Tweets*

This project focuses on classifying the sentiment of tweets into **positive**, **neutral**, or **negative** using a variety of machine learning techniques, including both traditional and neural network-based models. It provides a comparative analysis of ensemble methods, shallow neural networks, and deep learning architectures to determine the most effective approach for sentiment prediction.

---

## Objective

To accurately classify tweets by sentiment using diverse machine learning approaches, with a focus on optimizing performance metrics like accuracy and F1-score. The project also explores the impact of class imbalance, preprocessing methods, and model tuning.

---

## Dataset

The dataset contains tweets labeled as **positive**, **negative**, or **neutral**. It is split into:
- **Training set**: 11,767 tweets
- **Development set**: 1,317 tweets
- **Test set**: 1,455 tweets

Each tweet is preprocessed and labeled as:
- **Negative** = 0
- **Neutral** = 1
- **Positive** = 2

---

## Exploratory Data Analysis

- Class distribution and imbalance analysis
- Word clouds and frequency charts by sentiment
- Token counts, text lengths, and image analysis (if applicable)

---

## Preprocessing

- Removal of URLs, mentions, hashtags, digits, and punctuation
- Lowercasing, tokenization, and optional lemmatization
- Stopword removal and n-gram configuration
- Label encoding and feature splitting (`X`, `y`)

---

## Models Used & Results

### **Random Forest**
- TF-IDF + CountVectorizer
- Tuned with GridSearchCV
- **Test Accuracy**: 77%
- **F1 Scores**: Neg=0.87, Pos=0.64, Neu=0.54

### **XGBoost**
- TF-IDF + CountVectorizer
- Tuned with GridSearchCV
- **Test Accuracy**: 77%
- **F1 Scores**: Neg=0.86, Pos=0.59, Neu=0.65

### **Shallow Neural Network (Best)**
- Conv1D + Dense + Dropout + GlobalAvgPooling
- **Test Accuracy**: 79.59%
- **F1 Scores**: Neg=0.87, Pos=0.69, Neu=0.64

### **Deep Neural Network**
- Multiple Conv1D layers + GlobalMaxPooling + Dense
- **Test Accuracy**: 74.64%
- **F1 Scores**: Neg=0.85, Pos=0.60, Neu=0.55

---

## Evaluation Metrics

- Accuracy
- Precision, Recall, F1-score (per class)
- Classification report
- Confusion matrix
- Observations on class imbalance

---

## Conclusion

Among all the models evaluated, the **shallow neural network** demonstrated the best overall performance, achieving a **test accuracy of 79.59%** and strong F1 scores across sentiment classes. The project provides valuable insights into the comparative strengths of traditional ML and deep learning approaches for sentiment analysis on Twitter data.

---

## License

This project is for academic and educational use only. Data should be used in accordance with original dataset licensing.

