# ⚖️ RAG for Legal Question Answering and Summarization

> A Retrieval-Augmented Generation (RAG) system for answering Indian constitutional legal queries — combining semantic retrieval and generative modeling for accurate, context-aware responses grounded in authoritative legal texts.

---

## 📄 Project Overview

**Objective:**
Develop a question-answering system that retrieves relevant legal content from the Indian Constitution and generates precise, contextually appropriate answers.

---

## ✨ Key Features

- 🔍 Retrieval of relevant articles using dense embeddings (Sentence Transformers)
- 🤖 Answer generation using **Qwen-3 4B** language model
- 🔐 User authentication (login / signup)
- 📜 Query history tracking
- 📱 Responsive frontend for ease of use

---

## 🛠️ Technologies Used

| Layer | Technology |
|-------|-----------|
| **Backend** | Python (Flask), MongoDB, FAISS |
| **Frontend** | HTML, CSS, JavaScript |
| **LLM** | Qwen-3 4B |
| **Embedding Model** | all-MiniLM-L6-v2 |
| **Deployment** | Google Colab + Ngrok, Netlify / GitHub Pages |

---

## 🏛️ Architecture

The system is structured into three layers:

```
┌─────────────────────────────────────┐
│          Frontend Tier              │
│  Login / Signup, Query Input,       │
│  Answer Display                     │
└────────────────┬────────────────────┘
                 │
┌────────────────▼────────────────────┐
│          Backend Tier               │
│  API Logic, Authentication,         │
│  Retrieval Pipeline (Flask)         │
└────────────────┬────────────────────┘
                 │
┌────────────────▼────────────────────┐
│           Model Tier                │
│  Retriever: FAISS                   │
│  Generator: Qwen-3 4B               │
└─────────────────────────────────────┘
```

---

## 💡 How It Works

1. **User Query** — User submits a legal question via the frontend
2. **Retrieval** — System retrieves the most relevant constitutional text chunks using embeddings
3. **Generation** — Qwen-3 4B generates a contextually relevant answer based on retrieved passages
4. **Response** — Answer is displayed to the user along with references to source articles

---

## 🚀 Getting Started

### Prerequisites
- Python 3.8+
- MongoDB
- Node.js (for frontend)

### Installation

**1. Clone the repository**
```bash
git clone https://github.com/YOURUSERNAME/rag-legal-qa.git
cd rag-legal-qa
```

**2. Install backend dependencies**
```bash
cd backend
pip install -r requirements.txt
```

**3. Run the backend**
```bash
python app.py
```

**4. Open the frontend**

Open `index.html` in your browser or deploy to Netlify/GitHub Pages.

---

## 📁 Project Structure

```
rag-legal-qa/
├── backend/
│   ├── app.py               # Flask API
│   ├── retriever.py         # FAISS retrieval logic
│   ├── requirements.txt
│   └── constitution_data/   # Legal text chunks
├── frontend/
│   ├── index.html
│   ├── style.css
│   └── script.js
└── README.md
```

---

## 🙋 Author

**Rohit**
- GitHub: [@YOURUSERNAME](https://github.com/YOURUSERNAME)
- LinkedIn: [Your LinkedIn](https://linkedin.com)

---

## 📃 License

This project is open source and available under the [MIT License](LICENSE).
