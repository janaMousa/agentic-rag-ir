# agentic-rag-ir
# Agentic RAG – IR Homework

This project demonstrates an **Agentic RAG workflow**:
- If the query is about **weather** → call an external **Weather API** (Open-Meteo)
- Otherwise → use **RAG**:
  1) chunk local documents (`data/docs.txt`)
  2) embed chunks (Sentence-Transformers)
  3) retrieve with FAISS
  4) generate an answer with citations using **Groq LLM**

## Repo structure
- `notebook.ipynb` – main implementation + demos
- `data/docs.txt` – knowledge base for RAG
- `requirements.txt` – dependencies
- `.env` – API keys (NOT committed)
- `presentation_notes.md` – explanation for the presentation/video

## Setup
### 1) Create venv + install dependencies
```bash
python -m venv .venv
.\.venv\Scripts\activate
pip install -r requirements.txt
