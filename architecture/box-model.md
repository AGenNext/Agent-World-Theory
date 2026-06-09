# Box Model

The Box Model defines the structure of an atomic capability boundary inside an agentic world.

A box is the smallest reusable building block of Fabric.

## Model

```text
Box
 ├── Schema
 ├── Relations
 ├── Policies
 ├── Events
 ├── Functions
 ├── APIs
 ├── UI Contracts
 ├── Tests
 ├── Observability
 └── Seed Data
```

## Schema

The schema defines the data owned by the box.

A box should make ownership explicit so that world state does not become hidden across tools, prompts, or workflows.

## Relations

Relations define how the box connects to other boxes.

In a SurrealDB-backed Fabric, relations may be represented as graph edges between records.

## Policies

Policies define what is allowed inside the box.

They may govern access, execution, approval, data handling, memory, tool use, and shutdown behavior.

## Events

Events define how the box reacts to changes and how it notifies the wider Fabric.

A box may emit events when state changes, decisions are created, approvals are requested, actions are executed, or outcomes are observed.

## Functions

Functions define reusable logic owned by the box.

They may validate state, compute scores, prepare context, transform evidence, or generate derived records.

## APIs

APIs expose the box capability to humans, agents, services, and other boxes.

## UI Contracts

UI contracts define how the box can be represented inside a console, workflow screen, dashboard, editor, or decision workspace.

## Tests

Tests prove that the box behaves correctly and safely.

A box must be independently testable before it is assembled into a buildpack.

## Observability

Observability defines the traces, logs, metrics, audit entries, and decision records required for the box.

## Seed Data

Seed data provides a minimal runnable example of the box.

## Box Manifest

A box should be described by a manifest.

```yaml
name: decision-box
version: 0.1.0
kind: fabric.box

description: Decision object, alternatives, recommendation, and approval state.

surreal:
  schema: schema.surql
  seed: seed.surql
  queries: queries.surql
  functions: functions.surql
  events: events.surql
  permissions: permissions.surql

contracts:
  api: openapi.yaml
  ui: ui.contract.json
  events: events.yaml

depends_on:
  - entity-box
  - context-box
  - evidence-box
  - policy-box

exports:
  tables:
    - decision
    - alternative
  relations:
    - has_alternative
    - supported_by
    - requires_approval
  apis:
    - POST /decisions
    - GET /decisions/:id
    - POST /decisions/:id/recommend
```

## Box rule

A box must be independently understandable, testable, composable, and replaceable.
