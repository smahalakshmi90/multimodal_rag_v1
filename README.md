# Multimodal RAG Application

A Streamlit application that implements Multimodal Retrieval-Augmented Generation (RAG) for PDF documents.

## Prerequisites

### Local LLM Setup
This application requires a local LLM running via Ollama. To set this up:

1. Install Ollama from [ollama.ai](https://ollama.ai)
2. Pull and run the required models:
```bash
ollama pull llama3.2    # For embeddings
ollama pull gemma3:27b  # For text generation
```
3. Ensure Ollama is running in the background before starting the application

### System Dependencies
- Tesseract OCR
- Poppler

## Setup

1. Install Python dependencies:
```bash
pip install streamlit langchain-core langchain-ollama unstructured
```

2. Install system dependencies:
- For Ubuntu/Debian:
  ```bash
  sudo apt-get install tesseract-ocr poppler-utils
  ```
- For macOS:
  ```bash
  brew install tesseract poppler
  ```
- For Windows:
  - Install Tesseract from: https://github.com/UB-Mannheim/tesseract/wiki
  - Install Poppler from: https://github.com/oschwartz10612/poppler-windows/releases/

## Running the Application

1. Start Ollama (if not already running)
2. Run the Streamlit application:
```bash
streamlit run Multimodal_RAG.py
```

## Usage

1. Upload a PDF document using the file uploader
2. Wait for the document to be processed
3. Ask questions about the document in the chat interface

## Notes

- The application uses Ollama's local LLM for both embeddings and text generation
- Make sure you have sufficient system resources to run the local LLM
- Processing time may vary depending on your system's capabilities and the size of the PDF 