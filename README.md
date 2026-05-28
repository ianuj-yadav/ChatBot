# Multi-Tenant FAQ Chatbot & Admin Portal

A full-stack web application that provides automated chatbot responses using configured FAQs while supporting multiple independent organizations through a multi-tenant architecture.

This project is designed to help companies manage their own FAQ knowledge base, serve accurate chatbot responses, store conversation history, and provide an admin portal for FAQ management.

---

## 🚀 Features

- Multi-tenant chatbot system
- Company-wise FAQ management
- Admin dashboard for managing FAQs
- User-facing chatbot interface
- SQLite-based local database
- PostgreSQL sync support
- Full-Text Search support using PostgreSQL
- Deterministic RAG-based response retrieval
- NLP-based query processing
- Synonym expansion and query rewriting
- Entity extraction such as date detection
- Conversation memory and session state handling
- Chat logs storage
- Prompt injection detection
- Sensitive data masking
- Rate limiting support
- Uploads directory for FAQ attachments
- Deployment-ready configuration using Procfile

---

## 🛠️ Technology Stack

### Backend
- Python 3
- FastAPI
- Uvicorn
- SQLite
- PostgreSQL
- asyncpg
- psycopg2

### Frontend
- HTML
- CSS
- JavaScript

### AI / NLP
- Deterministic RAG
- NLTK
- RapidFuzz
- Query normalization
- Synonym expansion
- Entity extraction
- Optional external LLM integration hooks

---


## 📁 Project Structure

```bash
Multi-Tenant-FAQ-Chatbot/
│
├── backend/
│   ├── main.py
│   └── db_wrapper.py
│
├── frontend/
│   ├── chat.html
│   ├── chat.js
│   ├── admin.html
│   ├── admin.css
│   └── styles.css
│
├── database/
│   └── chatbot.db
│
├── uploads/
│
├── requirements.txt
├── STARTUP.bat
├── Procfile
├── apply_patch.py
├── check_ast.py
├── search.py
└── README.md
