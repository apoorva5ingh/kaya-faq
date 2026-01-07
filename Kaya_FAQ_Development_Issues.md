---
name: Kaya FAQ - Development Summary
about: Details of project idea, challenges, and solutions
title: "Project Development Summary: Kaya FAQ"
labels: "enhancement, documentation, discussion"
assignees: ""
---

# Kaya FAQ - Development Summary

## Project Idea
Kaya FAQ is a local question-answering system built using Python, LangChain, Cohere embeddings, and FAISS.  
It allows querying documents and retrieving contextually relevant answers using embeddings and a vector store—essentially a mini local GPT for your own files.

## Tech Stack
- Python 3.12
- LangChain
- Cohere (`langchain-cohere`)
- FAISS

## Challenges Faced & Solutions
- **ModuleNotFoundError**  
  *Issue:* Imports not found.  
  *Solution:* Fixed imports and updated packages.

- **Cohere Unauthorized (401)**  
  *Issue:* API token invalid errors.  
  *Solution:* Generated new API key and switched to `langchain-cohere`.

- **build_qa_chain TypeError**  
  *Issue:* Passing `api_key` to `build_qa_chain` caused error.  
  *Solution:* Pass the key inside `CohereEmbeddings` instead.

- **Missing documents**  
  *Issue:* `data/college_info.txt` not found.  
  *Solution:* Added the required text file in `data/`.

- **Deprecation / Pydantic validation errors**  
  *Issue:* Deprecated classes and validation errors.  
  *Solution:* Updated to the latest LangChain & Cohere API methods.

- **Version conflicts & package issues**  
  *Issue:* Incompatible versions caused warnings/errors.  
  *Solution:* Aligned LangChain, Coherence, and other dependencies.

## Outcome
- Local QA chain works successfully.  
- Embeddings & FAISS vector store functional.  
- Learned the importance of managing API keys, version control, and handling API deprecations.

## Usage
1. Add your text documents in the `data/` folder.  
2. Set your Cohere API key in environment variables or in code.  
3. Run `app.py` to query your documents locally.

## Key Lessons
- Always check package versions & dependencies.  
- Stay updated with API changes to prevent breaks.  
- Proper management of API keys is essential.

---
