# RAG PDF Chat Assistant

A unified Streamlit application that combines FastAPI backend and frontend for PDF document chat using Retrieval-Augmented Generation (RAG).

## Features

- Single-file deployment with embedded FastAPI backend
- PDF document upload and processing
- AI-powered question answering with source citations
- Real-time chat interface
- Automatic vector store management

## Quick Start

1. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

2. **Run the application:**
   ```bash
   streamlit run streamlit_app.py
   ```

3. **Access the app** at `http://localhost:8501`

## Usage

1. Upload a PDF file via the sidebar
2. Wait for document processing
3. Ask questions about the content
4. View responses with source citations

## Architecture

- **streamlit_app.py**: Main application combining FastAPI backend and Streamlit frontend
- **backend/**: FastAPI components for document processing and RAG
  - `app/main.py`: FastAPI server with lifespan management
  - `app/ingest.py`: PDF processing and vectorization
  - `app/rag.py`: Question answering logic
  - `app/vectorstore.py`: FAISS vector database management

## Dependencies

Core packages:
- `streamlit>=1.28.0`
- `fastapi` + `uvicorn`
- `sentence-transformers>=2.2.0`
- `faiss-cpu>=1.9.0`
- `PyPDF2>=3.0.0`

## Technical Details

- Backend runs on port 8001
- Uses FAISS for vector storage
- Sentence transformers for embeddings
- Background document processing
- Session-based progress tracking