# CentralInfraCore

## Introduction

CentralInfraCore is a unified infrastructure descriptor system providing complete lifecycle management, from hardware procurement to fully operational hybrid cloud environments. Its goal is to create a declarative, object-oriented infrastructure management model offering transparency, modularity, and comprehensive state management with version control.

## Key Features

- **Declarative Description**: Unified YAML-based configuration organized into hierarchical, graph-like structures for infrastructure definition.
- **Modular Architecture**: Implementation details encapsulated in modular components, independently understandable and maintainable.
- **Event-Driven Operations**: Components communicate through event-driven processes and scheduled state queries, enabling dynamic scalability and rapid response.
- **State Management**: Continuous tracking, versioning, and auditability of all changes, ensuring accurate infrastructure representation.

## Infrastructure Descriptor Object Model

The infrastructure descriptor is structured as a directed graph:

- **Core Objects**: Independently meaningful entities with standalone lifecycle management.
- **Submodules**: Objects containing parameter sets, default values, or derived values.
- **Mutually Exclusive Values**: Certain variables exclude each other to maintain consistency (e.g., variable "A" excludes the presence of "B").

## Implementation and Integration

The system supports diverse implementations:

- **Kubernetes Integration**: Supports Helm Charts via FluxCD, ArgoCD, and Rancher Fleet.
- **Traditional System Integration**: Unified APIs manage non-cloud-native environments.
- **Modular API Layer**: External operators and management tools interface through modular APIs, separating specific implementation details from infrastructure definitions.

## GitOps Approach

CentralInfraCore adheres to a GitOps-driven operational model:

- **Central Git Repository**: Version-controlled infrastructure descriptions organized within a clear directory structure.
- **Automated Deployment**: Automated application and validation of state changes driven by Git commits.
- **Continuous Integration (CI) & Continuous Delivery (CD)**: Enhanced testability and rapid iteration, minimizing redundancy.

## Use Cases

CentralInfraCore is ideal for enterprise environments:

- Operating complex infrastructures (physical, virtualized, Kubernetes).
- Requiring precise version control, auditability, and rapid recovery capabilities.
- Managing hybrid infrastructure with a need for flexibility and modular scalability.

## Documentation

Complete documentation is available as part of the project:

- Infrastructure Description: `docs/spec.md`
- Module Development: `modules/`
- CRD and Operator Development: `operator/`
- [CIC as a Cognitive Model – Full Essay](https://github.com/CentralInfraCore/.github/blob/main/docs/CIC_as_a_Cognitive_Model.md)

## Additional Information

Contact and Support:

- Project Lead: Gábor Zoltán Sinkó

## 🔐 License

This work is licensed under  
**Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International (CC BY-NC-SA 4.0)**  
See [`LICENSE.md`](./LICENSE.md) for full terms.

> Commercial integration into proprietary systems is only allowed with explicit written permission.

