# Retrieval-Augmented Generation pipeline

## Project Overview
This project implements an intelligent query system for books using a Retrieval-Augmented Generation (RAG) architecture. The system processes books (PDF format), extracts rich metadata, and enables semantic search and question answering capabilities.

## Features
- PDF document processing and text extraction
- Advanced metadata enrichment with progressive improvement phases
- Text chunking with optimized parameters
- Vector embeddings for semantic search
- Evaluation framework for metadata extraction quality

## Key Components

### Document Processing
The system uses PyPDFLoader to extract content from PDFs and process it into manageable document objects.

### Metadata Extraction
The project implements a progressive enhancement approach to metadata extraction:
1. **Baseline**: Basic metadata extraction
2. **Phase 1**: Context-Enhanced Tagger with book structure knowledge
3. **Phase 2**: Schema-Driven Enhancement with detailed field descriptions

### Metadata Schema
Rich metadata is extracted for each document chunk, including:
- section_type (chapter, introduction, quote, etc.)
- section_heading
- chapter_number
- stoic_principle
- contains_quote
- historical_figure
- theme

### Evaluation Framework
- Completeness score
- Field coverage
- Value distributions
- Performance improvement between phases

## Technologies Used
- Python 3.x
- LangChain / LangChain Expression Language
- OpenAI embeddings and models (text-embedding-3-small, gpt-4.1-nano)
- Chroma vector database
- Matplotlib for visualization

## Results
The metadata extraction system achieves progressive improvement:
- Baseline: 17.66% completeness
- Phase 1: 59.23% completeness (+41.57%)
- Phase 2: 99.11% completeness (+81.45% from baseline)
