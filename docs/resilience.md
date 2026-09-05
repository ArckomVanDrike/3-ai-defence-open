# 3AI Defence Resilience

## Overview

Resilience is a primary architectural objective of 3AI Defence.

The system is designed around:

- separation
- containment
- trusted recovery
- local analysis
- reduced external dependency
- revalidation
- auditability

---

# Resilience Is More Than Detection

A system that can detect an incident but cannot continue or recover is only
partially resilient.

3AI Defence considers:

```text
Detect
   +
Contain
   +
Recover
   +
Revalidate
   =
Operational Resilience
```

---

# Separation of Responsibilities

The three-module architecture reduces functional concentration.

```text
Akali
Integrity / Recovery

Caronte
Containment

Outy
Analysis / Orchestration
```

A single module does not intentionally own every defensive function.

---

# Avoiding a Monolithic Defensive Dependency

Conceptually:

```text
Monolithic Defence
       |
       v
One Failure
       |
       v
Broad Defensive Loss
```

3AI Defence instead aims for:

```text
Separated Roles
      |
      v
Partial Failure
      |
      v
Remaining Defensive Capability
```

Actual degraded behavior depends on deployment.

---

# Trusted Recovery

Resilience requires a path back to trusted operation.

```text
Compromise
   |
   v
Contain
   |
   v
Trusted Recovery
   |
   v
Revalidate
   |
   v
Resume
```

---

# Containment as Resilience

Containment can preserve unaffected areas.

```text
Incident
   |
   v
Limit Scope
   |
   v
Protect Remaining Assets
```

This can reduce the blast radius of an incident.

---

# Local Analysis

Local analysis helps resilience when external services become unavailable.

```text
External Service Lost
        |
        v
Local Outy Analysis
        |
        v
Continued Defensive Context
```

---

# Offline Capability

Offline-first operation contributes directly to resilience.

```text
Internet Available
      |
      v
Defence Works


Internet Unavailable
      |
      v
Defence Still Operates Locally
```

See [Offline Operation](offline-operation.md).

---

# Known-Good State

Resilience depends on the ability to distinguish healthy from untrusted state.

```text
Current State
      |
      v
Compare with Trusted State
      |
      v
Decision
```

Without a trustworthy reference, recovery becomes less reliable.

---

# Revalidation

Recovery is not the end of the cycle.

```text
Recovered
   |
   v
Revalidate
   |
   v
Trusted
```

Only then should normal operation be resumed according to policy.

---

# Degraded Modes

A resilient architecture should consider partial capability.

Conceptually:

```text
Full Capability
      |
      v
Module / Dependency Failure
      |
      v
Degraded Defensive Mode
```

Degraded mode may mean:

- reduced automation
- additional human review
- restricted operation
- isolated operation
- recovery-first behavior

Exact policies remain private.

---

# External Dependency Resilience

Potential external dependencies may include:

- Internet connectivity
- update sources
- external intelligence
- remote services
- remote AI

The architecture seeks to avoid requiring continuous availability of these
dependencies for core local defensive operation.

---

# Protected-Service Continuity

Where safe, containment may allow unaffected services to continue.

```text
Incident Scope
      |
      v
Contained
      |
      +--> Affected Area Restricted
      |
      `--> Safe Area Continues
```

Safety requirements remain deployment-specific.

---

# Recovery Material Resilience

Recovery capability itself must be protected.

Conceptually:

```text
Recovery Material
      |
      v
Protected + Verified
      |
      v
Usable During Incident
```

A recovery system that becomes compromised with the protected system provides
little value.

---

# Audit Resilience

Defensive events should remain reviewable.

```text
Incident
   |
Response
   |
Recovery
   |
   v
Durable Audit Context
```

Audit records can support:

- incident review
- defensive improvement
- operational accountability
- future analysis

---

# Learning

Resilience can improve over time.

```text
Incident
   |
   v
Evidence
   |
   v
Analysis
   |
   v
Improved Defensive Context
```

This does not imply unrestricted autonomous retraining.

---

# Human Resilience

Operators remain part of the system.

Clear module roles can help operators understand:

- what detected the issue
- what was isolated
- what was restored
- what remains uncertain

Human-readable defensive context is therefore part of operational resilience.

---

# CashOut Context

CashOut is currently one protected environment where the architecture can
participate.

3AI Defence should remain resilient as an independent architecture rather than
depending on CashOut-specific implementation.

See [CashOut Integration](cashout-integration.md).

---

# Public Boundary

This repository may document:

- resilience principles
- separation of roles
- recovery concepts
- degraded-mode concepts
- local operation
- auditability

It intentionally does not expose:

- production failover policy
- real recovery infrastructure
- private service dependencies
- production thresholds
- real topology
- internal incident policy
- private continuity plans

---

# Design Principle

> **Resilience means preserving the ability to understand, contain and recover even when part of the environment is already failing.**
