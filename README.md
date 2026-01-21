# ASU Student Advising Agent (RAG-Based Information System)

This project develops a 24/7 academic advising agent using Retrieval-Augmented Generation (RAG) to provide students with accurate and policy-aligned answers based on official ASU documentation. The system retrieves information directly from university handbooks, Registrar policies, ISSC guidance, and related academic resources to ensure consistent and reliable advising support.

## Objective
To reduce advising wait times and prevent misinformation by enabling students to receive immediate, citation-backed guidance on common topics such as:
- Academic deadlines
- Course registration and enrollment rules
- Degree planning requirements
- Tuition and fee-related policies
- CPT/OPT and international student regulations

## Problem Context
Students often face delays when seeking advising due to high appointment demand, slow email turnaround, and fragmented policy information spread across multiple PDFs and websites. Advisors spend a significant portion of time responding to repetitive procedural questions. This system addresses both issues by centralizing knowledge and automating the retrieval of policy-accurate responses.

## System Overview

1. Extract text from official ASU documents (PDF and web-based sources).
2. Segment text into labeled sections for more precise retrieval.
3. Generate embeddings using MiniLM and store them in ChromaDB.
4. Perform hybrid retrieval:
   - BM25 for keyword relevance
   - Dense vector similarity for semantic match
5. Provide top relevant text segments to the LLM through Ollama.
6. The LLM generates an answer using only the supplied context. If the information is not available, the system abstains.

## Previous Prototype (Version 1)
- Single-turn question answering in Jupyter Notebook environment.
- Responses grounded in retrieved policy text.
- Demonstrates reduction of misinformation and improved access to information.

## Current System (Version 1 Evo)
- Implement a lightweight memory buffer to enable multi-turn conversations.
- Develop a student-facing web or chat interface.
- Expand coverage to additional advising-related documents.
- Add Admin access

## Technology Stack
- Embeddings: sentence-transformers (MiniLM)
- Vector Store: ChromaDB
- Retrieval: BM25 + Dense Embedding Similarity
- Model Runtime: Ollama (Mistral / LLaMA)
- Prototyping: Python / Jupyter

## Summary
This system provides policy-grounded advising support by retrieving and citing official ASU information, reducing advisor workload and improving student access to accurate guidance. Future development will focus on interactive usability and broader document coverage.

UI:
<img width="1500" height="738" alt="image" src="https://github.com/user-attachments/assets/3b29749b-a6f4-4e4a-8689-77f4c3882884" />


Policy Related Guidance:
<img width="1500" height="728" alt="image" src="https://github.com/user-attachments/assets/aab8a329-d8a5-4275-993f-b8b24d4735de" />



Intelligent Curriculum Planning :
<img width="1500" height="707" alt="image" src="https://github.com/user-attachments/assets/4fbed1ad-b8c1-4bda-8c30-bd66bdcbc79d" />



