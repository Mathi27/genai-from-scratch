# ReAct Prompting (Reason + Act)

## What is ReAct Prompting?

**ReAct (Reason + Act)** is a prompting technique introduced by researchers at **Princeton University** and **Google Research** that enables Large Language Models (LLMs) to:

- **Reason step-by-step**
- **Take actions using tools**
- **Observe results**
- Improve final answers through iterative reasoning

Instead of only generating text, the model alternates between:
> **Thought → Action → Observation → Thought → ... → Final Answer**

---

## Why ReAct?

Traditional prompting:
- Model reasons internally
- Directly outputs final answer
- No external verification

ReAct prompting:
- Makes reasoning explicit
- Uses external tools (search, calculator, database)
- Updates reasoning based on real observations
- Reduces hallucination

---

## Core Structure

A typical ReAct pattern looks like:

