# RAG Sales Playbook Chatbot

[![Python](https://img.shields.io/badge/Python-3.10+-blue.svg)](https://python.org)
[![RAG](https://img.shields.io/badge/RAG-Retrieval-green.svg)](https://python.langchain.com/)
[![ChromaDB](https://img.shields.io/badge/ChromaDB-Vector-orange.svg)](https://www.trychroma.com/)
[![Groq](https://img.shields.io/badge/Groq-LLM-red.svg)](https://groq.com)

Chatbot that answers questions from sales playbooks using RAG (Retrieval-Augmented Generation).

## Features

- **Document Upload** - Upload sales playbooks (TXT/PDF)
- **Smart Retrieval** - Finds relevant chunks using vector search
- **Grounded Answers** - LLM answers only from your document
- **Source Citations** - Shows where each answer came from

## Architecture

Upload PDF → Split into Chunks → Create Embeddings → Store in ChromaDB
↓
User Question ← Find Similar Chunks ← Vector Search ←─────┘
↓
LLM Answers (using only retrieved chunks)



## Tech Stack

| Technology | Purpose |
|------------|---------|
| LangChain | RAG orchestration |
| ChromaDB | Vector database |
| Groq API | Free LLM inference (Llama 3.1) |
| Sentence Transformers | Text embeddings |
| Gradio | Web interface |

## Quick Start

### Run in Colab (No Setup)

1. Click the badge below
2. Get free API key from [console.groq.com](https://console.groq.com)
3. Run all cells

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)]
(https://colab.research.google.com/drive/1umumT2dHq5jnjy12ngbJ20t28ydoXMAK?usp=sharing)

### Run Locally

```bash
git clone https://github.com/anshchordiya2002/rag-sales-playbook-chatbot.git
cd rag-sales-playbook-chatbot
pip install -r requirements.txt
export GROQ_API_KEY="your_key_here"
python rag_sales_chatbot.ipynb


Example Output

User: What do I say when a customer says the product is too expensive?
Assistant:
Focus on ROI. Our customers save 15 hours per week using automation. 
At $50/hour, that's $750 saved weekly.

---
📖 Source: "Objection: Too expensive - Response: Focus on ROI. 
Customers save 15 hours per week."

Author
Ansh Chordiya

GitHub: github.com/anshchordiya2002
LinkedIn: linkedin.com/in/anshchordiya
