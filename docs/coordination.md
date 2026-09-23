# 3AI Defence Coordination

## Overview

3AI Defence is not simply a collection of three defensive modules.

Its defining characteristic is coordinated operation between:

- Akali
- Caronte
- Outy

while preserving separation of responsibilities.

Conceptually:

```text
                    3AI DEFENCE
                         |
          +--------------+--------------+
          |              |              |
          v              v              v
        AKALI          CARONTE         OUTY
      Integrity      Containment      Analysis
       Recovery        Decoys      Orchestration
          |              |              |
          +--------------+--------------+
                         |
                         v
               Coordinated Defence
```

---

# Separation Before Coordination

Coordination does not mean collapsing every defensive function into one node.

The architecture intentionally keeps distinct concerns.

```text
Akali
  |
  `--> Is the system state trustworthy?


Caronte
  |
  `--> Can suspicious activity be isolated?


Outy
  |
  `--> What does the combined evidence mean?
```

---

# Signal Flow

At a public architectural level:

```text
Protected Environment
        |
        v
Defensive Signals
        |
   +----+----+
   |         |
   v         v
 Akali    Caronte
   |         |
   +----+----+
        |
        v
       Outy
        |
        v
Correlated Defensive Context
        |
        v
Coordinated Response
```

This describes logical flow rather than production protocol.

---

# Akali to Outy

Akali can provide information such as:

- integrity state
- integrity anomalies
- recovery readiness
- trusted-state validation context

Conceptually:

```text
Akali
  |
  +--> Integrity Signal
  +--> Trusted-State Context
  `--> Recovery Context
           |
           v
          Outy
```

Outy can combine these observations with other defensive evidence.

---

# Caronte to Outy

Caronte can provide information such as:

- containment state
- isolation state
- controlled-environment observations
- incident context

Conceptually:

```text
Caronte
   |
   +--> Containment State
   +--> Defensive Observation
   `--> Incident Context
            |
            v
           Outy
```

---

# Outy to Akali

Outy can coordinate with Akali when trusted recovery may be required.

```text
Correlated Incident Context
          |
          v
         Outy
          |
          v
Recovery Coordination
          |
          v
         Akali
```

The exact decision rules remain private.

---

# Outy to Caronte

Outy can coordinate with Caronte when containment may be required.

```text
Correlated Incident Context
          |
          v
         Outy
          |
          v
Containment Coordination
          |
          v
        Caronte
```

---

# Evidence-to-Reconstruction Flow

A coordinated incident investigation can include an explicit reconstruction
stage before containment or recovery decisions.

```text
Observe
   |
   v
Preserve Evidence
   |
   v
Build Timeline
   |
   v
Correlate
   |
   v
Separate Facts / Evidence / Hypotheses
   |
   v
Explain Defensive Context
```

Akali contributes trusted evidence and event context.

Caronte contributes observations from containment and controlled environments.

Outy correlates the available evidence, reconstructs the incident context and
communicates uncertainty where the evidence is incomplete.

This is an architectural description, not a public incident-response playbook.

---

# Coordination Loop

A simplified defensive loop:

```text
Observe
   |
   v
Detect
   |
   v
Preserve / Reconstruct
   |
   v
Correlate
   |
   v
Contain
   |
   v
Recover
   |
   v
Revalidate
   |
   v
Audit
```

Not every incident requires every stage.

---

# Conditional Response

A defensive signal should not automatically trigger the most disruptive action.

Conceptually:

```text
Signal
  |
  v
Evaluate
  |
  +--> Benign
  |
  +--> Suspicious
  |
  `--> Incident
```

The classification logic remains private.

---

# Human and Policy Boundaries

Coordination may involve:

- automatic low-risk defensive actions
- policy-controlled actions
- human authorization
- mixed workflows

Conceptually:

```text
Defensive Context
       |
       v
Proposed Action
       |
       v
Authorization Boundary
       |
       v
Execution
```

The deployment determines which actions require additional approval.

---

# Recovery Coordination

Containment and recovery should cooperate.

```text
Incident
   |
   v
Containment
   |
   v
Affected Scope Identified
   |
   v
Trusted Recovery
   |
   v
Revalidation
```

Recovery should not proceed from untrusted material.

---

# Revalidation

After recovery, defensive state should be reconsidered.

```text
Recovered State
      |
      v
Integrity Check
      |
      v
Trusted?
  +---+---+
  |       |
 Yes      No
  |       |
  v       v
Resume   Continue Response
```

---

# Audit Coordination

The combined defensive sequence should be reviewable.

```text
Detection
   |
Containment
   |
Recovery
   |
Decision Context
   |
   v
Audit
```

This enables later analysis without exposing private operational details.

---

# Degraded Coordination

The architecture should account for partial module availability.

Conceptually:

```text
All Modules Available
        |
        v
Full Coordination
```

and:

```text
One Module Degraded
        |
        v
Remaining Defensive Functions
        |
        v
Reduced / Safe Operation
```

Exact failover behavior depends on deployment.

---

# No Single Defensive Authority

3AI Defence avoids assuming that one signal alone always determines final state.

```text
One Signal
   |
   v
Context
   |
   v
Correlated Decision
```

This helps separate observation from response.

---

# Offline Coordination

Coordination is designed to remain possible within a local or closed
environment.

```text
Akali -----+
           |
Caronte ---+--> Local Coordination --> Outy
           |
Local Data-+
```

See [Offline Operation](offline-operation.md).

---

# Public Boundary

This repository may document:

- module relationships
- logical signal flow
- defensive stages
- human-control concepts
- revalidation
- audit principles
- incident reconstruction
- evidence provenance
- uncertainty-aware explanation

It intentionally does not expose:

- production messaging protocols
- internal event schemas
- exact trigger rules
- confidence thresholds
- production automation policies
- incident playbooks
- real infrastructure topology
- credentials
- private telemetry

---

# Design Principle

> **Coordination should improve defensive context without removing the separation that makes the architecture resilient.**
