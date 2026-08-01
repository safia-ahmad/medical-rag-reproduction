# Evaluation

The retrieval pipeline is evaluated using the BioASQ benchmark.

## Dataset

- BioASQ Training Dataset
- PubMed Abstract Corpus

---

## Evaluation Procedure

For each BioASQ question:

1. Retrieve Top-k documents.
2. Extract PubMed IDs.
3. Compare retrieved PMIDs against BioASQ ground-truth PMIDs.

---

## Metrics

Typical retrieval metrics include:

- Recall@K
- Precision@K
- Mean Reciprocal Rank (MRR)

This project primarily focuses on reproducing the retrieval and generation pipeline rather than reproducing the exact benchmark scores reported in the original paper.
