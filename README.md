# 📰 Fake News Detection using Deep Learning (LSTM, BiLSTM, CNN+BiLSTM)

## 📌 Project Overview

This project focuses on detecting fake news using deep learning models such as **LSTM**, **Bidirectional LSTM (BiLSTM)**, and a hybrid **CNN + BiLSTM** architecture. The models are trained on labeled news datasets to classify whether a news article is **real** or **fake** based on its title.

---

## 📂 Dataset# 📰 Fake News Detection using Deep Learning (LSTM, BiLSTM, CNN+BiLSTM)

## 📌 Project Overview

This project focuses on detecting fake news using deep learning models such as LSTM, Bidirectional LSTM (BiLSTM), and a hybrid CNN + BiLSTM architecture. The models are trained on labeled news datasets to classify whether a news article is real or fake based on its title.

---

## 📂 Dataset

The project uses two datasets:

* `True.csv` → Contains real news articles
* `Fake.csv` → Contains fake news articles

Each dataset includes:

* `title` → Headline of the news
* `text` → Full article (used partially)
* `subject` → Category of the news

---

## ⚙️ Installation

Install the required libraries before running the notebook:

```bash
pip install nltk
pip install wordcloud
pip install gensim
pip install keras
pip install tensorflow
pip install seaborn
```

---

## 🚀 Workflow

### 1. Data Loading

* Load datasets using pandas
* Inspect and visualize the data

### 2. Data Visualization

* Distribution of news subjects
* Word clouds for real and fake news titles
* Title length distribution

### 3. Data Preprocessing

* Add labels:

  * `1` → Real news
  * `0` → Fake news
* Merge datasets
* Shuffle data
* Split into:

  * Training set (64%)
  * Validation set (16%)
  * Test set (20%)

### 4. Text Cleaning

* Tokenization using gensim
* Remove stopwords
* Remove short words (≤2 characters)

### 5. Tokenization & Padding

* Convert text into sequences using Keras Tokenizer
* Apply padding to ensure equal input length

---

## 🧠 Models Implemented

### 🔹 1. LSTM Model

* Embedding layer
* LSTM layer
* Dense output layer

### 🔹 2. Bidirectional LSTM (BiLSTM)

* Embedding layer
* Bidirectional LSTM
* Dropout for regularization

### 🔹 3. CNN + BiLSTM Model

* Embedding layer
* Convolutional layer (Conv1D)
* MaxPooling layer
* Bidirectional LSTM
* Dense output layer

---

## 📊 Training

* Loss function: Binary Crossentropy
* Optimizer: Adam
* Batch size: 64
* Model training performed on training set
* Validation done using validation set

---

## 📈 Evaluation

* Predictions made on test dataset
* Output converted to binary labels (0 or 1)
* Accuracy calculated using sklearn metrics

---

## 🔍 Manual Testing

A custom function is implemented to test new news headlines:

```python
predict_news_cnn_bilstm("Sample news headline here")
```

---

## 🛠️ Key Libraries Used

* TensorFlow / Keras
* Pandas, NumPy
* NLTK
* Gensim
* Matplotlib, Seaborn
* WordCloud

---

## 📌 Results

* All three models are evaluated and compared
* Hybrid CNN + BiLSTM generally improves feature extraction and performance

---

## 📎 Future Improvements

* Use full article text instead of only titles
* Apply pretrained embeddings (Word2Vec, GloVe)
* Hyperparameter tuning
* Deploy as a web application

---

## 👨‍💻 Author

Developed as part of a machine learning/deep learning project on fake news detection.

---


The project uses two datasets:

* `True.csv` → Contains real news articles
* `Fake.csv` → Contains fake news articles

Each dataset includes:

* `title` → Headline of the news
* `text` → Full article (used partially)
* `subject` → Category of the news

---

## ⚙️ Installation

Install the required libraries before running the notebook:

```bash
pip install nltk
pip install wordcloud
pip install gensim
pip install keras
pip install tensorflow
pip install seaborn
```

---

 🚀 Workflow

 1. Data Loading

* Load datasets using pandas
* Inspect and visualize the data

 2. Data Visualization

* Distribution of news subjects
* Word clouds for real and fake news titles
* Title length distribution

 3. Data Preprocessing

* Add labels:

  * `1` → Real news
  * `0` → Fake news
* Merge datasets
* Shuffle data
* Split into:

  * Training set (64%)
  * Validation set (16%)
  * Test set (20%)

 4. Text Cleaning

* Tokenization using `gensim`
* Remove stopwords
* Remove short words (≤2 characters)

 5. Tokenization & Padding

* Convert text into sequences using Keras Tokenizer
* Apply padding to ensure equal input length

---

 🧠 Models Implemented

 🔹 1. LSTM Model

* Embedding layer
* LSTM layer
* Dense output layer

🔹 2. Bidirectional LSTM (BiLSTM)

* Embedding layer
* Bidirectional LSTM
* Dropout for regularization

 🔹 3. CNN + BiLSTM Model

* Embedding layer
* Convolutional layer (Conv1D)
* MaxPooling layer
* Bidirectional LSTM
* Dense output layer

---

 📊 Training

* Loss function: Binary Crossentropy
* Optimizer: Adam
* Batch size: 64
* Model training performed on training set
* Validation done using validation set


 📈 Evaluation

* Predictions made on test dataset
* Output converted to binary labels (0 or 1)
* Accuracy calculated using sklearn metrics



 🔍 Manual Testing

A custom function is implemented to test new news headlines:

```python
predict_news_cnn_bilstm("Sample news headline here")
```



 🛠️ Key Libraries Used

* TensorFlow / Keras
* Pandas, NumPy
* NLTK
* Gensim
* Matplotlib, Seaborn
* WordCloud

---

 📌 Results

* All three models are evaluated and compared
* Hybrid CNN + BiLSTM generally improves feature extraction and performance

---

📎 Future Improvements

* Use full article text instead of only titles
* Apply pretrained embeddings (Word2Vec, GloVe)
* Hyperparameter tuning
* Deploy as a web application

