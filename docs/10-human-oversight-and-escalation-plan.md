# Human Oversight and Escalation Plan

## PLG RouteAssist

**Organization:** Peachtree Logistics Group (fictional)  
**AI system:** PLG RouteAssist  
**System identifier:** `AI-SYS-001`  
**Use-case identifier:** `UC-001`  
**Plan owner:** Dispatch Director  
**Plan coordinator:** GRC Analyst  
**Approval authority:** AI Governance Committee  
**Assessment stage:** Predeployment  
**Document status:** Draft portfolio artifact  
**Version:** 1.0  
**Review frequency:** Monthly during pilot; quarterly after stabilization; upon material trigger

---

## 1. Purpose

This plan defines how authorized personnel review, challenge, approve, modify, reject, override, escalate, pause, and document RouteAssist recommendations.

Its purpose is to ensure that human involvement is meaningful rather than ceremonial. A reviewer must have the information, competence, time, authority, and practical ability to prevent or limit harm.

---

## 2. Oversight Objective

Human oversight will:

- Preserve human accountability for dispatch decisions.
- Detect inaccurate, unsafe, unfair, misleading, or out-of-scope recommendations.
- Reduce automation bias and rubber-stamping.
- Protect drivers, couriers, customers, recipients, and PLG operations.
- Provide clear override and escalation authority.
- Support traceability, monitoring, investigation, and improvement.
- Trigger manual fallback or system suspension when continued use is unsafe or unreliable.

---

## 3. Operating Boundary

RouteAssist is an advisory decision-support system.

It may recommend:

- Delivery priority.
- Driver or courier assignment.
- Route or sequence.
- Scheduling adjustments.
- Exception flags for human attention.

It may not independently:

- Dispatch a driver or courier.
- Change a delivery priority.
- Execute a route change.
- Rank, discipline, terminate, or evaluate a worker.
- Approve medical-delivery handling.
- Override safety rules or human stop decisions.
- Expand to an unapproved use, population, service, or geography.

An authorized human remains responsible for the final operational action.

---

## 4. Oversight Roles

| Role ID | Role | Oversight responsibility |
| --- | --- | --- |
| `ROLE-011` | Dispatcher | Performs first-line review; approves, modifies, rejects, or escalates recommendations |
| `ROLE-010` | Dispatch Supervisor | Reviews high-impact, ambiguous, unusual, disputed, and escalated cases; monitors reviewer behavior |
| `ROLE-004` | Dispatch Director | Owns the oversight process, operational boundaries, staffing, and corrective actions |
| `ROLE-012` | Operations Manager | Supports field feasibility, continuity, and manual fallback |
| `ROLE-006` | Data / AI Lead | Investigates model behavior, data limitations, drift, and technical defects |
| `ROLE-005` | CIO / IT Director | Addresses outages, integration failures, access issues, logging, and rollback |
| `ROLE-007` | Information Security Lead | Handles suspected manipulation, unauthorized access, and security events |
| `ROLE-008` | Legal / Privacy Advisor | Advises on privacy, notice, rights, contractual, and legal concerns |
| `ROLE-013` | Human Resources Manager | Handles worker-impact, prohibited employment use, and retaliation concerns |
| `ROLE-014` | Customer Service Manager | Manages customer and recipient complaints, disputes, and corrections |
| `ROLE-016` | Incident Manager | Coordinates material AI incidents, containment, communications, and recovery |
| `ROLE-003` | GRC Analyst | Tracks risks, evidence, metrics, exceptions, escalation, and governance decisions |
| `ROLE-002` | AI Governance Committee | Approves oversight design, reviews systemic issues, and authorizes material changes |

---

## 5. Oversight Levels

| Level | Situation | Required reviewer | Required action |
| --- | --- | --- | --- |
| Level 1 — Standard | Routine, in-scope, non-medical recommendation with complete and current data | Trained Dispatcher | Review required fields and approve, modify, reject, or escalate |
| Level 2 — Enhanced | Ambiguous, unusual, conflicting, low-confidence, high-value, repeated override, or customer-sensitive case | Dispatch Supervisor | Perform enhanced review and document rationale |
| Level 3 — High impact | Safety-sensitive or other high-impact case authorized for use | Dispatch Supervisor plus designated business authority | Confirm classification, supporting evidence, fallback, and explicit approval |
| Level 4 — Stop and escalate | Medical use during excluded pilot, severe safety concern, suspected misuse, security event, missing traceability, or material threshold breach | Supervisor and relevant incident or governance authority | Stop automated assistance, preserve evidence, use fallback, and escalate |

Medical-delivery recommendations remain outside the initial pilot. Their appearance is a Level 4 event unless separately authorized.

---

## 6. Required Information Presented to Reviewers

Before acting, the reviewer must be able to see or access:

- Unique recommendation or transaction identifier.
- Recommendation type and proposed action.
- Material input data and source timestamps.
- Data-freshness and completeness indicators.
- Delivery type and approved impact classification.
- Relevant constraints, including vehicle, location, capacity, timing, and safety.
- Recommendation basis or contributing factors.
- Uncertainty, confidence, or limitation information that has been validated for use.
- Conflicts, exceptions, or missing-data warnings.
- System and model version.
- Available alternatives when feasible.
- Approved, prohibited, and unsupported-use reminders.
- Actions to approve, modify, reject, escalate, or invoke fallback.

The interface must not use misleading certainty, hidden defaults, manipulative design, or time pressure that prevents meaningful review.

---

## 7. Standard Review Procedure

The reviewer will complete the following steps before downstream action:

1. **Confirm identity and authority.** Verify that the reviewer is signed in under an authorized named account.
2. **Confirm scope.** Verify that the recommendation concerns an approved service, geography, delivery type, and user population.
3. **Confirm data quality.** Review missing, stale, conflicting, implausible, or unusual input indicators.
4. **Confirm operational feasibility.** Consider current road, vehicle, capacity, timing, weather, safety, and field conditions.
5. **Assess affected-party impact.** Consider driver or courier burden, customer impact, recipient harm, and repeat assignment patterns.
6. **Review rationale and uncertainty.** Determine whether the recommendation basis is understandable and sufficiently supported.
7. **Compare alternatives.** Consider reasonable alternatives when the proposed action presents elevated risk or uncertainty.
8. **Choose an action.** Approve, modify, reject, or escalate.
9. **Document the decision.** Record the action and required rationale or reason code.
10. **Verify execution.** Confirm that the downstream system reflects the human-approved action rather than an unapproved output.

If the reviewer cannot complete these steps, the recommendation must not be approved.

---

## 8. Decision Actions

| Action | When used | Documentation requirement |
| --- | --- | --- |
| Approve | Recommendation is in scope, supported, feasible, and within tolerance | Reviewer identity, timestamp, approval, and required acknowledgment |
| Modify | Recommendation is useful but requires adjustment | Original output, modified action, reason code, and free-text rationale when material |
| Reject | Recommendation is inaccurate, unsafe, unfair, unsupported, or unnecessary | Rejection reason, relevant evidence, and defect or feedback link when appropriate |
| Escalate | Reviewer lacks authority, information, confidence, or ability to resolve the concern | Escalation category, urgency, recipient, and temporary action |
| Invoke fallback | System, data, interface, integration, or review process cannot be trusted or used | Fallback start time, reason, scope, supervisor notification, and recovery link |
| Stop or suspend | Continued use could cause severe harm, violates scope, or meets a stop condition | Immediate notification, preserved evidence, affected scope, and incident record |

---

## 9. Override Requirements

An override is a human decision to reject or materially change a RouteAssist recommendation.

### 9.1 Reviewer rights

Authorized reviewers may override when they reasonably believe that:

- The recommendation is unsafe, impractical, inaccurate, unfair, incomplete, or out of scope.
- Source data is stale, conflicting, missing, or implausible.
- Current conditions are not represented.
- A customer, recipient, worker, or delivery constraint requires a different action.
- The rationale or uncertainty is insufficient.
- Manual handling better protects safety, service, rights, or continuity.

### 9.2 Non-retaliation

Good-faith overrides, safety concerns, and escalations must not negatively affect performance evaluation, scheduling, discipline, compensation, or work opportunity.

Suspected retaliation must be reported to Human Resources and the AI Governance Committee Chair.

### 9.3 Override monitoring

PLG will monitor:

- Override rate by user, team, recommendation type, service, geography, and time period.
- Approval rate and unusually low override behavior.
- Repeat override reasons.
- Overrides associated with better or worse outcomes.
- Differences between employed-driver and independent-courier assignments.
- Reviewer patterns indicating rubber-stamping, workarounds, or inadequate training.

Neither a high nor a low override rate is inherently good or bad. Patterns require contextual investigation.

---

## 10. Mandatory Escalation Triggers

| Trigger | Initial recipient | Required immediate action |
| --- | --- | --- |
| Actual or potential injury | Supervisor and Incident Manager | Stop affected use, protect people, preserve evidence, initiate incident response |
| Medical-delivery recommendation during excluded pilot | Supervisor and Dispatch Director | Reject recommendation, use approved manual process, open governance review |
| Unsafe or impossible route | Supervisor | Reject or modify; flag scenario for technical and safety review |
| Stale, missing, conflicting, or corrupted critical data | Data / AI Lead and IT | Block recommendation; use fallback until integrity is confirmed |
| Suspected manipulated input, output, account, or integration | Information Security Lead | Contain affected access or integration and initiate security response |
| Unauthorized employment or performance use | HR Manager and GRC Analyst | Stop use, preserve evidence, protect affected worker, investigate |
| Material assignment disparity or repeated worker complaint | HR Manager, Dispatch Director, and GRC | Pause affected logic when warranted and conduct impact review |
| Recommendation cannot be reconstructed from logs | CIO / IT Director and GRC | Restrict affected use until traceability is restored |
| Vendor or model changed without approval | Procurement, Data / AI Lead, and GRC | Hold or roll back change and begin material-change assessment |
| Drift or performance threshold breach | Data / AI Lead | Restrict affected capability and begin investigation and revalidation |
| System outage or failed review workflow | IT and Operations Manager | Activate manual fallback and continuity procedures |
| Significant privacy concern or unauthorized data exposure | Legal / Privacy Advisor and Security Lead | Limit processing, preserve evidence, and initiate incident assessment |
| Reviewer cannot safely complete review due to workload or interface failure | Dispatch Supervisor | Reduce use, reassign workload, or invoke fallback |
| Complaint indicates ongoing or severe harm | Customer Service Manager and Incident Manager | Prioritize correction, preserve evidence, and assess broader impact |

---

## 11. Stop Conditions

RouteAssist use must be paused or restricted when any of the following occurs:

- Severe harm has occurred or appears imminent.
- Medical-delivery functionality appears during an unauthorized stage.
- Mandatory human review can be bypassed or is unavailable.
- Critical inputs are unreliable and safe operation cannot be confirmed.
- Logs cannot support reconstruction of material decisions.
- Unauthorized access, manipulation, or data exposure is suspected.
- A mandatory safety, fairness, security, privacy, or performance threshold fails.
- The deployed version cannot be identified or differs from the approved version.
- A material vendor, model, data, or integration change has not been reviewed.
- Manual fallback is unavailable when required.
- Reviewers are systematically rubber-stamping or cannot exercise meaningful judgment.
- The AI Governance Committee or authorized emergency role orders a pause.

A stop condition remains active until an authorized return-to-service decision is documented.

---

## 12. Escalation Path

### 12.1 Operational path

1. Dispatcher identifies concern.
2. Dispatcher selects the appropriate action and notifies the Dispatch Supervisor.
3. Supervisor determines whether to resolve, invoke fallback, or escalate.
4. Functional owner investigates the issue.
5. Incident Manager coordinates when severity or cross-functional impact warrants.
6. AI Governance Committee reviews material or systemic issues.
7. Chief Operating Officer resolves matters beyond committee authority.

### 12.2 Functional routing

| Concern | Functional owner |
| --- | --- |
| Data quality, performance, drift, explanation | Data / AI Lead |
| Access, manipulation, vulnerability, integration security | Information Security Lead |
| Outage, logging, configuration, rollback | CIO / IT Director |
| Worker impact, employment use, retaliation | Human Resources Manager |
| Privacy, notice, contractual or legal concern | Legal / Privacy Advisor |
| Vendor failure or unannounced change | Procurement / Vendor Manager |
| Complaint, dispute, or customer correction | Customer Service Manager |
| Safety, dispatch feasibility, and operational procedure | Dispatch Director |
| Material incident and recovery | Business Continuity / Incident Manager |
| Risk acceptance, evidence, POA&M, governance record | GRC Analyst and AI Governance Committee |

If ownership is uncertain, the issue is routed to the Incident Manager and GRC Analyst rather than delayed.

---

## 13. Severity and Response Targets

| Severity | Example | Acknowledge | Escalate | Operational expectation |
| --- | --- | ---: | ---: | --- |
| Severity 1 — Critical | Actual or imminent severe harm, major security compromise, or unauthorized medical use with potential harm | Immediately | Immediately | Stop affected use and activate incident command |
| Severity 2 — High | Material control failure, significant disparity, major outage, or unapproved change | Within 15 minutes | Within 30 minutes | Restrict affected capability and begin investigation |
| Severity 3 — Moderate | Repeated inaccurate output, localized workflow failure, or threshold warning | Within 1 hour | Within 4 hours | Apply workaround and assign investigation |
| Severity 4 — Low | Isolated minor error with no material impact | Within 1 business day | As needed | Correct through routine support and trend monitoring |

Targets are internal planning goals for this fictional project and do not replace emergency, legal, contractual, or regulatory obligations.

---

## 14. Manual Fallback

Manual fallback must provide:

- A clear activation authority and communication method.
- Current manual dispatch, routing, priority, and assignment procedures.
- Access to necessary source systems without RouteAssist.
- Adequate trained staffing for expected volume.
- A method to identify high-impact or time-sensitive deliveries.
- Manual quality checks and supervisor review.
- A log of decisions made during fallback.
- Backlog and recovery procedures.
- Criteria for returning to RouteAssist.

Fallback exercises will test realistic workload, staffing, timing, safety, and recovery rather than only confirming that a written procedure exists.

---

## 15. Return-to-Service Criteria

RouteAssist or an affected capability may return to service only when:

- The issue and affected scope are understood.
- Immediate harm has been contained.
- Required data, access, logging, integration, and review controls are functioning.
- Corrective actions are implemented or approved temporary safeguards exist.
- Required testing or regression testing passes.
- Residual risk is documented.
- The appropriate authority approves restoration.
- Monitoring is increased when uncertainty remains.
- A rollback or renewed suspension remains available.

Restoration authority must match incident severity and the approval requirements in the governance charter.

---

## 16. Training and Competency

Reviewers must complete training before access and at least annually thereafter.

Training must cover:

- Approved and prohibited uses.
- System capabilities and limitations.
- Data-quality and freshness indicators.
- Automation bias, confirmation bias, and time-pressure effects.
- Route safety and operational feasibility.
- Assignment fairness and cumulative worker impact.
- Privacy, sensitive data, and prohibited secondary use.
- Rationale and uncertainty interpretation.
- Approval, modification, rejection, override, and escalation.
- Stop conditions and manual fallback.
- Incident and complaint reporting.
- Non-retaliation protections.

Competency must be demonstrated through scenario-based assessment. Training attendance alone is insufficient.

---

## 17. Oversight Testing

The evaluation program will test whether reviewers can:

- Detect incorrect, unsafe, stale, incomplete, biased, or out-of-scope recommendations.
- Resist an incorrect recommendation presented with high apparent confidence.
- Identify when information is insufficient.
- Select the correct escalation route.
- Override without unnecessary delay.
- Activate manual fallback.
- Document decisions accurately.
- Perform under realistic workload and time pressure.

Testing will include normal cases, ambiguous cases, rare high-impact cases, misleading explanations, missing-data cases, repeated recommendations, and interface or system failures.

---

## 18. Oversight Metrics

| Metric | Purpose | Review frequency |
| --- | --- | --- |
| Approval, modification, rejection, and escalation rates | Identify reviewer and system behavior patterns | Weekly during pilot; monthly thereafter |
| Override rate and reasons | Detect model weaknesses, automation bias, or workarounds | Weekly during pilot; monthly thereafter |
| Review completion time | Determine whether meaningful review is operationally feasible | Weekly during pilot |
| Missed-error rate | Measure harmful recommendations approved by reviewers | Each evaluation; monthly trend |
| Correct-challenge rate | Measure reviewers' ability to detect seeded or confirmed problems | Each simulation and periodic sample |
| Escalation timeliness | Measure adherence to severity targets | Monthly |
| Documentation completeness | Support traceability and investigations | Weekly sample during pilot |
| Fallback activation and recovery time | Assess continuity readiness | Each exercise or event |
| Reviewer workload | Identify conditions that undermine meaningful oversight | Daily operational monitoring |
| Complaint and retaliation indicators | Detect affected-party harm and cultural barriers | Monthly |

Metrics must be interpreted together. For example, a near-zero override rate may indicate excellent model performance or ineffective challenge.

---

## 19. Records and Evidence

Oversight records must include, as applicable:

- Transaction identifier.
- System and model version.
- Reviewer identity and role.
- Recommendation and relevant input references.
- Data-quality and limitation indicators.
- Reviewer action and timestamp.
- Override or escalation reason.
- Supervisor decision.
- Downstream action.
- Outcome, complaint, incident, or corrective-action link.
- Fallback and restoration information.

Records must be access-controlled, protected from unauthorized alteration, and retained according to approved requirements.

---

## 20. Related Risks and Controls

| Area | Risks | Controls |
| --- | --- | --- |
| Safety and high-impact delivery | `AIR-001`, `AIR-002` | `AIC-017`, `AIC-020`, `AIC-021`, `AIC-022`, `AIC-026` |
| Automation bias and explanation | `AIR-005`, `AIR-012` | `AIC-019`, `AIC-020`, `AIC-021`, `AIC-024` |
| Workforce fairness and misuse | `AIR-004`, `AIR-006`, `AIR-018`, `AIR-019` | `AIC-004`, `AIC-018`, `AIC-020`, `AIC-025` |
| Traceability and monitoring | `AIR-014`, `AIR-015` | `AIC-023`, `AIC-024`, `AIC-030` |
| Continuity and response | `AIR-016`, `AIR-017` | `AIC-026`, `AIC-027` |
| Scope and governance | `AIR-013`, `AIR-020` | `AIC-003`, `AIC-004`, `AIC-028` |

---

## 21. NIST AI RMF Alignment

| Function | Plan contribution |
| --- | --- |
| GOVERN | Defines oversight ownership, authority, competence, non-retaliation, and accountability |
| MAP | Connects review to context, affected parties, impact, limitations, and operational conditions |
| MEASURE | Tests human performance and monitors overrides, errors, workload, complaints, and escalation |
| MANAGE | Enables approval, rejection, restriction, fallback, suspension, correction, and recovery |

---

## 22. Document Control

| Field | Value |
| --- | --- |
| Document title | Human Oversight and Escalation Plan |
| Repository path | `docs/10-human-oversight-and-escalation-plan.md` |
| Version | 1.0 |
| Status | Draft portfolio artifact |
| Owner | Dispatch Director |
| Coordinator | GRC Analyst |
| Approver | AI Governance Committee |
| Review frequency | Monthly during pilot; quarterly after stabilization; upon material trigger |
| Classification | Public fictional portfolio content |

### Version history

| Version | Date | Author | Change summary |
| --- | --- | --- | --- |
| 1.0 | 2026-09-20 | Tommy Marshall | Created the initial RouteAssist human-oversight model, review procedure, override rules, escalation paths, stop conditions, fallback criteria, and metrics. |

---

## 23. Related Documents

- [Project README](../README.md)
- [Project Overview and Methodology](00-project-overview-and-methodology.md)
- [Organization Profile and AI Use Case](01-organization-profile-and-ai-use-case.md)
- [Stakeholder and Accountability Map](02-stakeholder-and-accountability-map.md)
- [AI System Inventory and Impact Screening](03-ai-system-inventory-and-impact-screening.md)
- [Data Flow and System Context](04-data-flow-and-system-context.md)
- [AI Risk Assessment Methodology](05-ai-risk-assessment-methodology.md)
- [AI Risk Register](06-ai-risk-register.md)
- [AI Governance Framework Crosswalk](07-framework-crosswalk.md)
- [AI Governance Charter](08-ai-governance-charter.md)
- [AI Control Matrix](09-ai-control-matrix.md)
- [AI Evaluation and Testing Plan](11-ai-evaluation-and-testing-plan.md)
- [Monitoring, Metrics, and Reporting Plan](12-monitoring-metrics-and-reporting-plan.md)
- [AI Incident Response Plan](13-ai-incident-response-plan.md)
- [Gap Assessment and POA&M](15-gap-assessment-and-poam.md)

---

## 24. Portfolio Notice

This plan is part of an educational portfolio project based on a fictional organization and fictional AI system. The roles, response targets, procedures, metrics, and evidence are illustrative.

This document does not establish compliance, legal sufficiency, system safety, emergency authority, or independent assurance for a real organization.
