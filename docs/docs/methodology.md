# Methodology

## Overview

This project reproduces a Medical Retrieval-Augmented Generation (Medical RAG) pipeline for biomedical question answering.

The system combines classical information retrieval with dense neural retrieval and a Large Language Model to generate evidence-grounded medical answers.

---

## Pipeline

1. User submits a biomedical question.
2. The question is encoded using BioBERT or MedCPT.
3. Similar documents are retrieved from PubMed using:
   - BM25
   - BioBERT
   - Hybrid Retrieval
   - MedCPT
4. Top-k relevant documents are selected.
5. Retrieved papers are formatted into a prompt.
6. Gemini generates the final answer using only the retrieved evidence.

---

## Retrieval Methods

- BM25 (Sparse Retrieval)
- BioBERT (Dense Retrieval)
- Hybrid Retrieval
- MedCPT Retrieval

---

## Generation

The retrieved documents are passed to Gemini, which synthesizes an answer grounded in the retrieved PubMed literature.

---

## Evaluation

The retrieval system is evaluated using the BioASQ biomedical question answering benchmark by comparing retrieved PubMed IDs against the ground-truth references.
