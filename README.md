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
```

---

## ⚙️ Installation & Setup

### 1. Clone the Repository

```bash
git clone https://github.com/ianuj-yadav/multi-tenant-faq-chatbot.git
cd multi-tenant-faq-chatbot
```

### 2. Create Virtual Environment

```bash
python -m venv venv
```

### 3. Activate Virtual Environment

For Windows:

```bash
venv\Scripts\activate
```

For macOS/Linux:

```bash
source venv/bin/activate
```

### 4. Install Dependencies

```bash
pip install -r requirements.txt
```

### 5. Start the Server

```bash
uvicorn backend.main:app --reload
```

The backend will start at:

```bash
http://127.0.0.1:8000
```

---

## ▶️ Quick Start for Windows

You can also run the project directly using:

```bash
STARTUP.bat
```

This script installs the required dependencies and starts the FastAPI server.

---

## 💬 Chatbot Interface

The user-facing chatbot interface is located inside:

```bash
frontend/chat.html
```

It allows users to ask questions and receive automated FAQ-based responses from the configured company knowledge base.

---

## 🧑‍💼 Admin Portal

The admin dashboard is available inside:

```bash
frontend/admin.html
```

Admins can use this portal to:

- Login to the dashboard
- Manage company-specific FAQs
- Add, update, or delete FAQ entries
- View chatbot-related data
- Manage tenant-specific knowledge bases

---

## 🗄️ Database

The project uses a dual-database approach.

### SQLite

SQLite is used as the primary local database.

```bash
database/chatbot.db
```

It stores:

- Companies
- Tenant FAQs
- Chat logs
- Conversation states
- Admin data

### PostgreSQL

PostgreSQL support is included for:

- Data syncing
- Advanced Full-Text Search
- Vector indexing
- Improved FAQ retrieval performance

---

## 🧠 How the Chatbot Works

1. User enters a query in the chatbot.
2. The backend normalizes and cleans the query.
3. Prompt injection and malicious input checks are performed.
4. NLP processing is applied.
5. Synonyms and related terms are expanded.
6. Important entities such as dates are extracted.
7. The system searches company-specific FAQs.
8. The best matching answer is returned.
9. Conversation state is saved for future context.

---

## 🔐 Security Features

- Prompt injection detection
- Sensitive data masking
- Email and phone number protection
- Rate limiting
- Tenant-wise data isolation
- Input normalization
- Secure API handling

---

## 🌐 Multi-Tenant Support

The system supports multiple companies using a shared backend.

Each company has its own isolated FAQ data using `company_id`.

This allows the same chatbot system to serve different organizations without mixing their data.

---

## 📦 Deployment

The project includes a `Procfile`, making it suitable for deployment on platforms like Heroku.

Example Procfile:

```bash
web: uvicorn backend.main:app --host=0.0.0.0 --port=${PORT:-8000}
```

---

## 📌 Future Enhancements

- Improve admin analytics dashboard
- Add role-based admin access
- Add chatbot theme customization
- Add file-based FAQ import
- Add PDF and document parsing
- Add better vector search support
- Add chatbot embed script for websites
- Add multilingual FAQ support
- Add cloud database support
- Add Docker support

---

## 📸 Screenshots

Add your project screenshots here.

```md
![Chatbot Interface](screenshots/chatbot.png)
![Admin Dashboard](screenshots/admin.png)
```

---

## 👨‍💻 Author

Developed by **Anuj Yadav**

GitHub: [ianuj-yadav](https://github.com/ianuj-yadav/)

This project was created as a full-stack Multi-Tenant FAQ Chatbot and Admin Portal using FastAPI, SQLite, PostgreSQL, HTML, CSS, and JavaScript.

---

## 📄 License

This project is licensed under the **MIT License**.

You are free to use, modify, and distribute this project for personal, academic, or commercial purposes.

```txt
MIT License

Copyright (c) 2026 Anuj Yadav

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files, to deal in the Software
without restriction, including without limitation the rights to use, copy,
modify, merge, publish, distribute, sublicense, and/or sell copies of the
Software, and to permit persons to whom the Software is furnished to do so.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND.
```

---

## ⭐ Support

If you found this project helpful, please consider supporting it by:

- Giving this repository a star
- Forking the project
- Sharing it with others
- Reporting bugs or issues
- Suggesting new features

Your support helps improve and maintain this project.
