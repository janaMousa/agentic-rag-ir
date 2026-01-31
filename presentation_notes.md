```md
## What is Agentic RAG in this project?
The system routes user queries:
- Weather-related → calls Open-Meteo API (real-time external data)
- IR/knowledge questions → uses RAG:
  - chunk local docs
  - embed
  - retrieve with FAISS
  - answer with Groq using citations [Source i]

## Why separate tools?
- Weather requires external factual data (API)
- IR explanations come from course notes in `data/docs.txt` (RAG)
- Groq is used only to generate the final response grounded in retrieved sources