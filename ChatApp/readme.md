# Chat App

## Overview
The Chat App is the conversational interface of **PerformanceX**, allowing athletes to ask questions and receive AI-powered, personalized coaching responses.  
It uses a **Retrieval-Augmented Generation (RAG)** workflow:  
1. Retrieve relevant knowledge from Pinecone (vector database).  
2. Use a Large Language Model (OpenAI GPT) to generate a natural, context-aware answer.  

---

## Files and Their Purpose

### **`app.py`**
- Main entry point for the Streamlit application.
- Loads environment variables, sets up page configuration, and initializes embeddings and Pinecone connection.
- Handles chat input/output, stores conversation history, and determines whether to answer from retrieved documents or directly via LLM.

### **`user_utils.py`**
- Contains helper functions for:
  - Connecting to Pinecone and retrieving stored embeddings.
  - Creating text embeddings (`all-mpnet-base-v2`).
  - Performing similarity search to find the most relevant documents.
  - Running the **question-answering chain** when relevant data exists.
  - Falling back to the **LLM prompt** when no relevant documents are found.
  - Checking query relevance with cosine similarity.

### **`requirements.txt`**
- Lists all Python dependencies needed to run the Chat App.


##  How to Run Locally
1. Install dependencies:
   ```bash
   pip install -r requirements.txt

2. Set your API keys in .env 

OPENAI_API_KEY

PINECONE_API_KEY

3.Run the Chat App Using VSCode:

```bash
    streamlit run app.py