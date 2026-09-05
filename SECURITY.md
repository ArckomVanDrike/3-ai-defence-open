# Security Policy

## Overview

3AI Defence is a proprietary distributed cyber-defence architecture.

This repository is a public technical and architectural surface.

It intentionally does not publish the production implementation, operational
security configuration, real protected infrastructure or sensitive defensive
logic.

---

## Responsible Disclosure

Please do not disclose exploitable vulnerabilities publicly through normal
issues, discussions or pull requests.

If you believe you have identified a security issue:

1. avoid destructive testing
2. avoid accessing real user, business or infrastructure data
3. collect only the minimum evidence required
4. use a private disclosure channel where available
5. provide clear reproduction information without unnecessary sensitive data

If GitHub private vulnerability reporting is enabled for the repository, it may
be used.

---

## Public Repository Is Not Authorization

This repository does not authorize testing against:

- production systems
- CashOut infrastructure
- third-party networks
- external providers
- private endpoints
- real protected environments
- systems not owned by or explicitly authorized for the tester

Public documentation is not permission to perform security testing.

---

## Defensive Scope

3AI Defence is documented exclusively as an authorized defensive architecture.

The project does not authorize:

- unauthorized system access
- credential attacks
- destructive testing
- denial-of-service activity
- exploitation of third-party infrastructure
- deployment of deceptive infrastructure against systems without permission
- malware deployment
- offensive persistence
- exfiltration of private data

---

## Sensitive Information

Do not include real:

- credentials
- private keys
- tokens
- passwords
- infrastructure addresses
- production topology
- private telemetry
- incident records
- customer information
- private application data
- recovery material
- production security configuration

in public reports or contributions.

---

## Protected Environment Information

3AI Defence may participate in real protected environments.

Security reports should avoid exposing:

- asset inventories
- internal service names
- monitoring configuration
- response policies
- containment design
- recovery architecture
- private network relationships
- internal defensive signals

---

## Module Security

The public architecture describes three defensive roles:

- Akali
- Caronte
- Outy

The repository intentionally does not expose production details such as:

- exact Akali integrity targets
- trusted recovery locations
- Caronte containment rules
- decoy deployment configuration
- Outy model configuration
- orchestration thresholds
- automated response policy

---

## CashOut

CashOut is currently one protected environment related to 3AI Defence.

This repository does not authorize testing against CashOut.

Do not use public architectural descriptions to probe or infer private CashOut
security implementation.

---

## Third-Party Systems

3AI Defence may conceptually interact with external systems or providers.

Any vulnerability primarily affecting a third-party service should also be
reported through that provider's responsible disclosure process where
appropriate.

This repository grants no authorization to test third-party systems.

---

## No Bug Bounty Commitment

Publication of this policy does not create a paid bug bounty program or
guarantee compensation.

Any compensation or recognition must be separately agreed.

---

## Public Boundary

This repository may document:

- defensive architecture
- role separation
- resilience
- offline operation
- high-level response lifecycle
- interoperability boundaries

It intentionally does not publish:

- detection signatures
- response thresholds
- production incident playbooks
- operational commands
- private telemetry
- model configuration
- real network topology
- credentials
- confidential integrations
- security bypass techniques

---

## Responsible Disclosure Principle

> **Protect the systems first, disclose the minimum necessary information, and never treat public architecture as authorization to attack.**
