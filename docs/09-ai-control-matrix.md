# AI Control Matrix

## PLG RouteAssist

**Organization:** Peachtree Logistics Group (fictional)  
**AI system:** PLG RouteAssist  
**System identifier:** `AI-SYS-001`  
**Use-case identifier:** `UC-001`  
**Document owner:** GRC Analyst  
**Approval authority:** AI Governance Committee  
**Assessment stage:** Predeployment  
**Document status:** Draft portfolio artifact  
**Version:** 1.0  
**Review frequency:** Monthly during assessment and pilot; quarterly after stabilization; upon material change

---

## 1. Purpose

This matrix defines the governance, operational, technical, human-oversight, vendor, monitoring, and incident controls planned for PLG RouteAssist.

It connects each control to:

- Identified AI risks.
- Accountable owners.
- Control type and frequency.
- Required implementation evidence.
- Testing procedures.
- NIST AI RMF functions.
- Current implementation and effectiveness status.

The matrix is the central control-design and assurance record for the project.

---

## 2. Control Status and Evidence Notice

RouteAssist remains in a fictional predeployment stage. Controls in this matrix are control designs, not claims of operating effectiveness.

Unless verified evidence states otherwise:

- Implementation status is **Planned**.
- Design effectiveness is **Not tested**.
- Operating effectiveness is **Not tested**.
- Planned controls do not reduce the current risk score.
- Target residual risk remains a planning objective.

### 2.1 Status definitions

| Status | Meaning |
| --- | --- |
| Planned | Control is documented but not implemented |
| In progress | Implementation has started but is incomplete |
| Implemented | Control has been deployed and evidence exists |
| Design effective | Control design reasonably addresses the stated risk |
| Operating effective | Testing shows the control operated consistently during the review period |
| Deficient | Control design or operation does not sufficiently address the risk |
| Not applicable | Control is not relevant based on documented scope and rationale |

### 2.2 Control-type definitions

| Type | Purpose |
| --- | --- |
| Preventive | Reduces the likelihood of an unwanted event |
| Detective | Identifies an event, failure, or harmful pattern |
| Corrective | Limits harm, restores operations, or prevents recurrence |
| Directive | Establishes required behavior, authority, or process |

---

## 3. Control Summary

| Control ID | Control title | Type | Owner | Frequency | Status |
| --- | --- | --- | --- | --- | --- |
| `AIC-001` | AI inventory and use-case registration | Directive / Preventive | GRC Analyst | At intake; annual; upon change | Planned |
| `AIC-002` | Impact screening and risk-tier assignment | Preventive | GRC Analyst | At intake and material change | Planned |
| `AIC-003` | Governance approval gates | Directive / Preventive | AI Governance Committee | Each lifecycle gate | Planned |
| `AIC-004` | Approved-use and prohibited-use enforcement | Preventive | Dispatch Director | Continuous; quarterly review | Planned |
| `AIC-005` | Risk assessment and treatment tracking | Directive / Corrective | GRC Analyst | Monthly; upon trigger | Planned |
| `AIC-006` | Segregation of duties and decision authority | Preventive | AI Governance Committee | Each approval; annual review | Planned |
| `AIC-007` | Data inventory, lineage, and ownership | Directive / Preventive | Data / AI Lead | Before use; upon change | Planned |
| `AIC-008` | Data minimization and purpose limitation | Preventive | Dispatch Director | Before use; quarterly review | Planned |
| `AIC-009` | Input validation and freshness controls | Preventive / Detective | Data / AI Lead | Each transaction; continuous | Planned |
| `AIC-010` | Sensitive-data and free-text restrictions | Preventive | Legal / Privacy Advisor | Continuous; quarterly review | Planned |
| `AIC-011` | Role-based access and multifactor authentication | Preventive | Information Security Lead | Continuous; quarterly review | Planned |
| `AIC-012` | Privileged-access governance | Preventive / Detective | Information Security Lead | Each request; quarterly review | Planned |
| `AIC-013` | Integration security and integrity validation | Preventive / Detective | Information Security Lead | Continuous; upon change | Planned |
| `AIC-014` | Vendor due diligence and contracting | Preventive / Directive | Procurement / Vendor Manager | Before contract; annually | Planned |
| `AIC-015` | Vendor and model change notification | Preventive / Detective | Procurement / Vendor Manager | Continuous; each change | Planned |
| `AIC-016` | Predeployment evaluation and acceptance thresholds | Preventive / Detective | Data / AI Lead | Before pilot and production | Planned |
| `AIC-017` | Safety and high-impact scenario testing | Preventive / Detective | Dispatch Director | Before approval; after change | Planned |
| `AIC-018` | Fairness and assignment-outcome testing | Detective / Corrective | Data / AI Lead | Before pilot; monthly during pilot | Planned |
| `AIC-019` | Explanation and uncertainty requirements | Preventive / Directive | Data / AI Lead | Each recommendation | Planned |
| `AIC-020` | Mandatory human review and override | Preventive | Dispatch Director | Each recommendation | Planned |
| `AIC-021` | Human-review competency and simulation | Preventive / Detective | Dispatch Director | Before access; annually | Planned |
| `AIC-022` | Enhanced review for high-impact deliveries | Preventive | Dispatch Director | Each applicable delivery | Planned |
| `AIC-023` | Decision, version, and audit logging | Detective | CIO / IT Director | Continuous | Planned |
| `AIC-024` | Performance, drift, and harmful-pattern monitoring | Detective / Corrective | Data / AI Lead | Continuous; monthly review | Planned |
| `AIC-025` | Complaint, dispute, and correction process | Detective / Corrective | Customer Service Manager | Continuous; monthly review | Planned |
| `AIC-026` | Manual fallback and continuity readiness | Corrective | CIO / IT Director | Before pilot; semiannually | Planned |
| `AIC-027` | AI incident response and evidence preservation | Corrective | Incident Manager | Continuous; annual exercise | Planned |
| `AIC-028` | Material-change and revalidation process | Preventive / Directive | AI Governance Committee | Each material change | Planned |
| `AIC-029` | Retention, deletion, and decommissioning | Preventive / Corrective | CIO / IT Director | Per schedule; at retirement | Planned |
| `AIC-030` | Independent assurance and corrective-action tracking | Detective / Corrective | Internal Audit / Assurance | Risk-based; at least annually | Planned |

---

## 4. Detailed Control Matrix

| ID | Control objective and required activity | Risks addressed | Evidence | Test procedure | NIST AI RMF |
| --- | --- | --- | --- | --- | --- |
| `AIC-001` | Maintain a complete inventory record for RouteAssist containing owner, purpose, capabilities, users, affected parties, data, vendor, impact tier, lifecycle stage, approvals, and retirement status. Unregistered AI use is prohibited. | `AIR-013`, `AIR-020` | Approved inventory record, annual review, change history | Inspect required fields; trace a sample of known capabilities and integrations to the inventory; search for unregistered use | GOVERN, MAP |
| `AIC-002` | Screen the use case for safety, rights, workforce, privacy, security, financial, legal, operational, and reputational impacts. Assign and approve an impact tier before development, procurement, pilot, or material change. | `AIR-001`, `AIR-004`, `AIR-006`, `AIR-007`, `AIR-013` | Completed screening, rationale, approval, reassessment records | Reperform the tier using approved criteria; verify severe impacts were not averaged away | GOVERN, MAP |
| `AIC-003` | Require documented approval at intake, design, pre-pilot, pilot review, production, material change, and retirement gates. Failed conditions block lifecycle advancement. | `AIR-013`, `AIR-020` | Gate checklist, evidence package, minutes, approval or rejection | Sample gate decisions; verify quorum, evidence, conditions, authority, and closure of blockers | GOVERN, MANAGE |
| `AIC-004` | Configure and communicate approved uses, prohibited uses, service boundaries, data boundaries, and autonomy limits. Periodically review actual use against approval. | `AIR-001`, `AIR-006`, `AIR-013` | Policy, configuration, user acknowledgment, usage review, exception log | Inspect settings and reports; interview users; test whether prohibited functions are blocked or detected | GOVERN, MAP, MANAGE |
| `AIC-005` | Maintain a risk register with cause-event-impact statements, ratings, uncertainty, owners, treatments, controls, evidence, milestones, target residual risk, and triggers. | All `AIR-*` risks | Risk register, review history, acceptance records, POA&M links | Sample risks; recalculate ratings; verify owners, evidence, treatment progress, and overdue escalation | GOVERN, MAP, MANAGE |
| `AIC-006` | Separate request, implementation, testing, approval, risk acceptance, and administrative responsibilities where conflicts could undermine independent challenge. | `AIR-006`, `AIR-008`, `AIR-013`, `AIR-020` | RACI, access roles, approval workflow, conflict disclosures | Sample changes and approvals; confirm no requester served as sole approver or sole effectiveness tester | GOVERN, MANAGE |
| `AIC-007` | Document approved data elements, sources, owners, classifications, lineage, transformations, destinations, retention, and known quality limitations. | `AIR-003`, `AIR-007`, `AIR-019` | Data dictionary, lineage diagram, owner approvals, quality profile | Trace sampled fields from source through output and logs; verify ownership and transformation records | MAP, MEASURE |
| `AIC-008` | Limit collection, transfer, storage, display, and reuse to data necessary for an approved purpose. Secondary use requires privacy and governance review. | `AIR-006`, `AIR-007`, `AIR-019` | Field allowlist, necessity assessment, privacy review, vendor terms | Compare actual payloads and reports with the allowlist; inspect secondary-use requests | GOVERN, MAP, MANAGE |
| `AIC-009` | Validate schema, type, range, completeness, conflict, duplication, plausibility, source, and freshness before generating a recommendation. Block or flag data outside approved rules. | `AIR-001`, `AIR-002`, `AIR-003`, `AIR-009` | Validation rules, rejected-input logs, freshness dashboard, test results | Submit valid, missing, stale, conflicting, and malformed inputs; verify expected handling and alerts | MEASURE, MANAGE |
| `AIC-010` | Restrict sensitive data and unstructured free text. Prevent unnecessary PHI, worker details, credentials, or confidential notes from entering prompts, outputs, or vendor systems. | `AIR-006`, `AIR-007`, `AIR-008` | Filtering rules, user guidance, privacy tests, incident records | Test prohibited values and free-text scenarios; inspect sampled transactions and false-negative handling | GOVERN, MEASURE, MANAGE |
| `AIC-011` | Require named accounts, MFA, least privilege, role-based access, timely provisioning and removal, session protection, and periodic access review. | `AIR-006`, `AIR-007`, `AIR-008` | Access matrix, MFA settings, approvals, review results, termination tests | Sample users across roles; verify access matches job need; test removal and authentication controls | GOVERN, MEASURE, MANAGE |
| `AIC-012` | Restrict privileged roles; require approval, separate administration from routine use, log privileged activity, and review anomalous or emergency access. | `AIR-008`, `AIR-009`, `AIR-014` | Privileged-user list, approvals, administrative logs, review tickets | Sample administrative actions and accounts; verify authorization, logging, review, and removal | GOVERN, MEASURE, MANAGE |
| `AIC-013` | Protect APIs and integrations with strong authentication, encryption, secrets management, schema validation, integrity controls, replay protection, rate limits, monitoring, and change control. | `AIR-002`, `AIR-003`, `AIR-008`, `AIR-009`, `AIR-016` | Architecture, configuration, secrets review, interface tests, alerts | Test unauthorized, altered, replayed, malformed, and excessive requests; verify safe failure and alerts | MEASURE, MANAGE |
| `AIC-014` | Complete risk-based vendor review and contract requirements covering security, privacy, performance, model documentation, data use, subprocessors, incidents, audit evidence, service levels, continuity, and exit. | `AIR-007`, `AIR-009`, `AIR-010`, `AIR-016`, `AIR-017` | Questionnaire, risk decision, contract, reports, remediation | Inspect due diligence and signed terms; verify identified gaps were resolved, accepted, or tracked | GOVERN, MAP, MANAGE |
| `AIC-015` | Require identifiable model and service versions, advance notice of material changes, impact information, PLG review, regression testing, and rollback or rejection rights. | `AIR-010`, `AIR-011`, `AIR-013`, `AIR-019` | Version inventory, change notices, impact assessments, approvals | Sample vendor changes; trace notice through assessment, testing, decision, deployment, and rollback readiness | GOVERN, MEASURE, MANAGE |
| `AIC-016` | Define evaluation questions, datasets, scenarios, methods, metrics, slices, thresholds, reviewers, limitations, and approval rules before testing. Failed mandatory thresholds block deployment. | `AIR-002`, `AIR-003`, `AIR-004`, `AIR-011`, `AIR-012`, `AIR-015` | Approved test plan, dataset record, results, sign-off | Review reproducibility; rerun a sample; verify thresholds were set before results and failures were not waived informally | MEASURE, MANAGE |
| `AIC-017` | Test unsafe routes, impossible routes, stale conditions, severe weather, vehicle constraints, urgent delivery, medical scenarios, system failure, adversarial input, and rare combinations. | `AIR-001`, `AIR-002`, `AIR-003`, `AIR-009`, `AIR-016` | Scenario library, expected results, defects, retest evidence | Execute representative normal, edge, high-impact, misuse, and failure scenarios; verify stop behavior | MAP, MEASURE, MANAGE |
| `AIC-018` | Measure assignment outcomes across relevant worker groups and operational slices, including workload, opportunity, distance, undesirable routes, earnings proxies, overrides, and complaints. Investigate material disparities. | `AIR-004`, `AIR-006`, `AIR-015`, `AIR-018`, `AIR-019` | Slice definitions, analysis, threshold approvals, investigation records | Recalculate selected metrics; assess sample size and confounders; trace threshold breaches to action | MAP, MEASURE, MANAGE |
| `AIC-019` | Present material inputs, recommendation basis, uncertainty, limitations, data freshness, conflicts, and available reviewer actions without unsupported certainty or misleading precision. | `AIR-005`, `AIR-012`, `AIR-018` | Interface requirements, screenshots, usability results, content review | Observe users interpreting outputs; test ambiguous cases; verify limitations and uncertainty remain visible | MAP, MEASURE |
| `AIC-020` | Require an authorized human to review, approve, reject, modify, or escalate each recommendation before downstream execution. Capture the action and rationale appropriate to risk. | `AIR-001`, `AIR-002`, `AIR-004`, `AIR-005`, `AIR-012` | Workflow configuration, review logs, override records, supervisor samples | Attempt to bypass review; sample decisions; verify identity, timestamps, rationale, authority, and downstream match | GOVERN, MEASURE, MANAGE |
| `AIC-021` | Train and assess reviewers on purpose, limits, data quality, automation bias, fairness, safety, privacy, escalation, override, stop conditions, and fallback under realistic time pressure. | `AIR-001`, `AIR-002`, `AIR-005`, `AIR-012`, `AIR-016` | Curriculum, attendance, assessment, simulation, remediation | Inspect content and completion; observe simulations; verify failed learners lose or do not gain access | GOVERN, MEASURE, MANAGE |
| `AIC-022` | Apply enhanced controls to high-impact deliveries, including verified priority, supervisor approval, explicit stop rules, additional logging, and heightened monitoring. Medical use remains excluded until separately authorized. | `AIR-001`, `AIR-002`, `AIR-005`, `AIR-017` | Scope restriction, rules, approval records, high-impact logs | Test classification and restricted scenarios; verify unauthorized medical use is blocked and approved use receives enhanced review | MAP, MEASURE, MANAGE |
| `AIC-023` | Record unique transaction ID, timestamp, user, input references, data freshness, system and model version, output, rationale, uncertainty, human action, override, downstream action, and outcome. Protect logs from alteration. | `AIR-008`, `AIR-009`, `AIR-014`, `AIR-017` | Log specification, samples, completeness dashboard, retention and access settings | Trace sampled decisions end to end; test completeness, time synchronization, restricted access, and tamper detection | GOVERN, MEASURE, MANAGE |
| `AIC-024` | Monitor accuracy, safety, drift, data quality, assignment outcomes, override behavior, complaints, availability, incidents, and control health using approved thresholds and accountable alerts. | `AIR-003`, `AIR-004`, `AIR-005`, `AIR-011`, `AIR-014`, `AIR-015`, `AIR-019` | Metric catalog, dashboard, alerts, investigations, governance reports | Recalculate samples; trigger test alerts; verify routing, timeliness, investigation, escalation, and closure | MEASURE, MANAGE |
| `AIC-025` | Provide accessible channels for workers, customers, and other affected parties to report, challenge, and correct RouteAssist-related outcomes without retaliation. Link cases to decision evidence and trend analysis. | `AIR-004`, `AIR-006`, `AIR-018`, `AIR-019` | Procedure, intake channels, cases, response metrics, corrections | Submit test cases; verify routing, acknowledgment, investigation, evidence linkage, response, correction, and escalation | GOVERN, MEASURE, MANAGE |
| `AIC-026` | Maintain a documented manual dispatch fallback with trained personnel, necessary access, current procedures, capacity assumptions, recovery objectives, and periodic exercises. | `AIR-001`, `AIR-002`, `AIR-016`, `AIR-017` | Continuity plan, exercise records, recovery results, actions | Conduct an outage exercise at realistic volume; measure activation, capacity, safety, recovery, and backlog handling | MEASURE, MANAGE |
| `AIC-027` | Define AI incident criteria, reporting, severity, roles, containment, suspension, evidence preservation, vendor coordination, notification, recovery validation, and lessons learned. | `AIR-001`, `AIR-008`, `AIR-009`, `AIR-014`, `AIR-017` | Incident plan, contact list, tickets, tabletop, post-incident review | Run a cross-functional scenario; verify detection, classification, authority, evidence, communications, recovery, and corrective action | GOVERN, MEASURE, MANAGE |
| `AIC-028` | Require impact assessment and reapproval for changes to purpose, autonomy, data, model, rules, vendor, interface, integration, geography, service, population, thresholds, or downstream use. | `AIR-010`, `AIR-011`, `AIR-013`, `AIR-019`, `AIR-020` | Change criteria, tickets, impact assessments, regression tests, approvals | Sample changes; verify correct classification, testing, approval, deployment control, version update, and rollback | GOVERN, MAP, MANAGE |
| `AIC-029` | Apply approved retention and deletion schedules; verify vendor deletion; remove access and integrations; preserve required records; and execute controlled decommissioning or exit. | `AIR-007`, `AIR-008`, `AIR-010`, `AIR-014`, `AIR-020` | Retention schedule, deletion logs, vendor certificate, exit checklist | Sample expired records and retired access; verify deletion, exceptions, evidence retention, and vendor completion | GOVERN, MANAGE |
| `AIC-030` | Perform risk-based independent review of governance, risk, controls, evidence, and reported outcomes. Track deficiencies through verified remediation and closure. | `AIR-014`, `AIR-015`, `AIR-017`, `AIR-020` | Audit plan, workpapers, findings, POA&M, closure tests | Inspect reviewer independence, scope, sampling, evidence, issue severity, due dates, retesting, and closure approval | GOVERN, MEASURE, MANAGE |

---

## 5. Risk-to-Control Traceability

| Risk ID | Key mitigating controls |
| --- | --- |
| `AIR-001` | `AIC-002`, `AIC-004`, `AIC-009`, `AIC-017`, `AIC-020`, `AIC-021`, `AIC-022`, `AIC-026`, `AIC-027` |
| `AIR-002` | `AIC-009`, `AIC-013`, `AIC-016`, `AIC-017`, `AIC-019`, `AIC-020`, `AIC-021`, `AIC-026` |
| `AIR-003` | `AIC-007`, `AIC-009`, `AIC-016`, `AIC-017`, `AIC-024` |
| `AIR-004` | `AIC-002`, `AIC-016`, `AIC-018`, `AIC-020`, `AIC-024`, `AIC-025` |
| `AIR-005` | `AIC-019`, `AIC-020`, `AIC-021`, `AIC-023`, `AIC-024` |
| `AIR-006` | `AIC-004`, `AIC-006`, `AIC-008`, `AIC-010`, `AIC-011`, `AIC-018`, `AIC-025` |
| `AIR-007` | `AIC-007`, `AIC-008`, `AIC-010`, `AIC-011`, `AIC-014`, `AIC-029` |
| `AIR-008` | `AIC-011`, `AIC-012`, `AIC-013`, `AIC-023`, `AIC-027`, `AIC-029` |
| `AIR-009` | `AIC-009`, `AIC-013`, `AIC-014`, `AIC-017`, `AIC-023`, `AIC-027` |
| `AIR-010` | `AIC-014`, `AIC-015`, `AIC-028`, `AIC-029` |
| `AIR-011` | `AIC-015`, `AIC-016`, `AIC-024`, `AIC-028` |
| `AIR-012` | `AIC-016`, `AIC-019`, `AIC-020`, `AIC-021` |
| `AIR-013` | `AIC-001`, `AIC-002`, `AIC-003`, `AIC-004`, `AIC-006`, `AIC-028` |
| `AIR-014` | `AIC-012`, `AIC-023`, `AIC-024`, `AIC-027`, `AIC-030` |
| `AIR-015` | `AIC-016`, `AIC-018`, `AIC-023`, `AIC-024`, `AIC-025`, `AIC-030` |
| `AIR-016` | `AIC-013`, `AIC-014`, `AIC-017`, `AIC-021`, `AIC-026`, `AIC-027` |
| `AIR-017` | `AIC-005`, `AIC-022`, `AIC-023`, `AIC-026`, `AIC-027`, `AIC-030` |
| `AIR-018` | `AIC-019`, `AIC-023`, `AIC-024`, `AIC-025` |
| `AIR-019` | `AIC-007`, `AIC-008`, `AIC-015`, `AIC-018`, `AIC-024`, `AIC-028` |
| `AIR-020` | `AIC-001`, `AIC-003`, `AIC-005`, `AIC-006`, `AIC-028`, `AIC-030` |

---

## 6. Control Testing Approach

### 6.1 Design-effectiveness review

The reviewer will determine whether the control:

- Has a clear objective and defined scope.
- Addresses the linked risk causes, events, or impacts.
- Has an accountable owner and required frequency.
- Defines inputs, activities, outputs, evidence, and escalation.
- Can operate within RouteAssist workflows and time constraints.
- Includes appropriate separation of duties.
- Covers relevant users, data, components, vendors, and affected parties.

### 6.2 Operating-effectiveness review

After implementation, the reviewer will:

1. Confirm the control was placed into operation.
2. Define the population and review period.
3. Select a risk-based sample.
4. Inspect evidence and reperform activities when practical.
5. Record exceptions and determine whether they are isolated or systemic.
6. Evaluate whether the control operated consistently and on time.
7. Link deficiencies to risks and POA&M items.
8. Retest corrective actions before closure.

### 6.3 Evidence quality criteria

Evidence should be:

- Relevant to the control objective.
- Complete for the defined period and population.
- Accurate and reproducible.
- Attributable to an authorized source.
- Time-stamped and version-controlled where appropriate.
- Protected from unauthorized alteration.
- Retained according to approved requirements.

Screenshots alone should not be relied upon when stronger configuration, log, ticket, report, or reperformance evidence is available.

---

## 7. Control Deficiency Ratings

| Severity | Description | Required response |
| --- | --- | --- |
| Critical | Control failure creates imminent or severe exposure, or required evidence cannot support safe operation | Restrict or suspend affected use; immediate executive escalation |
| High | Control is absent or materially ineffective for a High or Critical risk | Remediate before approval or obtain authorized, time-limited exception |
| Moderate | Control weakness may reduce reliability but compensating controls limit immediate exposure | Assign corrective action and monitor to closure |
| Low | Limited weakness with minor risk effect | Correct through routine control improvement |

A control deficiency may affect several risks simultaneously and must be evaluated for aggregate impact.

---

## 8. Minimum Pre-Pilot Control Set

The limited pilot must not begin until the committee verifies, at minimum:

- `AIC-001` through `AIC-005` — inventory, classification, governance, boundaries, and risk tracking.
- `AIC-007` through `AIC-010` — data governance, minimization, validation, and sensitive-data restrictions.
- `AIC-011` through `AIC-015` — access, privileged use, integrations, vendor governance, and change notice.
- `AIC-016` through `AIC-021` — evaluation, safety, fairness, transparency, human review, and competency.
- `AIC-023` through `AIC-028` — logging, monitoring, complaints, continuity, incident response, and change control.

`AIC-022` must prevent medical-delivery use during the initial pilot. If medical use is later proposed, its enhanced controls must be implemented and independently validated before approval.

---

## 9. NIST AI RMF Alignment Summary

| Function | Control application |
| --- | --- |
| GOVERN | Inventory, classification, approval, accountability, use restrictions, risk management, vendor governance, assurance |
| MAP | Context, data lineage, affected parties, impact tier, limitations, high-impact scenarios, change analysis |
| MEASURE | Validation, evaluation, security testing, fairness testing, human-factor testing, logging, monitoring, feedback |
| MANAGE | Treatment, approval gates, human review, restriction, fallback, incident response, corrective action, retirement |

Detailed framework mappings are maintained in [`07-framework-crosswalk.md`](07-framework-crosswalk.md).

---

## 10. Matrix Maintenance

The GRC Analyst will coordinate updates when:

- A risk, control, owner, system component, data source, vendor, metric, or framework mapping changes.
- A control is implemented, tested, found deficient, replaced, or retired.
- An incident, complaint, override pattern, evaluation result, or audit finding affects control design.
- A POA&M item is opened or closed.
- RouteAssist passes through a lifecycle gate.

Control identifiers must not be reused. Retired controls remain in history with their final status and replacement reference.

---

## 11. Document Control

| Field | Value |
| --- | --- |
| Document title | AI Control Matrix |
| Repository path | `docs/09-ai-control-matrix.md` |
| Version | 1.0 |
| Status | Draft portfolio artifact |
| Owner | GRC Analyst |
| Approver | AI Governance Committee |
| Review frequency | Monthly during assessment and pilot; quarterly after stabilization; upon material change |
| Classification | Public fictional portfolio content |

### Version history

| Version | Date | Author | Change summary |
| --- | --- | --- | --- |
| 1.0 | 2026-09-20 | Tommy Marshall | Created the initial RouteAssist control matrix with 30 controls, risk traceability, evidence requirements, and test procedures. |

---

## 12. Related Documents

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
- [Human Oversight and Escalation Plan](10-human-oversight-and-escalation-plan.md)
- [AI Evaluation and Testing Plan](11-ai-evaluation-and-testing-plan.md)
- [Monitoring, Metrics, and Reporting Plan](12-monitoring-metrics-and-reporting-plan.md)
- [AI Incident Response Plan](13-ai-incident-response-plan.md)
- [Gap Assessment and POA&M](15-gap-assessment-and-poam.md)

---

## 13. Portfolio Notice

This matrix is part of an educational portfolio project based on a fictional organization and fictional AI system. The controls, statuses, evidence, tests, and mappings are illustrative.

This document does not demonstrate that any control has been implemented or tested and does not establish compliance, certification, legal sufficiency, system safety, or independent assurance.
