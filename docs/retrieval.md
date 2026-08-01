# Retrieval Pipeline

This project implements four retrieval strategies.

## BM25

BM25 is a sparse retrieval algorithm based on keyword matching and term frequency.

Advantages:
- Fast
- Interpretable
- Strong lexical matching

---

## BioBERT

BioBERT generates dense embeddings for biomedical text.

Documents and questions are embedded into the same vector space, and cosine similarity is used for retrieval.

Advantages:
- Semantic understanding
- Handles synonyms and related biomedical concepts

---

## Hybrid Retrieval

Hybrid retrieval combines BM25 and BioBERT.

BM25 retrieves lexically similar documents while BioBERT captures semantic similarity.

This approach often improves retrieval quality.

---

## MedCPT

MedCPT is a retrieval model trained specifically for biomedical question answering.

Unlike BioBERT, MedCPT is optimized directly for retrieval tasks, making it highly effective for finding relevant PubMed papers.
