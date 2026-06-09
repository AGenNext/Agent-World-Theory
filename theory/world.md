# World

A World is a bounded operating environment where agents, humans, systems, data, policies, decisions, actions, and outcomes interact.

A world is not a prompt. A world is not a workflow. A world is not a tool list.

A world is the explicit operating boundary inside which agentic activity becomes understandable, governable, observable, and testable.

## Definition

A World contains:

- Identity
- Context
- State
- Policy
- Memory
- Decisions
- Actions
- Outcomes
- Humans
- Agents
- Tools
- Evidence
- Approvals
- Observability

## Principle

Agentic systems fail when the world is implicit.

If the world is hidden inside prompts, agents cannot reliably know what exists, what changed, who approved action, what policies apply, or what outcome occurred.

## World model

```text
World
 ├── Identity
 ├── Context
 ├── State
 ├── Policy
 ├── Memory
 ├── Decisions
 ├── Actions
 ├── Outcomes
 ├── Humans
 ├── Agents
 ├── Tools
 ├── Evidence
 ├── Approvals
 └── Observability
```

## World boundary

A world must define:

- What exists
- Who owns it
- What state it is in
- What can act on it
- What policies apply
- What data can be used
- What actions require approval
- What evidence supports decisions
- What outcomes are expected
- What must be logged
- What must trigger shutdown

## World and agents

An agent operates inside a world.

The world provides the context, constraints, permissions, memory, tools, and safety boundary. The agent may reason or act, but the world governs the action.

## World and decisions

A decision is a first-class object inside a world.

A decision connects signal, context, evidence, alternatives, recommendation, approval, action, outcome, and memory.

## World and Fabric

Fabric is the runtime operating layer of a world.

Fabric connects boxes, buildpacks, policies, agents, humans, actions, and outcomes into a coherent system.
