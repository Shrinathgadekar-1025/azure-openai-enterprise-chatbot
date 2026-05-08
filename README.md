# 🤖 Azure OpenAI Enterprise Chatbot

A production-grade RAG (Retrieval-Augmented Generation) chatbot built on 
an enterprise dataset using Azure OpenAI services.

> ⚠️ **Note:** Source code is proprietary and not publicly available.
> This repository documents the architecture, approach, and outcomes.

---

## 🧠 Architecture Overview

User Query → React Frontend → Azure OpenAI API
                                    ↓
                         Vector Search (ada-002)
                                    ↓
                         Azure Blob Storage (Dataset)
                                    ↓
                         GPT-3.5 Turbo (Answer Generation)
                                    ↓
                         Cosmos DB (Chat History)

---

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| LLM | Azure OpenAI – GPT-3.5 Turbo |
| Embeddings | text-embedding-ada-002 |
| Vector Search | Azure Cognitive Search |
| Storage | Azure Blob Storage |
| Chat Persistence | Azure Cosmos DB |
| Frontend | React JS |
| Deployment | Azure Web Apps |

---

## ⚙️ How It Works (RAG Pipeline)

1. **Data Ingestion** — Enterprise JSON dataset uploaded to Azure Blob Storage
2. **Chunking & Embedding** — Data chunked and converted to vectors using ada-002
3. **Vector Index** — Semantic search index created in Azure Cognitive Search
4. **Query Flow** — User query → vector search retrieves relevant chunks → 
   GPT-3.5 generates grounded answer
5. **Chat History** — Cosmos DB persists full conversation context per session
6. **Frontend** — React JS UI integrated with deployed API endpoint

---

## ✅ Key Outcomes

- Chatbot answers are grounded entirely in enterprise data — no hallucinations
- Semantic search finds relevant content even when keywords don't match
- Persistent chat history enables multi-turn enterprise conversations
- Successfully deployed and validated in Azure Web Apps

---

## 📌 Status
✅ Completed | Enterprise Project | 2022

---

## 📬 Contact
www.linkedin.com/in/shrinath-gadekar-a2745a128 | shrinath658@gmail.com
