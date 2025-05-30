# 🧠 CIC Documentation – System Overview

Welcome to the **Central Infrastructure Controller (CIC)** documentation!
This system introduces a fundamentally different approach to infrastructure management:
📌 declarative, state-based, validated, and role-driven.

Documents are structured by language and purpose. Supported languages: `hu/` (Hungarian) and `en/` (English).

---

## 📁 Directory Structure and Purpose

| Directory      | Purpose                               | Keywords                   |
| -------------- | ------------------------------------- | -------------------------- |
| `concept/`     | Why does CIC exist?                   | philosophy, mindset        |
| `reality/`     | How does the system think and behave? | state logic, schema, relay |
| `interaction/` | Who interacts with it and how?        | roles, entry points        |
| `usage/`       | What does it look like in practice?   | workflows, examples        |
| `deployment/`  | System bootstrapping and integration  | init, bootstrap, runtime   |

---

## 🔍 Directory Details

### `concept/` – 🌐 System Philosophy

The core ideas that define CIC’s operation.
This section doesn’t explain mechanics — it explains **purpose and mindset**.

* `cic_gondolkodasmod.md`: Core model thinking
* `cic_brain.md`: Logical core of the system
* `alapelvek.md`: Principles — state is not desire, but verified truth

### `reality/` – 🧬 Internal Mechanics

Describes how CIC perceives itself: structure, decisions, behavior.

* `schema.md`: Structural rules and typing
* `state_model.md`: Comparison of actual and expected state
* `relay_flow.md`: CIC’s control and routing mechanism
* `error_logic.md`: Fault detection and propagation logic

### `interaction/` – 🧍 Human Perspective

Role-based entry points. Each role has its own angle into CIC’s world.

* `*_intro.md` files (DevOps, Developer, QA, Executive, etc.)
* Purpose: place system logic in **human context**

### `usage/` – 🛠️ Practical Application

Concrete examples, reusable flows, real-life implementations.

* `node_lifecycle.md`: Node lifecycle within CIC
* `deploy_with_validation.md`: Deployments through validation
* `rollback_flow.md`: How reversions are handled
* `schema_upgrade.md`: Safe schema evolution

### `deployment/` – 🚀 Bootstrapping and Environments

Technical and procedural guides for introducing CIC into an environment:

* `bootstrap.md`: Initialization and first deployment
* `env_profiles.md`: Environment-specific schema and permission deltas
* `init_matrix.md`: Schema-module startup matrix
* `integration_bridge.md`: Connecting to external systems

---

## 🎯 Purpose of This Documentation

The goal is not just to show **how CIC works**,
but also **why thinking in CIC terms changes how you see infrastructure**.

> Think in state. Validate intent. Accept only what is true.