# Contextual Academic Copilot

A context-aware AI workspace built with **FastAPI** (backend) and **React** (frontend).  
Uses **OpenAI embeddings** + **Chroma vector database** to implement Retrieval-Augmented Generation (RAG).

---

## 🧱 Prerequisites

Make sure you have the following installed:

| Tool | Version |
|------|---------|
| Python | 3.9+ |
| Node.js | 18+ |
| npm | Latest |
| Git | Latest |

Verify your installations:

```bash
python --version
node --version
npm --version
```

---

## 🚀 Running Locally

### Step 1 — Clone the Repository

```bash
git clone <YOUR_REPO_URL>
cd contextual-academic-copilot
```

### Step 2 — Set Up the Backend

```bash
cd backend

# Create and activate a virtual environment
python -m venv venv

# macOS / Linux
source venv/bin/activate

# Windows
venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt
```

### Step 3 — Configure Environment Variables

Create a `.env` file inside the `backend/` folder with the following:

```env
OPENAI_API_KEY=sk-your-openai-key
LLM_MODEL=gpt-4o-mini
EMBEDDING_MODEL=text-embedding-3-small
VECTOR_STORE_PATH=./vector_store
CHUNK_SIZE=512
CHUNK_OVERLAP=64
ALLOWED_ORIGINS=["http://localhost:5173"]
```

### Step 4 — Start the Backend Server

```bash
uvicorn app.main:app --reload
```

The backend will be available at:

- **API:** `http://127.0.0.1:8000`
- **Docs:** `http://127.0.0.1:8000/docs`

> Keep this terminal running.

### Step 5 — Set Up & Start the Frontend

Open a **new terminal** and run:

```bash
cd frontend
npm install
npm run dev
```

The frontend will be available at: `http://localhost:5173`

---

## 🛠️ Tech Stack

| Layer | Technology |
|-------|-----------|
| Backend | FastAPI, Python |
| Frontend | React, Vite |
| AI / Embeddings | OpenAI API |
| Vector Database | ChromaDB |
| Auth | JWT |