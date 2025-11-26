# 🏥 MedBot-MVP — RAG-based Medical Assistant Chatbot

A minimal **Retrieval-Augmented Generation (RAG)** based medical assistant chatbot built for AIML Engineer technical assignment.

This MVP demonstrates:
- End-to-end Python development
- RAG pipeline architecture with FAISS vector DB
- Knowledge base scraping, filtering, and indexing
- Open-source LLM (Flan-T5) integration
- Multiple digital twin (patient profile) support
- System design (HLD, LLD, diagrams)
- Gradio web UI for demo

---

## 🚀 Key Features

### 🔍 Retrieval-Augmented Generation (RAG)
- SentenceTransformer embeddings (`all-MiniLM-L6-v2`)
- FAISS vector store for fast similarity search
- Chunked medical knowledge base (Healthline articles)
- Context-aware, fact-grounded LLM answers

### 🤖 LLM Integration
- Uses HuggingFace Flan-T5 for answer generation (open-source, efficient)
- Prompt augmented with both relevant KB chunks and patient context

### 🧠 Knowledge Base
- Real-world medical articles scraped and stored as JSON
- Automatic chunking, filtering, and vectorization

### 🧑‍⚕️ Digital Twin Patient Profiles
- 5 different patient scenarios selectable in UI (age, gender, conditions, symptoms, etc.)
- Chatbot answers are context-aware and profile-personalized

### 🖥 Gradio Web UI
- Select digital twin/profile from dropdown
- Enter any medical question (text)
- View retrieved passages and generated answers
- Simple, responsive frontend

---

## ⚙️ Installation & Setup

### 1️⃣ Create environment (optional)

python -m venv venv

source venv/bin/activate # mac/linux

venv\Scripts\activate # windows


### 2️⃣ Install dependencies

pip install requests beautifulsoup4 sentence-transformers faiss-cpu transformers gradio


### 3️⃣ Build and index KB and Start the demo UI

Run `webscrape.ipynb` to scrape articles and generate KB, metadata, and FAISS index files.


---

## 💬 How to Use

- Select any patient profile from the dropdown (simulates different health scenarios)
- Enter a medical question ("What foods improve anemia?", "What is the treatment for dengue?", etc.)
- Review the digital twin details and the chatbot’s answer—fact-based and context-aware

---

## 🧠 Architecture & Design

- System architecture, class design, data flow, and DB schema diagrams included (`diagrams/`)
- RAG pipeline:
    - user query → semantic retrieval via FAISS → context chunk + patient profile → Flan-T5 LLM → answer
- Patient profile logic ensures answers can be personalized and filtered for relevance

---

## 🔒 Safety Notice
This system is **NOT a medical diagnostic tool**.  
It answers fact-based questions from a curated KB and is for educational/demonstration purposes only.

---

## 🛠 Future Enhancements
- Voice input/output (speech recognition + TTS)
- Expand KB with more diseases and clinical scenarios
- More advanced digital twin features (dashboard, health charting)
- Real database backend (SQLite/Postgres) for user/session tracking
- Multi-turn conversation support

---

## 👩‍💻 Author

**Diya Desai**  
AI/ML Engineer (AIML project submission)  
GitHub: [https://github.com/diyadesai1904](https://github.com/diyadesai1904)

---

## 📚 References

- Healthline, CDC, PubMed (scraped articles for KB)
- HuggingFace models (Flan-T5, MiniLM, Transformers)
- FAISS, Gradio Python libraries



