 NLP Tasks Overview

 1. Sentiment Analysis  
**Objective:** Classify tweets as having positive or negative sentiment.  
**Techniques Used:**  
- **Traditional ML:**
  - Preprocessing with `tweet-preprocessor`
  - Feature extraction using `TfidfVectorizer`
  - Classification using `RandomForestClassifier`
- **Transformer Model:**
  - `DistilBERT` via Hugging Face's `pipeline("sentiment-analysis")` for direct sentence-level classification

---

2. Named Entity Recognition (NER)  
**Objective:** Detect and classify named entities in text (e.g., person names, locations, organizations).  
**Techniques Used:**  
- **Transformer Model:**
  - Hugging Face’s `bert-large-cased-finetuned-conll03-english` via `pipeline("ner")`
- **Traditional ML:**
  - Dataset: CoNLL-style NER dataset (`ner_dataset.csv`)
  - Preprocessing using `TfidfVectorizer`
  - Classification using `LogisticRegression`

---

 3. Text Summarization  
**Objective:** Generate a concise summary from a longer input text.  
**Techniques Used:**  
- **Traditional NLP:**
  - Frequency-based summarization using SpaCy (based on word importance)
- **Transformer Model:**
  - `facebook/bart-large-cnn` from Hugging Face via `pipeline("summarization")`

---

 4. Translation (English ⇄ Arabic)  
**Objective:** Translate text between English and Arabic in both directions.  
**Techniques Used:**  
- **Transformer Model:**
  - `MarianMTModel` from Hugging Face
  - Models: `Helsinki-NLP/opus-mt-en-ar` and `opus-mt-ar-en`
  - Tokenization using `MarianTokenizer`

---

Data Sources
- `twitter_sentiment.csv` – used for training sentiment classifiers  
- `ner_dataset.csv` – used for training NER models with classical ML  

