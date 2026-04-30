📰 Fake News Detection Using NLP and Machine Learning
________________________________________
📌 1. Problem Statement
With the explosion of digital news sources, fake news has become a major threat to public trust and informed decision-making. The objective of this project is to develop an NLP-based machine learning model to classify news articles as either true or fake, based on their textual content.
________________________________________
🧪 2. Methodology (Tasks from Starter Notebook)
1. Data Preparation
•	Combined True.csv and Fake.csv datasets, each containing title, text, and publication date.
•	Assigned labels: 1 for true, 0 for fake.
2. Text Preprocessing
•	Performed tokenization, lowercasing, punctuation and digit removal.
•	Used spaCy for lemmatization and stopword removal.
3. Train-Validation Split
•	Split data using an 80:30 ratio for training and validation.
4. Exploratory Data Analysis (EDA)
•	Plotted distribution of character lengths before and after preprocessing.
•	Generated word clouds to analyze common terms in both true and fake news.
•	Displayed top 10 unigrams, bigrams, and trigrams for both fake and true news.
5. Feature Extraction
•	Applied TF-IDF Vectorization to transform text into numerical format.
•	Additionally, used pre-trained embedding’s with word2vec-google-news-300 from the Gensim API:
o	import gensim.downloader as api
o	word2vec_model = api.load('word2vec-google-news-300')
•	These embedding’s enabled semantic similarity checks and enhanced understanding of context beyond surface-level token frequency.
6. Model Training and Evaluation
•	Trained and tested Random Forest, Logistic Regression, and Decision Tree classifiers.
•	Chose Random Forest as the best model based on evaluation metrics.
________________________________________
📊 3. Visualizations
🏢 Distribution of Character Lengths – Cleaned Text
⚙️ Distribution of Character Lengths – Lemmatized Text
✅ Word Cloud – True News
❌ Word Cloud – Fake News
________________________________________
⚙️ 4. Techniques Used
•	Preprocessing: spaCy for lemmatization and stopword removal
•	TF-IDF Vectorization: Converted text to weighted word vectors
•	Word Embedding’s: Pre-trained Word2Vec (word2vec-google-news-300) for semantic vectorization
•	Classification Models: Random Forest (best), Logistic Regression, Decision Tree
•	Metrics: Accuracy, Precision, Recall, F1 Score, Confusion Matrix
________________________________________
🏆 5. Model Results
•	Best Model: ✅ Random Forest
•	Accuracy: 0.9003
•	Precision: 0.9082
•	Recall: 0.8817
•	F1 Score: 0.8947
F1 Score was prioritized to balance false positives and false negatives.
________________________________________
🔍 6. Insights & Conclusion
•	True news used structured language tied to real events; fake news favored sensational tone.
•	Semantic classification via TF-IDF and Word2Vec helped reveal deeper contextual meaning.
•	Random Forest achieved nearly 90% accuracy and generalizable results.
•	Effective for real-world tools in news filtering, fact-checking, and misinformation detection.


