# LLM-Based-RAG-ASSISTANT-Q-A-SYSTEM
# LLM-Driven RAG Question Answering System

## 📌 Project Overview

The **LLM-Driven RAG Question Answering System** is an AI application designed to answer user questions using information retrieved from a relevant knowledge source.

The system follows a **Retrieval-Augmented Generation (RAG)** pipeline. It loads Python tutorial content from a website, processes the content into smaller chunks, converts those chunks into vector embeddings, and stores them in a **FAISS vector database**. When a user submits a question, the application retrieves the most relevant information and sends it along with the question to a **Large Language Model (LLM)** to generate a context-aware response.

This approach helps the application provide answers based on the retrieved content instead of relying only on the LLM's general knowledge.

## 🎯 Problem Statement

Large Language Models can sometimes generate responses that are not directly supported by a specific data source. This project addresses that problem by implementing a **Retrieval-Augmented Generation (RAG)** pipeline.

The system retrieves relevant information from the available knowledge source before generating an answer. This makes the responses more relevant and grounded in the provided context.

## 💡 Solution

The application combines the following components:

- **WebBaseLoader** to load content from a website.
- **RecursiveCharacterTextSplitter** to divide documents into smaller chunks.
- **OpenAI Embeddings** to convert text into numerical vector representations.
- **FAISS** to store and search document vectors efficiently.
- **Similarity Search** to retrieve the most relevant documents.
- **ChatOpenAI** as the Large Language Model for answer generation.
- **LangChain** to build and manage the RAG pipeline.
- **Flask** to provide a simple web-based interface.

## 🔄 Application Workflow

The complete workflow of the application is:

```text
User Question
      │
      ▼
Flask Web Application
      │
      ▼
Similarity Search
      │
      ▼
FAISS Vector Database
      │
      ▼
Retrieve Relevant Documents
      │
      ▼
Provide Context to LLM
      │
      ▼
Generate Context-Aware Answer
      │
      ▼
Display Response to User
