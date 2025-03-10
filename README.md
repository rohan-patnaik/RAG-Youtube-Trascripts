# Retrieval Augmented Generation with Python, LangChain, and OpenAI API

This is a basic implementation of a RAG application built from scratch using Python, LangChain, and the OpenAI API. \
Inspired by the YouTube video "[Building a RAG application from scratch](http://www.youtube.com/watch?v=BrsocJb-fAo)".

This repo acts as a starting point to understand and implement RAG applications.\
Shows the basic steps to build a RAG pipeline.\
Use LangChain for managing the RAG process.\
Leverages LLM APIs (OpenAI in my case) for language model features.

## Setup Instructions

1. **Install Dependencies:**  
   Install the required packages by running:  
   ```bash
   pip install -r requirements.txt
   ```

2. **Project Structure Example:**
   ```bash
   rag-application/
   ├── app.py          
   ├── data/               # Data files
   ├── requirements.txt    
   └── README.md         
   ```

3. **Implement the RAG Application (app.py):**  

   Implement the core logic of our RAG application in `app.py`. This involves:

   - **Document Loading:** Load our data source (e.g., text files, PDFs). LangChain provides document loaders for various formats.
   - **Text Splitting:** Split large documents into smaller chunks for better retrieval.
   - **Embedding Generation:** Use OpenAI embeddings to convert text chunks into vector embeddings.
   - **Vector Store and Indexing:** Create a vector store (e.g., using ChromaDB, FAISS, or others) and index the embeddings for efficient similarity search.
   - **Retrieval:** Define a retrieval mechanism to fetch relevant document chunks based on a user query.
   - **Generation:** Use the OpenAI API (example `ChatOpenAI`) and LangChain to generate answers based on the retrieved context and the user query.

4. **Set up required API Keys:**  

   You will need an OpenAI API key, Pinecone API Key to use the models and vector DB. Ensure to  set up the required keys as an environment variables.
   ```bash

   # .env file
   OPENAI_API_KEY = YOUR_KEY_HERE
   PINECONE_API_KEY = YOUR_KEY_HERE
   PINECONE_API_ENV = YOUR_ENV_REGION_HERE
   INDEX_NAME = 'youtube-transcripts'
   ```

5. **Run the Application with an example:**  

   ```bash
   python app.py "What are the benefits of RAG applications?"
   ```

---
