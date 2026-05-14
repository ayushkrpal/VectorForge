# NeuralIndex

A high-performance vector search engine built in C++ with support for semantic retrieval, approximate nearest neighbor search, and RAG-based document querying.

## Features

- HNSW graph-based vector indexing
- KD-Tree and Brute Force search implementations
- Cosine, Euclidean, and Manhattan distance metrics
- Interactive visualization dashboard
- Real-time vector insertion and search
- RAG pipeline using Ollama
- Document chunking and embedding generation
- REST API for indexing and retrieval
- Benchmark comparison between search algorithms

## Tech Stack

C++17  
HTML  
CSS  
JavaScript  
Ollama  
REST API  

## Algorithms Implemented

### HNSW
Hierarchical graph-based ANN search structure optimized for fast retrieval on high-dimensional vectors.

### KD-Tree
Tree-based nearest neighbor search optimized for lower-dimensional data.

### Brute Force
Linear scan baseline implementation for comparison and benchmarking.

## System Architecture

```text
Input Text
   ↓
Embedding Model
   ↓
Vector Index
   ↓
Nearest Neighbor Retrieval
   ↓
LLM Response Generation
```

## Running Locally

### Prerequisites

- g++ with C++17 support
- Ollama installed locally

### Install Models

```bash
ollama pull nomic-embed-text
ollama pull llama3.2
```

### Compile

```bash
g++ -std=c++17 -O2 main.cpp -o db -lws2_32
```

### Run

```bash
./db
```

Open:

```text
http://localhost:8080
```

## API Endpoints

| Endpoint | Description |
|---|---|
| `/search` | Vector similarity search |
| `/insert` | Insert vectors/documents |
| `/delete` | Remove vectors |
| `/benchmark` | Compare algorithm latency |
| `/ask` | RAG-based querying |

## Future Improvements

- Persistent vector storage
- Hybrid lexical + semantic retrieval
- Metadata filtering
- Distributed indexing
- GPU acceleration

## Project Goal

The project was built to explore vector indexing systems, approximate nearest neighbor search, and retrieval-augmented generation pipelines using low-level systems programming in C++.