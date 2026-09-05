# Protected Environments

## Overview

3AI Defence is designed as a reusable defensive architecture rather than as a
security layer tied to one application.

The same architectural principles can be adapted to different authorized
digital environments.

---

# Environment Categories

Potential protected environments may include:

- application servers
- local business infrastructure
- smart homes
- offices
- IoT environments
- local edge systems
- territorial platforms
- semi-disconnected networks
- other authorized digital infrastructure

The exact deployment model depends on the environment being protected.

---

# Architectural Independence

3AI Defence should remain distinct from the protected system.

```text
Protected Environment
        |
        v
Defensive Boundary
        |
        v
3AI Defence
        |
        +--> Akali
        +--> Caronte
        `--> Outy
```

The protected platform is the subject of defense, not the identity of the
defensive architecture.

---

# Application Servers

An application environment may expose:

- services
- application state
- configuration
- local data
- dependencies
- operational telemetry

3AI Defence can conceptually provide:

```text
Application Environment
        |
        +--> Integrity Context --> Akali
        +--> Containment Context --> Caronte
        `--> Defensive Context --> Outy
```

The public repository does not document real production integration points.

---

# Business Infrastructure

Local business infrastructure may include:

- operational applications
- local networks
- terminals
- business services
- connected devices
- internal systems

The architectural objective is resilience without requiring every business
system to become directly exposed to the defensive modules.

---

# Smart Environments

A smart environment may combine:

- automation
- sensors
- networked devices
- local services
- edge processing

Conceptually:

```text
Smart Environment
       |
       v
Local Defensive Layer
       |
       +--> Integrity
       +--> Containment
       `--> Analysis
```

The exact device integration remains deployment-specific.

---

# IoT Environments

IoT environments can be highly heterogeneous.

A defensive architecture should therefore avoid assuming one universal device
model.

Potential concerns include:

- device integrity
- local communication
- service availability
- anomalous behavior
- containment boundaries
- recovery capability

3AI Defence describes the roles, not a universal IoT control protocol.

---

# Edge Infrastructure

3AI Defence is compatible with environments where defensive capability needs
to remain close to the protected system.

```text
Protected Edge System
        |
        v
Local Defensive Nodes
        |
        v
Local Analysis + Recovery
```

This is especially relevant where continuous cloud dependence is undesirable.

---

# Offline / Closed Environments

Some protected environments may operate:

- fully offline
- inside closed networks
- with intermittent connectivity
- through controlled synchronization windows

See [Offline Operation](offline-operation.md).

---

# Territorial Platforms

A territorial platform can combine:

- public services
- user-facing applications
- local data
- geospatial systems
- community activity
- business integrations
- AI systems

CashOut is one current example of this type of protected environment.

See [CashOut Integration](cashout-integration.md).

---

# Protection Boundaries

A protected environment should define clear boundaries between:

```text
Public / External Surface
        |
        v
Application Boundary
        |
        v
Protected Internal Systems
        |
        v
3AI Defence Context
```

The exact placement of each module depends on risk and deployment design.

---

# Role Adaptation

The defensive responsibilities remain conceptually stable even when deployment
changes.

```text
Akali
  `--> Integrity / Recovery


Caronte
  `--> Containment


Outy
  `--> Analysis / Orchestration
```

What changes is the protected context.

---

# Authorization

3AI Defence is intended only for environments where the operator has explicit
authorization to deploy defensive monitoring and response capabilities.

The architecture does not authorize interaction with third-party systems
without permission.

---

# Data Minimization

A deployment should avoid collecting unrelated information simply because it is
available.

Conceptually:

```text
Available Data
      |
      v
Required Defensive Context
      |
      v
3AI Defence
```

This is particularly important in environments containing user or business
data.

---

# Deployment-Specific Risk

Different environments have different risk profiles.

Examples:

- home environment
- SME
- local server
- IoT environment
- territorial platform
- critical local service

No single defensive policy is assumed to fit all deployments.

---

# Failure Modes

A protected environment may encounter:

- loss of connectivity
- service failure
- compromised state
- partial hardware failure
- unavailable module
- inconsistent telemetry

The defensive architecture should degrade safely where possible.

---

# Public Boundary

This repository may document:

- protected-environment categories
- role relationships
- deployment independence
- authorization principles
- data minimization
- local resilience

It intentionally does not expose:

- real infrastructure topology
- production network maps
- actual asset inventories
- real endpoints
- credentials
- internal service names
- deployment-specific security rules
- customer environments

---

# Design Principle

> **3AI Defence protects an environment without becoming inseparable from that environment.**
