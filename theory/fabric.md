# Fabric

Fabric is the operating layer of an agentic world.

Fabric connects worlds, buildpacks, boxes, humans, agents, policies, decisions, actions, outcomes, and memory.

Fabric is responsible for continuity, governance, observability, and execution.

## Definition

Fabric is the runtime operating layer that makes a world work.

A world defines the operating boundary.

Boxes define reusable capabilities.

Buildpacks define assembly.

Fabric coordinates the assembled system.

## Responsibilities

Fabric is responsible for:

- State continuity
- Identity continuity
- Context delivery
- Policy enforcement
- Decision traceability
- Approval orchestration
- Action routing
- Outcome observation
- Memory creation
- Learning loops
- Auditability
- Shutdown coordination

## Fabric model

```text
World
  -> Fabric
    -> Buildpacks
      -> Boxes
        -> Runtime substrate
```

## Fabric principle

A world defines what exists.

Boxes define capabilities.

Buildpacks define assembly.

Fabric makes the system operate.

## Fabric runtime

Fabric coordinates:

- Humans
- Agents
- Policies
- Decisions
- Actions
- Outcomes
- Memory
- Tools
- Evidence
- Approvals

while preserving:

- Safety
- Auditability
- Traceability
- Explainability
- Accountability
- Reversibility where required

## Fabric and decisions

Decision Intelligence is the first application of Fabric.

In a Decision Intelligence world, Fabric connects:

```text
Signal -> Context -> Evidence -> Decision -> Approval -> Action -> Outcome -> Memory
```

The decision is not hidden inside an agent response.

The decision is a governed world object.

## Fabric and agents

Agents operate inside Fabric.

An agent may recommend, execute, observe, or learn, but Fabric provides the control boundary.

Fabric decides when policy must be checked, when approval is required, when action is blocked, and when shutdown must occur.

## Fabric and SurrealDB

SurrealDB is the toolbox substrate.

Fabric is the operating model.

SurrealDB provides:

- Records
- Graph relations
- Search
- Memory
- Events
- Permissions
- Transactions
- Live queries

Fabric uses those capabilities to create governed, observable, and executable worlds.

## Fabric is not

Fabric is not only a database.

Fabric is not only a workflow engine.

Fabric is not only an agent runtime.

Fabric is not only a dashboard.

Fabric is the connective operating layer that makes agentic systems governable.
