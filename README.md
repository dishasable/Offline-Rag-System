# 🧠 Offline RAG System using Local LLMs

A fully offline **Retrieval-Augmented Generation (RAG)** system that allows users to query their own documents (PDF, DOCX, images) using local Large Language Models (LLMs) like **Gemma** and **DeepSeek** via Ollama.

---

## 🚀 Features

* 📂 Upload and process documents (PDF, DOCX, TXT, Images)
* 🔍 Semantic search using embeddings
* 🧠 Local LLM inference (no internet required)
* 🔐 Privacy-preserving (data never leaves your system)
* ⚡ Fast retrieval using ChromaDB
* 🎛️ Switch between multiple models (Gemma, DeepSeek)
* 🖥️ Interactive UI using Streamlit

---

## 🏗️ System Architecture

1. Document Upload
2. Text Extraction (PDF/DOCX/OCR)
3. Text Cleaning & Chunking
4. Embedding Generation
5. Store in Vector DB (ChromaDB)
6. User Query → Embedding
7. Similarity Search
8. Prompt Construction
9. LLM Response Generation

---

## 🧰 Tech Stack

* **Frontend:** Streamlit
* **Backend:** Python
* **LLM:** Ollama (Gemma, DeepSeek)
* **Embeddings:** nomic-embed-text
* **Vector DB:** ChromaDB
* **Framework:** LangChain

---

## 📁 Project Structure

```
offline_rag/
├── app.py
├── ingest.py
├── query.py
├── vector_store.py
├── embeddings.py
├── llm.py
├── config.py
├── requirements.txt
├── data/
├── chroma_db/
└── utils/
    ├── pdf_loader.py
    ├── docx_loader.py
    ├── ocr_loader.py
    └── text_cleaner.py
```

---

## ⚙️ Installation & Setup

### 1️⃣ Clone the repository

```bash
git clone <your-repo-link>
cd offline_rag
```

---

### 2️⃣ Create virtual environment

```bash
python -m venv rag_env
```

#### Activate:

**Windows**

```bash
rag_env\Scripts\activate
```

**Mac/Linux**

```bash
source rag_env/bin/activate
```

---

### 3️⃣ Install dependencies

```bash
pip install -r requirements.txt
```

---

### 4️⃣ Install Ollama

Download from: https://ollama.com

---

### 5️⃣ Pull required models

```bash
ollama pull nomic-embed-text
ollama pull gemma2:2b
# Optional:
ollama pull deepseek-r1:7b
```

---

## ▶️ Running the Application

```bash
streamlit run app.py
```

Then open:

```
http://localhost:8501
```

---

## 🧪 How to Use

1. Upload your documents
2. Click **⚡ Ingest Documents**
3. Ask a question
4. Get context-aware answers

---

## 📊 Example Queries

* “Explain the methodology of the system”
* “What are the advantages of offline RAG?”
* “Summarize the document”
* “What are the limitations?”

---

## ⚠️ Limitations

* Performance depends on local hardware
* Smaller models may give less detailed answers
* First query may be slow due to model loading

---

## 🔮 Future Improvements

* Deploy on edge devices (Jetson Nano)
* Improve response quality with better models
* Add voice-based querying
* Multi-language support
* UI enhancements

---

## 🧠 Key Concept

> This system uses **RAG (Retrieval-Augmented Generation)** instead of fine-tuning, allowing dynamic and efficient document-based responses without retraining models.

---

## 👩‍💻 Author

**Disha Sable**


---

## ⭐ Acknowledgements

* Ollama
* LangChain
* ChromaDB
* Streamlit

---

## 📜 License

This project is for academic and educational purposes.
