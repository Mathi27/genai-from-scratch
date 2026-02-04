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

## 2.2 The Embedding Matrix

The complete embedding space is represented as a matrix:

```
W ∈ ℝ^(V × d)
```

Where row i contains the embedding vector for token i. For a 50K vocabulary with d=4096:

**Parameters:** 50,000 × 4,096 = **204.8** million

**Memory**: **~410 MB** (in bfloat16)

