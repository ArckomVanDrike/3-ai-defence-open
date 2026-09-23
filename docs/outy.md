# Outy

## Analysis and Orchestration

Outy is the analytical and orchestration module of 3AI Defence.

Its primary responsibility is to answer:

> **What is happening, how confident are we, and how should the defensive modules coordinate?**

Outy operates as the analytical bridge between integrity, containment and
recovery.

---

# Role

Conceptually:

```text
Akali Signals -------+
                     |
                     v
                    Outy
                     |
                     +--> Analysis
                     +--> Correlation
                     +--> Defensive Context
                     `--> Coordination
                     |
                     v
Caronte Signals -----+
```

---

# Core Responsibilities

At the architectural level, Outy can:

- analyse security telemetry
- correlate signals from Akali and Caronte
- evaluate overall defensive context
- detect patterns and anomalies
- support defensive decisions
- coordinate responses between modules
- reconstruct incident timelines from trusted evidence
- distinguish observed facts from hypotheses
- support operator queries about what happened and why
- use local AI where appropriate
- contribute to learning from previous incidents

Production models and decision logic remain private.

---

# Correlation

A single signal may be ambiguous.

Outy can combine multiple observations.

```text
Integrity Signal
      +
Containment Observation
      +
Local Telemetry
      |
      v
Correlation
      |
      v
Defensive Context
```

Correlation is distinct from blindly treating every signal as an incident.

---

# Incident Reconstruction

Outy can correlate evidence preserved by Akali, observations from Caronte and
other authorized defensive telemetry to reconstruct an incident timeline.

Conceptually:

```text
Akali Evidence -------+
                      |
Caronte Observations -+--> Outy --> Incident Timeline
                      |              |
Other Telemetry ------+              +--> Facts
                                     +--> Evidence
                                     `--> Hypotheses
```

The objective is not to force a single explanation.

Where evidence is incomplete, Outy should be able to express uncertainty and
identify what information is missing.

An operator-facing deployment may support questions such as:

```text
What happened before the service failed?
Why did this host restart?
Which events are confirmed facts?
Which conclusions are still hypotheses?
What evidence is missing?
```

The exact natural-language interface, models and reasoning mechanisms remain
private.

---

# Defensive Context

Outy can build a contextual view of system state.

Conceptually:

```text
Signals
   |
   v
Context
   |
   +--> Normal
   +--> Suspicious
   +--> Degraded
   `--> Incident
```

The exact classifications, confidence mechanisms and thresholds remain private.

---

# Local AI

A defining characteristic of the architecture is the use of AI locally where
appropriate.

```text
Local Telemetry
      |
      v
Local AI Analysis
      |
      v
Outy
      |
      v
Defensive Context
```

The objective is to reduce dependence on continuous remote AI services.

---

# Offline-First Analysis

Outy is designed to operate in offline, closed or semi-disconnected
environments.

```text
Local Network
    |
    v
Telemetry
    |
    v
Outy
    |
    v
Local Defensive Decision Support
```

External model or rule updates should cross controlled boundaries.

See [Offline Operation](offline-operation.md).

---

# Outy and Akali

Akali provides integrity-focused information.

```text
Akali
  |
  +--> Integrity State
  +--> Recovery State
  |
  v
Outy
```

Outy can correlate that information with broader security context.

---

# Outy and Caronte

Caronte provides containment-focused information.

```text
Caronte
  |
  +--> Isolation State
  +--> Defensive Observations
  |
  v
Outy
```

Outy can use this context to understand whether containment should continue,
change or participate in recovery coordination.

---

# Orchestration

Outy coordinates defensive responsibilities without collapsing them into one
module.

```text
                 Outy
                  |
        +---------+---------+
        |                   |
        v                   v
      Akali              Caronte
Integrity / Recovery   Containment
```

The coordination layer remains logically distinct from the functions it
coordinates.

---

# Recommendation vs Execution

Depending on deployment, Outy may support different levels of automation.

Conceptually:

```text
Defensive Context
       |
       v
Recommendation
       |
       +--> Human / Policy Approval
       |
       `--> Authorized Automation
```

The public architecture does not assume that every response is fully automatic.

---

# Human Control

For high-impact actions, deployments may require human or policy-based
authorization.

```text
Outy Analysis
      |
      v
Proposed Response
      |
      v
Authorization Boundary
      |
      v
Execution
```

The exact approval model depends on the protected environment.

---

# Learning from Incidents

Past incidents can improve future defensive understanding.

Conceptually:

```text
Incident
   |
   v
Recorded Evidence
   |
   v
Analysis
   |
   v
Defensive Improvement
```

This public description does not expose training data, model pipelines or
production learning systems.

---

# Model Updates

Local AI systems may require updates.

At an architectural level:

```text
Verified Model / Rule Source
          |
          v
Controlled Update Boundary
          |
          v
Outy
```

Production verification mechanisms remain private.

---

# Data Minimization

Outy should consume only the information required for defensive analysis.

```text
Available Telemetry
       |
       v
Relevant Security Context
       |
       v
Outy
```

The goal is not unrestricted collection.

---

# Protected Environment Integration

Outy can conceptually interact with local defensive infrastructure such as:

- application systems
- local network sensors
- IoT environments
- local storage
- protected platform telemetry

Exact production integrations remain private.

---

# CashOut

CashOut is currently one real protected environment in which the 3AI Defence
architecture participates.

Conceptually:

```text
CashOut
   |
   v
Defensive Telemetry
   |
   v
Outy
   |
   v
3AI Defence Coordination
```

CashOut does not define Outy's complete purpose.

See [CashOut Integration](cashout-integration.md).

---

# Outy in 3AI Defence vs Outy in the Broader Ecosystem

Outy is also a broader territorial AI technology.

Within 3AI Defence, Outy's role is specifically defensive:

```text
Outy
 |
 +--> Territorial / General AI Context
 |
 `--> 3AI Defence Role
       Analysis + Security Orchestration
```

The defensive role should not be confused with every capability of the broader
Outy ecosystem.

---

# Resilience

Local analysis contributes to resilience by allowing defensive context to
remain available when external services are unavailable.

```text
External Connectivity Lost
          |
          v
Local Defensive Environment
          |
          v
Outy
          |
          v
Continued Analysis
```

See [Resilience](resilience.md).

---

# Audit

Outy can participate in creating a coherent record of defensive decisions.

Conceptually:

```text
Signals
   |
   v
Analysis
   |
   v
Decision
   |
   v
Response
   |
   v
Audit Context
```

Exact records and retention remain private.

---

# Public Boundary

This repository may document:

- analytical role
- correlation concepts
- orchestration
- local AI
- offline operation
- cooperation with Akali
- cooperation with Caronte
- audit principles
- incident reconstruction concepts
- uncertainty and evidence provenance
- human-control concepts

It intentionally does not expose:

- production models
- model weights
- internal prompts
- detection thresholds
- proprietary classifiers
- private telemetry
- production orchestration rules
- response playbooks
- credentials
- real infrastructure
- private training data
- security-sensitive model configuration

---

# Design Principle

> **Outy does not replace Akali or Caronte. It gives their separate defensive signals a shared context.**

For incident reconstruction:

> **Akali preserves what happened. Outy explains what it means.**
