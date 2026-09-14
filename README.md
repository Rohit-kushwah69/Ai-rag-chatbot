# 🤖 AI Chatbot with RAG & PDF Question Answering

An AI-powered conversational chatbot built with **FastAPI, LangChain, Groq LLM, FAISS, Sentence Transformers, SQLite, and Docker**.

The application supports normal AI conversations as well as **PDF-based Question Answering using Retrieval-Augmented Generation (RAG)**.

The application is containerized using Docker and can be deployed to **Microsoft Azure**.

---

## 🚀 Features

- 💬 AI-powered conversational chat
- 🧠 LangChain-based conversational AI
- 📄 Upload PDF documents
- 🔍 Ask questions from uploaded PDFs
- 🧠 Retrieval-Augmented Generation (RAG)
- 🔎 Hybrid document search
  - Vector similarity search
  - Keyword matching
- 📚 PDF summarization
- 📝 Ask questions about main topics and key points of PDFs
- 💾 Persistent chat history using SQLite
- 🗑️ Delete chat conversations
- 📋 Copy AI responses
- ⏱️ Message timestamps
- ⚡ FastAPI backend
- 🎨 Responsive web interface
- 🔐 Secure API key management using environment variables
- 🐳 Docker containerization
- ☁️ Azure deployment ready

---

## 🛠️ Tech Stack

| Technology | Purpose |
|---|---|
| Python | Backend programming |
| FastAPI | REST API and backend |
| LangChain | LLM and conversational AI framework |
| Groq | Large Language Model |
| FAISS | Vector similarity search |
| Sentence Transformers | Text embeddings |
| PyMuPDF | PDF text extraction |
| SQLite | Chat history and database |
| HTML | Frontend structure |
| CSS | Frontend styling |
| JavaScript | Frontend functionality |
| Docker | Containerization |
| Microsoft Azure | Cloud deployment |

---

## 🏗️ Project Architecture

```text
                         ┌──────────────────┐
                         │    User / UI     │
                         └────────┬─────────┘
                                  │
                                  ▼
                         ┌──────────────────┐
                         │  HTML / CSS / JS │
                         └────────┬─────────┘
                                  │
                                  ▼
                         ┌──────────────────┐
                         │     FastAPI      │
                         │     Backend      │
                         └────────┬─────────┘
                                  │
                 ┌────────────────┼────────────────┐
                 │                │                │
                 ▼                ▼                ▼
          ┌────────────┐   ┌────────────┐   ┌────────────┐
          │  LangChain │   │    RAG     │   │   SQLite   │
          │    + LLM   │   │  Pipeline  │   │  Database  │
          └──────┬─────┘   └──────┬─────┘   └────────────┘
                 │                │
                 ▼                ▼
          ┌────────────┐   ┌────────────┐
          │    Groq    │   │   FAISS    │
          │    LLM     │   │Vector Index│
          └────────────┘   └──────┬─────┘
                                  │
                                  ▼
                       ┌─────────────────────┐
                       │ Sentence Transformers│
                       │  all-MiniLM-L6-v2   │
                       └─────────────────────┘
                                  │
                                  ▼
                           ┌─────────────┐
                           │   Docker    │
                           │  Container  │
                           └──────┬──────┘
                                  │
                                  ▼
                         ┌──────────────────┐
                         │ Microsoft Azure  │
                         │  Cloud Hosting   │
                         └──────────────────┘