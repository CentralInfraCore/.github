# Schema in CIC

In CentralInfraCore (CIC), **schema** is the backbone of system logic — not just a data definition. It encodes structural rules, validation logic, default inheritance, and interaction constraints for each object type.

## What is a Schema?

A schema in CIC defines:

* **Required fields**: What must be present in a valid object
* **Optional fields with defaults**: Parameters that can be omitted but have known fallback values
* **Type constraints**: Accepted formats (string, list, bool, etc.)
* **Nested logic**: Object substructures and inheritance behavior
* **Semantic exclusions**: Mutually exclusive attributes or combinations

Schemas are declared as YAML objects and versioned (e.g. `v0.1/node/basic`).

## Schema Roles

* **Input validation**: Validate incoming declarative definitions
* **Relay configuration**: Enable conditional execution paths
* **State derivation**: Generate default or computed values
* **Documentation aid**: Guide both AI and human comprehension

## Example Fragment

```yaml
kind: cic-node
version: v0.1
schema:
  required:
    - os
    - network.ip
  optional:
    hostname: auto
    ssh: false
  mutually_exclusive:
    - [ip, dhcp]
```

This schema ensures:

* An object must define `os` and `network.ip`
* `hostname` is optional but defaults to `auto`
* Cannot define both `ip` and `dhcp`

## Schema vs Static Typing

| Feature          | Static Typing     | CIC Schema                         |
| ---------------- | ----------------- | ---------------------------------- |
| Target           | Code              | Infrastructure descriptors         |
| Runtime context  | Compilation       | Validation + derivation + relay    |
| Extendable logic | Limited           | Fully YAML-defined modular schemas |
| Usage            | Developer tooling | Operator + AI + Relay integrations |

## Design Goals

* Provide **strict, testable contracts** between layers
* Allow for **modular expansion** and inheritance
* Enable **runtime validation without runtime coding**

---

*Created in collaboration with AI. Human-authored, schema-validated.*
