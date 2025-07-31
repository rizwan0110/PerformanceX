# PerformanceX – Personalized GEN AI Sports Coaching  App

## Overview
PerformanceX is an AI sports coaching assistant that combines **Retrieval-Augmented Generation (RAG)** with **Large Language Models (LLMs)** to support athletes in achieving peak performance and maintaining mental well-being.

Unlike normal chatbots, PerformanceX retrieves relevant sports science, mental wellness, and injury prevention information from a specific database before generating responses. This ensures that the answers are **personalized, accurate, and contextually relevant**.

---

## Use Case
Athletes at all levels face both **physical challenges** and **mental health pressures**. Traditional coaching often focuses heavily on physical training, overlooking psychological well-being.

PerformanceX bridges this gap by:
- Providing **personalized mental health guidance**.
- Offering **evidence-based coaching advice** from dedicated content.
- Supporting **athletes in recovery and resilience building**.

Example applications:
- **Sports teams** using AI-powered mental health support.
- **Personal trainers** offering AI-assisted coaching.
- **Athletes** seeking quick, reliable, and science-backed advice.

---

## How RAG Works?
Retrieval-Augmented Generation (RAG) operates in **two steps**:
1. **Retrieval Phase** – Search a **vector database** (Pinecone- in this implementation) for relevant knowledge chunks based on a user’s query.
2. **Generation Phase** – Pass those retrieved chunks to an **LLM** (OpenAI GPT-4) to create a natural, coherent, and grounded answer.

This approach outperforms standard LLMs by ensuring:
- **Factual accuracy** – grounded in domain data.
- **Personalization** – tailored to sports and mental wellness contexts.
- **Up-to-date content** – from your private dataset.

---

##  Technologies Stack
- **[Streamlit](https://streamlit.io/)** – Interactive frontend for both chat and upload apps.
- **[LangChain](https://www.langchain.com/)** – Framework for working with LLMs and retrieval.
- **[OpenAI GPT-4](https://platform.openai.com/)** – High-quality LLM for response generation.
- **Embedding Model** - all-MiniLM-L12-v2 
- **[Pinecone](https://www.pinecone.io/)** – Vector database for fast semantic search.

## Folder Structure

- PerformanceX/
- --Chat App/ # Files for chatbot
- --Data Upload App/ # Files for Document ingestion & embedding app
- --Data/ # Dataset used



## 🚀 How to Run
1. **Clone repo**:
   ```bash
   git clone https://github.com/rizwan0110/PerformanceX.git
   cd PerformanceX