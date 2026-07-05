🤖 Q&A Chatbot with LangChain & RAG
An elegant and intelligent virtual assistant powered by Retrieval-Augmented Generation for course-specific querying.

📖 Project Overview
This repository features an advanced language model-powered application designed to automate customer support and student Q&A. Built using Python and the LangChain framework, this chatbot acts as a dedicated assistant for the Introduction to Tableau course, providing highly accurate, context-aware responses to user queries.

The core engine relies on Retrieval-Augmented Generation (RAG) to ground the AI's responses in factual course material, eliminating hallucinations. The entire pipeline is seamlessly orchestrated using the LangChain Expression Language (LCEL), connecting independent executable components into a fluid, efficient data flow.

⚙️ The 3-Stage RAG Architecture
This project implements a robust, end-to-end RAG pipeline encompassing three core stages:

Document Indexing: The raw PDF course transcript is ingested and parsed. Using LangChain's Markdown header and token splitters, the text is divided into semantically meaningful chunks. These chunks are converted into numerical vectors via an embedding model and stored in a Chroma vector database for rapid similarity search.

Context Retrieval: When a user submits a query, a custom retriever scans the vector store to extract the most relevant snippets of the course material.

Augmented Generation: The extracted context and the original question are injected into a meticulously designed prompt template. The Large Language Model (LLM) processes this augmented prompt to generate a precise, contextualized response, which is then formatted via an output parser.

🎯 Technical Skills & Concepts Demonstrated
This project serves as a practical application of advanced AI and NLP engineering concepts.

LangChain & Framework Architecture
LCEL (LangChain Expression Language): Architecting and chaining end-to-end executable pipelines.

Runnable Interfaces: Constructing RunnableLambdas from standard Python functions to create custom chain components.

Prompt Engineering: Designing dynamic chat prompt templates to guide LLM behavior and format outputs.

Data Processing & NLP
Document Parsing: Utilizing text splitters to manage chunk size, token limits, and semantic overlap.

Vector Embeddings: Generating and managing high-dimensional numerical representations of text data.

Vector Databases: Implementing and querying ChromaDB for efficient similarity search and context retrieval.

LLM Integration
API Management: Securely integrating OpenAI's language and embedding models.

Contextual Grounding: Applying RAG principles to constrain model outputs to specific, verified data sources.
