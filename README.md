# 🤖 AI Chatbot with RAG & PDF Question Answering

An AI-powered chatbot built with **FastAPI, Groq LLM, FAISS, Sentence Transformers, and SQLite**.

The application supports normal AI conversations as well as **PDF-based Question Answering using Retrieval-Augmented Generation (RAG)**.

---

## 🚀 Features

- 💬 AI-powered normal chat
- 📄 Upload PDF documents
- 🔍 Ask questions from uploaded PDFs
- 🧠 RAG-based document search
- 🔎 Hybrid search using:
  - Vector similarity
  - Keyword matching
- 📚 PDF summarization
- 📝 Ask questions about the main topics and key points of a PDF
- 💾 Persistent chat history using SQLite
- 🗑️ Delete chat conversations
- 📋 Copy AI responses
- ⏱️ Message timestamps
- ⚡ FastAPI backend
- 🎨 Responsive web interface
- 🔐 API key stored securely using environment variables

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
                    └───────┬──────────┘
                            │
              ┌─────────────┼─────────────┐
              │             │             │
              ▼             ▼             ▼
        ┌──────────┐  ┌──────────┐  ┌──────────┐
        │  Groq    │  │   RAG    │  │ SQLite   │
        │   LLM    │  │ Pipeline │  │ Database │
        └──────────┘  └────┬─────┘  └──────────┘
                            │
                            ▼
                     ┌─────────────┐
                     │    FAISS    │
                     │ Vector Index│
                     └──────┬──────┘
                            │
                            ▼
                  ┌────────────────────┐
                  │ SentenceTransformers│
                  │ all-MiniLM-L6-v2   │
                  └────────────────────┘