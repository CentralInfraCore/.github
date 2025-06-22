# Versioning in CIC

In CentralInfraCore (CIC), versioning is not just a label on a file — it is a **formal declaration of contextual meaning, behavioral expectations, and knowledge scope**.

---

## 🧠 What Versioning Means

In CIC, versions define:

* the **semantic interpretation** (e.g. schema v0.1 vs v1.0)
* the **execution pathway** (e.g. relays that only support v1.0)
* the **AI navigation context** (e.g. prompts valid only in certain versions)

---

## 📌 Where Versions Apply

* **Schemas**: `schema/version: v0.1`, `cert/selfsigned/v1.0`
* **Objects**: embedded into `object.kind` references
* **Relays**: listed via `supports: [v0.1, v0.2]`
* **Prompts**: bound to specific schema contexts

---

## 🧩 Types of Versioning

| Type     | Example         | Purpose                                   |
| -------- | --------------- | ----------------------------------------- |
| Stable   | v1.0            | Frozen and documented                     |
| Preview  | v0.2-beta       | AI-navigable but not production           |
| Internal | internal-202506 | Used for internal tests or migration only |

---

## 🔁 Version Transition Flow

1. Schema update (`v0.2`): new fields or inheritance logic
2. Relay update: compatibility matrix adjustment
3. Prompt revision: response logic or context shift

---

## 🎯 Why It Matters

* Enables **safe knowledge evolution** without system breakage
* Supports **parallel PoC and production schema usage**
* Helps AI **select the right interpretation path**

---

*Created in collaboration with AI. Knowledge doesn't just evolve — it versions.*
