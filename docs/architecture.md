# 3AI Defence Architecture

## Overview

3AI Defence is a distributed cyber-defence architecture composed of three
separate defensive roles:

```text
Akali
Integrity + Trusted Recovery

Caronte
Containment + Controlled Decoys

Outy
Analysis + Orchestration
```

The modules cooperate while maintaining distinct responsibilities.

---

# High-Level Architecture

```text
                     PROTECTED SYSTEMS
                            |
                            v
                    Defensive Signals
                            |
         +------------------+------------------+
         |                  |                  |
         v                  v                  v
       AKALI              CARONTE             OUTY
     Integrity          Containment          Analysis
      Recovery            Decoys          Orchestration
         |                  |                  |
         +------------------+------------------+
                            |
                            v
                    Coordinated Defence
                            |
             +--------------+--------------+
             |                             |
             v                             v
        Containment                    Recovery
             |                             |
             +--------------+--------------+
                            |
                            v
                     Trusted Operation
```

---

# Architectural Objectives

The architecture aims to provide:

- defensive responsibility separation
- local resilience
- trusted recovery
- incident containment
- reduced dependency on permanent Internet connectivity
- coordinated analysis
- auditability
- controlled defensive evolution

---

# Module Separation

The modules have intentionally different responsibilities.

## Akali

Primary concern:

```text
Can this state be trusted?
```

Akali focuses on integrity and recovery.

---

## Caronte

Primary concern:

```text
Can suspicious activity be contained away from protected assets?
```

Caronte focuses on isolation and controlled defensive environments.

---

## Outy

Primary concern:

```text
What is happening, and how should the defensive modules coordinate?
```

Outy focuses on analysis and orchestration.

---

# Cooperative Model

The modules are not intended to operate as unrelated defensive tools.

They form a cooperative system.

```text
Akali
  |
  +--> integrity signal --------+
                                |
                                v
                              Outy
                                |
                                v
                         Defensive Context
                                |
                                v
                             Caronte
                                |
                                +--> containment state
                                |
                                v
                              Outy
                                |
                                v
                        Recovery Decision
                                |
                                v
                              Akali
```

This diagram describes logical cooperation rather than a production protocol.

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
      `--> Caronte remains ready for containment
```

The precise implementation and observation mechanisms remain private.

---

# Anomaly Handling

At the public architectural level:

```text
Anomaly Signal
      |
      v
Correlation / Evaluation
      |
      v
Containment if Required
      |
      v
Trusted Recovery if Required
      |
      v
Healthy State
```

No public documentation should expose production thresholds, triggering rules or
response policies.

---

# Trusted Recovery

Recovery is based on returning affected components toward known-good state.

Conceptually:

```text
Compromised / Untrusted State
            |
            v
      Trusted Reference
            |
            v
     Selective Recovery
            |
            v
       Healthy State
```

The production storage, validation and restoration mechanisms remain private.

---

# Containment

Containment separates suspicious activity from protected assets.

```text
Suspicious Activity
        |
        v
Containment Boundary
        |
        +--> Protected Assets
        |
        `--> Controlled Defensive Environment
```

The public architecture does not expose operational network topology or
production containment rules.

---

# Controlled Decoy Environments

Caronte can participate in controlled defensive decoy environments.

Their role is defensive:

- divert suspicious activity away from real assets
- observe incident behavior in a controlled context
- provide additional defensive evidence

This repository does not document deployment recipes or offensive usage.

---

# Local Analysis

Outy can correlate defensive signals locally.

```text
Integrity Signals
        +
Containment Signals
        +
Local Telemetry
        |
        v
Outy
        |
        v
Defensive Context
```

Local analysis supports operation in environments where constant external
connectivity is undesirable or unavailable.

---

# Offline / Semi-Disconnected Operation

The architecture can operate in:

- offline environments
- closed local networks
- semi-disconnected networks
- controlled edge deployments

Conceptually:

```text
External Network
      |
      v
Controlled Boundary
      |
      v
Local Defensive Environment
      |
      +--> Akali
      +--> Caronte
      `--> Outy
```

External updates should cross explicitly controlled trust boundaries.

---

# Audit

Defensive activity should produce sufficient records for later review.

```text
Incident
   |
   v
Detection
   |
   v
Response
   |
   v
Recovery
   |
   v
Audit Record
```

Specific logging formats and retention policies remain implementation details.

---

# Resilience Model

The architecture is designed around the idea that defensive capability should
not disappear when one component becomes unavailable.

```text
Separate Roles
     +
Local Operation
     +
Trusted Recovery
     +
Controlled Containment
     =
Resilience
```

---

# Deployment Independence

3AI Defence is not architecturally limited to CashOut.

Potential protected environments may include:

```text
3AI Defence
     |
     +--> Territorial Platforms
     +--> Business Infrastructure
     +--> Local Networks
     +--> Application Servers
     +--> IoT Environments
     `--> Other Authorized Systems
```

The protected system remains separate from the defensive architecture.

---

# Public Architecture Boundary

This document intentionally describes:

- role separation
- high-level information flow
- containment concepts
- recovery concepts
- local analysis
- offline-first operation
- resilience

It intentionally excludes:

- production topology
- network addressing
- exact detection rules
- exact containment rules
- model configuration
- operational commands
- credentials
- production endpoints
- private security telemetry
- incident playbooks
- proprietary algorithms

---

# Architectural Principle

> **Detection, containment, analysis and recovery should cooperate without becoming a single point of defensive failure.**
