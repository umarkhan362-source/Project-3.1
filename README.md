# 🏢 Company Knowledge Assistant (Semantic RAG Chatbot)

**Course Project:** Project 3 of AI  
**Student Name:** Ammara Akhtar  
**Registration No:** 04102213008  

An interactive Retrieval-Augmented Generation (RAG) chatbot built to query internal company policies semantically. This project is optimized to run completely locally or within resource-constrained environments (like Kaggle) by utilizing open-source text embeddings and an efficient local vector database, bypassing reliance on active external LLM API quotas.

---

## 🚀 Features

* **Semantic Search vs. Keyword Search:** Utilizes deep-learning embeddings to understand query intent rather than basic keyword matching (e.g., matching "PTO rules" to "Vacation Policy").
* **Zero-Cost Embedding Layer:** Uses the open-source `all-MiniLM-L6-v2` transformer model generating 384-dimensional dense vectors locally.
* **Persistent Vector DB:** Powered by **ChromaDB** to index, store, and query document chunks efficiently.
* **Interactive UI:** A sleek, conversational chat interface built using **Streamlit** featuring real-time document search tracking and chat history metrics.
* **Production Workaround/Fallback:** Features a smart fail-safe mechanism that instantly delivers exact context matches cleanly if external LLM generation is blocked by API limits or network constraints.

---

## 🛠️ Tech Stack

* **Frontend UI:** Streamlit
* **Orchestration & Loading:** LangChain & LangChain-Community
* **Vector Database:** ChromaDB (Persistent Storage)
* **Embedding Model:** Hugging Face `sentence-transformers/all-MiniLM-L6-v2`
* **Tunneling/Deployment:** Serveo / Localtunnel (for cloud execution access)

---

## 📁 Project Structure

```text
├── company_docs/          # Raw policy text documents (Vacation, WFH, Maternity)
├── chromadb/              # Persistent vector store binary directory
├── app.py                 # Streamlit web application source code
├── project3-rag-llm-chatbot-ipynb.ipynb # Step-by-step development notebook
└── README.md              # Project documentation
