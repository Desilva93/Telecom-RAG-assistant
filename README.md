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
├── telecom_guide.pdf
├── RAG.ipynb
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
RAG.ipynb
```

Run all cells sequentially.

---

## 📈 RAG Pipeline

### 1. Document Loading
The system loads the PDF document using LangChain's `PyPDFLoader`. Each page is extracted and converted into a structured document object.

### 2. Text Chunking
The extracted text is divided into smaller overlapping chunks using `RecursiveCharacterTextSplitter`.

Benefits:
- Better retrieval accuracy
- Fits embedding model limits
- Preserves context through overlap

### 3. Embedding Generation
Each chunk is converted into a dense vector representation using the HuggingFace embedding model:

```text
sentence-transformers/all-MiniLM-L6-v2
```

The embedding captures the semantic meaning of the text.

### 4. Vector Storage
The generated embeddings are stored in ChromaDB, a vector database optimized for similarity search.

Each record contains:
- Chunk text
- Embedding vector
- Metadata

### 5. User Query Processing
When a user asks a question, the query is embedded using the same embedding model to ensure both documents and queries exist in the same vector space.

### 6. Retrieval
ChromaDB performs similarity search and retrieves the top-k most relevant chunks related to the user's question.

### 7. Context Augmentation
The retrieved chunks are combined and inserted into a prompt template along with the user question.

### 8. Answer Generation
The augmented prompt is sent to the Groq-hosted Qwen3-32B model, which generates an answer grounded in the retrieved context.

### 9. Final Response
The generated response is returned to the user along with information retrieved from the PDF, reducing hallucinations and improving factual accuracy.
