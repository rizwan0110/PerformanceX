# Data Folder 

## Overview
The **Data** folder contains the specific knowledge base used by the RAG (Retrieval-Augmented Generation) system.  
All text files stored here are used to build embeddings and uploaded to the Pinecone vector database via the **Data Upload App**.

The content was **manually collected** from:
- Articles
- Websites
- Research papers
- Other publicly available resources

---

## Folder Structure
The data is organized into four thematic categories:

1. **Injury Prevention**  
   - Guidance on avoiding sports-related injuries.  
   - Includes best practices, warm-up techniques, recovery methods, and preventive measures.

2. **Mental Wellness**  
   - Mental health strategies for athletes.  
   - Covers mindfulness, stress management, coping mechanisms, and resilience-building techniques.

3. **Performance Optimisation**  
   - Tips and science-backed methods to enhance athletic performance.  
   - Includes nutrition, sleep, training schedules, and focus improvement.

4. **Preparation Technique**  
   - Methods and strategies to prepare for competitions and training.  
   - Includes visualization, tactical planning, and mental preparation techniques.

---

## How It’s Used
- These `.txt` files are uploaded using the **Data Upload App**.
- The app:
  1. Reads and cleans the text.
  2. Splits it into semantic chunks.
  3. Creates embeddings (`all-MiniLM-L12-v2`).
  4. Stores them in **Pinecone** for retrieval by the Chat App.



