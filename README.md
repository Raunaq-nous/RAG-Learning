<div align="center">
  <h1>🧠 RAG-Learning</h1>
  <p><strong>A Playground for Retrieval-Augmented Generation (RAG) Architecture & Experiments</strong></p>
  
  <p>
    <img src="https://img.shields.io/badge/Status-Active_Learning-success?style=flat-square" alt="Status" />
    <img src="https://img.shields.io/badge/Focus-LLMs_%7C_Vector_DBs-blue?style=flat-square" alt="Focus" />
    <img src="https://img.shields.io/badge/Language-Python-3776AB?style=flat-square&logo=python&logoColor=white" alt="Python" />
  </p>
</div>

---

## 📖 Overview

Welcome to the **RAG-Learning** repository. This is my dedicated engineering space for exploring, building, and optimizing Retrieval-Augmented Generation (RAG) systems. 

As Large Language Models (LLMs) continue to evolve, the ability to ground their generations in external, verifiable knowledge bases is critical. This repository serves as a log of my experiments, from basic document ingestion to advanced multi-agent orchestrations and knowledge graph integrations.

### 🎯 Objectives
- **Understand the Core:** Build foundational RAG pipelines from scratch.
- **Evaluate Vector Databases:** Test and benchmark different vector storage solutions.
- **Optimize Retrieval:** Experiment with chunking strategies, hybrid search, and semantic routing.
- **Scale with Agents:** Integrate RAG into Multi-Agent LLM architectures.

---

## 🏗️ Architecture & Modules (Planned)

*Note: This repository is a living document and will grow as new concepts are tested.*

1.  **`01_Basics/`**
    *   Simple document ingestion and embedding generation.
    *   Basic vector similarity search.
2.  **`02_Advanced_Retrieval/`**
    *   Semantic chunking and metadata filtering.
    *   Hybrid search (Keyword + Semantic).
3.  **`03_Agentic_RAG/`**
    *   Routing queries to appropriate data sources.
    *   Self-correcting retrieval loops using LangChain / LlamaIndex.
4.  **`04_Knowledge_Graphs/`**
    *   Graph-RAG implementations to capture entity relationships.

---

## 🛠️ Core Technologies

The experiments in this repository typically utilize the following stack:

*   **Languages:** Python
*   **Orchestration:** LangChain, LlamaIndex
*   **Embeddings & LLMs:** OpenAI, Anthropic (Claude), Open-source models
*   **Vector Databases:** Pinecone, ChromaDB, Qdrant (Depending on the experiment)
*   **Frameworks:** Streamlit / FastAPI for testing interfaces

---

## 🚀 How to Use This Repository

If you are following along or want to run these experiments locally:

### 1. Clone the repository
```bash
git clone https://github.com/Raunaq-nous/RAG-Learning.git
cd RAG-Learning
```

### 2. Set up a virtual environment
```bash
python -m venv venv
source venv/bin/activate  # On Windows use `venv\Scripts\activate`
```

### 3. Install dependencies
```bash
pip install -r requirements.txt
```

### 4. Environment Variables
You will need to set up your API keys. Copy the `.env.example` file (once created) to `.env` and add your keys:
```bash
OPENAI_API_KEY=your_api_key_here
ANTHROPIC_API_KEY=your_api_key_here
```

---

<div align="center">
  <i>Built for solving problems where you have to figure out the question before the answer.</i>
</div>