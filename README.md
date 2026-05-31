# 🧠 RAG Mastery Track — From Fundamentals to Production

> A structured, hands-on learning track covering the complete Retrieval-Augmented Generation (RAG) stack — from document ingestion and chunking to advanced retrieval strategies, re-ranking, hybrid search, and production-grade agentic RAG architectures.

---

## 📌 Overview

This repository is a concept-driven, implementation-first learning track for building RAG systems. Each module is self-contained with code examples, diagrams, and explanations — designed to take you from first principles all the way to deploying robust, production-grade RAG pipelines.

Whether you're building a document Q&A system, a multi-agent research assistant, or a guardrailed enterprise chatbot, this track covers every layer of the stack.

---

## 🗂️ Track Structure

### 🔷 Module 1 — Foundations

| Concept | Description |
|---|---|
| **Document Loaders** | Load data from PDFs, web pages, Notion, databases, APIs, and more |
| **Text Splitters** | Chunk documents using character, recursive, token, and semantic splitting strategies |
| **Embedding Models** | Dense vector representations using OpenAI, HuggingFace, Cohere, and local models |
| **Vector Stores** | Indexing and similarity search with FAISS, Chroma, Pinecone, Weaviate, and Qdrant |

---

### 🔷 Module 2 — Core Retrieval

| Concept | Description |
|---|---|
| **Naive RAG** | Basic retrieve-then-generate pipeline |
| **Dense Retrieval** | Semantic similarity search over embedded document chunks |
| **Sparse Retrieval (BM25)** | Keyword-based retrieval using TF-IDF and BM25 scoring |
| **Hybrid Search** | Combining dense and sparse retrieval for best-of-both-worlds performance |
| **Reciprocal Rank Fusion (RRF)** | Score fusion across multiple ranked lists without score normalization |

---

### 🔷 Module 3 — Advanced Retrieval

| Concept | Description |
|---|---|
| **Re-Ranking** | Cross-encoder re-ranking to improve top-k result precision |
| **Multi-Query Retrieval** | Generate multiple query variants to improve recall |
| **HyDE** | Hypothetical Document Embeddings — generate a hypothetical answer, then retrieve |
| **Contextual Compression** | Extract only the relevant portion of each retrieved chunk |
| **Parent-Child Retrieval** | Retrieve small chunks but pass parent context to the LLM |
| **Ensemble Retrieval** | Combine multiple retrieval strategies and merge results |

---

### 🔷 Module 4 — Advanced RAG Architectures

| Concept | Description |
|---|---|
| **Corrective RAG (CRAG)** | Evaluate retrieved documents and fall back to web search when retrieval quality is low |
| **Self-RAG** | LLM decides when to retrieve, critiques its own outputs, and selects the best response |
| **Modular RAG** | Compose RAG pipelines from interchangeable modules for flexibility and extensibility |
| **DraftRAG** | Generate a draft answer first, then retrieve to refine and ground it |
| **Multi-Modal RAG** | Retrieve and reason over text, images, tables, and charts together |

---

### 🔷 Module 5 — Production & Agentic Systems

| Concept | Description |
|---|---|
| **RAG-as-a-Service** | Serve RAG pipelines as REST APIs with streaming, caching, and observability |
| **Agentic RAG** | LLM-driven agents that plan, retrieve, reason, and act in a loop |
| **Guardrailed RAG** | Input/output safety filters, hallucination detection, and policy enforcement layers |
| **RAG Evaluation** | Measure faithfulness, answer relevancy, context precision, and context recall |
| **RAG Optimization** | Latency tuning, chunk strategy ablations, retriever vs. reader trade-offs |

---

## 🛠️ Tech Stack

- **Orchestration**: LangChain, LangGraph
- **Embedding Models**: OpenAI `text-embedding-3`, HuggingFace `BAAI/bge`, Cohere
- **Vector Stores**: FAISS, Chroma, Pinecone, Qdrant
- **LLMs**: OpenAI GPT-4o, Anthropic Claude, Mistral, local models via Ollama
- **Rerankers**: Cohere Rerank, `cross-encoder/ms-marco-MiniLM`
- **Evaluation**: RAGAS, DeepEval
- **APIs & Serving**: FastAPI, LangServe

---

## 🚀 Getting Started

```bash
git clone https://github.com/<your-username>/rag-mastery-track.git
cd rag-mastery-track
python -m venv .venv && source .venv/bin/activate
pip install -r requirements.txt
```

Copy the environment template and add your API keys:

```bash
cp .env.example .env
```

Then navigate to any module folder and run the notebook or script:

```bash
cd modules/01-foundations/document-loaders
jupyter notebook
```

---

## 📁 Repository Structure

```
rag-mastery-track/
├── modules/
│   ├── 01-foundations/
│   │   ├── document-loaders/
│   │   ├── text-splitters/
│   │   ├── embedding-models/
│   │   └── vector-stores/
│   ├── 02-core-retrieval/
│   │   ├── naive-rag/
│   │   ├── dense-retrieval/
│   │   ├── hybrid-search/
│   │   └── rank-fusion/
│   ├── 03-advanced-retrieval/
│   │   ├── reranking/
│   │   ├── multi-query/
│   │   ├── hyde/
│   │   └── contextual-compression/
│   ├── 04-advanced-architectures/
│   │   ├── corrective-rag/
│   │   ├── self-rag/
│   │   ├── modular-rag/
│   │   ├── draft-rag/
│   │   └── multimodal-rag/
│   └── 05-production/
│       ├── rag-as-a-service/
│       ├── agentic-rag/
│       ├── guardrailed-rag/
│       └── evaluation/
├── notebooks/
├── utils/
├── .env.example
├── requirements.txt
└── README.md
```

---

## 📚 Learning Path

```
Foundations → Core Retrieval → Advanced Retrieval → Advanced Architectures → Production
```

Each module builds on the previous one. If you're new to RAG, start with Module 1. If you already have retrieval basics down, jump straight to Module 3 or 4.

---

## 🤝 Contributing

Contributions, corrections, and new module suggestions are welcome. Open an issue or submit a PR.

---

## 📄 License

MIT License — see [LICENSE](LICENSE) for details.

---

> Built with ❤️ for engineers who want to go beyond basic RAG and build systems that actually work in production.
