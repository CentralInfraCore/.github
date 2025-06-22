# Modularity in the CIC System

In CentralInfraCore (CIC), modularity is not just code reuse — it is **schema-driven functional separation** and **graph-level recomposability**.

---

## 🧱 What is a Module in CIC?

A module:

* is identified by a `kind` and `version`
* defines its own schema (input, state, relay behavior)
* can act as a relayable component or self-contained processor

Examples:

* `cert/selfsigned`
* `vault/secret`
* `node/basic`

---

## 🧩 Principles of Modularity

### 1. **Schema-Based Isolation**

Each module has its own schema and inheritance path.

### 2. **Graph Integration**

Modules act as attachable nodes within the relay-execution graph.

### 3. **AI Navigability**

Modules can be discovered and explained via prompts, linked schemas, or context logic.

### 4. **Execution Isolation**

Modules can handle their own state transitions and relay decisions independently.

---

## 🔗 Module Relationships

Modules can have:

* **Inheritance** (e.g. `node/k8s` inherits `node/basic`)
* **Relay Routing** (e.g. `cert/selfsigned` → `vault/secret`)
* **Role-Based Activation** (e.g. visible only in specific prompt paths)

---

## 📌 Example Module

```yaml
kind: cert/selfsigned
version: v0.1
schema:
  required: [cn, duration]
relay:
  triggers: [vault/secret]
```

---

## 🎯 Why It Matters

* Modular structure enables **scaling PoCs into real systems**
* Supports **role-based control, filtering, and validation**
* Gives AI systems **structured building blocks** to interpret and route logic

---

*Created in collaboration with AI. Every module is a directed function.*
