📧 Spam SMS & Email Classifier (NLP + Machine Learning)

A machine learning model that classifies text messages as Spam or Ham using Natural Language Processing and TF-IDF vectorization.
This project demonstrates data preprocessing, feature engineering, model training, evaluation, and model deployment using .pkl files.

🚀 Features

✔️ Classifies SMS & emails as spam or not spam

✔️ Uses TF-IDF for text vectorization

✔️ Achieved 95–98% accuracy with Multinomial Naive Bayes

✔️ Complete text cleaning pipeline:

lowercasing

punctuation removal

stopword removal

stemming

✔️ Trained model + TF-IDF vectorizer saved as .pkl files

✔️ Well-structured and easily deployable

📂 Project Structure
│── data/
│   └── spam.csv
│
│── model/
│   ├── spam_model.pkl
│   └── tfidf.pkl
│
│── notebook/
│   └── spam_classifier.ipynb
│
│── README.md
│── requirements.txt
📊 Dataset

The dataset used is the SMS Spam Collection Dataset.

📌 Kaggle Source:
https://www.kaggle.com/datasets/uciml/sms-spam-collection-dataset

It contains 5574 labeled messages:

ham → legitimate message

spam → unwanted advertisement / scam

🧠 Machine Learning Workflow

Load dataset

Cleaning & Preprocessing

lowercase

remove punctuation

remove stopwords

stemming using PorterStemmer

Vectorization

TF-IDF using TfidfVectorizer

Train/Test Split

Model Training

Multinomial Naive Bayes

Evaluation

accuracy score

classification report

Save Model

spam_model.pkl

tfidf.pkl

🛠️ Technologies Used

Python

Pandas, NumPy

NLTK

Scikit-learn

TF-IDF Vectorizer

Multinomial Naive Bayes

Pickle

Google Colab

📈 Model Performance
Metric	Score
Accuracy	95–98%
Precision	High
Recall	High
F1-Score	High
🧪 Testing the Model

Example:

import pickle

model = pickle.load(open('model/spam_model.pkl', 'rb'))
tfidf = pickle.load(open('model/tfidf.pkl', 'rb'))

msg = "Congratulations! You won a free iPhone! Click here!"
# preprocess message
msg_clean = preprocess(msg)
vector = tfidf.transform([msg_clean])

prediction = model.predict(vector)
print(prediction)  # 1 = spam, 0 = ham
📦 Installation
pip install -r requirements.txt
📜 How to Run

Clone this repository

Open the notebook:

notebook/spam_classifier.ipynb

Run all cells

Model files will be generated inside /model/

Test with your own messages

🙌 Author

Gaurav Kumar
(You can add your GitHub link here: https://github.com/gauravkumar82q
)

⭐ Show Your Support

If you like this project, please ⭐ the repository!