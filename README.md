# VectorForge

A high-performance vector search engine built in C++ for semantic retrieval, approximate nearest neighbor search, and retrieval-augmented generation workflows.

## Features

- HNSW-based approximate nearest neighbor indexing
- KD-Tree and brute-force similarity search
- Cosine, Euclidean, and Manhattan distance metrics
- Real-time vector insertion and querying
- Interactive visualization dashboard
- Retrieval-Augmented Generation (RAG) pipeline
- REST API endpoints for indexing and search
- Benchmarking tools for latency comparison

## Tech Stack

C++17  
HTML  
CSS  
JavaScript  
Ollama  
REST APIs  

## Algorithms

### HNSW
Graph-based ANN indexing structure optimized for fast semantic search on high-dimensional vectors.

### KD-Tree
Tree-based nearest neighbor search for lower-dimensional retrieval tasks.

### Brute Force
Linear similarity search implementation used as a baseline benchmark.

## Architecture

```text
Input Query
    ↓
Embedding Generation
    ↓
Vector Index Search
    ↓
Nearest Neighbor Retrieval
    ↓
RAG Response Generation
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
db.exe
```

Open in browser:

```text
http://localhost:8080
```

## API Endpoints

| Endpoint | Description |
|---|---|
| `/search` | Semantic vector search |
| `/insert` | Insert vectors/documents |
| `/delete` | Delete indexed vectors |
| `/benchmark` | Compare retrieval latency |
| `/ask` | RAG-based document querying |

## Future Improvements

- Persistent storage support
- Metadata filtering
- Hybrid lexical + semantic search
- GPU acceleration
- Distributed vector indexing

## Project Goal

VectorForge was built to explore vector databases, semantic retrieval systems, approximate nearest neighbor algorithms, and RAG pipelines using low-level systems programming in C++.
