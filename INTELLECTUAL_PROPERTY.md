# 3AI Defence Intellectual Property

## Overview

3AI Defence is a proprietary distributed cyber-defence architecture.

This public repository documents selected architecture, module
responsibilities, defensive workflows, resilience principles and
interoperability boundaries.

Publication is intended to make the system technically understandable without
publishing the private implementation that provides its operational and
commercial value.

---

# Prior Technical Documentation

The 3AI Defence architecture is supported by prior notarized technical
documentation establishing authorship and a date-certain description of the
architecture.

That documentation describes the original system concept, including the
separation and cooperation of:

- Akali
- Caronte
- Outy

and the broader defensive model around:

- integrity
- trusted recovery
- containment
- controlled defensive decoys
- local AI
- orchestration
- offline / semi-disconnected operation
- coordinated detection, containment and recovery

The notarized source document itself is intentionally not published in this
repository.

---

# Why the Source Document Is Private

The source documentation contains information that is unnecessary for public
technical evaluation, including personal and legal-identification details.

The public repository therefore exposes the technical architecture while
keeping the original legal evidence private.

---

# Public Technical Surface

This repository may publicly document:

- the 3AI Defence architecture
- Akali responsibilities
- Caronte responsibilities
- Outy defensive responsibilities
- coordination concepts
- detection-response-recovery lifecycle
- offline operation
- resilience
- protected-environment concepts
- CashOut integration boundaries
- roadmap
- public security principles

These materials are public documentation, not a transfer of ownership.

---

# Core Architectural Identity

The public architecture can be summarized as:

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

# Proprietary Implementation

Private implementation may include:

- production source code
- integrity-monitoring logic
- trusted-state validation
- recovery infrastructure
- recovery material
- containment mechanisms
- real decoy configuration
- network isolation logic
- private telemetry
- model configuration
- internal prompts
- defensive classifiers
- confidence logic
- orchestration rules
- response policy
- audit infrastructure
- deployment tooling
- hardware configuration
- operational security
- CashOut production integration
- commercially sensitive security logic

Publication of high-level architecture does not grant permission to use or
reproduce these private implementations.

---

# Akali

Public documentation may describe Akali as the module responsible for:

- integrity
- trusted state
- recovery

Private implementation may include:

- actual monitored assets
- validation mechanisms
- recovery storage
- restoration logic
- production state references

---

# Caronte

Public documentation may describe Caronte as the module responsible for:

- containment
- isolation
- controlled defensive decoys

Private implementation may include:

- production containment rules
- network topology
- decoy configuration
- isolation policy
- observation mechanisms

---

# Outy

Public documentation may describe Outy as the module responsible for:

- analysis
- correlation
- local AI
- orchestration

Private implementation may include:

- model configuration
- internal prompts
- proprietary classifiers
- private telemetry
- decision logic
- response orchestration
- learning systems

---

# CashOut Relationship

CashOut is currently one protected environment related to 3AI Defence.

Public documentation may describe that relationship at a high level.

Private CashOut defensive implementation remains outside this repository.

No publication here grants rights to private CashOut technology or data.

---

# Copyright

Original documentation, diagrams, authored text, source code and original
visual materials may be protected by copyright.

Copyright protects the expression of those materials, not abstract ideas by
themselves.

Other technical subject matter may be protected separately where applicable
through:

- trade secret
- contract
- patent
- trademark
- other legal mechanisms

---

# Trade Secrets and Confidential Information

Some competitive value is intentionally not published.

Examples may include:

- algorithms
- thresholds
- orchestration logic
- model configuration
- response policies
- private telemetry
- operational procedures
- infrastructure design
- recovery systems
- containment implementation

Public documentation does not waive confidentiality or trade-secret protection
for information that remains private.

---

# Patents

No patent license is granted by publication of this repository.

This repository is not a patent filing and does not state that any particular
feature is patented or patent-pending.

Where patent protection is relevant, it is handled separately.

---

# Trademarks and Branding

Project names, logos and visual identity may be protected separately from
source code or documentation.

Public access to this repository does not grant permission to use 3AI Defence,
Akali, Caronte, Outy or related branding in a way that implies official
authorization, affiliation or endorsement.

Third-party trademarks remain the property of their respective owners.

---

# Third-Party Technology

3AI Defence may rely on or interact with third-party:

- hardware
- operating systems
- libraries
- AI models
- security intelligence
- infrastructure

Those technologies remain subject to their own ownership, licenses and terms.

---

# Public Repository Is Not Open Source

Unless a specific file or component explicitly states otherwise, materials in
this repository are provided under the proprietary terms in [LICENSE](LICENSE).

Public visibility does not imply:

- unrestricted copying
- commercial reuse
- permission to reproduce private implementation
- permission to access protected infrastructure
- transfer of patent rights
- transfer of trademarks
- authorization for security testing

---

# Separate Commercial Agreements

Commercial use, deployment rights, integration rights or broader technology
licensing require separate agreement where applicable.

---

# Principle

> **Document the architecture, preserve the evidence, protect the implementation.**
