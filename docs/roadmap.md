# 3AI Defence Public Roadmap

## Overview

3AI Defence is an evolving distributed cyber-defence architecture.

This roadmap describes architectural direction rather than a release calendar.

It does not imply that every capability is currently active in every
deployment.

---

# Current Foundation

The current architectural foundation includes:

- Akali
- Caronte
- Outy
- separation of defensive responsibilities
- local analysis
- containment concepts
- trusted recovery concepts
- offline / semi-disconnected operation
- integration with the broader CashOut environment

---

# Phase 1 — Public Architecture Surface

Establish a clear public technical description of:

- architecture
- module roles
- coordination
- resilience
- offline operation
- protected-environment model
- CashOut relationship
- security boundaries
- intellectual-property boundaries

Objective:

> Make the architecture understandable without exposing operational defensive
> implementation.

---

# Phase 2 — Dedicated Project Separation

3AI Defence currently participates inside the broader CashOut technical
environment.

A future milestone is dedicated separation.

Potential direction:

```text
Current
  |
  v
Integrated CashOut Environment
  |
  v
Dedicated 3AI Defence Environment
```

This may include:

- dedicated repository
- dedicated runtime
- dedicated development lifecycle
- independent testing
- independent release management

---

# Phase 3 — Akali Evolution

Potential architectural priorities include:

- stronger trusted-state management
- recovery validation
- selective restoration
- integrity evidence
- resilience under partial failure
- safer update boundaries

Implementation details remain private.

---

# Phase 4 — Caronte Evolution

Potential priorities include:

- clearer containment boundaries
- controlled decoy lifecycle
- safer separation from protected systems
- observation quality
- degraded-mode containment
- environment-independent deployment patterns

No offensive capability is implied.

---

# Phase 5 — Outy Defensive Evolution

Potential directions include:

- local defensive reasoning
- better signal correlation
- confidence-aware context
- explainable defensive recommendations
- controlled orchestration
- improved offline analysis
- human authorization boundaries

Private models and orchestration remain protected.

---

# Phase 6 — Coordination

Continue strengthening cooperation between modules.

```text
Akali
   \
    \
     Outy
    /
   /
Caronte
```

Potential focus:

- clearer signal contracts
- degraded coordination
- safe state transitions
- recovery coordination
- containment coordination
- audit consistency

---

# Phase 7 — Detection to Recovery Lifecycle

Expand the complete defensive lifecycle.

```text
Observe
   |
Detect
   |
Correlate
   |
Contain
   |
Recover
   |
Revalidate
   |
Audit
```

The objective is resilience rather than detection alone.

---

# Phase 8 — Offline-First Maturity

Continue reducing unnecessary external dependency.

Potential priorities include:

- local operation
- controlled synchronization
- verified update channels
- local audit continuity
- safe reconnection
- dependency failure handling

---

# Phase 9 — Protected Environment Profiles

Develop implementation-neutral deployment profiles for authorized environments
such as:

- business infrastructure
- local servers
- smart environments
- IoT
- edge systems
- territorial platforms

Profiles should document architecture without exposing real customer or
production infrastructure.

---

# Phase 10 — CashOut Maturity

Continue exercising the architecture in the CashOut context.

Potential goals include:

- clearer defensive boundaries
- stronger resilience testing
- separation from application logic
- improved auditability
- independent failure handling

CashOut remains a protected environment, not the identity of 3AI Defence.

---

# Phase 11 — Dedicated Hardware Architecture

The original 3AI Defence concept is built around physically separated defensive
roles.

Future dedicated deployments may strengthen that separation through independent
nodes.

Public documentation may describe roles and boundaries.

Private implementation will retain:

- real hardware topology
- production networking
- management paths
- credentials
- operational configuration

---

# Phase 12 — Resilience Testing

Potential future work includes testing:

- module unavailability
- connectivity loss
- partial telemetry
- recovery validation
- containment continuity
- degraded mode
- restart / recovery behavior

The objective is to understand system behavior under failure.

---

# Phase 13 — Audit and Explainability

A defensive system should be reviewable.

Potential priorities include:

- module-level event context
- decision provenance
- response timeline
- recovery timeline
- operator-readable summaries

Private telemetry and incident data remain private.

---

# Phase 14 — Human Control

Continue defining which actions may be:

- informational
- recommended
- policy-controlled
- human-approved
- automated

High-impact operations should preserve explicit authorization boundaries.

---

# Phase 15 — Security Intelligence Updates

Potential direction includes controlled use of:

- trusted public defensive information
- verified indicators
- validated model updates
- approved rule updates

External data should cross controlled trust boundaries.

---

# Phase 16 — Independent Research Surface

As the project becomes more independent, the public repository may include:

- architecture experiments
- resilience evaluations
- implementation-neutral simulations
- benchmark concepts
- public defensive test methodology

without publishing operational attack or defense bypass procedures.

---

# Cross-Cutting Priorities

## Separation

Maintain distinct defensive responsibilities.

## Resilience

Preserve capability under failure.

## Locality

Prefer local defensive operation where appropriate.

## Trust

Do not restore or update from unverified state.

## Human Control

Preserve authorization for high-impact actions.

## Auditability

Make defensive reasoning reviewable.

## Privacy

Use only necessary defensive context.

## Defensive Scope

Keep the project focused on authorized defense.

---

# What This Roadmap Does Not Mean

This roadmap does not mean:

- every capability is currently implemented
- all decisions are autonomous
- all deployments use the same hardware
- every protected environment uses the same policy
- operational security details will become public
- the project provides offensive security tooling

---

# Public vs Private Evolution

Public work may include:

- architectural documentation
- conceptual diagrams
- public interfaces
- resilience principles
- safe examples
- selected non-sensitive tests

Private work may include:

- production source code
- real detection logic
- model configuration
- operational security
- incident playbooks
- private telemetry
- response automation
- infrastructure topology
- recovery infrastructure
- confidential integrations

---

# Long-Term Direction

The long-term architecture can be summarized as:

```text
Separated Defensive Roles
          +
Local Intelligence
          +
Controlled Containment
          +
Trusted Recovery
          +
Independent Operation
          |
          v
Distributed Cyber Resilience
```

---

# Roadmap Principle

> **Evolve from an integrated defensive architecture into an independent, testable and resilient defensive system without sacrificing separation or trust boundaries.**
