# AutoGen Multi-Agent Cover Letter Generator (Groq + RAG )

Generate tailored, ATS-friendly cover letters from a resume PDF and job description using a **multi-agent AutoGen pipeline** powered by **Groq-hosted LLaMA-3**.  
The app performs **RAG** over your resume (FAISS + MiniLM), then orchestrates agents (Parser → JD Analyzer → Matchmaker → Writer → Reviewer) to produce a concise letter.  
It also computes **quantitative metrics** (JD coverage, baseline vs semantic alignment, % improvement) so you can back claims with data.

---

## ✨ Features
- **Multi-agent workflow (AutoGen):** Parser, JD Analyzer, Matchmaker, Writer, Reviewer.
- **RAG over your resume:** FAISS + `all-MiniLM-L6-v2` embeddings for context retrieval.
- **Groq LLaMA-3 models:** Fast LLM inference via Groq’s OpenAI-compatible endpoint.
- **Robust PDF parsing:**  PyPDF2.
- **Metrics built-in:**
  - JD coverage (semantic) — % of JD lines mapped to resume achievements
  - Baseline vs semantic alignment accuracy
  - Relative improvement (%) over keyword overlap baseline
- **Gradio UI:** Upload PDF, enter role/company/JD, generate letter + metrics in one click.

---

## 🧱 Tech Stack
- **UI:** Gradio  
- **Agents:** AutoGen  
- **LLM:** Groq-hosted LLaMA-3 (OpenAI-compatible API)  
- **RAG:** FAISS (vector search) + MiniLM embeddings (SentenceTransformers)  
- **LangChain:** Community vector store + text splitters (with backwards-compatible imports)  
- **PDF:** PyPDF2  

---

