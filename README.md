# 📚 Telecom RAG Assistant

An end-to-end Retrieval-Augmented Generation (RAG) system that answers questions from PDF documents using:

- LangChain
- ChromaDB
- HuggingFace Embeddings
- Groq LLM (Qwen3-32B)

---

## 🚀 Features

- PDF document ingestion
- Intelligent chunking
- Semantic embeddings
- Vector database storage
- Similarity search retrieval
- Grounded question answering
- Interactive chatbot

---


## 🛠️ Tech Stack

- Python
- LangChain
- ChromaDB
- HuggingFace Embeddings
- Sentence Transformers
- Groq
- Qwen3-32B
- VS Code

---

## 📂 Project Structure

```bash
telecom-rag-assistant/
│
├── telecom_guide.pdf
│
├── RAG_Pipeline.ipynb
│
├── .env
├── .gitignore
├── LICENSE
├── README.md
└── requirements.txt
```

---

## ▶️ Installation

```bash
git clone https://github.com/yourusername/telecom-rag-assistant.git

cd Telecom-RAG-assistant

pip install -r requirements.txt
```

---

## 🔑 Configure API Key

Create a `.env` file:

```text
GROQ_API_KEY=your_api_key
```

---

## ▶️ Run

Open:

```bash
RAG_Pipeline.ipynb
```

Run all cells sequentially.

---

## 📈 Pipeline

1. Load PDF
2. Split into chunks
3. Generate embeddings
4. Store vectors in ChromaDB
5. Retrieve relevant chunks
6. Generate answer using Groq LLM

---
