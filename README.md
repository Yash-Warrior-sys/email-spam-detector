# Email Spam Detection Using Machine Learning

**Email Spam Detection** is a Machine Learning project built to classify emails/messages as **Spam** or **Ham (Not Spam)** based on their text content.

The system uses natural language processing and classic ML models to learn spam patterns from a labeled dataset, then serves predictions through a simple Streamlit web app.

---

## Features

- Text preprocessing: lowercase conversion, punctuation removal
- Feature extraction using TF-IDF Vectorizer
- Multiple ML models trained and compared on the same data
- Best model automatically selected by F1 score (not fixed to one algorithm)
- Live prediction frontend built with Streamlit

---

## Models Trained & Evaluated

The following models are trained and evaluated using accuracy, precision, recall, and F1 score:

- Naive Bayes
- Logistic Regression
- Linear SVM

> The model used in the Streamlit app is **whichever of the three scores highest on F1** during training — the notebook prints which one was picked.

---

## Tech Stack

- Python
- Streamlit
- scikit-learn
- pandas
- pickle
- nltk

---

## Dataset

- File: `mail_data.csv`
- Labeled text data with a `label` column (spam/ham) and a `text` column.

---

## How It Works

1. User pastes email/message text into the Streamlit app.
2. The text is cleaned and transformed using the trained TF-IDF vectorizer.
3. The vectorized input is passed to the selected model.
4. The app outputs `Spam` or `Ham` as the prediction.

---

## Project Structure

```
email-spam-detector/
├── app/
│   ├── app.py          # Streamlit app
│   ├── model.pkl        # Trained model
│   └── vectorizer.pkl   # Trained TF-IDF vectorizer
├── data/
│   └── mail_data.csv    # Training dataset
├── notebooks/
│   └── email_spam_training.ipynb   # Preprocessing, training, model selection
├── requirements.txt
└── README.md
```

---

## Running Locally

```
pip install -r requirements.txt
cd app
streamlit run app.py
```

---

## Team — Group D

- Yash Kharode
- Vibhavari Shrikant Kadam
- Monika
- Shriratn Ramkishan Atpalwad
- Aditya Shrikant Nigde

---

## License

This project is licensed under the [MIT License](LICENSE).
