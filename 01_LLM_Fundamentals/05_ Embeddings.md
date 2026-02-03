# Embeddings: Geometry and Meaning in LLMs

## 1. Introduction: From Symbols to Vectors

Traditional NLP treated words as discrete symbols—indices in a dictionary. Modern LLMs transform these symbols into continuous vector representations (embeddings) that capture semantic meaning through geometric relationships in high-dimensional space.

## 2. Mathematical Foundations

### 2.1 The Embedding Function

An embedding is a mapping from discrete tokens to continuous vectors:

```
E: V → ℝ^d
token_id → [x₁, x₂, ..., x_d]
```

Where:
-   V is vocabulary size (typically 10K-100K)
-   d is embedding dimension (typically 512-8192)

Each token gets a unique d-dimensional vector

