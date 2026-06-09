# World Stack

The World Stack describes how Agent World Theory is implemented as a layered system.

```text
World
  -> Fabric
    -> Buildpacks
      -> Boxes
        -> SurrealDB Toolbox
```

## Layer 1: World

A World is the bounded operating environment.

It defines what exists, who participates, what policies apply, what can happen, what must be observed, and how outcomes are recorded.

## Layer 2: Fabric

Fabric is the operating layer of the world.

It connects boxes, buildpacks, humans, agents, policies, decisions, actions, outcomes, and memory.

Fabric is responsible for continuity, governance, observability, and execution.

## Layer 3: Buildpacks

Buildpacks assemble boxes into runnable capabilities.

A buildpack defines required boxes, dependency rules, graph wiring, runtime workers, UI screens, APIs, deployment recipes, verification checks, and safety gates.

## Layer 4: Boxes

Boxes are the atomic reusable capability boundaries.

A box contains schema, relations, events, policies, functions, APIs, UI contracts, tests, observability, and seed data.

## Layer 5: SurrealDB Toolbox

SurrealDB provides the database toolbox used by boxes and Fabric.

It may provide records, graph relations, full-text search, vector search, events, permissions, transactions, and live queries.

## Operating flow

```text
Signal enters World
  -> Fabric receives and routes it
  -> Buildpack selects required capability path
  -> Boxes process state, policy, context, and evidence
  -> SurrealDB stores and queries the graph
  -> Fabric records decision, action, outcome, and memory
```

## Core principle

The world defines the boundary.

Fabric operates the boundary.

Buildpacks assemble capabilities.

Boxes provide reusable building blocks.

SurrealDB provides the toolbox.
