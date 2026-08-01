<h1 align="center">🩺 Medical Retrieval-Augmented Generation (Medical RAG)</h1>

<p align="center">
A complete end-to-end Medical Retrieval-Augmented Generation (RAG) system for biomedical question answering using <b>PubMed</b>, <b>BioASQ</b>, <b>BioBERT</b>, <b>BM25</b>, <b>MedCPT</b>, <b>FAISS</b>, and <b>Gemini</b>.
</p>

<p align="center">

![Python](https://img.shields.io/badge/Python-3.11-blue?style=for-the-badge&logo=python)
![PyTorch](https://img.shields.io/badge/PyTorch-Deep%20Learning-red?style=for-the-badge&logo=pytorch)
![Transformers](https://img.shields.io/badge/HuggingFace-Transformers-yellow?style=for-the-badge)
![FAISS](https://img.shields.io/badge/FAISS-Vector%20Search-green?style=for-the-badge)
![BioBERT](https://img.shields.io/badge/BioBERT-Biomedical-blueviolet?style=for-the-badge)
![Gemini](https://img.shields.io/badge/Gemini-LLM-orange?style=for-the-badge)

</p>

---

# 📖 Overview

This project reproduces the complete retrieval and generation pipeline of a **Medical Retrieval-Augmented Generation (Medical RAG)** system for biomedical question answering.

The system retrieves the most relevant biomedical literature from **PubMed**, augments the user's question with the retrieved evidence, and generates medically grounded answers using a Large Language Model.

Unlike traditional LLMs, the model answers questions **using retrieved scientific literature instead of relying solely on its internal knowledge**, reducing hallucinations while providing evidence-backed responses.

---

# ✨ Features

- 🔍 Dense Retrieval using BioBERT
- 📚 Sparse Retrieval using BM25
- ⚡ Hybrid Retrieval (BM25 + BioBERT)
- 🧬 MedCPT Embedding-based Retrieval
- 🚀 FAISS Vector Search
- 📖 PubMed Knowledge Base
- ❓ BioASQ Biomedical QA Benchmark
- 🤖 Gemini-powered Answer Generation
- 📄 PMID Citation Tracking
- 📊 Retrieval Evaluation

---

# 🏗 Architecture

```text
                User Question
                      │
                      ▼
            Question Encoder
       (BioBERT / MedCPT Encoder)
                      │
                      ▼
             Similarity Search
        (FAISS / BM25 / Hybrid)
                      │
                      ▼
        Top-k Relevant PubMed Papers
                      │
                      ▼
            Prompt Construction
                      │
                      ▼
              Gemini LLM
                      │
                      ▼
         Evidence-grounded Answer
```

---

# 📂 Datasets

## PubMed

Used as the biomedical knowledge base.

Contains:

- Title
- Abstract
- PMID

---

## BioASQ

Used for evaluation.

Contains:

- Biomedical Questions
- Ground Truth Documents
- Ideal Answers
- Exact Answers

---

# 🔬 Retrieval Methods

## 1️⃣ BioBERT Retrieval

Uses BioBERT embeddings and cosine similarity for dense semantic retrieval.

---

## 2️⃣ BM25 Retrieval

Traditional sparse lexical retrieval based on keyword matching.

---

## 3️⃣ Hybrid Retrieval

Combines

- BM25
- BioBERT

to leverage both lexical and semantic retrieval.

---

## 4️⃣ MedCPT Retrieval

Uses

**MedCPT Article Encoder**

to generate document embeddings specifically optimized for biomedical retrieval.

---

# 🧠 Large Language Model

Retrieved PubMed papers are converted into a structured prompt and passed to

**Google Gemini**

which generates the final medical answer while citing the PubMed papers used.

---

# ⚙️ Technologies Used

- Python
- PyTorch
- HuggingFace Transformers
- FAISS
- NumPy
- Scikit-learn
- Elasticsearch
- BioBERT
- MedCPT
- BM25
- Google Gemini API

---

# 📁 Project Structure

```
medical-rag/

│
├── notebooks/
│     ├── 01_dataset.ipynb
│     ├── 02_biobert.ipynb
│     ├── 03_bm25.ipynb
│     ├── 04_medcpt.ipynb
│     ├── 05_hybrid.ipynb
│     └── 06_generation.ipynb
│
├── data/
│
├── models/
│
├── README.md
│
└── requirements.txt
```

---

# 🚀 Pipeline

```
Question
    ↓

Retriever
(BM25 / BioBERT / Hybrid / MedCPT)

    ↓

Top-k PubMed Papers

    ↓

Prompt Construction

    ↓

Gemini

    ↓

Final Medical Answer
```

---

# 📊 Example

## Question

> Is Hirschsprung disease a Mendelian or a multifactorial disorder?

---

## Retrieved Documents

```
PMID 15858239

PMID 20598273

PMID 6650562
...
```

---

## Generated Answer

```
Coding sequence mutations in RET, GDNF,
EDNRB, EDN3 and SOX10 contribute to
Hirschsprung disease.

The disorder shows both Mendelian and
multifactorial inheritance depending
on the underlying genetic cause.
```

---

# 📈 Future Improvements

- Cross-Encoder Re-ranking
- Reciprocal Rank Fusion
- Larger PubMed Corpus
- Quantized Local LLMs
- ClinicalBERT Retrieval
- Med-PaLM Integration
- Evaluation using Recall@K and MRR

---

# 🎯 Skills Demonstrated

- Retrieval-Augmented Generation (RAG)
- Dense Retrieval
- Sparse Retrieval
- Hybrid Search
- Biomedical NLP
- Semantic Search
- Vector Databases
- FAISS Indexing
- Large Language Models
- Information Retrieval
- Prompt Engineering

---

# 🙏 Acknowledgements

- PubMed
- BioASQ Challenge
- Hugging Face
- NCBI
- Google Gemini
- BioBERT
- MedCPT

---

# ⭐ If you found this project useful

Please consider giving the repository a ⭐.
