# P2-5: GRC Policies & Risk

## Overview

This repo is planned to document Governance, Risk, and Compliance (GRC) work that supports broader cybersecurity programs.

It is intended to focus on security policies, risk matrices, governance documentation, and framework mapping aligned to standards such as NIST CSF, NIST 800-53, ISO 27001, and PCI-DSS.

This project is part of Portfolio 2 and is planned as a follow-on phase after completion of Portfolio 1, which provides the technical lab foundation that can later supply evidence, findings, and scenarios for GRC documentation and risk analysis.

---

## Status

**Current state:** Planned  
**Execution state:** Not yet started  
**Prerequisite:** Portfolio 1 completion

This repo is being prepared in advance so that the project scope, document structure, policy set, and risk-management workflow are already defined before hands-on work begins.

---

## Planned Objectives

This project is intended to build practical GRC skills, including:

- creating enterprise-style security policies
- performing qualitative and semi-quantitative risk analysis
- building a standardized risk matrix
- documenting governance requirements
- mapping controls to recognized industry frameworks
- translating technical findings into business risk language

---

## Planned Repository Structure

- `docs/` — policies, risk matrices, templates, framework mappings, and governance documentation
- `lab/` — optional supporting evidence such as screenshots, findings, posture data, or validation notes
- `scripts/` — optional automation for CSV handling, policy tracking, or lightweight analysis support
- `.github/` — issue or pull request templates (optional)

---

## Planned Security Policies

This repo is expected to include foundational policy documents such as:

- Acceptable Use Policy
- Access Control Policy
- Incident Response Policy
- Change Management Policy
- Vulnerability Management Policy
- Logging and Monitoring Policy
- Backup and Recovery Policy

Additional policies may be added later as the portfolio expands.

Each policy is planned to follow a consistent structure, such as:

- purpose
- scope
- roles and responsibilities
- requirements
- enforcement
- definitions where needed
- versioning or revision history

---

## Planned Risk Management Content

This repo is expected to include:

- a risk matrix using likelihood and impact
- a simple heat map representation
- a risk scoring approach
- controls mapped to identified risks
- recommendations or treatment options

Planned risk entries may be based on scenarios such as:

- network scan findings
- cloud configuration issues
- identity and access misconfigurations
- policy or control gaps
- general security scenarios relevant to small enterprise environments

The goal is to practice documenting risk in a way that connects technical issues to governance and decision-making.

---

## Planned Use of Supporting Evidence

Most GRC work in this repo is planned to be documentation-driven.

However, the repo may also reference supporting evidence such as:

- screenshots from Azure Secure Score
- findings from vulnerability scans
- endpoint hardening gaps
- audit logs showing misconfigurations
- screenshots or exports from related projects

These can be placed in `lab/` when useful to support risk scoring, control mapping, or policy justification.

---

## Planned Workflow

Once execution begins, the intended workflow for this repo is:

### 1. Define or refine the policy set
Planned activities may include:

- selecting the initial policies to draft
- using a consistent policy template
- aligning language across all documents
- documenting ownership, scope, and enforcement expectations

### 2. Build the risk matrix
Planned activities may include entering realistic risks such as:

- weak password policies
- open RDP exposure
- missing MFA
- vulnerable software
- lack of logging or monitoring
- lack of backups
- excessive privileges or poor access control

Each entry may include:

- likelihood
- impact
- overall risk rating
- mapped controls
- recommended treatment or mitigation

### 3. Map policies and risks to frameworks
Planned framework mapping may include:

- NIST CSF
- NIST 800-53
- ISO 27001 Annex A
- PCI-DSS
- CIS Controls

The goal is to show how governance documents and risk treatment relate to common industry standards.

### 4. Support the documentation with evidence where useful
Planned activities may include:

- referencing findings from related portfolio projects
- linking technical observations to risk entries
- storing optional screenshots or exported evidence in `lab/`

---

## Planned Deliverables

This repo is expected to eventually include:

- security policy documents
- a completed risk matrix
- control mapping to industry frameworks
- governance documentation
- optional audit or lab evidence
- optional diagrams or supporting visuals

---

## Planned Skill Areas

This project is intended to help build experience in:

- security policy writing
- governance documentation
- qualitative and semi-quantitative risk scoring
- framework mapping
- control thinking
- translating technical issues into business risk
- understanding how governance supports cybersecurity maturity

---

## Planned Next Steps

When work begins on this repo, the initial implementation focus will likely be:

- draft the first core policy documents
- build the initial risk matrix template
- define a simple scoring methodology
- map selected risks to appropriate controls
- connect selected technical findings from other portfolio projects to governance documentation

Future expansion may include:

- a Data Classification and Handling Policy
- a Mobile Device or BYOD Security Policy
- a formal risk register
- a NIST CSF checklist
- audit-evidence examples in `lab/`
- a policy exception request form for realism and workflow completeness

---

## Planned Related Projects

### Repo 2 — Vulnerability Management
This repo may later pull findings from vulnerability assessments into the risk matrix and treatment documentation.

### Repo 3 — Endpoint Hardening
This repo may later use hardening gaps or validation findings as supporting evidence for risk scoring or control justification.

---

## License

MIT — see `LICENSE`.
