
# ⚖️ LegalLens — AI-Powered Legal Assistance Platform

> Making legal help accessible to every Indian citizen through AI.

![Python](https://img.shields.io/badge/Python-3.11-blue?style=flat-square&logo=python)
![FastAPI](https://img.shields.io/badge/FastAPI-0.110-green?style=flat-square&logo=fastapi)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-16-blue?style=flat-square&logo=postgresql)
![TailwindCSS](https://img.shields.io/badge/TailwindCSS-CDN-38bdf8?style=flat-square&logo=tailwindcss)
![License](https://img.shields.io/badge/License-MIT-purple?style=flat-square)

---

## 🧠 What is LegalLens?

LegalLens is a production-grade full-stack AI platform that helps Indian citizens understand their legal rights, analyze documents, generate legal drafts, manage cases, and connect with verified lawyers — all in one secure platform.

---

## ✨ Core Features

| Module | Description |
|---|---|
| 🤖 AI Legal Assistant | Ask any legal question in plain language. Get cited answers from Indian law. |
| 📄 Document Analyzer | Upload contracts/agreements. AI highlights risky, missing, or unfair clauses. |
| ✍️ Draft Generator | Generate FIRs, Legal Notices, NDAs, Complaints — export as PDF. |
| ✅ Smart Checklists | Personalized step-by-step legal action plans. |
| 🕐 Timeline Builder | Visualize case milestones and upcoming hearings. |
| 💰 Cost Estimator | Transparent legal cost breakdowns before you commit. |
| 📚 Legal Awareness Hub | Learn your rights across property, family, consumer, and criminal law. |
| 🗂️ Case Management | Full case lifecycle from filing to resolution. |
| 🔒 Immutable Evidence Vault | SHA-256 hashed, timestamped, AWS S3 WORM-locked evidence storage. |

---

## 👥 Role-Based Access

```
Citizen   → Create cases, upload docs, use AI tools, connect with lawyers
Lawyer    → Self-register, AI + admin verified, access only assigned cases
Judge     → Admin-created, view all cases, schedule hearings
Admin     → Full platform control, approve lawyers, create judges
```

---

## 🔐 Security Architecture

- **JWT Authentication** — Stateless token-based sessions
- **Case-Based Isolation** — Lawyers can NEVER access unassigned cases
- **Backend-Only Authorization** — All permission checks server-side
- **No Public File URLs** — Every document request is validated against ownership
- **Role Spoofing Prevention** — Role is read from JWT, never from client input

---

## 🛠️ Tech Stack

**Backend**
- Python 3.11 + FastAPI
- PostgreSQL 16
- SQLAlchemy + Alembic
- JWT (python-jose)
- Uvicorn

**Frontend**
- HTML5 + Tailwind CSS (CDN)
- Vanilla JavaScript
- Served via FastAPI StaticFiles

**AI / ML**
- Groq API (document analysis, legal Q&A)
- Custom ML models for risk scoring


---

## 📁 Project Structure

```
.
├── app/                     # Backend (FastAPI)
│   ├── api/v1/              # API routes
│   ├── core/                # Security & dependencies
│   ├── models/              # Database models
│   ├── schemas/             # Pydantic schemas
│   ├── services/            # Business logic & AI services
│   ├── utils/               # Helper utilities
│   ├── config.py
│   ├── database.py
│   └── main.py
│
├── frontend/                # HTML frontend
│   ├── assets/              # Images & icons
│   ├── js/                  # Frontend scripts
│   └── *.html
│
├── uploads/                 # Uploaded files
│   ├── documents/
│   ├── evidence/
│   └── lawyer_verification/
│
├── .env.example
├── requirements.txt
├── README.md
└── main.py
```

---

## 🚀 Getting Started

```bash
# 1. Clone the repo
git clone https://github.com/kartikeyp011/LegalLens.git
cd LegalLens

# 2. Create and activate virtual environment
python -m venv venv
venv\Scripts\activate

# 3. Install dependencies
pip install -r requirements.txt

# 4. Set up environment variables
copy .env.example .env
# Edit .env with your PostgreSQL credentials and API keys

# 5. Run the server
uvicorn main:app

# 6. Open in browser
# http://localhost:8000
```

---

## ⚠️ Disclaimer

LegalLens provides AI-assisted legal information and document analysis tools. It does **not** constitute professional legal advice.

---

## 📄 License

MIT License © 2025 Kartikey Narain Prajapati

---
