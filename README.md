## 📖 Project Overview
This repository features an advanced language model application designed to automate customer support and student Q&A. The core engine relies on a production-grade RAG pipeline to ground the AI's responses directly in factual course material (PDF transcripts). 

The entire architecture is seamlessly orchestrated using the **LangChain Expression Language (LCEL)**, connecting independent executable components into a fluid, highly efficient data flow.

---

## ⚙️ The 3-Stage RAG Architecture
This project implements a robust, end-to-end RAG pipeline encompassing three core stages:

### 1. Document Indexing
* **Ingestion:** Parses the raw PDF course transcript.
* **Chunking:** Uses LangChain's Markdown header and token splitters to divide the text into semantically meaningful chunks with controlled token limits and overlapping.
* **Storage:** Converts text chunks into high-dimensional numerical vectors via OpenAI's embedding model and stores them in a **Chroma vector database** for rapid similarity search.

### 2. Context Retrieval
* **Querying:** When a user submits a question, the input is vectorized.
* **Matching:** A custom retriever scans the Chroma vector store to extract the most relevant snippets of the course material using vector similarity.

### 3. Augmented Generation
* **Prompt Engineering:** The extracted context and the original question are injected into a meticulously designed chat prompt template.
* **Execution:** The Large Language Model (LLM) processes this augmented prompt to generate a precise response, completely constrained to the provided data source.
* **Parsing:** An output parser cleanly formats the final response for the user.

---

## 🛠️ Tech Stack & Frameworks
* **Orchestration Framework:** `langchain` & LangChain Expression Language (LCEL)
* **Vector Database:** `chroma` (ChromaDB)
* **LLM & Embeddings:** OpenAI API (`gpt-4o` / `text-embedding-3-small` or equivalent)
* **Data Ingestion:** LangChain Directory/PDF loaders, Text Splitters (`MarkdownHeaderTextSplitter`, `RecursiveCharacterTextSplitter`)
* **Environment Management:** `python-dotenv`

---

## 🎯 Technical Skills & Concepts Demonstrated

### LangChain & Framework Architecture
* **LCEL (LangChain Expression Language):** Architecting, debugging, and chaining end-to-end executable pipelines.
* **Runnable Interfaces:** Constructing `RunnableLambdas` from standard Python functions to create custom components within the chain.
* **Prompt Engineering:** Designing dynamic chat prompt templates to guide LLM behavior and format complex outputs.

### Data Processing & NLP
* **Document Parsing:** Managing chunk sizes, token limits, and semantic overlap to maintain contextual integrity.
* **Vector Management:** Generating, managing, and querying dense embeddings within a localized vector database.

### LLM Integration & Safety
* **API Management:** Securely integrating and managing commercial foundation model APIs.
* **Contextual Grounding:** Applying RAG principles to eliminate hallucination risks by strictly constraining model outputs to verified data sources.

---
