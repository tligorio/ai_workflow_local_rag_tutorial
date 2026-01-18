# Simple AI Workflow with Local RAG using Ollama and Postgres
#### Tiziana Ligorio for *AI Agents - CSCI 395.32* taught at Hunter College of The City University of New York

In this demo, we build a simple AI workflow that demonstrates the Retrieval Augmented Generation (RAG) pattern by creating a FastHTML tutor that can answer questions about the FastHTML library — using a **fully local stack** with no API calls required.

The workflow consists of the following stages:
1. **Document Loading** — Load the FastHTML documentation from a text file
2. **Chunking** — Split the documentation into manageable pieces
3. **Embedding** — Create vector embeddings for each chunk using Ollama
4. **Storage** — Store the embeddings in a local Postgres database with pgvector
5. **Retrieval** — Query the database for relevant chunks based on user questions
6. **Generation** — Use the retrieved context to generate accurate answers

This tutorial mirrors the hosted RAG tutorial (using OpenRouter and Supabase) but runs entirely on your local machine. This approach offers:
- **Full privacy** — Your data never leaves your machine
- **No API costs** — After initial setup, everything runs locally
- **Offline capability** — Works without an internet connection

We use Ollama for local LLM and embeddings, and Postgres with pgvector for vector storage.

## Getting Started

This tutorial runs locally only (no Colab option due to Docker requirements).

Clone this repository and follow the instructions in [SETUP.md](SETUP.md).
