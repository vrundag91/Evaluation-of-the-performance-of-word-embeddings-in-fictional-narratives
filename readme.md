# 📚 Evaluating Word Embeddings in Fictional Narratives

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue.svg)](https://www.python.org/)  
[![Jupyter Notebook](https://img.shields.io/badge/Jupyter_Notebook-%F0%9F%93%96-orange)](https://jupyter.org/)  

### 🚀 A Comparative Study of Word2Vec, FastText, and GloVe in Literary Text Analysis

This repository provides a **Jupyter Notebook implementation** of a research study comparing **Word2Vec, FastText, and GloVe** for analyzing **fictional narratives**. The code processes text from **epic, fantasy, and detective fiction** to examine how these word embeddings handle **semantic relationships, analogy tasks, and word clustering**.

---

## 📌 Features
✅ **Preprocesses Fictional Text** – Tokenization, stopword removal, lemmatization  
✅ **Trains Word2Vec & FastText Models** – Captures semantic meaning from text  
✅ **Loads Pretrained GloVe Vectors** – Uses Stanford's 100D embeddings  
✅ **Evaluates Cosine Similarity** – Measures semantic closeness of words  
✅ **Performs Analogy Tasks** – Tests conceptual relationships between words  
✅ **Visualizes Embeddings (PCA/t-SNE)** – Shows word clusters in 2D space  
✅ **Computes Clustering Quality (Silhouette Score)** – Evaluates embedding effectiveness  

---

## 📂 Repository Structure

```bash
📂 word-embeddings-fiction
│── 📜 README.md            # Documentation for the repository
│── 📜 requirements.txt      # List of required Python dependencies
│── 📜 word_embeddings.ipynb # Jupyter Notebook with full implementation
│── 📜 glove.6B.100d.txt     # Pretrained GloVe embeddings (downloaded)
│── 📜 word2vec_fiction.model # Saved Word2Vec model
│── 📜 fasttext_fiction.model # Saved FastText model
```
## 🔧 Installation & Setup

### 1️⃣ **Clone the Repository**
Clone the GitHub repository to your local system:
```bash
git clone https://github.com/vrundag91/Evaluation-of-the-performance-of-word-embeddings-in-fictional-narratives.git
cd word-embeddings-fiction
```
###2️⃣ **Create a Virtual Environment (Optional but Recommended)**
```bash
python3 -m venv env
source env/bin/activate  # For Mac/Linux
env\Scripts\activate     # For Windows
```
### 3️⃣ **Install Required Dependencies**
```bash
pip install -r requirements.txt
```
### 4️⃣ **Download & Extract Pretrained GloVe Embeddings**
Run the following command inside a Python script or Jupyter Notebook:
```bash
import urllib.request
import zipfile

glove_url = "http://nlp.stanford.edu/data/glove.6B.zip"
urllib.request.urlretrieve(glove_url, "glove.6B.zip")

with zipfile.ZipFile("glove.6B.zip", 'r') as zip_ref:
    zip_ref.extractall("glove_data")

print("GloVe embeddings downloaded and extracted!")

```

## 📊 Key Findings

1️⃣ **FastText performs best for fictional text** as it handles **rare words & invented vocabulary** (e.g., *"Muggle"* in Harry Potter).  
2️⃣ **Word2Vec is effective for structured texts** but struggles with **out-of-vocabulary (OOV) words**.  
3️⃣ **GloVe performs well on general NLP tasks** but lacks **genre-specific adaptability** for fiction.  
4️⃣ **FastText produces better-defined clusters** in **t-SNE and PCA visualizations**.  
5️⃣ **Silhouette Score confirms FastText forms stronger semantic clusters** compared to Word2Vec & GloVe.  


