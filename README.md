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
The project follows a standard NLP pipeline to ensure robust classification performance:

- **Data Loading and Exploration:** Initial audit of the dataset to understand class distribution and potential issues.
- **Data Quality Assessment:** Verification of null and missing values, including checking for placeholders like "None" to ensure data integrity.
- **Exploratory Data Analysis (EDA):** Analysis of message length distributions, revealing that non-spam (ham) emails typically cluster under 100 characters, whereas spam emails tend to be longer, peaking around 160 characters.
- **Label Encoding:** Conversion of categorical labels ("ham", "spam") into numerical values (0, 1) for model compatibility.
- **Train-Test Split:** Splitting the data into training (80%) and testing (20%) sets, using stratification to maintain the original class proportions.
- **Text Vectorization:** - **Bag of Words:** Used `CountVectorizer` to convert raw text into numerical frequency matrices for Naive Bayes models.
    - **Tokenization & Padding:** Applied `Tokenizer` and `pad_sequences` to transform text into numerical sequences, preserving word order for the RNN architecture.

---

## Models
Three distinct modeling strategies were implemented to address different business priorities:

- **Multinomial Naive Bayes:** A baseline model leveraging word frequency counts.
- **Bernoulli Naive Bayes:** A model utilizing binary features to indicate the presence or absence of specific terms.
- **Recurrent Neural Network (SimpleRNN):** A deep learning approach incorporating an Embedding layer (dimension=100), a SimpleRNN layer (128 units), and Dropout (0.3) to capture semantic relationships and sequential dependencies.

---

## Results

### Multinomial Naive Bayes
- Precision (Spam): 0.95  
- Recall (Spam): 0.93  
- ROC-AUC: 0.98  

### Bernoulli Naive Bayes
- Precision (Spam): 0.98  
- Recall (Spam): 0.87  
- ROC-AUC: 0.997  

### RNN Model
- Precision (Spam): 0.98  
- Recall (Spam): 0.91  
- ROC-AUC: 0.992  
- Best balance between precision and recall  

---

## Business Impact
This system is designed for deployment within real-world email or SMS filtering pipelines. Key benefits include:

- **Enhanced Security:** High recall for spam allows for the proactive identification of phishing and fraudulent links, minimizing user risk.
- **Platform Trust:** Automated filtering improves the overall user experience by reducing exposure to unwanted content.
- **Efficiency:** Reducing the volume of spam increases operational efficiency and lowers the costs associated with manual moderation.
- **Business Continuity:** High precision ensures that legitimate communications are not incorrectly flagged (false positives), avoiding potential revenue loss or negative impacts on customer relationships.

---

## How to Run

```bash
# Clone repository
git clone https://github.com/your-username/spam-detection

# Install dependencies
pip install -r requirements.txt

# Open notebooks
jupyter notebook
