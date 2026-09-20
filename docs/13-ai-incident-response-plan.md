# AI Incident Response Plan

## PLG RouteAssist

**System:** `AI-SYS-001` — PLG RouteAssist  
**Plan owner:** Business Continuity / Incident Manager  
**Approver:** AI Governance Committee  
**Status:** Draft portfolio artifact  
**Version:** 1.0  
**Date:** 2026-09-20

---

## 1. Purpose

This plan defines how PLG identifies, reports, assesses, contains, investigates, communicates, recovers from, and learns from RouteAssist incidents.

An AI incident may involve harmful output, unsafe reliance, misuse, unfair impact, privacy loss, security compromise, data failure, vendor change, monitoring failure, or ineffective human oversight.

---

## 2. Incident Criteria

An event becomes an AI incident when it causes or could reasonably cause:

- Injury, unsafe routing, or severe delivery harm.
- Delayed or mishandled time-sensitive medical delivery.
- Unauthorized employment or performance use.
- Material assignment disparity or cumulative worker harm.
- Unauthorized access, disclosure, manipulation, or system change.
- Use outside approved scope or bypass of human review.
- Loss of traceability for a material decision.
- Significant model, data, integration, or vendor failure.
- Failure of fallback, monitoring, escalation, or recovery.
- Widespread or repeated inaccurate or misleading recommendations.

Near misses are recorded when controls prevented harm but the underlying condition could recur.

---

## 3. Severity Matrix

| Severity | Description | Examples | Initial target |
| --- | --- | --- | --- |
| Severity 1 — Critical | Actual or imminent severe harm or widespread compromise | Injury, dangerous route at scale, major breach, or unauthorized medical use with potential harm | Immediate response and suspension authority |
| Severity 2 — High | Material impact or failure of a critical control | Significant disparity, unapproved model change, human-review bypass, or major outage | Acknowledge within 15 minutes |
| Severity 3 — Moderate | Localized impact with manageable exposure | Repeated inaccurate output, incomplete logs, or limited privacy event | Acknowledge within 1 hour |
| Severity 4 — Low | Minor issue with limited risk effect | Isolated display error or low-impact defect | Acknowledge within one business day |

These are fictional internal targets and do not replace legal, emergency, contractual, or regulatory requirements.

---

## 4. Roles

| Role | Responsibility |
| --- | --- |
| Incident Manager | Leads coordination, severity, actions, communications, recovery, and closure |
| Dispatch Director | Protects operations, affected deliveries, drivers, couriers, and recipients |
| CIO / IT Director | Contains technical failures, preserves systems, and manages rollback and recovery |
| Information Security Lead | Leads cyber investigation, access containment, threat analysis, and evidence handling |
| Data / AI Lead | Analyzes model, data, output, drift, and technical behavior |
| Legal / Privacy Advisor | Assesses notification, privacy, contractual, and legal implications |
| Human Resources Manager | Handles workforce impact, retaliation, and prohibited employment use |
| Customer Service Manager | Coordinates affected customer and recipient cases |
| Procurement / Vendor Manager | Coordinates vendor notification, evidence, remediation, and contract escalation |
| GRC Analyst | Links incidents to risks, controls, decisions, POA&M items, and governance records |
| AI Governance Committee | Reviews material incidents, restrictions, residual risk, and return to service |
| Chief Operating Officer | Provides executive decisions for severe incidents and High-risk acceptance |

---

## 5. Reporting Channels

Personnel must report suspected incidents through the designated operational or security channel and notify a supervisor when immediate harm may occur.

Reports should include, when available:

- Reporter and contact information.
- Time detected and time of the underlying event.
- Transaction, delivery, user, system, and version identifiers.
- Description of the event and affected parties.
- Current or potential harm.
- Screenshots, logs, messages, or other evidence.
- Actions already taken.
- Whether the issue remains active.

Personnel may report suspected incidents in good faith without retaliation.

---

## 6. Response Lifecycle

### 6.1 Detect and report

- Receive an alert, complaint, observation, vendor notice, audit finding, or automated detection.
- Protect people and time-sensitive operations first.
- Create an incident record and preserve the original report.

### 6.2 Triage

- Confirm whether RouteAssist contributed to or affected the event.
- Assign a preliminary severity and incident commander.
- Identify the affected capability, data, users, deliveries, geography, and time period.
- Determine whether emergency services, manual dispatch, privacy, legal, security, HR, or vendor support is needed.

### 6.3 Contain

Potential containment actions include:

- Rejecting or correcting the recommendation.
- Pausing a capability or user role.
- Activating manual fallback.
- Revoking access or credentials.
- Isolating an integration or data source.
- Blocking medical or other high-impact use.
- Rolling back a version or configuration.
- Suspending RouteAssist.

### 6.4 Investigate

Preserve and analyze:

- Inputs, source timestamps, transformations, and validation results.
- Model, service, rule, prompt, and configuration versions.
- Recommendation, rationale, uncertainty, and alternatives.
- Human review, override, escalation, and downstream action.
- Access, administrative, integration, security, and monitoring logs.
- Vendor notices, support records, and relevant assurance evidence.
- Complaints, impacts, and related prior events.

The investigation will determine:

- Timeline.
- Root cause.
- Contributing factors.
- Affected population.
- Actual and potential impact.
- Control performance.
- Whether similar events occurred.
- Potential for recurrence.

### 6.5 Communicate

Communications must be:

- Accurate.
- Authorized.
- Audience-appropriate.
- Timely.
- Coordinated with Legal / Privacy.
- Limited to necessary information.

Possible audiences include leadership, affected workers, customers, recipients, healthcare clients, vendors, insurers, law enforcement, and regulators when applicable.

### 6.6 Eradicate and remediate

- Correct data, logic, access, integration, configuration, process, or training failures.
- Address affected outcomes where possible.
- Update risks, controls, tests, thresholds, and procedures.
- Create POA&M actions for unresolved gaps.
- Require vendor remediation where appropriate.

### 6.7 Recover

Restore service only after:

- Required controls are functioning.
- Testing or regression testing passes.
- Residual risk is documented.
- Monitoring is increased when appropriate.
- Authorized approval is recorded.

### 6.8 Close and learn

Document:

- Final severity.
- Affected scope and impact.
- Root cause and contributing factors.
- Response timeline and actions.
- Evidence collected.
- Notifications made.
- Corrective actions.
- Remaining risk.
- Approval and closure.
- Lessons learned.

---

## 7. Evidence Preservation

PLG responders must:

- Use a unique incident identifier.
- Preserve original records.
- Maintain chain of custody when required.
- Restrict evidence access.
- Record the source, collector, collection time, and method.
- Avoid altering production evidence during analysis.
- Preserve relevant model, system, configuration, and data versions.
- Follow approved retention and legal-hold requirements.

Missing evidence or a logging failure is itself evaluated as a control deficiency.

---

## 8. Containment Authority

The following roles may order an immediate temporary restriction or suspension within their assigned authority:

- Incident Manager.
- Dispatch Director.
- CIO / IT Director.
- Information Security Lead.
- Chief Operating Officer.

Emergency action must be documented and reviewed by the AI Governance Committee as soon as practical.

---

## 9. Return-to-Service Criteria

Return to service requires:

- Harm has been contained.
- The affected scope is understood.
- Root cause or sufficient causal understanding is documented.
- Critical controls are restored.
- Corrective action and regression testing are completed.
- Data, version, access, integrations, logging, monitoring, and human review are verified.
- Residual risk and temporary conditions are documented.
- Authorized approval is recorded.
- Rollback and renewed suspension remain available.

Severity 1 restoration requires executive and committee review.

---

## 10. Incident Record

Each incident record should include:

| Field | Requirement |
| --- | --- |
| Incident ID | Unique, permanent identifier |
| Detection | Date, time, source, and reporter |
| Classification | AI-related category and severity |
| System context | System, model, configuration, and vendor version |
| Affected scope | Capabilities, users, deliveries, data, geography, and period |
| Impact | Actual and potential effects |
| Timeline | Detection through closure |
| Actions | Triage, containment, investigation, remediation, and recovery |
| Evidence | Logs, records, screenshots, reports, and chain of custody |
| Notifications | Internal and external communications |
| Cause | Root cause and contributing factors |
| Controls | Controls that failed, succeeded, or were absent |
| Corrective action | Owner, due date, POA&M linkage, and validation |
| Closure | Residual risk, approver, date, and lessons learned |

---

## 11. Tabletop Exercise

At least annually and before the pilot, PLG will exercise a scenario involving:

- An unsafe recommendation and delayed detection.
- Missing or incomplete logs.
- A vendor or model change.
- Manual fallback under peak workload.
- A worker or customer complaint.
- Cross-functional containment and communication.

The exercise report will record:

- Participants.
- Scenario.
- Decisions.
- Response timing.
- Successful controls.
- Gaps.
- Corrective actions.
- Owners and due dates.
- Retesting requirements.

---

## 12. Related Risks and Controls

| Risks | Controls |
| --- | --- |
| `AIR-001`, `AIR-002`, `AIR-009`, `AIR-014`, `AIR-016`, `AIR-017`, `AIR-018` | `AIC-020`, `AIC-022`, `AIC-023`, `AIC-024`, `AIC-025`, `AIC-026`, `AIC-027`, `AIC-030` |

---

## 13. NIST AI RMF Alignment

| Function | Contribution |
| --- | --- |
| GOVERN | Defines incident accountability, authority, evidence, and reporting |
| MAP | Identifies affected context, parties, dependencies, and impacts |
| MEASURE | Uses alerts, complaints, logs, and investigation evidence |
| MANAGE | Contains, restricts, remediates, recovers, and prevents recurrence |

---

## 14. Document Control

| Field | Value |
| --- | --- |
| Document title | AI Incident Response Plan |
| Repository path | `docs/13-ai-incident-response-plan.md` |
| Version | 1.0 |
| Status | Draft portfolio artifact |
| Author | Tommy Marshall |
| Owner | Business Continuity / Incident Manager |
| Approver | AI Governance Committee |
| Review frequency | At least annually and after material incidents or exercises |
| Classification | Public fictional portfolio content |

### Version History

| Version | Date | Author | Change summary |
| --- | --- | --- | --- |
| 1.0 | 2026-09-20 | Tommy Marshall | Created the initial RouteAssist AI incident-response process, severity model, containment authority, evidence requirements, and return-to-service criteria. |

---

## 15. Portfolio Notice

This fictional portfolio plan does not replace a real emergency, security, privacy, legal, or regulatory response plan and does not demonstrate operational readiness.
