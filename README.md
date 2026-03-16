# Global Retail Intelligence Engine (Advanced RAG)

Advanced RAG system for a global retail inventory — filters by country metadata, combines vector + BM25 hybrid search, and enforces security guardrails to prevent internal data leaks. Built with LangChain, ChromaDB, HuggingFace embeddings, and a Gradio chat UI.

## Setup

Requires Python 3.12+ and [uv](https://docs.astral.sh/uv/).

```bash
# Clone the repo
git clone <repo-url>
cd team_project

# Install dependencies
uv sync

# Add your OpenRouter API key
echo 'OPENROUTER_API_KEY=sk-or-v1-...' > .env

# Input guardrails use meta-llama/Prompt-Guard-86M (gated). Accept the Llama 3.1 license at
# https://huggingface.co/meta-llama/Prompt-Guard-86M then authenticate:
#   huggingface-cli login
# or add HF_TOKEN=... to .env
```

## Run

Open `squad2_rag.ipynb` and run all cells. The Gradio chat UI will launch automatically with a shareable link.

Select a kernel that points to the `.venv` created by `uv sync`.
