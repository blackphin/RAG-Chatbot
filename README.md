# RAG-Chatbot

A lightweight Retrieval-Augmented Generation (RAG) chatbot built using `Streamlit`, `OpenAI`, and `ChromaDB`. This chatbot lets you ingest custom knowledge (`data.txt`) and ask questions over it using OpenAI or Gemini models.

---
# Architechure
<img src="https://github.com/user-attachments/assets/f8a048bb-e49a-4c6f-834e-e2450b828c82" alt="RAG Chatbot Architecture" width="10000" height="600">

---

## 🧩 Features

- ✅ Custom data ingestion and retrieval (via ChromaDB)
- 💬 Conversational chatbot interface using Streamlit
- 🔍 RAG architecture powered by OpenAI or Gemini
- 🗃️ Local vector store with persistent embeddings
- ✍️ Markdown-rich responses
- 🛠️ Easy to set up on any machine (Windows-friendly scripts included)

---

## 📁 Folder Structure

```
.
├── pages/
│   ├── chatbot_page.py         # Streamlit chatbot interface
│   └── ingest_page.py          # Data ingestion interface
├── chroma_services.py          # ChromaDB vector operations
├── genai_services.py           # OpenAI and Gemini API wrappers
├── main.py                     # Streamlit main entry
├── data.txt                    # Text data for ingestion
├── requirements.txt            # Dependencies
├── .gitignore
├── template.env                # Environment variable template
├── create_venv.bat             # Script to set up virtual environment
├── activate.bat                # Script to activate environment
```

---

## 🚀 Installation & Running

### 1. Clone the Repository

```bash
git clone https://github.com/blackphin/RAG-Chatbot.git
cd RAG-Chatbot
```

### 2. Set Up Virtual Environment (Windows)

```bash
create_venv.bat
activate.bat
```

Or on macOS/Linux:

```bash
python3 -m venv venv
source venv/bin/activate
```

### 3. Install Python Dependencies

```bash
pip install -r requirements.txt
```

### 4. Prepare Environment Variables

Rename `template.env` to `.env` and fill it like so:

```env
# Choose only one (OpenAI or Gemini)

MODEL_BASE_URL = "https://generativelanguage.googleapis.com/v1beta/openai/"
MODEL_API_KEY = "GEMINI_API_KEY"
MODEL_NAME = "gemini-2.0-flash"


CHROMA_COLLECTION_NAME = "rag_collection"
```

> **Note**: You can leave one of the keys empty depending on the model you wish to use.

### 5. Add Custom Data

Edit `data.txt` and paste your reference knowledge (e.g., documentation, notes, FAQs).

### 6. Run the App

```bash
streamlit run main.py
```

---

## 📄 Usage Flow

1. **Go to "Ingest Page"** – Ingest your `data.txt` into ChromaDB.
2. **Switch to "Chatbot Page"** – Ask questions. The bot will respond using your data as context.

---

## 🔐 API Keys

- **OpenAI**: Get your key from https://platform.openai.com/account/api-keys  
- **Gemini (Google Generative AI)**: Get your key from https://makersuite.google.com/app/apikey

---

## 🛠 Requirements

```
streamlit
openai
tiktoken
chromadb
markdown[all]
```

---

## 📃 License

MIT License
