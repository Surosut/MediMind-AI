# MediMind AI 🧠💊

**Intelligent Medical Diagnosis and Report Analysis**

MediMind AI is an AI-powered healthcare assistant that analyzes user-reported symptoms, extracts and interprets medical report data, and identifies abnormal laboratory values. It uses machine learning, natural language processing, and generative AI to provide easy-to-understand explanations, evidence-based health information, and appropriate next-step guidance to support informed healthcare decisions.

---

## 🚀 Features

- **Symptom Analysis** — Input symptoms and receive AI-driven preliminary health assessments with potential condition mapping.
- **Medical Report Parsing** — Upload medical reports (PDF/images) for automated data extraction using OCR and NLP.
- **Abnormal Value Detection** — Automatically flags out-of-range laboratory values with severity classification (mild, moderate, critical).
- **AI-Powered Explanations** — Translates complex medical terminology into simple, patient-friendly language using generative AI.
- **Evidence-Based Guidance** — Provides next-step recommendations backed by trusted medical sources (MedlinePlus, WHO, PubMed).
- **RAG Pipeline** — Retrieval-Augmented Generation ensures responses are grounded in verified medical literature.

---

## 🏗️ Tech Stack

| Layer | Technologies |
|-------|-------------|
| **Frontend** | React.js, TypeScript, Tailwind CSS |
| **Backend** | Node.js, Express.js |
| **AI/ML Server** | Python, FastAPI |
| **Database** | MongoDB |
| **AI/ML** | Scikit-learn, NLP, LLMs, RAG |
| **Document Processing** | PyMuPDF, Tesseract OCR |
| **Vector Database** | ChromaDB / FAISS |

---

## 📁 Project Structure

```
MediMind-AI/
├── client/                  # React.js frontend
│   ├── public/
│   ├── src/
│   │   ├── components/      # Reusable UI components
│   │   ├── pages/           # Page components
│   │   ├── services/        # API service functions
│   │   ├── hooks/           # Custom React hooks
│   │   ├── utils/           # Utility functions
│   │   ├── types/           # TypeScript type definitions
│   │   └── App.tsx
│   ├── package.json
│   └── tsconfig.json
│
├── server/                  # Node.js + Express backend
│   ├── src/
│   │   ├── controllers/     # Route controllers
│   │   ├── models/          # MongoDB models
│   │   ├── routes/          # API routes
│   │   ├── middleware/      # Auth, error handling
│   │   ├── config/          # DB & app configuration
│   │   ├── utils/           # Helper functions
│   │   └── index.js
│   └── package.json
│
├── ai-service/              # Python FastAPI AI/ML service
│   ├── app/
│   │   ├── routers/         # API endpoints
│   │   ├── services/        # ML model services
│   │   ├── models/          # ML model definitions
│   │   ├── utils/           # OCR, NLP utilities
│   │   ├── rag/             # RAG pipeline
│   │   └── main.py
│   ├── requirements.txt
│   └── Dockerfile
│
├── docs/                    # Documentation & presentations
├── .gitignore
├── README.md
└── LICENSE
```

---

## ⚙️ System Architecture

```
┌─────────────────────────────────────────────────────┐
│                    USER INTERFACE                     │
│              (React.js + Tailwind CSS)                │
└──────────────────────┬──────────────────────────────┘
                       │
                       ▼
┌─────────────────────────────────────────────────────┐
│                   API GATEWAY                        │
│             (Node.js + Express.js)                    │
│         Auth · Routing · Rate Limiting                │
└──────────┬──────────────────────────┬───────────────┘
           │                          │
           ▼                          ▼
┌──────────────────┐      ┌──────────────────────────┐
│    MongoDB        │      │   AI Processing Layer     │
│  (User Data,      │      │   (Python + FastAPI)      │
│   Reports,        │      │                           │
│   History)        │      │  ┌─────────────────────┐  │
│                   │      │  │  OCR + NLP Pipeline  │  │
└──────────────────┘      │  │  (PyMuPDF, Tesseract)│  │
                          │  └─────────────────────┘  │
                          │  ┌─────────────────────┐  │
                          │  │  Symptom Classifier  │  │
                          │  │  (Scikit-learn)      │  │
                          │  └─────────────────────┘  │
                          │  ┌─────────────────────┐  │
                          │  │  RAG Engine          │  │
                          │  │  (LLM + ChromaDB)    │  │
                          │  └─────────────────────┘  │
                          └──────────┬───────────────┘
                                     │
                                     ▼
                          ┌──────────────────────────┐
                          │   External Medical APIs   │
                          │  MedlinePlus · WHO · PMID │
                          └──────────────────────────┘
```

---

## 🛠️ Getting Started

### Prerequisites

- **Node.js** v18+
- **Python** 3.11+
- **MongoDB** (local or Atlas)
- **Tesseract OCR** installed on system
- **Git**

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/Surosut/MediMind-AI.git
   cd MediMind-AI
   ```

2. **Setup Frontend**
   ```bash
   cd client
   npm install
   npm run dev
   ```

3. **Setup Backend**
   ```bash
   cd server
   npm install
   npm run dev
   ```

4. **Setup AI Service**
   ```bash
   cd ai-service
   pip install -r requirements.txt
   uvicorn app.main:app --reload
   ```

5. **Environment Variables**
   
   Create `.env` files in `server/` and `ai-service/` directories (refer to `.env.example` files).

---

## 👥 Team

| Name | Role |
|------|------|
| **Surosut Senior** | Team Lead & Developer |
| **Priyanshu Kumar** | Developer |
| **Tavish Bedi** | Developer |
| **Shourya Tripathi** | Developer |

**Supervisor:** Prof. Kanishk Tolani (Assistant Professor)  
**Department:** Computer Science & Engineering  
**Session:** 2026–2027

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).

---

## ⚠️ Disclaimer

MediMind AI is designed for **informational purposes only**. It is not intended to replace professional medical advice, diagnosis, or treatment. Always consult a qualified healthcare provider for medical decisions.
