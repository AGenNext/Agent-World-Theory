# Fabric Runtime

Fabric Runtime is the execution and coordination layer of an agentic world.

It connects humans, agents, policies, approvals, context, decisions, actions, outcomes, memory, and observability.

## Runtime Model

```text
Fabric Runtime
 ├── Humans
 ├── Agents
 ├── Policies
 ├── Approvals
 ├── Context
 ├── Decisions
 ├── Actions
 ├── Outcomes
 ├── Memory
 ├── Tools
 └── Observability
```

## Responsibilities

Fabric Runtime is responsible for:

- Receiving signals
- Resolving context
- Enforcing policy
- Routing work to agents or humans
- Creating decision records
- Managing approvals
- Executing allowed actions
- Recording outcomes
- Creating governed memory
- Emitting traces and audit records
- Triggering shutdown when safety limits are exceeded

## Runtime Flow

```text
Signal
  -> Context resolution
  -> Policy check
  -> Decision creation
  -> Agent recommendation
  -> Human approval
  -> Action execution
  -> Outcome observation
  -> Memory update
  -> Audit record
```

## Humans

Humans provide intent, review, approval, correction, override, and accountability.

## Agents

Agents operate as workers inside Fabric.

They may recommend, execute, observe, or learn, but they do not own the world boundary.

## Policies

Policies determine whether a decision or action is allowed.

Policies may be evaluated before context access, before tool use, before memory write, before action execution, and before outcome publication.

## Approvals

Approvals create human control points.

High-impact actions must require explicit approval before execution.

## Decisions

Decisions are durable records.

A decision connects objective, context, evidence, alternatives, recommendation, approval, action, outcome, and learning.

## Actions

Actions are governed execution steps.

No action should execute without policy, trace, and approval checks where required.

## Outcomes

Outcomes close the loop.

Every action must produce an observable result or an explicit failure record.

## Memory

Memory is created only from governed observations, outcomes, traces, and human review.

## Observability

The runtime must produce:

- Logs
- Traces
- Metrics
- Audit records
- Policy results
- Decision records
- Approval records
- Tool-call records
- Outcome records

## Runtime Rule

Fabric Runtime must make agentic execution traceable, governable, reviewable, and stoppable.
