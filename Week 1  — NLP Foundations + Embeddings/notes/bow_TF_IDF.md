
---

## 🧰 Bag of Words (BoW)

### 🔹 What it is:
- Represents text as a **collection of words** (ignores grammar and word order).
- Creates a **vocabulary** from all documents.
- Each document is represented as a **vector of word counts**.

### 🔹 Key Features:
- Simple and fast.
- Each word becomes a feature.
- Values are just **frequencies** (how many times a word appears).

### 🔹 Example:
For two sentences:
- "I love NLP"
- "NLP is fun"

Vocabulary: `["I", "love", "NLP", "is", "fun"]`

Vectors:
- Sentence 1 → `[1, 1, 1, 0, 0]`
- Sentence 2 → `[0, 0, 1, 1, 1]`

---

## 📊 TF-IDF (Term Frequency–Inverse Document Frequency)

### 🔹 What it is:
- A **weighted version** of BoW.
- Highlights **important words** by reducing the weight of common ones.

### 🔹 Formula:
- **TF** = Term Frequency (how often a word appears in a document)
- **IDF** = Inverse Document Frequency (how rare a word is across documents)
- **TF-IDF** = TF × IDF

### 🔹 Key Features:
- Reduces impact of **common words** (like "the", "is").
- Better for **information retrieval** and **text classification**.

### 🔹 Example:
If "NLP" appears often in one document but rarely in others, it gets a **high TF-IDF score**.

---

## 🆚 BoW vs TF-IDF

| Feature           | BoW                          | TF-IDF                              |
|------------------|------------------------------|-------------------------------------|
| Simplicity        | Very simple                  | Slightly more complex               |
| Word Importance   | Not considered               | Considered via IDF                  |
| Common Words      | High weight                  | Low weight                          |
| Use Cases         | Basic NLP tasks              | Search engines, classification      |

---
