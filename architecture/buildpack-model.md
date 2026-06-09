# Buildpack Model

The Buildpack Model defines how boxes are assembled into runnable worlds, capabilities, applications, and decision systems.

A buildpack is the BuildKit for Agent World Theory.

## Model

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

## Boxes

A buildpack declares which boxes are required and which are optional.

Required boxes must be present before the buildpack can run.

## Dependencies

Dependencies define ordering and compatibility between boxes.

For example, a Decision Box may require Context, Evidence, Policy, Approval, and Outcome boxes.

## Wiring

Wiring defines how boxes connect.

In a SurrealDB-backed Fabric, wiring can map to graph relations between records.

Example:

```text
Signal -> has_context -> Context
Signal -> produces_decision -> Decision
Decision -> supported_by -> Evidence
Decision -> requires_approval -> Approval
Decision -> triggers_action -> Action
Decision -> produced_outcome -> Outcome
Outcome -> creates_memory -> Memory
```

## Policies

Policies define what must be enforced before, during, and after execution.

A buildpack may require identity checks, data-handling checks, approval gates, safety gates, audit gates, or shutdown gates.

## Workers

Workers are runtime processes used by the buildpack.

Examples:

- Decision recommender
- Policy checker
- Context retriever
- Evidence ranker
- Approval router
- Outcome observer
- Memory writer

## APIs

The buildpack defines which APIs the assembled system exposes.

Examples:

- POST /signals
- GET /decisions/:id
- POST /decisions/:id/recommend
- POST /decisions/:id/approve
- POST /decisions/:id/outcome

## UI Screens

The buildpack may define screens for a console or workspace.

Examples:

- Signal inbox
- Context workspace
- Evidence view
- Decision graph
- Recommendation review
- Approval gate
- Outcome report

## Deployment

Deployment defines where and how the assembled system runs.

Targets may include local sandbox, Kubernetes, edge box, private cloud, or hosted Fabric.

## Verification

Verification proves that the buildpack is valid.

It must check dependency resolution, schema validity, relation validity, policy presence, test coverage, and safety conformance.

## Safety Gates

Safety gates block execution if required safety controls are missing.

A buildpack must not run unsafe autonomous workflows without identity, policy, approval, audit, trace, and shutdown controls.

## Buildpack Manifest

```yaml
name: decision-intelligence-buildpack
version: 0.1.0
kind: fabric.buildpack

description: Composes boxes into a full decision intelligence loop.

boxes:
  - entity-box
  - signal-box
  - context-box
  - evidence-box
  - decision-box
  - policy-box
  - approval-box
  - action-box
  - outcome-box
  - memory-box
  - agent-box

wiring:
  - from: signal
    relation: has_context
    to: context
  - from: signal
    relation: produces_decision
    to: decision
  - from: decision
    relation: supported_by
    to: evidence
  - from: decision
    relation: has_alternative
    to: alternative
  - from: decision
    relation: requires_approval
    to: approval
  - from: decision
    relation: triggers_action
    to: action
  - from: decision
    relation: produced_outcome
    to: outcome
  - from: outcome
    relation: creates_memory
    to: memory

runtime:
  workers:
    - decision-recommender
    - policy-checker
    - approval-router
    - outcome-observer
    - memory-writer

ui:
  screens:
    - signals
    - context
    - evidence
    - decision-graph
    - recommendation
    - approval
    - outcome

deploy:
  target: sandbox
  database: surrealdb

safety:
  human_approval_required: true
  audit_log_required: true
  trace_required: true
  shutdown_required: true
```

## Buildpack rule

A buildpack must make assembly repeatable, testable, portable, and safe.
