# HealthCare
Developed a multi-modal AI system that processes both text and image-based data, used to summarize medical reports,  interpret X-rays, CT scans, MRI scans and recommend medications that improve decision-making for doctors and enhances  understanding for patients.

## Features
1. *Medical Report Summarization*:
   - Upload and process medical reports (PDF, DOCX, TXT, etc.)
   - Query the system for summaries and specific information
   - View relevant medical images when available

2. *Medical Image Analysis*:
   - Upload medical images (X-rays, MRIs, CT scans, etc.)
   - Get AI-powered analysis of the images
   - Customize prompts for specific analysis requests

3. *Medication Information*:
   - Query about medications for various conditions
   - Upload documents to expand the knowledge base
   - Get detailed medication recommendations

## Installation
1. Clone this repository
2. Install required packages:
   bash
   pip install transformers torch qwen-vl-utils llama-index qdrant-client gradio
   
3. Set up your API keys in a .env file or directly in the code:
   - LlamaParse API key
   - Groq API key
   - Qdrant URL and API key
   - Nomic API key
   - Clip api key

## Usage
1. Run the Jupyter notebook or convert it to a Python script
2. The application will launch a Gradio interface with three tabs:
   - Medical Report Summarization
   - Medical Image Analysis
   - Medications

3. For each feature:
   - *Report Summarization*: Upload documents and ask questions
   - *Image Analysis*: Upload images and optionally provide custom prompts
   - *Medications*: Ask about medications for specific conditions

## Technical Details
- *Backend*: Uses Qdrant for vector storage and retrieval
- *Models*:
  - Qwen-VL for image understanding
  - CLIP for image embeddings 
  - Nomic for text embeddings
  - Groq's Llama-3 for text generation

## File Structure
- Main notebook: C-18(CODE).ipynb
- Data folder: Contains uploaded documents and images
- Parsed data: Stored in pickle files for caching

## Requirements
- Python 3.8+
# Core dependencies
transformers==4.49.0
torch==2.6.0
qwen-vl-utils==0.0.10
gradio==4.29.0
# Vector store and indexing
qdrant-client==1.9.0
llama-index-core==0.10.33
llama-index-vector-stores-qdrant==0.10.33
llama-index-embeddings-nomic==0.10.33
llama-index-llms-groq==0.10.33
# Document processing
llama-parse==0.4.0
python-dotenv==1.0.1
nest-asyncio==1.6.0
# Image processing
Pillow==10.4.0
av==14.3.0
# Utilities
numpy==1.26.4
pandas==2.2.2
python-multipart==0.0.9
typing-extensions==4.11.0
filelock==3.13.1
safetensors==0.5.2
