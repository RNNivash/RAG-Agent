
# RAG Agent: Smart Retrieval with LangChain Agents

RAG Agent is a modular Retrieval-Augmented Generation (RAG) project using LangChain, Gemini embeddings, FAISS, and agent-based reasoning.
It demonstrates three progressive implementations of RAG — from simple vector retrieval to an intelligent agent that selects tools like Wikipedia and arXiv.

## 🧠 Project Structure

### 1. Simple RAG
- Load documents (PDF/Web).
- Chunk and embed using Gemini (`embedding-001`).
- Store in FAISS vector store.
- Perform basic similarity search and LLM response.

### 2. Retriever + Chain
- Add ChatPromptTemplate and `stuff_documents_chain`.
- Integrate retriever with prompt-based reasoning.
- Query through a full retrieval chain.

### 3. RAG Agent (ReAct)
- Use LangChain tools: Wikipedia, Arxiv, and custom retrievers.
- Setup ReAct-style agent using `create_react_agent`.
- Invoke LLM with multiple tool choices and reasoning ability.

## 🔧 Tech Stack

- **LangChain**
- **Google Gemini (Embedding + LLM)** via `langchain_google_genai`
- **FAISS** for vector similarity search
- **WebBaseLoader, PyPDFLoader** for data ingestion
- **LangChain Tools**: Wikipedia, Arxiv
- **ReAct Agent Architecture**

## 🚀 Getting Started

### 1. Install Requirements

```bash
pip install langchain langchain-google-genai faiss-cpu python-dotenv
pip install langchain-community langchainhub
```

### 2. Set Your Google API Key

Create a `.env` file in your root directory with:
```
GOOGLE_API_KEY=your-api-key-here
```

### 3. Run Each Notebook/Script in Order

- `01_simple_rag.ipynb` or notebook: Basic chunking, embeddings, and retrieval.
- `02_retriever_chain.ipynb`: Builds a retrieval chain with a custom prompt.
- `03_rag_agent.ipynb`: Integrates LangChain tools and agents for reasoning.

## 📚 Example Queries

- "Who are the authors of Attention is All You Need?"
- "What is Scaled Dot-Product Attention?"
- "What's the paper 1605.08386 about?"

## ✨ Inspiration

This project showcases how to scale a simple RAG system into a fully agentic and tool-enhanced reasoning pipeline using LangChain.

---

> Designed with ❤️ by Nivash | Powered by LangChain + Gemini
