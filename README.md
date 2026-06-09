# Agent World Theory

A theory of executable worlds for governed agentic systems.

Agent World Theory defines a composable model for building agentic systems from governed worlds, boxes, contexts, decisions, actions, and outcomes.

An agent does not operate in empty space.

An agent operates inside a world.

A world is made of boxes. A box contains state, tools, context, policy, memory, and observable boundaries.

A buildpack assembles boxes into runnable agentic environments.

Fabric is the operating layer that connects boxes, buildpacks, agents, decisions, actions, and outcomes.

SurrealDB is the toolbox substrate used to model records, graph relations, search, memory, events, permissions, and state transitions.

> **Researcher-only testing**
>
> Tests may only be run by researchers who have implemented and acknowledged **ALL Agent Safety Protocols** defined in this GitHub organization.
>
> If safety conformance fails, testing is blocked.

## Start reading

Use this repository as a GitBook source. Start with [SUMMARY.md](SUMMARY.md).

## Core stack

```text
World
  └── Fabric
        └── Buildpacks
              └── Boxes
                    └── SurrealDB Toolbox
```

## Product grammar

```text
Build with Boxes.
Assemble with Buildpacks.
Run on Fabric.
Store in SurrealDB.
```
