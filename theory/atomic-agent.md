# Atomic Agent Spec v0.1

## 1. Purpose

An Atomic Agent is the smallest valid agent that may exist in the Fabric without distortion.

It must be able to:

- receive intent
- check scope
- make one bounded decision
- take one bounded action
- emit evidence
- update trust
- stop safely

## 2. Required properties

- identity
- domain
- purpose
- capability
- policy refs
- trust requirement
- resource bounds
- decision log requirement
- evidence requirement
- lifecycle state
- revocation path

## 3. Atomic Agent contract

```
apiVersion: agent.agennext.io/v1alpha1
kind: AtomicAgent
metadata:
  name: atomic-billing-status-agent
spec:
  identity: agent.atomic.billing-status
  tenant: tenant/acme
  domain: finance.billing
  purpose: "Return billing status for an authorized request"
  capability:
    name: billing-status-read
    scope: single-purpose
  inputs:
    - request.billing_id
    - request.actor_id
  outputs:
    - billing_status
    - decision_summary
  allowedResources:
    tools:
      - tool.invoice.lookup
    models:
      - model.small-policy-safe
    data:
      - data.invoice.status
  policies:
    - policy.tenant-data-only
    - policy.pii-minimized
    - policy.jit-access-required
  trust:
    minimumScore: 0.75
  runtime:
    timeout: 5s
    maxSteps: 1
    retry: 0
  logs:
    decisionLog: required
    evidence: required
  lifecycle:
    state: Active
  revoke:
    killSwitch: true
```

## 4. Atomic Agent rules

- One domain minimum
- One bounded purpose
- One primary capability
- No standing access
- No hidden memory dependency
- No silent tool use
- No silent model switch
- No multi-step autonomy without upgrade

## 5. Atomic Agent decision log minimum

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

## 6. Atomic Agent validity test

A valid Atomic Agent MUST:

- preserve spec
- stay in domain
- perform only declared capability
- emit decision log
- emit evidence
- support suspension or revocation
- complete within bounded runtime
