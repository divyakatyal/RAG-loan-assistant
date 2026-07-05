# Loan Application RAG Assistant

An LLM-powered Retrieval-Augmented Generation (RAG) assistant that answers natural language questions about loan application data using semantic search and OpenAI's GPT-3.5.

## Overview

This project combines vector embeddings, semantic retrieval, and large language models to provide grounded responses based on a structured loan application dataset.

Instead of relying solely on the language model's internal knowledge, the assistant retrieves the most relevant records from the dataset before generating a response, improving factual accuracy and reducing hallucinations.

## Features

- Natural language question answering
- Retrieval-Augmented Generation (RAG)
- Semantic search using Sentence Transformers
- FAISS vector database for efficient similarity search
- Flask REST API backend
- OpenAI GPT-3.5 integration

## Tech Stack

- Python
- Flask
- OpenAI API
- Sentence Transformers
- FAISS
- Pandas
- NumPy

## How It Works

1. Load a loan application dataset into memory.
2. Convert each record into a dense vector embedding using the `all-MiniLM-L6-v2` Sentence Transformer model.
3. Store the embeddings in a FAISS vector index.
4. When a user submits a question:
   - Generate an embedding for the query.
   - Retrieve the most semantically similar records.
   - Inject the retrieved context into the LLM prompt.
   - Generate a grounded response using GPT-3.5.

## Example Questions

- Which applicants have the highest income?
- What factors affect loan approval?
- Which applicants have the longest employment history?
- Summarize common characteristics of approved loans.

## Project Structure
├── app.py

├── Training Dataset.csv

├── requirements.txt

└── README.md


## Future Improvements

- Conversation memory
- Streaming responses
- Source citation highlighting
- Hybrid keyword + vector retrieval
- Web interface for interactive use
