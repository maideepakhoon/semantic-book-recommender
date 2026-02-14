 📚 Semantic Book Recommender

## Overview📌
This project is a semantic book recommendation system that uses vector embeddings and large language models to return relevant books based on natural language queries.

Instead of keyword matching, the system compares the **meaning** of a user’s query with book descriptions using vector similarity. This allows queries like:
> “A book about personal growth and overcoming challenges”

---

## Key Features
- Semantic search using vector embeddings  
- Natural language query support  
- Fiction / Non-Fiction classification using zero-shot learning  
- Sentiment and emotion analysis on book descriptions  
- Simple web interface built with Gradio  

---

## How It Works
- Book descriptions are cleaned and preprocessed in `data-exploration.ipynb`.
- Text is converted into vector embeddings using an LLM in `vector-search.ipynb`.
- Embeddings are stored and queried from a vector database built in `vector-search.ipynb`.
- User queries are embedded and compared with stored vectors using cosine similarity.
- Books are optionally filtered and enriched using:
  - zero-shot classification logic in `text-classification.ipynb`
  - sentiment and emotion extraction in `sentiment-analysis.ipynb`
- Final recommendations are displayed through a Gradio-based UI implemented in `gradio-dashboard.py`.


---

## Tech Stack
- Python 3.11  
- LangChain  
- OpenAI API  
- Chroma (Vector Database)  
- Transformers  
- Pandas  
- Gradio  

---

## Running the Project
```bash
pip install -r requirements.txt
python gradio-dashboard.py
