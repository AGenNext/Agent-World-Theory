# Decision Intelligence World

Decision Intelligence World is the first reference world for Agent World Theory.

It demonstrates how a governed world turns signals, context, evidence, decisions, approvals, actions, outcomes, and memory into a closed operating loop.

## Purpose

A Decision Intelligence World makes decisions first-class objects.

A decision is not hidden inside a prompt, chat response, workflow, or dashboard.

A decision is stored, explained, approved, executed, measured, learned from, and governed.

## World Stack

```text
Decision Intelligence World
  -> Fabric
    -> Decision Intelligence Buildpack
      -> Decision Boxes
        -> SurrealDB Toolbox
```

## World Objects

The world contains:

- Signal
- Context
- Evidence
- Decision
- Alternative
- Recommendation
- Approval
- Action
- Outcome
- Memory
- Agent
- Policy

## Box Composition

The Decision Intelligence Buildpack assembles:

- Signal Box
- Context Box
- Evidence Box
- Decision Box
- Alternative Box
- Approval Box
- Action Box
- Outcome Box
- Memory Box
- Agent Box
- Policy Box

## Runtime Loop

```text
Observe
  -> Contextualize
    -> Evaluate
      -> Recommend
        -> Approve
          -> Act
            -> Measure
              -> Learn
                -> Govern
                  -> Observe
```

## Decision Flow

```text
Signal
  -> Context
    -> Evidence
      -> Decision
        -> Alternatives
          -> Recommendation
            -> Approval
              -> Action
                -> Outcome
                  -> Memory
```

## Graph Model

```text
Signal
  -> has_context -> Context
  -> supported_by -> Evidence
  -> produces_decision -> Decision

Decision
  -> has_alternative -> Alternative
  -> requires_approval -> Approval
  -> triggers_action -> Action
  -> produced_outcome -> Outcome

Outcome
  -> creates_memory -> Memory
```

## Example Scenario

A revenue drop is detected in APAC enterprise accounts.

```text
Signal:
Revenue decline in APAC enterprise segment

Context:
APAC, enterprise customers, Q3, renewal period

Evidence:
CRM report, support tickets, renewal history, account notes

Decision:
Launch account outreach program

Approval:
Growth Manager approval required

Action:
Create outreach campaign in CRM

Outcome:
Retention improves by 9.8 percent

Memory:
Outreach worked better than discounting for high-value accounts
```

## Decision Contract

```yaml
decision:
  id:
  objective:
  signal:
  context:
  evidence:
  alternatives:
  recommendation:
  confidence:
  approval:
  action:
  outcome:
  memory:
```

## Approval Contract

```yaml
approval:
  required: true
  approver:
  timestamp:
  decision_id:
  result:
  comment:
```

## Outcome Contract

```yaml
outcome:
  decision_id:
  expected:
  actual:
  variance:
  confidence:
  lessons:
```

## Memory Contract

```yaml
memory:
  source_decision:
  outcome:
  confidence:
  summary:
  reusable:
```

## Buildpack Manifest

```yaml
name: decision-intelligence-buildpack
version: 0.1.0
kind: fabric.buildpack

boxes:
  - signal-box
  - context-box
  - evidence-box
  - decision-box
  - alternative-box
  - approval-box
  - action-box
  - outcome-box
  - memory-box
  - agent-box
  - policy-box

runtime:
  fabric

database:
  surrealdb

safety:
  human_approval_required: true
  audit_log_required: true
  trace_required: true
  shutdown_required: true
```

## Natural End State

The Decision Intelligence World is complete when every important action can answer:

- What signal started this?
- What context was used?
- What evidence supported it?
- What alternatives were considered?
- What decision was made?
- Who or what approved it?
- What action happened?
- What outcome occurred?
- What did the world learn?
- What policy governed the loop?

When those questions are answerable, the world is observable, governable, and ready for safe research testing.

This closes the first loop of Agent World Theory.
