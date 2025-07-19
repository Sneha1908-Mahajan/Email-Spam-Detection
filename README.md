<h1>Email Spam Detection Project</h1>
<br><br>
<h3> Overview:</h3>
<p>This project focuses on detecting spam emails using Natural Language Processing (NLP) and Machine Learning. 
  The goal is to classify emails as "spam" or "non-spam" by analyzing text content and extracting key features.</p>

---

<b> Dataset:The dataset (spam.csv) contains:</b>
- type: Label indicating whether the email is "spam" or "non-spam".
- messages: The actual email text.

---

<b>Data Preprocessing</b>
1. Data Cleaning
- Dropped unnecessary columns (Unnamed: 2,Unnamed: 3, Unnamed: 4).
- Renamed columns for clarity (v1 → type, v2 → messages).
- Encoded the target variable (type) using LabelEncoder.
- Removed duplicate entries.
  </br></br>
2. Feature Engineering
- Added new features:
  - total_characters: Length of the email in characters.
  - total_words: Number of words in the email.
  - total_sentences: Number of sentences in the email.

---

 <b>Exploratory Data Analysis (EDA)</b>
1. Class Distribution
- Pie Chart shows an imbalance:
  - Non-spam: Majority (~87%).
  - Spam: Minority (~13%).
<br></br>
2. Email Length Analysis
- Spam emails tend to be longer (more characters) than non-spam emails.
- Histogram confirms this trend.

---

<b>Model Training</b>
Algorithms Used
- Naive Bayes
- Logistic Regression
- Random Forest
- Support Vector Machine (SVM)

<b>Steps</b>
1. Text Vectorization (TF-IDF, CountVectorizer).
2. Train-Test Split (80% training, 20% testing).
3. Model Evaluation (Accuracy, Precision, Recall, F1-Score).
4. Pickle Export(Saved models for deployment).

---

 <b>Streamlit Web App</b>
A user-friendly web app was built using Streamlit to:
-Input an email text.
-Predict** whether it is spam or not-spam.
-Display confidence scores.

<h3>How to Run the App</h3>
```bash
streamlit run spam_classifiaction_app.py
```

---

 <h3>Conclusion</h3>
- The model successfully classifies spam vs. non-spam emails with high accuracy.
- Spam emails are typically longer and contain specific patterns.

|
---

<h3></h3> Repository Structure</h3>
```
📁 email-spam-classification/</br>
<pre>├── notebooks&graphs</br></pre>
    <pre>-spam_classifier.ipynb                   # Jupyter Notebook (EDA & Modeling)</br></pre>
    <pre>-CorrelationHeatmap.png</br> </pre>
    <pre>-Heatmap.png</br></pre>
    <pre>-HistplotCharacter.png</br></pre>
    <pre>-HistplotWords.png</br></pre>
    <pre>-RocCurve.png</br></pre>
    <pre>-SVMConfusionMatrix.png</br></pre>
    <pre>-BarplotNotSpamCorpus.png</br></pre>
    <pre>-BarplotSpamCorpus.png</br></pre>
    <pre>-piechart.png</br></pre>
    <pre>├── spam.csv                             # Dataset</br></pre>
<pre>├── app  </br></pre>                
    <pre>-spam_classification_app.py              # Streamlit App</br></pre>  
<pre>├── models </br></pre>  
    <pre>-spam_classifier.pkl</br></pre>         
    <pre>-vectorizer.pkl                          # Trained Model (Pickle)</br></pre>  
<pre>├── requirements.txt</br></pre>  
<pre>├── .gitignore</br></pre>  
<pre>└──  README.md                               # Project Documentation</br></pre>  
```

