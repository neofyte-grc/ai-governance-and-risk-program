# Third-Party and Vendor AI Risk Review

## PLG RouteAssist

**System:** `AI-SYS-001` — PLG RouteAssist  
**Review owner:** Procurement / Vendor Manager  
**Co-reviewers:** Information Security, Legal / Privacy, Data / AI, IT, and GRC  
**Status:** Draft portfolio artifact  
**Version:** 1.0  
**Date:** 2026-09-20

---

## 1. Purpose

This review defines the due-diligence, contracting, monitoring, change, incident, continuity, and exit requirements for any third party supporting RouteAssist.

No vendor selection or production connection is approved by this document. Vendor evidence remains fictional and unavailable; therefore, all review conclusions are preliminary.

---

## 2. Vendor Scope

The review applies to:

- AI model or decision-support provider.
- Cloud and hosting provider.
- Mapping, traffic, weather, or geolocation provider.
- Integration, implementation, support, and monitoring provider.
- Vendor subprocessors with access to PLG data or critical service functions.

---

## 3. Initial Risk Rating

| Factor | Assessment |
| --- | --- |
| Data sensitivity | High: workforce, customer, recipient, location, and potential medical-delivery information |
| Operational dependency | High: dispatch recommendations and time-sensitive workflows |
| Potential impact | Critical for certain safety or medical-delivery scenarios |
| Substitutability | Unknown until vendor and exit analysis |
| Transparency | Unknown until vendor documentation is received |
| Overall preliminary tier | Critical vendor review required before use |

---

## 4. Due-Diligence Checklist

| Review ID | Domain | Required information | Status |
| --- | --- | --- | --- |
| `VDR-001` | Organization | Ownership, financial stability, AI experience, and key contacts | Not received |
| `VDR-002` | AI governance | Policies, accountable roles, risk process, prohibited uses, and escalation | Not received |
| `VDR-003` | System documentation | Model or service purpose, architecture, versions, limitations, and intended users | Not received |
| `VDR-004` | Training and evaluation data | Data sources, rights, quality, representation, provenance, and reuse | Not received |
| `VDR-005` | Performance | Metrics, test sets, known failures, slice results, and drift practices | Not received |
| `VDR-006` | Safety and human oversight | High-impact controls, human-review design, stop conditions, and fallback | Not received |
| `VDR-007` | Fairness | Harm analysis, subgroup testing, mitigation, and complaint handling | Not received |
| `VDR-008` | Privacy | Data roles, purposes, minimization, retention, deletion, location, and requests | Not received |
| `VDR-009` | Security | Security program, access, encryption, logging, vulnerabilities, and testing | Not received |
| `VDR-010` | Integrations | Authentication, validation, rate limits, integrity, and error handling | Not received |
| `VDR-011` | Subprocessors | Complete list, locations, functions, data access, and change notice | Not received |
| `VDR-012` | Incidents | Notification targets, cooperation, evidence, and prior material incidents | Not received |
| `VDR-013` | Resilience | Availability, backup, disaster recovery, recovery objectives, and testing | Not received |
| `VDR-014` | Change management | Versioning, advance notice, release notes, rollback, and customer control | Not received |
| `VDR-015` | Assurance | Independent reports, certifications, test summaries, and remediation | Not received |
| `VDR-016` | Exit | Portability, deletion, transition support, lock-in, and termination assistance | Not received |

---

## 5. Vendor Questionnaire

The vendor should answer:

### 5.1 AI governance

1. Who is accountable for the service’s AI governance and risk management?
2. What policies govern intended use, prohibited use, safety, fairness, privacy, security, and incidents?
3. How are material risks identified, treated, accepted, and monitored?
4. How may customers report harmful output or request correction?
5. What independent assurance covers the service?

### 5.2 System and model

1. What model or decision technology is used?
2. How are versions identified?
3. What are the intended uses, prohibited uses, and known limitations?
4. What data is required to operate the service?
5. Can customer data be used for training, tuning, evaluation, or product improvement?
6. How are explanations, uncertainty, and limitations generated and validated?

### 5.3 Performance and safety

1. What metrics and thresholds are used?
2. How does performance vary across operating conditions and relevant groups?
3. How are rare and high-impact scenarios tested?
4. How are unsafe or unsupported outputs blocked or escalated?
5. How are drift and degradation detected?
6. What rollback and suspension mechanisms are available?

### 5.4 Privacy and security

1. Where is PLG data stored and processed?
2. Which personnel and subprocessors can access it?
3. How are access, encryption, secrets, logs, vulnerabilities, and incidents managed?
4. What are the retention and deletion practices?
5. How are data-subject, customer, and deletion requests supported?
6. What security and privacy assurance reports are available?

### 5.5 Continuity and exit

1. What availability and recovery commitments apply?
2. When was disaster recovery last tested?
3. How will PLG export data and configurations?
4. How will deletion be verified at termination?
5. What transition assistance is available?
6. What functions will fail if the service becomes unavailable?

---

## 6. Mandatory Contract Requirements

Contracts should address:

- Defined service, approved purpose, and prohibited uses.
- PLG ownership and control of PLG data.
- No vendor training or unrelated reuse without express written approval.
- Field, purpose, retention, location, and deletion requirements.
- Security controls, access restrictions, encryption, logging, and vulnerability management.
- Named subprocessors and advance notice of changes.
- Identifiable system and model versions.
- Advance notice and impact information for material changes.
- Performance, safety, availability, support, and recovery commitments.
- Prompt incident and security notification.
- Cooperation with investigation, notification, correction, and evidence preservation.
- Audit, assessment, and evidence rights.
- Correction, rollback, suspension, and termination rights.
- Data return, verified deletion, portability, and transition assistance.
- Allocation of responsibility, liability, insurance, and indemnification as approved by counsel.

---

## 7. Evidence Evaluation

Vendor claims must be assessed for:

- Relevance to the contracted service and deployed version.
- Coverage period and expiration.
- Independent versus self-attested status.
- Scope, exclusions, exceptions, and complementary customer controls.
- Whether findings and remediation are material to RouteAssist.
- Whether evidence can be retained and shared with authorized reviewers.

A certification or assurance report does not replace RouteAssist-specific testing.

---

## 8. Material Change Triggers

Vendor review and PLG revalidation are required for changes to:

- Model, major version, rules, prompts, or decision logic.
- Training, tuning, evaluation, or customer-data use.
- Hosting region, architecture, integration, or security control.
- Subprocessor or critical dependency.
- Data fields, purpose, retention, or deletion.
- Performance, limitation, explanation, or safety behavior.
- Terms, service level, incident process, or exit rights.

PLG may delay, reject, restrict, or roll back an unapproved change.

---

## 9. Ongoing Monitoring

| Area | Evidence | Cadence |
| --- | --- | --- |
| Service performance and availability | SLA report, outages, and support cases | Monthly |
| Model and service changes | Version record, release notes, and impact assessment | Each change |
| Security and privacy | Incidents, assurance reports, vulnerabilities, and subprocessors | Quarterly and upon event |
| Performance and drift | PLG and vendor metrics, limitations, and defect trends | Monthly |
| Contract compliance | Notices, evidence delivery, deletion, and audit obligations | Quarterly |
| Financial and continuity risk | Business condition, recovery evidence, and concentration risk | Annually |

---

## 10. Exit and Contingency Requirements

Before production use, PLG will document:

- Alternative manual or vendor-supported process.
- Data and configuration export format.
- Integration-disconnection procedure.
- Access and credential removal.
- Required records retained by PLG.
- Vendor data return and verified deletion.
- Transition responsibilities and timeline.
- Service continuity during termination.
- Final risk, legal, privacy, and contract review.

---

## 11. Preliminary Gaps

| Gap ID | Gap | Required action |
| --- | --- | --- |
| `VGP-001` | No vendor or model documentation | Obtain and review required technical documentation |
| `VGP-002` | Vendor data-use rights are unknown | Define contractual purpose and training restrictions |
| `VGP-003` | Subprocessors are unknown | Obtain complete list and change-notice rights |
| `VGP-004` | Material-change process is unknown | Require versioning, advance notice, testing, and rollback |
| `VGP-005` | AI performance and fairness evidence is unavailable | Obtain evidence and conduct PLG-specific testing |
| `VGP-006` | Incident notification and cooperation are undefined | Establish contractual targets and evidence duties |
| `VGP-007` | Exit and verified deletion are untested | Document and exercise export, deletion, and transition |

---

## 12. Preliminary Decision

**Decision:** Not approved pending evidence.

The vendor relationship may proceed only after:

1. Critical due-diligence evidence is reviewed.
2. Material gaps are remediated or formally accepted.
3. Contract requirements are approved.
4. RouteAssist-specific evaluation passes.
5. Exit and continuity arrangements are viable.
6. The AI Governance Committee authorizes the applicable lifecycle gate.

---

## 13. Related Risks and Controls

| Risks | Controls |
| --- | --- |
| `AIR-007`, `AIR-009`, `AIR-010`, `AIR-011`, `AIR-016`, `AIR-017` | `AIC-014`, `AIC-015`, `AIC-026`, `AIC-027`, `AIC-028`, `AIC-029` |

---

## 14. NIST AI RMF Alignment

| Function | Contribution |
| --- | --- |
| GOVERN | Establishes third-party accountability, contracting, and evidence requirements |
| MAP | Identifies vendor dependencies, data, limitations, and affected context |
| MEASURE | Requires vendor and PLG evaluation, assurance, monitoring, and evidence |
| MANAGE | Supports remediation, restriction, rollback, termination, and exit |

---

## 15. Document Control

| Field | Value |
| --- | --- |
| Document title | Third-Party and Vendor AI Risk Review |
| Repository path | `docs/14-third-party-and-vendor-ai-risk-review.md` |
| Version | 1.0 |
| Status | Draft portfolio artifact |
| Author | Tommy Marshall |
| Owner | Procurement / Vendor Manager |
| Approver | AI Governance Committee |
| Review frequency | Before contract, annually, and upon material trigger |
| Classification | Public fictional portfolio content |

### Version History

| Version | Date | Author | Change summary |
| --- | --- | --- | --- |
| 1.0 | 2026-09-20 | Tommy Marshall | Created the initial vendor-AI review, due-diligence checklist, contractual requirements, gaps, and preliminary decision. |

---

## 16. Portfolio Notice

This fictional vendor review contains no actual vendor evidence or approval. It does not establish contractual, legal, security, privacy, compliance, or assurance conclusions.
