# localRAG

**localRAG** is a lightweight, local-first Retrieval-Augmented Generation (RAG) framework designed for efficient knowledge-augmented LLM (Large Language Model) applications. It enables users to index, search, and retrieve documents locally, empowering privacy-preserving, fast, and customizable generative AI experiences.

## Features

- **Local Document Indexing:** Ingest and index your own documents to create a local knowledge base.
- **Flexible Search:** Supports semantic and lexical search for accurate and relevant retrieval.
- **RAG Pipeline:** Seamlessly integrates retrieval results with LLMs for enhanced, context-aware responses.
- **Privacy-first:** All data processing and search happen locally—no data leaves your machine.
- **Extensible:** Modular design allows easy swapping of vector stores, retrievers, and LLMs.

## Installation

Clone the repository and install the dependencies:

```bash
git clone https://github.com/govindcss/localRAG.git
cd localRAG
pip install -r requirements.txt
```

## Usage

### 1. Index Your Documents

Place your text, Markdown, or PDF files into the `data/` directory.

Run the indexing script:

```bash
python index.py --data_dir data/
```

### 2. Query with Retrieval-Augmented Generation

Use the RAG interface to ask questions:

```bash
python rag_query.py --question "What is the architecture of localRAG?"
```

### 3. Customization

- **LLM Model:** Configure the LLM backend in `config.yaml`.
- **Vector Store:** Switch between FAISS, ChromaDB, or other vector stores by editing `vector_store.py`.
- **Retrievers:** Implement custom retrievers in the `retrievers/` directory.

## Example

```bash
python rag_query.py --question "How does localRAG keep my data private?"
```

**Output:**
> "localRAG performs all indexing and retrieval operations locally on your machine, ensuring that your documents never leave your environment..."

## Project Structure

```
localRAG/
├── data/                # Your documents
├── index.py             # Script to build the document index
├── rag_query.py         # RAG pipeline entrypoint
├── vector_store.py      # Vector DB interface
├── retrievers/          # Pluggable retriever implementations
├── llm/                 # LLM integration code
├── config.yaml          # Configuration file
└── requirements.txt     # Dependencies
```

## Requirements

- Python 3.8+
- See `requirements.txt` for specific packages

## Acknowledgements

Inspired by open-source RAG frameworks and the mission to democratize private, local AI.

## License

[MIT License](LICENSE)

---

*For questions or contributions, please open an issue or submit a pull request!*
