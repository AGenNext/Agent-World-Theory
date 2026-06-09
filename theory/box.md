# Box

A Box is the atomic reusable capability boundary of an agentic world.

A box is not only a container, not only a microservice, and not only a database table.

A box is a governed building block that packages state, schema, relations, policy, events, interfaces, tests, and observability.

## Definition

A Box contains:

- Schema
- Relations
- Events
- Policies
- Functions
- APIs
- UI contracts
- Tests
- Observability
- Seed data
- Runtime assumptions

## Principle

A world becomes scalable only when its building blocks are explicit.

Without boxes, systems collapse into hidden coupling, unclear boundaries, unsafe execution, and untestable behavior.

## Box model

```text
Box
 ├── Schema
 ├── Relations
 ├── Events
 ├── Policies
 ├── Functions
 ├── APIs
 ├── UI Contracts
 ├── Tests
 ├── Observability
 └── Seed Data
```

## Box contract

Each box must define:

- What it owns
- What it depends on
- What it exports
- What policies apply
- What events it emits
- What events it consumes
- What APIs it exposes
- What UI surfaces it supports
- What tests prove conformance
- What traces must be produced

## Box examples

Common boxes include:

- Entity Box
- Signal Box
- Context Box
- Evidence Box
- Decision Box
- Policy Box
- Approval Box
- Agent Box
- Action Box
- Outcome Box
- Memory Box

## Box and SurrealDB

SurrealDB acts as the toolbox substrate for boxes.

A box may use SurrealDB records, graph relations, full-text indexes, vector search, functions, events, permissions, and transactions.

SurrealDB is not the box.

SurrealDB provides the tools the box uses.

## Box and Buildpack

A buildpack assembles boxes into runnable capabilities.

Boxes remain independent capability boundaries. Buildpacks define how boxes are wired together.
