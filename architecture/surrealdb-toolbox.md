# SurrealDB Toolbox

SurrealDB is the toolbox substrate for Fabric.

SurrealDB is not the world. SurrealDB is not the Fabric. SurrealDB is the database toolbox used by boxes, buildpacks, and Fabric runtime.

## Toolbox Model

```text
SurrealDB Toolbox
 ├── Records
 ├── Graph Relations
 ├── Full Text Search
 ├── Vector Search
 ├── Functions
 ├── Events
 ├── Permissions
 ├── Transactions
 └── Live Queries
```

## Records

Records represent world objects.

Examples:

- signal
- context
- evidence
- decision
- alternative
- approval
- action
- outcome
- memory
- agent

## Graph Relations

Relations connect world objects.

Example:

```text
signal -> has_context -> context
signal -> produces_decision -> decision
decision -> supported_by -> evidence
decision -> requires_approval -> approval
decision -> triggers_action -> action
decision -> produced_outcome -> outcome
outcome -> creates_memory -> memory
```

## Full Text Search

Full text search supports evidence discovery, document search, and explanation retrieval.

## Vector Search

Vector search supports semantic memory, contextual retrieval, and similarity-based evidence matching.

## Functions

Functions support reusable logic near the data layer.

Examples:

- score alternatives
- validate decision state
- compute outcome accuracy
- prepare context bundles
- check graph completeness

## Events

Events support reactive world behavior.

Examples:

- signal received
- decision created
- approval requested
- action triggered
- outcome recorded
- memory created

## Permissions

Permissions enforce access boundaries for humans, agents, and systems.

Access must be explicit and scoped.

## Transactions

Transactions preserve consistency across decision, approval, action, and outcome records.

## Live Queries

Live queries support real-time consoles, decision workspaces, and observability surfaces.

## Fabric Mapping

```text
Fabric Need             SurrealDB Capability
--------------------------------------------
World objects           Records
Relationships           Graph relations
Evidence search         Full text search
Memory retrieval        Vector search
Runtime reactions       Events
Access control          Permissions
Consistency             Transactions
Realtime UI             Live queries
Reusable logic          Functions
```

## Toolbox Rule

SurrealDB provides the tools.

Fabric provides the operating model.

Boxes define the capability boundaries.

Buildpacks assemble the boxes.

Worlds define the environment.
