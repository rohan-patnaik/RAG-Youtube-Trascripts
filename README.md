# Retrieval Augmented Generation with Python, LangChain, and OpenAI API

This repository is a basic implementation of a Retrieval Augmented Generation (RAG) application built using Python, LangChain, and the OpenAI API.

Inspired by:
- The YouTube video "[Building a RAG application from scratch](http://www.youtube.com/watch?v=BrsocJb-fAo)"  
- My article "[From YouTube to Answers: Building a RAG System on youtube transcripts](https://medium.com/@rohan-patnaik1997/from-youtube-to-answers-building-a-rag-system-with-python-whisper-and-langchain-480da3ffaffd)"

This repo serves as a starting point to understand and implement RAG pipelines using LangChain and language model APIs.

## Setup Instructions

1. **Install Dependencies:**  
   Run the following command to install the required packages:
   ```bash
   pip install -r requirements.txt
   ```

2. **Project Structure Example:**
   ```bash
   rag-application/
   ├── app.py            # Core RAG application logic
   ├── data/             # Data files (transcripts, media, etc.)
   ├── requirements.txt  
   └── README.md         
   ```

3. **Implement the RAG Application (`app.py`):**  
   The core steps include:
   - **Document Loading:** Load data sources (e.g., transcripts, PDFs).
   - **Text Splitting:** Divide documents into manageable chunks.
   - **Embedding Generation:** Convert text chunks to embeddings using OpenAI embeddings.
   - **Vector Store & Indexing:** Create and index embeddings using a vector database (e.g., ChromaDB, FAISS).
   - **Retrieval & Generation:** Retrieve relevant document chunks and generate answers using the OpenAI API via LangChain.

4. **Set Up API Keys:**  
   Create a `.env` file with your API keys (make sure not to commit real keys):
   ```bash
   # .env file
   OPENAI_API_KEY=YOUR_KEY_HERE
   PINECONE_API_KEY=YOUR_KEY_HERE
   PINECONE_API_ENV=YOUR_ENV_REGION_HERE
   INDEX_NAME=youtube-transcripts
   ```
   *(Consider committing a `.env.example` with placeholder values instead.)*

5. **Run the Application:**  
   Execute the application with an example query:
   ```bash
   python app.py "What are the benefits of RAG applications?"
   ```