🤖 Create a Q&A Chatbot with LangChain
An elegant and intelligent virtual assistant powered by RAG for the "Introduction to Tableau" course.

📖 Case Description
LangChain is an advanced framework for developing language model-powered applications. A famous use case is creating customer support or Q&A chatbots. In this project, you will discover how to create a chatbot using Python and LangChain to answer questions about the Introduction to Tableau course by Ned Krastev.

To achieve this goal, we employ Retrieval Augmented Generation (RAG)—a highly popular technique for building AI-powered chatbots. To seamlessly implement the pipeline representing the Q&A chatbot, we utilize the LangChain Expression Language (LCEL) protocol. This allows us to connect Runnable components so the output of one serves directly as the input to the next.

⚙️ The 3-Stage RAG Architecture
This LangChain tutorial encompasses three core stages to ensure accurate and contextual answers:

Indexing: We divide the course transcript into shorter sections using LangChain's Markdown header and token splitters. These sections are converted into numerical vectors through an embedding model and stored in a Chroma vector store.

Retrieval: A retriever extracts the specific portion of the course that is most valuable for addressing a student's inputted question.

Augmented Generation: The chat model uses the retrieved text and the student's question—combined via a prompt template—to generate an "augmented" response. Finally, an output parser ensures the result is returned as a clean string.

🎯 Skills You Will Master
This project is designed to challenge and expand your AI engineering capabilities:

Utilizing LangChain's text splitters for document parsing.

Managing chat messages and constructing prompt templates.

Applying LLMs and building LCEL chains for course transcription correction.

Generating embeddings for storage in a vector database.

Constructing RunnableLambdas from regular Python and lambda functions.

Creating end-to-end LCEL chains for a fully functional Q&A chatbot.

🛠️ Project Requirements & Setup
Prerequisites
Python Environment: Version >= 3.9 and < 4.0. (Creating a dedicated virtual environment is highly recommended).

IDE: Jupyter Notebook installed and running.

API Access: A valid OpenAI API key.
