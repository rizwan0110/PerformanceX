# Data Upload App 

## Overview
The Data Upload App is responsible for **ingesting text-based data** into the PerformanceX knowledge base.  
It processes  the uploaded `.txt` files, cleans and chunks the content, converts it into embeddings, and stores it in a **Pinecone vector database** for retrieval by the Chat App.

---

## Files and Their Purpose

### **`UploadData.py`**
- The main Streamlit app for uploading and processing text files.
- Provides a simple UI for file upload and displays progress messages for each processing step.
- Calls backend functions to read, split, clean, embed, and upload data to Pinecone.

### **`UploadData_Backend.py`**
- Contains helper functions for:
  - **Reading** uploaded `.txt` files.
  - **Splitting** content into logical sections and manageable chunks.
  - **Cleaning** text by removing formatting characters and unwanted spaces.
  - **Creating embeddings** using `all-MiniLM-L12-v2` model.
  - **Pushing** processed embeddings into Pinecone.

### **`requirements.txt`**
- Lists Python dependencies for both the Streamlit UI and backend processing.
- Key dependencies:
  - **Streamlit** – App UI.
  - **LangChain** – Data processing and embeddings.
  - **SentenceTransformers** – Embedding generation.
  - **Pinecone Client** – Vector database storage.
