# Akali

## Integrity and Trusted Recovery

Akali is the integrity and trusted-recovery module of 3AI Defence.

Its primary responsibility is to answer:

> **Can the protected system still be trusted?**

Akali focuses on the state of critical files, configurations and recovery
material rather than on external interaction.

---

# Role

Conceptually:

```text
Protected System
      |
      v
Integrity Observation
      |
      v
Akali
      |
      +--> Trusted State
      +--> Integrity Signals
      +--> Recovery Material
      `--> Restoration Capability
```

---

# Core Responsibilities

Akali is responsible at the architectural level for:

- monitoring critical integrity state
- identifying unexpected modification
- comparing current state with trusted reference state
- maintaining trusted recovery material
- supporting selective restoration
- participating in coordinated defensive response

The exact production implementation remains private.

---

# Trusted State

A central concept in Akali is the existence of a state considered known and
trusted.

```text
Current State
      |
      v
Compare
      |
      v
Trusted Reference
      |
      +--> Match
      |
      `--> Difference
```

A difference does not automatically mean compromise.

It creates an integrity signal that can participate in broader defensive
analysis.

---

# Integrity Signals

Akali may generate information indicating that important system state has
changed.

Conceptually:

```text
Observed Change
      |
      v
Integrity Evaluation
      |
      v
Integrity Signal
      |
      v
Outy
```

Outy may correlate that signal with other context before a broader defensive
response is selected.

---

# Trusted Recovery Material

Akali maintains or manages access to recovery material representing known-good
state.

At a public architectural level:

```text
Known-Good State
      |
      v
Trusted Recovery Material
      |
      v
Akali
      |
      v
Selective Recovery
```

The repository intentionally does not expose:

- storage layout
- backup locations
- retention policy
- signing material
- validation secrets
- restoration commands
- production recovery procedures

---

# Selective Recovery

Recovery does not necessarily require rebuilding an entire protected system.

Conceptually:

```text
Affected Component
       |
       v
Identify Trusted Reference
       |
       v
Restore Required State
       |
       v
Revalidate
       |
       v
Return to Trusted Operation
```

The exact recovery policy depends on the protected environment.

---

# Akali and Outy

Akali does not need to make every security decision alone.

```text
Akali
  |
  +--> Integrity Signal
  |
  v
Outy
  |
  v
Defensive Context
```

Outy can correlate integrity information with other defensive evidence.

This separation allows Akali to remain focused on trust and recovery.

---

# Akali and Caronte

Containment and recovery are distinct responsibilities.

```text
Caronte
Containment
    |
    v
Isolated Incident
    |
    v
Akali
Trusted Recovery
```

Caronte can help protect unaffected assets while Akali participates in
restoring compromised state.

---

# Integrity Before Recovery

A restoration process is only useful if the restored state can itself be
trusted.

Conceptually:

```text
Recovery Material
      |
      v
Validation
      |
      v
Trusted?
  +---+---+
  |       |
 Yes      No
  |       |
  v       v
Restore   Reject
```

This principle prevents recovery from becoming a simple copy operation.

---

# Internal Defensive Role

Akali is intended as an internal defensive component.

Its architectural function is integrity and resilience, not direct public
service exposure.

Conceptually:

```text
Internet
   |
   X
   |
Akali
   |
Protected Environment
```

Any production management or update path should cross explicit trust
boundaries.

---

# Updates

Trusted references, detection information or supporting material may evolve.

At the public architectural level:

```text
Approved Update Source
        |
        v
Controlled Verification
        |
        v
Akali Update
```

The exact update mechanism remains private.

---

# Offline Operation

Akali is compatible with the offline-first philosophy of 3AI Defence.

```text
Local Protected Environment
          |
          v
        Akali
          |
          v
Integrity + Recovery
```

Continuous Internet access is not an architectural requirement.

See [Offline Operation](offline-operation.md).

---

# Failure Isolation

Akali represents a distinct defensive responsibility.

If another defensive module is unavailable, Akali can still preserve its role
as an integrity and recovery component, subject to deployment design.

This reduces dependence on a single monolithic defence mechanism.

---

# Protected Assets

Depending on deployment, Akali may conceptually protect:

- critical application state
- configuration
- trusted system components
- selected service state
- local infrastructure
- recovery references

The public repository does not identify real production assets.

---

# Audit

Integrity and recovery events should support later review.

Conceptually:

```text
Integrity Change
      |
      v
Evaluation
      |
      v
Response / Recovery
      |
      v
Audit Record
```

Exact audit formats and retention remain private.

---

# Public Boundary

This repository may document:

- integrity principles
- trusted-state concepts
- recovery architecture
- cooperation with Outy
- cooperation with Caronte
- offline-first design
- audit principles

It intentionally does not expose:

- monitored production paths
- production hashes
- signing keys
- backup locations
- recovery images
- restore commands
- thresholds
- production configuration
- real infrastructure details
- credentials

---

# Design Principle

> **Recovery is only useful when the state being restored is itself trusted.**
