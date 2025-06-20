# CentralInfraCore

## Introduction

CentralInfraCore is a unified infrastructure descriptor system offering full lifecycle management—from hardware procurement to fully operational hybrid cloud environments. It introduces not only a technical toolkit, but also a structured way of thinking that has the potential to reshape infrastructure management and the DevOps mindset.

## Key Architectural Features

* **Declarative Infrastructure Definition**: Every component is described using a YAML-based, graph-like structure, providing full transparency into the system's design and state.
* **Object-Oriented Modularity**: Each function is organized into modules that are independently understandable, testable, and verifiable.
* **Event- and State-Driven Operation**: Instead of executing commands, the system tracks and reacts to state—each change passes through validated relay logic.
* **Versioned and Auditable State Logic**: All state and structural changes are logged and traceable, supporting full reproducibility and introspection.

## Infrastructure Descriptor Object Model

The CentralInfraCore model is a directed graph in which every object has a well-defined role and connection logic. This allows both semantic and state-based interpretation of the entire infrastructure.

* **Core Objects**: Independent entities with their own lifecycle, such as physical nodes, clusters, or relay endpoints.
* **Submodules**: Supporting components containing parameter sets or derived/default values. They cannot function independently but are essential for higher-level objects.
* **Semantic Exclusions**: Certain attributes exclude one another to ensure system consistency (e.g., if attribute “A” is active, “B” must be absent).

## Implementation and Integration

CentralInfraCore is not bound to a specific platform. Instead, it adapts to different environments through modular APIs and logic-based adapters tailored to the infrastructure.

* **Kubernetes Integration**: Supports Helm Chart-based deployments and tools like FluxCD, ArgoCD, or Rancher Fleet. Synchronization includes both deployment and state.
* **Traditional Environments**: The declarative model can be applied via API to virtualized or traditional Linux systems.
* **Modular API Layer**: Interfaces are exposed as standalone modules, allowing external systems to integrate at the exact level required, without compromising stability or scalability.

## GitOps Approach

CentralInfraCore not only adopts GitOps—it extends it. The system treats Git not just as a version source, but as a real-time reference of infrastructure state.

* **Central Git Repository**: Infrastructure states and descriptions are stored in structured directories. A Git commit triggers not just a change, but a validated state transition.
* **Automated and Validated Execution**: Every change is applied through schema validation and relay-controlled flows, enabling meaningful automation.
* **CI/CD at the Knowledge Level**: Integration occurs not just at code level, but at the knowledge layer. Logic and state are both testable and traceable.

## Use Cases

CentralInfraCore is more than a toolset for managing complex infrastructures—it is a mindset shift in how infrastructure is described, validated, and maintained.

It is especially effective in environments that:

* Require unified visibility and control over physical, virtualized, and container-based systems.
* Demand traceable, versioned, and rollback-capable state representation.
* Need scalable, modular architecture that supports organizational growth.
* Value configurations that are interpretable, enforceable, and reversible by both humans and machines.

CIC is especially powerful when the goal is to align thinking with execution—not just deploy code, but operate with infrastructure-level cognition.

## Documentation Structure

This repository provides a layered documentation system for both human and machine understanding:

* **Bilingual conceptual knowledge base**: `docs/`

    * `interaction/`: role-based introductory content (e.g., DevOps, PM, Architect)
    * `reality/`: infrastructure logic (e.g., relay, state, schema)
    * `concept/`: the mindset and theoretical foundations
    * `usage/`: lifecycle, rollback, schema evolution examples

* **AI-compatible navigation layer**:

    * Educational prompts: `prompts/`
    * Machine navigation map: `_ai_prompt_index.yaml`
    * Structural metadata: `meta/cic.yaml`

This structure enables users—human or AI—to access the system’s logic at different depths and perspectives.

## Additional Information

Contact and Support:

* Project Lead: Gábor Zoltán Sinkó

## License

This project is licensed under the [Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International (CC BY-NC-SA 4.0)](https://creativecommons.org/licenses/by-nc-sa/4.0/).

*This document was created in collaboration with artificial intelligence and refined through human validation.*
