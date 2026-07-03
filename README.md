## Project Overview
Spam Email Detection using Machine Learning and RNN
<br><br>
This project builds a spam detection system using machine learning and deep learning techniques. <br>
It classifies email messages as Spam or Ham using Naive Bayes models and a Recurrent Neural Network (RNN).<br>
<br>
## Dataset
Datset: Kaggle - Spam Emails<br>
Contains labeled emails: Spam and Non-Spam (Ham)<br>
License: Apache 2.0
<br>
## Methodology
The project follows a standard NLP pipeline:<br>
Data loading and exploration<br>
Text preprocessing (cleaning and normalization)<br>
Train-test split<br>
Text vectorization using CountVectorizer (for Naive Bayes models)<br>
Tokenization and padding (for RNN model)<br>
<br>
## Models
Three models were implemented:
Multinomial Naive Bayes – based on word frequency (Bag-of-Words representation)
Bernoulli Naive Bayes – based on binary word presence/absence
Recurrent Neural Network (SimpleRNN) – captures sequential dependencies in text using embeddings

## Results
The models were evaluated using Accuracy, Precision, Recall, F1-score, and ROC-AUC.
<br><br>
Multinomial Naive Bayes<br>
Accuracy: ~98%<br>
ROC-AUC: 0.98<br>
Bernoulli Naive Bayes<br>
ROC-AUC: 0.997<br>
Strong ham recall (1.00), lower spam recall (0.87)<br>
RNN Model<br>
Accuracy: 99%<br>
ROC-AUC: 0.992<br>
Best balance between precision and recall<br>
<br>
## Business Impact
This system can be used to automatically filter spam messages in email or messaging platforms. It helps:<br>
<br>
Reduce phishing and scam exposure<br>
Improve user experience by filtering unwanted content<br>
Lower operational costs by reducing manual moderation<br>
Increase platform security and trust

