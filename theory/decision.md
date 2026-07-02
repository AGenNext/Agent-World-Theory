# Decision

A decision is a first-class world object connecting objective, context, evidence, alternatives, recommendation, approval, action, outcome, and learning.

## Definition

Every important action must connect back to a decision record. A decision is not hidden inside an agent response. A decision is a governed world object.

## Decision record

```
decision_id
agent_id
request_id
purpose
policy_result
trust_before
resource_used
decision
action_taken
evidence_ref
trust_after
verdict
```

## Decision lifecycle

```
Signal → Context → Evidence → Decision → Approval → Action → Outcome → Memory
```
