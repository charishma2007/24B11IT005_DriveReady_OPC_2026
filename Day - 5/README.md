# Day 5 – PDF Question Answering using RAG

## Overview
Developed a Retrieval-Augmented Generation (RAG) system that allows users to upload PDF documents and ask questions based on their content. The system combines semantic search with an LLM to generate context-aware responses.

## Key Features
- Text extraction from normal and scanned PDFs using OCR.
- Text chunking with overlapping segments.
- Semantic similarity search using vector embeddings.
- Context-based answer generation using Groq API.
- Interactive question-answering interface.
- Prompt instructions to minimize hallucinations.

## Workflow

PDF Upload → Text Extraction → Text Chunking → Vector Embeddings → FAISS Indexing → Context Retrieval → LLM Response

## Technologies Used

| Technology | Purpose |
|---|---|
| Python | Core implementation |
| PyMuPDF | PDF text extraction |
| Tesseract OCR | Scanned document processing |
| Sentence Transformers | Vector embeddings |
| FAISS | Similarity search |
| Groq API | Answer generation |
| Google Colab | Development environment |

## Implementation Details
- Compared `all-MiniLM-L6-v2` and `all-mpnet-base-v2` embedding models.
- Divided extracted text into 500-character chunks with 100-character overlap.
- Retrieved the top 3 relevant chunks using FAISS.
- Used `openai/gpt-oss-20b` through Groq for response generation.

## Learning Outcomes
- Understanding RAG architecture and its practical implementation.
- Working with embeddings and vector indexing.
- Processing structured and scanned documents.
- Integrating external LLM APIs with document retrieval systems.

## Conclusion
This task demonstrates how RAG can transform static PDF documents into interactive knowledge sources, enabling relevant and context-grounded question answering.
