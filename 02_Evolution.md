# Evolution of Language Models  
n-grams → RNNs → Transformers

---

## 1. n-gram Language Models

### Core Idea
Predict the next token using the previous **n minus 1** tokens.

Probability of the current token given the previous n minus 1 tokens.

P(current token | previous n−1 tokens)

### Strengths
- Simple and interpretable
- Fast to train
- Strong baseline for small datasets

### Limitations
- Fixed context window
- Exponential growth in parameters
- Poor generalization to unseen sequences
- Sparse data problem

### Key Takeaway
Local statistics without real language understanding.

---

## 2. Recurrent Neural Networks (RNNs)

### Core Idea
Maintain a hidden state that summarizes all past tokens.

Hidden state at time t is computed from:
- Hidden state at time t minus 1
- Current input token

This allows information to flow through time.

### Common Variants
- Vanilla RNN
- Long Short-Term Memory (LSTM)
- Gated Recurrent Unit (GRU)

### Strengths
- Handles variable-length sequences
- Learns temporal dependencies
- Better generalization than n-grams

### Limitations
- Vanishing and exploding gradient problems
- Sequential computation limits speed
- Long-range dependencies are difficult
- Inefficient hardware utilization

### Key Takeaway
Introduced memory, but did not scale well.

---

## 3. Transformers

### Core Idea
Replace recurrence with self-attention.

Each token computes how much attention to pay to every other token in the sequence.
The output is a weighted sum of all tokens based on their relevance.

### Strengths
- Global context available in every layer
- Fully parallel computation
- Scales effectively with data and compute
- Strong modeling of long-range dependencies

### Limitations
- Attention cost grows quadratically with sequence length
- High memory consumption
- Requires large datasets for training

### Key Takeaway
Attention enables scale, and scale enables intelligence.

---

## 4. Comparison Summary

| Property | n-grams | RNNs | Transformers |
|--------|--------|------|--------------|
| Context handling | Fixed window | Sequential memory | Global attention |
| Parallelism | High | Low | Very high |
| Long-range dependency | No | Limited | Yes |
| Scalability | Poor | Limited | Excellent |
| Modern usage | Obsolete | Rare | Standard |

---

## 5. Why Transformers Won

- Parallelism matches modern GPU and TPU hardware
- Stable training for very large models
- Better inductive bias for language understanding
- Foundation architecture for large language models

---

## 6. Final Insight

Language modeling evolved from counting words,
to remembering sequences,
to attending over all context.

Transformers did not just improve performance.
They changed how intelligence scales.

---
Author : Mathi Yuvarajan T.K