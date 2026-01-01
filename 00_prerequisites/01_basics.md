# Basics — Before Touching Generative AI

> This document sets the **minimum mental model** required before learning Generative AI properly.

Generative AI looks magical on the surface, but underneath it is built on **very basic ideas** from:
- programming
- probability
- linear algebra
- systems engineering

If these foundations are weak, GenAI will feel confusing and random.
This file exists to **reset intuition** before moving forward.

---

## Why Prerequisites Matter

Most GenAI confusion comes from:
- jumping directly to tools
- memorizing APIs without understanding behavior
- treating LLMs like black boxes

This repository intentionally starts **slow**.

> Strong foundations reduce hallucinations — not just in models, but in learners.

---

## What You Do *Not* Need (Yet)

You **do NOT** need:
- advanced deep learning math
- transformer derivations
- research papers
- GPU programming
- fancy frameworks

Those come later.

---

## What You *Do* Need

### 1. Programming Mindset (Python-Level)

You should be comfortable with:
- variables, functions
- loops and conditionals
- lists / dictionaries
- reading simple code

Why this matters:
- GenAI workflows are *pipelines*
- prompts, responses, embeddings → all data transformations

> You don’t need to be a Python expert — just not afraid of code.

---

### 2. Deterministic vs Probabilistic Thinking

Traditional programs are **deterministic**:
same input → same output

LLMs are **probabilistic**:

This single shift explains:
- randomness
- creativity
- inconsistency
- hallucinations

If you expect GenAI to behave like `if-else`, you will be disappointed.

---

### 3. Very Basic Probability Intuition

You don’t need formulas — only intuition.

Key ideas:

- Models don’t “know” answers
- They assign probabilities to next tokens
- The highest probability token is not always chosen

Think of it as:
> “What word is most *likely* to come next?”

---

### 4. Vectors (Without Math Fear)

At a basic level:

- text → numbers
- numbers → vectors
- vectors → positions in space

Why this matters:

- embeddings
- similarity search
- retrieval (RAG)

You do NOT need to solve equations — only accept that:
> Meaning can be represented geometrically.

---

### 5. Systems Thinking (Very Important)

GenAI applications are **systems**, not models.

A typical GenAI system includes:

- input handling
- prompt construction
- model inference
- post-processing
- safety checks
- logging
- monitoring

Most failures happen **outside** the model.

---

## Common Beginner Mistakes

- Treating LLMs as databases
- Expecting exact answers every time
- Ignoring randomness
- Copying prompts without understanding them
- Overusing tools instead of learning concepts

---

## Mental Model to Carry Forward

Keep this mindset as you continue:

> LLMs do not think.  
> They predict.  
> Good systems guide prediction in useful directions.

---

## What Comes Next

Next files will cover:
- ML vs DL vs GenAI (clearly separated)
- Tokens and embeddings
- Why transformers changed everything

Do not rush.
GenAI rewards patience.

---
