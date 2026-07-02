# Atomic Kube Spec v0.1

## 1. Purpose

An Atomic Kube is the smallest valid delivery unit that can run, prove, heal, and stop inside the Fabric.

It must be able to:

- declare one promise
- start
- be observed
- emit evidence
- be reconciled
- stop safely

## 2. Required properties

- identity
- domain
- promise
- runtime contract
- port binding
- policy refs
- health contract
- evidence contract
- lifecycle state
- revocation path

## 3. Atomic Kube contract

```
apiVersion: kube.agennext.io/v1alpha1
kind: AtomicKube
metadata:
  name: atomic-billing-status-kube
spec:
  identity: kube.atomic.billing-status
  tenant: tenant/acme
  domain: finance.billing
  promise: "Serve authorized billing status requests"
  workload:
    image: ghcr.io/acme/billing-status:1.0.0
    command: ["/app/run"]
    port: 8080
  ports:
    ingress:
      - port.billing-status.read
    egress: []
  policies:
    - policy.tenant-data-only
    - policy.signed-artifact-only
    - policy.jit-access-required
  health:
    path: /healthz
    readiness: required
    liveness: required
  trust:
    minimumScore: 0.80
  evidence:
    logs: required
    metrics: required
    traces: required
  runtime:
    replicas: 1
    autoscale: false
    timeout: 30s
  lifecycle:
    state: Active
  revoke:
    killSwitch: true
```

## 4. Atomic Kube rules

- One promise minimum
- One bounded runtime contract
- One observable health model
- No opaque side effects
- No undeclared port
- No unsigned artifact
- No evidence-free execution
- No drift without reconciliation

## 5. Atomic Kube validity test

A valid Atomic Kube MUST:

- start from declared spec
- expose only declared ports
- satisfy health contract
- emit runtime evidence
- support reconciliation
- support suspension and revocation
- preserve promise under observation

## 6. Relation between Atomic Agent and Atomic Kube

Atomic Agent decides and acts.

Atomic Kube runs and delivers.

Binding:

- Atomic Agent MAY run inside an Atomic Kube
- Atomic Kube MAY host one or more Atomic Agents
- A non-trivial agent system SHOULD compose many atomic agents over many atomic kubes
