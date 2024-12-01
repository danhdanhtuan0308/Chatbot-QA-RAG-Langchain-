# Q&A with Retrieval-Augmented Generation (RAG)

This project implements a **Retrieval-Augmented Generation (RAG)** pipeline for answering questions using document retrieval combined with text generation. It uses modern machine learning models and libraries like LangChain, Sentence-Transformers, FAISS, and Gradio.

## Features

- **Retrieval-Augmented Generation (RAG)**:
  Combines document retrieval with language generation for contextually relevant answers.
- **LoRA Fine-Tuning**:
  Efficient fine-tuning of language models like T5 using Low-Rank Adaptation (LoRA).
- **Interactive UI**:
  Gradio provides an intuitive user interface for querying and receiving responses.


## Installation

To set up the environment, install the required libraries:

```bash
pip install langchain
pip install sentence-transformers
pip install chromadb
pip install faiss-cpu
pip install gradio
pip install peft
pip install pypdf
pip install transformers
pip install -U langchain-community
```
##**Workflow**

1. Document Loading
Documents (e.g., PDFs) are loaded using PyPDFLoader.

2. Text Splitting
The documents are split into smaller, manageable chunks using RecursiveCharacterTextSplitter.

3. Embedding Generation
Generate embeddings for the chunks using Sentence-Transformers.

4. Vector Storage
Store the embeddings in a FAISS vector database for efficient similarity searches.

5. Query Handling
Retrieve relevant document chunks using FAISS and generate answers using a T5 model (or another language model).

6. User Interaction
Use Gradio to provide an interactive interface where users can input questions and get answers.

## **Customization**

Replace the Model
The current model is T5. To use a different model like GPT-3.5 or LLaMA:
Update the AutoModelForSeq2SeqLM and tokenizer initialization.
Adjust configurations for LoRA fine-tuning if required.
Add Custom Documents
Replace the existing document (e.g., a PDF) with your own.
Update the loading and embedding steps to include the new data.

## **References**
LangChain Documentation
Sentence-Transformers
FAISS
Hugging Face Transformers
Gradio

## **License**
This project is open-source and available under the MIT License.
