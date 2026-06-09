# Buildpack

A Buildpack is the BuildKit for agentic worlds.

A buildpack assembles boxes into runnable capabilities, applications, environments, or decision systems.

A buildpack does not replace boxes. It defines how boxes are selected, wired, verified, and deployed.

## Definition

A Buildpack contains:

- Required boxes
- Dependency rules
- Graph wiring
- Policies
- Runtime workers
- APIs
- UI screens
- Deployment recipe
- Verification checks
- Safety gates
- Observability requirements

## Principle

A world should not be assembled manually every time.

Reusable worlds need reusable assembly logic.

Buildpacks make world construction repeatable, testable, auditable, and portable.

## Buildpack model

```text
Buildpack
 ├── Boxes
 ├── Dependencies
 ├── Wiring
 ├── Policies
 ├── Workers
 ├── APIs
 ├── UI Screens
 ├── Deployment
 ├── Verification
 └── Safety Gates
```

## Buildpack responsibilities

A buildpack must define:

- Which boxes are required
- Which boxes are optional
- How boxes are connected
- Which policies are enforced
- Which workers are started
- Which APIs are exposed
- Which screens are available
- Which deployment targets are supported
- Which test suites must pass
- Which safety gates block execution

## Example buildpacks

Common buildpacks include:

- Decision Intelligence Buildpack
- Agent Runtime Buildpack
- Governance Buildpack
- Workflow Buildpack
- Learning Buildpack
- RAG Buildpack
- Commerce Buildpack
- Identity Buildpack

## Decision Intelligence Buildpack

The Decision Intelligence Buildpack composes:

- Signal Box
- Context Box
- Evidence Box
- Decision Box
- Alternative Box
- Policy Box
- Approval Box
- Action Box
- Outcome Box
- Memory Box
- Agent Box

into a full decision lifecycle:

```text
Signal -> Context -> Evidence -> Decision -> Approval -> Action -> Outcome -> Memory
```

## Buildpack and Fabric

Fabric runs buildpacks.

The buildpack defines the assembly plan. Fabric executes, observes, and governs the assembled system.
