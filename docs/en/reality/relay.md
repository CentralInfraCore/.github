# Relay in CIC

In the CentralInfraCore (CIC) system, a **relay** is not a transport protocol or message queue — it's a logical control point. It governs how state transitions are validated, applied, and propagated in a schema-bound infrastructure.

## What is a Relay?

A relay is a **schema-aware execution node** that receives input (e.g. new configuration or object declaration), validates it against a known schema, and:

* applies it to the appropriate object scope,
* tracks state transitions,
* optionally forwards to downstream systems (renderers, modules, CRD handlers).

Relays are composable and chainable: a relay can both terminate and relay further, enabling DAG-like execution logic.

## Relay Responsibilities

* **Schema validation**: Ensure inputs conform to structural and semantic rules.
* **Relay headers**: Use metadata to control propagation, versioning, and context.
* **State mutation**: Apply changes only if delta exists and validation passes.
* **Context handoff**: Provide output in a relay-ready format for the next system.

## Example Workflow (Self-Signed Certificate)

```yaml
- input: new object "selfsigned-cert-abc"
- relay: validates schema (v0.1/cert/selfsigned)
- updates: desired state with expiry, DNS SAN, key parameters
- forwards to: state-tracker and secret generator
```

## Relay vs Traditional Execution

| Feature          | Traditional CI/CD  | CIC Relay                      |
| ---------------- | ------------------ | ------------------------------ |
| Trigger          | Commit or webhook  | State + schema-delta + headers |
| Validation       | Manual or implicit | Schema-enforced                |
| Flow logic       | Pipeline steps     | Directed relay paths           |
| Reusability      | Scripted modules   | Composable schema-linked nodes |
| Failure handling | Runtime error      | Structured reverse relay       |

## Design Goals

* Make infrastructure state changes **verifiable and reversible**
* Support both **human and AI-originated input**
* Allow **fine-grained control** over execution flow

---

*Created in collaboration with AI. Human-authored, schema-aligned.*
