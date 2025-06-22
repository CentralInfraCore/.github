# AI Prompt Index – Explanation

This document explains the purpose, structure, and strategic role of the `_ai_prompt_index.yaml` file within the CentralInfraCore (CIC) system.

## Purpose

The AI prompt index is a machine-readable entrypoint that allows AI systems (like GPTs or internal assistants) to:

* Discover available prompts
* Navigate CIC concepts by topic
* Load context-specific guidance based on user roles or questions

It is not a human documentation file — it’s a relay node for intelligent assistance.

## Structure

```yaml
project: CIC
version: 0.1
prompts:
  - id: intro_to_cic
    title: What is the CIC PoC?
    file: prompts/intro_to_cic.md
```

Each prompt is declared with:

* `id`: a unique, stable identifier
* `title`: a human-facing label for display or voice interaction
* `file`: the path to the content, typically a Markdown file with the full prompt

## Role in CIC

This index supports the **relay-based execution model** of CIC by allowing the AI to:

* fetch schema-related queries
* expose only relevant guidance depending on entrypoint (UI / CLI / LLM)
* align answers with the current PoC scope and roadmap

This makes the CIC system **self-descriptive and AI-navigable**.

## Future Extensions

* Role-based prompt views (e.g. DevOps vs PM)
* Semantic filters (conceptual layer, lifecycle phase, etc.)
* Prompt chaining or relay-routing based on graph structure

## Best Practice

Keep the `_ai_prompt_index.yaml`:

* simple
* flat (not deeply nested)
* versioned (e.g. v0.1, v1.0)
* and tightly scoped to the current documentation phase

Avoid speculative entries or excessive nesting.

---

*Created in collaboration with AI. Human-authored, machine-assisted.*
