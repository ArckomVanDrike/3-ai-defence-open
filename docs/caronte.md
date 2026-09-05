# Caronte

## Containment and Controlled Decoy Environments

Caronte is the containment module of 3AI Defence.

Its primary responsibility is to answer:

> **Can suspicious activity be separated from the real protected environment?**

Caronte focuses on containment, isolation and controlled defensive
environments.

---

# Role

Conceptually:

```text
Suspicious Activity
        |
        v
      Caronte
        |
    +---+---+
    |       |
    v       v
Isolate   Decoy
    |       |
    +---+---+
        |
        v
Protected Assets Remain Separated
```

---

# Core Responsibilities

At the architectural level, Caronte can participate in:

- containment of suspicious activity
- isolation of affected areas
- separation of real assets from incident activity
- controlled defensive decoy environments
- observation of behavior inside contained contexts
- providing defensive evidence to Outy

The public repository does not expose production containment procedures.

---

# Containment

Containment aims to limit the relationship between suspicious activity and real
assets.

```text
Incident
   |
   v
Containment Boundary
   |
   +--> Real Assets
   |
   `--> Controlled Environment
```

The objective is defensive separation.

---

# Isolation

Isolation can reduce the ability of an incident to affect additional parts of
the protected environment.

Conceptually:

```text
Affected Area
     |
     v
Isolation
     |
     +--> Unaffected Assets
     |
     `--> Controlled Incident Scope
```

The exact network mechanisms remain private.

---

# Controlled Decoy Environments

Caronte can deploy or coordinate controlled decoy environments.

Their defensive purpose is to:

- divert suspicious activity away from real assets
- maintain separation between real and simulated environments
- observe incident behavior
- improve defensive understanding

This repository intentionally avoids deployment recipes or offensive
instruction.

---

# Decoy Is Not Production

A fundamental architectural distinction is:

```text
REAL ENVIRONMENT
      !=
CONTROLLED DECOY
```

The decoy environment should not require access to protected production assets.

---

# Caronte and Outy

Caronte contributes defensive observations.

```text
Caronte
   |
   +--> Containment State
   +--> Defensive Observations
   |
   v
Outy
   |
   v
Correlated Defensive Context
```

Outy can use this context when coordinating the broader response.

---

# Caronte and Akali

Caronte and Akali solve different problems.

```text
Caronte
  |
  `--> Keep suspicious activity away from trusted assets


Akali
  |
  `--> Restore trusted state where required
```

Together:

```text
Contain
   |
   v
Recover
```

---

# Defensive Observation

Contained activity may produce useful defensive evidence.

Conceptually:

```text
Controlled Incident
       |
       v
Observation
       |
       v
Defensive Evidence
       |
       v
Outy
```

The production data collected, how it is stored and how it is analysed remain
private.

---

# Local Operation

Caronte is designed for local defensive operation.

```text
Protected Local Network
        |
        v
      Caronte
        |
        v
Containment Boundary
```

Its defensive function should not depend on permanent Internet access.

See [Offline Operation](offline-operation.md).

---

# Security Boundary

Caronte should preserve separation between:

```text
Protected Assets
      |
      X
      |
Controlled Decoy
```

A defensive environment that unintentionally exposes real production assets
would violate the intended architecture.

---

# Response Coordination

Caronte can respond to defensive context originating from more than one source.

Conceptually:

```text
Akali Signal ------+
                   |
                   v
                 Outy
                   |
                   v
            Defensive Decision
                   |
                   v
                Caronte
                   |
                   v
             Containment
```

The exact response policy remains private.

---

# Resilience

Containment contributes to resilience because an incident affecting one area
does not necessarily require full shutdown of the protected environment.

```text
Incident
   |
   v
Contain Scope
   |
   v
Preserve Unaffected Operation
```

Availability and safety requirements depend on deployment.

---

# Audit

Containment activity should support later defensive review.

```text
Incident
   |
   v
Containment
   |
   v
Observation
   |
   v
Audit
```

Production logging and retention remain implementation details.

---

# Authorized Defensive Use

Caronte is described only in the context of protecting systems for which the
operator has authorization.

This public repository does not provide authorization to:

- monitor third-party infrastructure
- interfere with external systems
- deploy deceptive environments against systems without permission
- capture unrelated third-party information
- perform offensive operations

---

# Public Boundary

This repository may document:

- containment principles
- isolation concepts
- controlled decoy architecture
- coordination with Akali and Outy
- local operation
- defensive observation
- resilience

It intentionally does not expose:

- production topology
- routing configuration
- firewall rules
- decoy deployment recipes
- operational commands
- detection thresholds
- real infrastructure identifiers
- private incident telemetry
- proprietary response logic
- credentials

---

# Design Principle

> **Contain suspicious activity without making the protected environment part of the experiment.**
