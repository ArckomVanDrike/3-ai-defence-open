# 3AI Defence + CashOut Integration

## Overview

CashOut is currently one real protected environment in which the 3AI Defence
architecture participates.

This relationship demonstrates the architecture in an active platform context,
while keeping 3AI Defence conceptually independent.

---

# Separation of Identity

CashOut and 3AI Defence have different responsibilities.

```text
CashOut
Territorial Digital Ecosystem
        |
        v
Protected Platform Context
        |
        v
3AI Defence
Distributed Cyber Defence
```

CashOut is not 3AI Defence.

3AI Defence is not limited to CashOut.

---

# Current Relationship

At a high level:

```text
CashOut Environment
       |
       v
Defensive Context
       |
  +----+----+
  |    |    |
  v    v    v
Akali Caronte Outy
```

The exact production integration remains private.

---

# Akali in the CashOut Context

Akali can participate in protecting trusted application state.

Conceptually:

```text
CashOut State
     |
     v
Integrity Observation
     |
     v
Akali
```

Public documentation does not identify production paths, recovery material or
protected internal assets.

---

# Caronte in the CashOut Context

Caronte can participate in containment when suspicious activity affects the
protected environment.

```text
Suspicious Activity
        |
        v
Containment Boundary
        |
        v
Caronte
```

The real network and isolation implementation are private.

---

# Outy in the CashOut Context

Outy can analyse authorized defensive telemetry and coordinate the defensive
roles.

```text
CashOut Defensive Context
          |
          v
         Outy
          |
   +------+------+
   |             |
   v             v
 Akali        Caronte
```

This role is separate from Outy's broader territorial-AI capabilities.

---

# Outy Role Separation

Outy exists in more than one architectural context.

```text
Outy
 |
 +--> CashOut Territorial AI
 |
 `--> 3AI Defence
       Security Analysis + Orchestration
```

The two contexts should not be treated as identical merely because they share
the Outy technology family.

---

# Protected Platform Boundary

3AI Defence should only receive defensive context required for its role.

```text
CashOut
   |
   v
Required Defensive Context
   |
   v
3AI Defence
```

It should not imply unrestricted access to:

- user information
- business data
- private conversations
- unrelated application content
- transaction information

unless explicitly required and authorized by the defensive design.

---

# Local Defensive Operation

CashOut can benefit from a defensive architecture that does not require
continuous dependence on external services.

```text
CashOut
   |
   v
Local Defensive Layer
   |
   +--> Akali
   +--> Caronte
   `--> Outy
```

This aligns with 3AI Defence's offline / semi-disconnected architectural
principles.

---

# Resilience

The integration aims to preserve:

- integrity awareness
- containment capability
- trusted recovery
- defensive context
- local operation
- auditability

See [Resilience](resilience.md).

---

# CashOut as a Real Deployment Context

CashOut provides a concrete environment in which the architectural principles
can be exercised.

This does not mean every capability documented in the public 3AI Defence
architecture is universally active or configured identically in the current
CashOut deployment.

The public repository distinguishes:

```text
Architectural Capability
        !=
Universal Production Configuration
```

---

# Private Implementation

The following remain private:

- real CashOut defensive telemetry
- production security configuration
- protected asset inventory
- real integration endpoints
- recovery material
- containment topology
- model configuration
- response policies
- incident records
- credentials

---

# Future Separation

3AI Defence currently participates within the broader CashOut technical
environment.

A future dedicated environment may separate:

```text
3AI Defence
   |
   +--> Dedicated Repository
   +--> Dedicated Runtime
   +--> Dedicated Hardware / Nodes
   `--> Independent Release Lifecycle
```

The public repository already documents the architecture independently in
preparation for that evolution.

---

# Interoperability Principle

A protected platform should be able to integrate with the defensive
architecture through explicit boundaries.

```text
Protected Platform
      |
      v
Documented Defensive Boundary
      |
      v
3AI Defence
```

This reduces unnecessary coupling.

---

# Public Boundary

This repository may document:

- the existence of the CashOut relationship
- high-level role separation
- integration boundaries
- local defensive principles
- independence of 3AI Defence

It intentionally does not expose:

- CashOut production security design
- real monitoring configuration
- private telemetry
- private application internals
- production incident data
- infrastructure topology
- credentials
- confidential business logic

---

# Design Principle

> **CashOut is a real protected environment for 3AI Defence, not the boundary of what 3AI Defence can become.**
