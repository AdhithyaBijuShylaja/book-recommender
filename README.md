# 📚 LLM Semantic Book Recommender

An AI-powered book recommendation system built with **LangChain**, **OpenAI embeddings**, and **Gradio**.  
This project demonstrates how to build a full semantic search and recommendation pipeline using large language models (LLMs).

---

## 🧩 Tutorial Components

There are five main parts to this tutorial:

1. **Text Data Cleaning**  
   📓 *Notebook:* `data-exploration.ipynb`  
   Cleans and explores raw book data downloaded from Kaggle.

2. **Semantic (Vector) Search & Vector Database**  
   📓 *Notebook:* `vector-search.ipynb`  
   Creates embeddings for each book description and stores them in a **Chroma** vector database for semantic search.  
   Example query: *“A book about a person seeking revenge.”*

3. **Text Classification (Zero-Shot LLM)**  
   📓 *Notebook:* `text-classification.ipynb`  
   Uses zero-shot classification to label each book as **Fiction** or **Non-Fiction**.

4. **Sentiment & Emotion Analysis**  
   📓 *Notebook:* `sentiment-analysis.ipynb`  
   Extracts emotional tones such as *Joy, Sadness, Fear, Anger, Surprise* so users can sort books by tone.

5. **Interactive Gradio Dashboard**  
   💻 *Script:* `gradio-dashboard.py`  
   A web application that lets users search for books by meaning, category, and emotion.

---

## 🧠 How It Works

1. Each book description is embedded using OpenAI’s `text-embedding-3-small` model (1 536-dimensional vectors).  
2. Vectors are stored in a local **Chroma** database.  
3. A user’s query is embedded the same way and compared using cosine similarity.  
4. The system filters by *Fiction/Non-Fiction* and sorts by emotion scores.  
5. Results appear instantly in a **Gradio** gallery interface.

---

## ⚙️ Requirements

This project was built with **Python 3.11**.

Install dependencies with:
```bash
pip install -r requirements.txt

Key libraries used:

kagglehub
pandas
matplotlib
seaborn
python-dotenv
langchain-community
langchain-opencv
langchain-chroma
transformers
gradio
notebook
ipywidgets

