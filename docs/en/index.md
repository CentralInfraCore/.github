# CentralInfraCore Documentation – English Overview

This page summarizes the entire English-language documentation structure of the CIC system. The goal is to clearly explain the system’s PoC-level functionality, core concepts, and design philosophy.

---

## 🧠 Introduction

* [`cic.md`](./meta/cic.md): What is CIC? Who is it for? What does it currently do?

---

## 🔍 Reality Layer (`reality/`)

* [`relay.md`](./reality/relay.md): Relays and execution logic
* [`state.md`](./reality/state.md): Declared, derived, and observed state
* [`schema.md`](./reality/schema.md): Schema as contract
* [`error.md`](./reality/error.md): Relay-based error handling

---

## 🧬 Meta Layer (`meta/`)

* [`graph.md`](./meta/graph.md): Relay and knowledge graph
* [`modularity.md`](./meta/modularity.md): Modular architecture
* [`philosophy.md`](./meta/philosophy.md): System philosophy and mindset
* [`versioning.md`](./meta/versioning.md): Schema and component versioning

---

## 🤖 AI Integration (`meta/` + root)

* [`_ai_prompt_index.yaml`](../../_ai_prompt_index.yaml): AI navigation entry point
* [`meta/ai_prompt_index.explained.md`](../../_ai_prompt_index.explained.md): Human explanation of prompt navigation

---

## 🧪 Knowledge Scope Target: v1.0

This documentation covers the CIC system **up to the self-signed certificate flow** and \*\*schema-driven state logic
