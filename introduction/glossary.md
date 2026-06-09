# Glossary

## World

A bounded operating environment where agents, humans, systems, data, policies, decisions, actions, and outcomes interact.

A world has state, identity, context, memory, tools, approvals, observations, and boundaries.

## Box

The smallest reusable capability boundary in a world.

A box contains schema, relations, events, policies, functions, APIs, UI contracts, tests, and observability rules.

## Buildpack

A BuildKit for agentic worlds.

A buildpack assembles boxes into runnable capabilities, applications, environments, or decision systems.

## Fabric

The operating layer that connects boxes, buildpacks, humans, agents, policies, decisions, actions, outcomes, and memory.

Fabric provides continuity, governance, observability, and execution flow.

## Agent

A worker operating inside a governed world.

An agent can reason, recommend, execute, observe, or learn, but it is not the world itself.

## Context

Structured state that gives meaning to signals, decisions, actions, and outcomes.

Context may include time, location, identity, ownership, permissions, history, relationships, and constraints.

## Policy

A rule that governs what can happen inside a world.

Policies may control access, approvals, tool use, data handling, execution, safety, and shutdown.

## Decision

A first-class world object connecting objective, context, evidence, alternatives, recommendation, approval, action, outcome, and learning.

## Action

A governed execution step caused by a decision, human request, system event, or agent recommendation.

## Outcome

The observed result of an action or decision.

Outcomes close the loop and create learning signals.

## Memory

Reusable knowledge derived from context, decisions, outcomes, traces, and human review.

Memory must be governed, scoped, auditable, and reversible where required.

## Signal

An observation entering the world from a system, human, event stream, document, API, or agent.

## Evidence

Information used to support, challenge, or explain a decision.

## Approval

A human or policy-mediated gate that authorizes a decision or action.

## Safety Conformance

The required verification that all Agent Safety Protocols are present, enabled, and enforceable before testing.

## Researcher-only Testing

A restricted testing mode available only to researchers who have implemented and acknowledged all required Agent Safety Protocols defined in this GitHub organization.
