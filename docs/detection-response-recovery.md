# Detection, Response and Recovery

## Overview

3AI Defence follows a defensive lifecycle built around:

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

The exact implementation varies by deployment.

---

# Normal Operation

During normal operation:

```text
Protected Systems
      |
      +--> Akali observes integrity
      |
      +--> Outy analyses defensive context
      |
      `--> Caronte remains prepared for containment
```

Normal operation should not require constant incident activity.

---

# Observation

Observation may originate from:

- integrity state
- local telemetry
- containment context
- protected-system state
- other authorized defensive sources

Conceptually:

```text
Protected Environment
        |
        v
Defensive Observation
```

---

# Detection

Detection identifies something that deserves evaluation.

```text
Observation
    |
    v
Potential Anomaly
    |
    v
Defensive Signal
```

A defensive signal is not automatically proof of compromise.

---

# Correlation

Outy can combine multiple signals.

```text
Akali Signal
     +
Caronte Context
     +
Local Telemetry
     |
     v
Outy
     |
     v
Correlated Context
```

This reduces dependence on isolated observations.

---

# Incident Evaluation

Conceptually:

```text
Correlated Context
        |
        v
Evaluate
  +-----+-----+
  |           |
  v           v
Normal     Suspicious
              |
              v
          Incident?
```

Production criteria remain private.

---

# Containment

When required, Caronte can participate in limiting incident scope.

```text
Incident
   |
   v
Caronte
   |
   v
Containment
   |
   +--> Protect Unaffected Assets
   `--> Isolate Affected Scope
```

---

# Controlled Defensive Environment

Where appropriate, suspicious activity may be redirected toward a controlled
defensive environment.

```text
Suspicious Activity
        |
        v
Controlled Boundary
        |
        v
Defensive Decoy
```

The objective is defensive isolation and observation.

No deployment instructions are provided in this public repository.

---

# Recovery

Akali can participate in restoring affected components from trusted state.

```text
Affected State
      |
      v
Trusted Reference
      |
      v
Recovery
      |
      v
Revalidation
```

---

# Known-Good State

Recovery depends on trustworthy recovery material.

```text
Recovery Source
      |
      v
Validate
      |
      v
Known Good?
  +---+---+
  |       |
 Yes      No
  |       |
  v       v
Use      Reject
```

---

# Revalidation

A recovered component should not automatically be assumed healthy.

```text
Recovered Component
        |
        v
Integrity Revalidation
        |
        v
Trusted State
```

If trust cannot be re-established, the defensive cycle continues.

---

# Return to Operation

Conceptually:

```text
Contained
   +
Recovered
   +
Revalidated
   |
   v
Healthy Operation
```

Return-to-service policy depends on deployment.

---

# Post-Incident Analysis

After an incident:

```text
Incident Evidence
      |
      v
Outy Analysis
      |
      v
Defensive Improvement
```

Lessons may improve:

- detection context
- operational understanding
- trusted-state management
- response policy

Private learning pipelines remain outside the public repository.

---

# Audit Trail

The lifecycle should support later review.

```text
Observation
   |
Detection
   |
Decision
   |
Containment
   |
Recovery
   |
Revalidation
   |
   v
Audit
```

---

# Minimal Disruption

The architecture aims to isolate affected scope where possible rather than
assuming complete system shutdown is always required.

Conceptually:

```text
Incident
   |
   v
Identify Scope
   |
   v
Contain Affected Area
   |
   v
Preserve Safe Operation Where Possible
```

---

# Failure Handling

The lifecycle should account for imperfect conditions.

Examples may include:

- incomplete telemetry
- unavailable module
- uncertain state
- partial connectivity
- delayed update material

In uncertain conditions, a deployment may prefer conservative defensive
behavior.

---

# Offline Recovery

Detection and recovery should remain possible without permanent external
connectivity.

```text
Local Defensive Environment
          |
          v
Detect
          |
          v
Contain
          |
          v
Recover
```

See [Offline Operation](offline-operation.md).

---

# Human Authorization

Certain actions may require human approval.

Conceptually:

```text
Detected Incident
       |
       v
Proposed Response
       |
       v
Authorization
       |
       v
Execute
```

Automation level is deployment-specific.

---

# Public Boundary

This repository may document:

- lifecycle stages
- role relationships
- containment concepts
- trusted recovery
- revalidation
- audit principles
- human-control boundaries

It intentionally does not expose:

- production incident thresholds
- detection signatures
- private telemetry
- real response playbooks
- production commands
- exact recovery procedures
- real network controls
- internal model configuration

---

# Lifecycle Principle

> **Do not stop at detection. A defensive system should be able to contain what it cannot trust and recover what it can verify.**
