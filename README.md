# Spam Email Detection using Machine Learning and RNN

## Project Overview
This project builds a spam detection system using machine learning and deep learning techniques. It classifies email messages as Spam or Ham using Naive Bayes models and a Recurrent Neural Network (RNN).

---

## Dataset
Dataset: Kaggle – Spam Emails  
Contains labeled emails: Spam and Non-Spam (Ham)  
License: Apache 2.0  

---

## Methodology
The project follows a standard NLP pipeline:

- Data loading and exploration  
- Text preprocessing (cleaning and normalization)  
- Train-test split  
- Text vectorization using CountVectorizer (for Naive Bayes models)  
- Tokenization and padding (for RNN model)  

---

## Models
Three models were implemented:

- Multinomial Naive Bayes – based on word frequency (Bag-of-Words representation)  
- Bernoulli Naive Bayes – based on binary word presence/absence  
- Recurrent Neural Network (SimpleRNN) – captures sequential dependencies in text using embeddings  

---

## Results

### Multinomial Naive Bayes
- Accuracy: ~98%  
- ROC-AUC: 0.98  

### Bernoulli Naive Bayes
- ROC-AUC: 0.997  
- Strong ham recall (1.00), lower spam recall (0.87)  

### RNN Model
- Accuracy: 99%  
- ROC-AUC: 0.992  
- Best balance between precision and recall  

---

## Business Impact
This system can be used to automatically filter spam messages in email or messaging platforms. It helps:

- Reduce phishing and scam exposure  
- Improve user experience by filtering unwanted content  
- Lower operational costs by reducing manual moderation  
- Increase platform security and trust  

---

## How to Run

```bash
# Clone repository
git clone https://github.com/your-username/spam-detection

# Install dependencies
pip install -r requirements.txt

# Open notebooks
jupyter notebook
