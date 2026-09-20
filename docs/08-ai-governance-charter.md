# AI Governance Charter

## PLG RouteAssist

**Organization:** Peachtree Logistics Group (fictional)  
**AI system:** PLG RouteAssist  
**System identifier:** `AI-SYS-001`  
**Use-case identifier:** `UC-001`  
**Charter owner:** AI Governance Committee  
**Executive sponsor:** Chief Operating Officer  
**Document coordinator:** GRC Analyst  
**Document status:** Draft portfolio artifact  
**Version:** 1.0  
**Effective date:** Upon approval  
**Review frequency:** At least annually and upon material change

---

## 1. Charter Purpose

This charter establishes the authority, membership, responsibilities, decision rights, meeting practices, escalation paths, and documentation requirements for governing PLG RouteAssist.

The charter is designed to ensure that AI-related decisions are:

- Accountable and traceable.
- Proportionate to risk and potential impact.
- Informed by business, technical, security, privacy, legal, workforce, and affected-party perspectives.
- Supported by documented evidence.
- Subject to meaningful human oversight.
- Reassessed throughout the AI system lifecycle.

---

## 2. Governance Objectives

The AI Governance Committee will:

1. Protect people, operations, customers, and PLG from unacceptable AI-related harm.
2. Confirm that RouteAssist remains within its approved purpose and scope.
3. Establish risk tolerance, approval gates, and accountability.
4. Review material risks, controls, evidence, exceptions, incidents, and changes.
5. Require effective human oversight and accessible escalation.
6. Govern vendor, data, model, integration, and lifecycle dependencies.
7. Promote transparent, fair, secure, private, reliable, and safe use.
8. Maintain alignment with the NIST AI Risk Management Framework.
9. Ensure that unresolved gaps are assigned and tracked.
10. Authorize, restrict, suspend, or discontinue RouteAssist use when warranted.

---

## 3. Scope

This charter applies to:

- RouteAssist design, procurement, configuration, testing, pilot, operation, monitoring, change, incident response, and retirement.
- Routing, delivery-prioritization, and driver or courier assignment recommendations.
- Source data, derived data, models, rules, interfaces, integrations, logs, reports, and feedback.
- PLG employees, independent couriers, contractors, vendors, and other parties who develop, administer, use, supervise, evaluate, or are affected by RouteAssist.
- Material changes to purpose, capability, autonomy, data, model, vendor, geography, service type, affected population, or downstream action.

This charter does not authorize RouteAssist for any use that has not completed the required assessment and approval process.

---

## 4. Governing Principles

| Principle | Governance expectation |
| --- | --- |
| Human accountability | A named person or governance body remains accountable for every consequential decision |
| Advisory-only operation | RouteAssist recommendations do not execute dispatch decisions without authorized human review |
| Proportionality | Oversight, testing, evidence, and approval increase with potential impact |
| Safety first | Safety and time-sensitive delivery concerns take priority over efficiency targets |
| Fairness | PLG evaluates whether assignment outcomes create unjustified disparities or cumulative worker harm |
| Privacy and minimization | Only necessary, approved data may be processed for defined purposes |
| Security and resilience | Access, integrations, logs, dependencies, fallback, and recovery must be protected and tested |
| Transparency | Users receive relevant information about AI involvement, rationale, uncertainty, limitations, and options |
| Effective challenge | Personnel may question, override, escalate, or stop use without retaliation when acting in good faith |
| Traceability | Material inputs, versions, recommendations, reviews, overrides, actions, and outcomes are recorded |
| Lifecycle governance | Approval is conditional and may be revised when evidence, context, or risk changes |

---

## 5. Governance Structure

### 5.1 Executive sponsor

The Chief Operating Officer serves as executive sponsor and:

- Provides organizational authority and resources.
- Resolves conflicts that exceed committee authority.
- Approves acceptance of qualifying High residual risks.
- Approves any future medical-delivery use after committee recommendation.
- May order immediate restriction or suspension.

### 5.2 AI Governance Committee

The AI Governance Committee is the primary cross-functional decision body for RouteAssist.

#### Voting members

| Role ID | Role | Primary governance responsibility |
| --- | --- | --- |
| `ROLE-002` | AI Governance Committee Chair | Leads meetings, confirms decisions, and escalates unresolved matters |
| `ROLE-004` | Dispatch Director | Owns operational use, safety, human oversight, and dispatch outcomes |
| `ROLE-005` | CIO / IT Director | Owns architecture, integrations, availability, access administration, and technical change |
| `ROLE-006` | Data / AI Lead | Owns data and model evaluation, limitations, drift, and technical monitoring |
| `ROLE-007` | Information Security Lead | Owns security risk, threat assessment, logging protection, and security incident input |
| `ROLE-008` | Legal / Privacy Advisor | Advises on legal, privacy, contractual, notice, and affected-party obligations |
| `ROLE-013` | Human Resources Manager | Represents employee impacts, training, workplace use restrictions, and worker disputes |

#### Standing non-voting participants

| Role ID | Role | Contribution |
| --- | --- | --- |
| `ROLE-003` | GRC Analyst | Coordinates agenda, risk records, evidence, minutes, actions, and framework alignment |
| `ROLE-009` | Procurement / Vendor Manager | Provides vendor due diligence, contracts, service performance, and change information |
| `ROLE-012` | Operations Manager | Provides field operations, continuity, and implementation input |
| `ROLE-014` | Customer Service Manager | Provides complaint, customer-impact, and dispute trends |
| `ROLE-015` | Internal Audit / Assurance | Provides independent challenge and assurance when assigned |
| `ROLE-016` | Business Continuity / Incident Manager | Coordinates incident, continuity, crisis, and recovery input |

Subject-matter experts, frontline users, worker representatives, vendors, or affected-party representatives may be invited when relevant. Vendor participation does not replace PLG accountability.

---

## 6. Committee Authority

The committee is authorized to:

- Approve, conditionally approve, defer, restrict, or reject lifecycle advancement.
- Define approved and prohibited uses.
- Require additional assessment, testing, monitoring, training, or evidence.
- Assign risk and control owners.
- Create or escalate corrective actions and POA&M items.
- Require temporary restriction, rollback, manual fallback, or suspension.
- Review and approve Moderate residual-risk acceptance within delegated authority.
- Recommend High residual-risk acceptance to the authorized executive.
- Reject any risk acceptance unsupported by evidence.
- Require vendor remediation, contractual protection, or replacement.
- Request independent review or audit.
- Reopen prior decisions when assumptions, evidence, or conditions change.

The committee may not waive applicable law, contractual commitments, safety requirements, or executive authority.

---

## 7. Decision Rights

| Decision | Recommends | Reviews | Final authority |
| --- | --- | --- | --- |
| Approve initial assessment scope | GRC Analyst and Dispatch Director | AI Governance Committee | Committee Chair |
| Approve intended and prohibited uses | Dispatch Director | Legal/Privacy, HR, Security, Data/AI | AI Governance Committee |
| Approve vendor selection | Procurement / Vendor Manager | IT, Security, Legal/Privacy, Data/AI | Authorized procurement executive |
| Approve evaluation plan and thresholds | Data / AI Lead | GRC, Dispatch, Security, HR, Legal/Privacy | AI Governance Committee |
| Approve limited non-medical pilot | Dispatch Director and Data / AI Lead | Full committee | AI Governance Committee |
| Approve medical-delivery use | Dispatch Director | Full committee | Chief Operating Officer |
| Accept Low residual risk | Risk owner | GRC Analyst | Risk owner within delegated authority |
| Accept Moderate residual risk | Risk owner | GRC Analyst and relevant SMEs | AI Governance Committee |
| Accept High residual risk | Risk owner | AI Governance Committee | Chief Operating Officer |
| Accept Critical residual risk | Not permitted for normal operation | AI Governance Committee | No routine acceptance; use must be avoided or reduced |
| Approve material change | Change owner | Relevant control owners and GRC | AI Governance Committee or delegated authority |
| Approve temporary emergency restriction | Incident Manager, Dispatch Director, IT Director, or Security Lead | As soon as practical | Any designated emergency authority |
| Restore service after material incident | Incident Manager and system owner | Security, Data/AI, GRC, Dispatch | AI Governance Committee or executive, based on severity |
| Retire RouteAssist | System owner | Full committee | Chief Operating Officer |

No individual may approve a decision when they are both the requester and the sole reviewer of the associated risk or control evidence.

---

## 8. Risk Appetite and Acceptance Rules

| Risk level | Governance position |
| --- | --- |
| Low | May be managed by the accountable owner with routine monitoring |
| Moderate | Requires documented treatment, evidence, committee acceptance, and periodic review |
| High | Requires executive awareness, strong justification, validated controls, defined conditions, and formal acceptance |
| Critical | Outside normal risk appetite; use must be avoided, redesigned, restricted, or suspended |

Additional rules:

- Target residual ratings are not accepted residual-risk determinations.
- Planned controls receive no effectiveness credit until implemented and tested.
- Risk acceptance must identify scope, rationale, conditions, monitoring, owner, approver, and expiration or review date.
- Acceptance expires when a material assumption, capability, data source, vendor, model, affected population, or operating context changes.
- No financial or efficiency benefit alone justifies unmanaged safety, rights, privacy, security, or severe workforce harm.

---

## 9. Lifecycle Approval Gates

| Gate | Minimum evidence | Possible decision |
| --- | --- | --- |
| Gate 1 — Intake and classification | Use case, owner, purpose, affected parties, preliminary impact tier | Proceed, revise, or reject |
| Gate 2 — Design and vendor review | Architecture, data flows, requirements, vendor assessment, initial risks | Proceed with conditions, remediate, or reject |
| Gate 3 — Pre-pilot readiness | Risk register, implemented controls, test results, training, monitoring, fallback, incident readiness | Approve limited pilot, defer, or reject |
| Gate 4 — Pilot review | Pilot metrics, overrides, complaints, incidents, disparities, control evidence, lessons learned | Expand, continue, restrict, suspend, or end pilot |
| Gate 5 — Production authorization | Validated residual risks, acceptance records, operating procedures, ownership, assurance results | Approve conditionally, defer, or reject |
| Gate 6 — Material change review | Change description, impact analysis, updated risks, regression tests, rollback plan | Approve, restrict, or require full reassessment |
| Gate 7 — Retirement | Exit plan, data disposition, access removal, record retention, vendor termination, operational transition | Approve retirement and verify closure |

Medical-delivery functions are excluded from the initial pilot and require a separate Gate 3 review and executive authorization.

---

## 10. Meeting and Voting Procedures

### 10.1 Cadence

- Monthly during assessment and pilot.
- Quarterly after stabilization.
- Within 24 hours for a potentially severe AI incident when practical.
- On demand for material changes, threshold breaches, unresolved High risks, or urgent exceptions.

### 10.2 Quorum

Quorum requires:

- The Committee Chair or formally delegated alternate.
- The accountable business owner.
- At least three additional voting members.
- Participation by Security, Legal/Privacy, HR, or Data/AI when the decision materially affects that function.

### 10.3 Voting

- Routine decisions require a simple majority of voting members present.
- A tie is escalated to the Chief Operating Officer.
- High-risk acceptance requires executive approval regardless of committee vote.
- Critical-risk acceptance is not available for normal operation.
- Members must disclose conflicts of interest and may be recused.
- Dissenting views and unresolved concerns must be recorded.

### 10.4 Emergency action

The Incident Manager, Dispatch Director, CIO / IT Director, Information Security Lead, or Chief Operating Officer may order an immediate temporary restriction or suspension when delay could increase harm.

Emergency action must be documented and reviewed by the committee as soon as practical.

---

## 11. Human Oversight Requirements

The committee will ensure that:

- RouteAssist remains advisory unless a separately assessed and approved change is authorized.
- Reviewers can understand relevant inputs, rationale, uncertainty, limitations, and alternatives.
- Reviewers have sufficient time, authority, training, and information to challenge recommendations.
- Approval, rejection, modification, override, and escalation actions are recorded.
- Good-faith overrides and safety escalations are protected from retaliation.
- Supervisors review patterns indicating automation bias, rubber-stamping, excessive override, or inconsistent treatment.
- Manual fallback is available and exercised.
- High-impact and medical-delivery decisions receive enhanced review.

Detailed requirements are maintained in [`10-human-oversight-and-escalation-plan.md`](10-human-oversight-and-escalation-plan.md).

---

## 12. Prohibited Uses

Unless separately assessed and expressly approved, RouteAssist must not be used to:

- Make fully autonomous dispatch, routing, prioritization, or assignment decisions.
- Rank, discipline, terminate, compensate, or evaluate workers.
- Infer protected or highly sensitive characteristics.
- Use protected characteristics or unjustified proxies in assignment decisions.
- Deny services or opportunities without meaningful human review.
- Process data outside the approved field and purpose allowlist.
- Repurpose personal or operational data for unrelated model training.
- Expand to new services, populations, geographies, or downstream actions without review.
- Conceal material AI involvement from authorized reviewers.
- Bypass required logging, approval, escalation, or monitoring controls.
- Continue operation during a stop condition or formal suspension.

---

## 13. Escalation and Stop Conditions

Immediate escalation is required for:

- Actual or potential injury or severe safety impact.
- Delayed or mishandled time-sensitive medical delivery.
- Evidence of unauthorized employment or performance use.
- Material disparity or repeated harmful assignment pattern.
- Unauthorized access, data exposure, manipulation, or security compromise.
- Missing or unreliable logs that prevent decision reconstruction.
- Material vendor or model change without review.
- Performance or drift threshold breach.
- Failed human oversight, fallback, or incident-response control.
- Significant complaint pattern or inability to correct an affected outcome.
- Use outside approved scope.

Authorized responders may:

1. Pause a recommendation type.
2. Restrict affected data, users, geography, or service class.
3. Revert to manual dispatch.
4. Roll back a version or configuration.
5. Disconnect an integration.
6. Suspend RouteAssist.
7. Escalate to executive, legal, privacy, security, HR, or emergency response.

---

## 14. Documentation and Evidence

The GRC Analyst will maintain or coordinate:

- Agendas, attendance, quorum, minutes, decisions, and dissent.
- System, use-case, risk, control, evidence, metric, incident, exception, and POA&M identifiers.
- Approval conditions and expiration dates.
- Risk acceptance records.
- Evaluation results and control tests.
- Vendor reviews and material-change notices.
- Training and exercise records.
- Complaints, disputes, corrective actions, and lessons learned.
- Version history for governance artifacts.

Records must be accurate, access-controlled, retained according to approved requirements, and sufficient to reconstruct material decisions.

---

## 15. Reporting

The committee will receive reporting appropriate to the lifecycle stage, including:

- Open risks by rating and owner.
- Overdue control and POA&M actions.
- Evaluation results and failed thresholds.
- Data-quality, performance, fairness, security, privacy, and resilience metrics.
- Human-review, override, escalation, and fallback trends.
- Complaints, disputes, incidents, and near misses.
- Vendor performance and material changes.
- Exceptions and expiring risk acceptances.
- Decisions required from leadership.

Severe events and stop conditions are reported immediately rather than waiting for the next scheduled meeting.

---

## 16. Conflicts, Exceptions, and Non-Retaliation

- Members must disclose actual or perceived conflicts of interest.
- Exceptions must identify the requirement, rationale, scope, compensating controls, risk, owner, approver, and expiration date.
- Permanent exceptions are discouraged; recurring exceptions require root-cause review.
- Personnel may report concerns, challenge recommendations, refuse unsafe actions, and escalate suspected misuse in good faith without retaliation.
- Alleged retaliation is escalated to Human Resources and the Committee Chair.

---

## 17. Charter Review and Amendment

This charter will be reviewed:

- At least annually.
- Before production authorization.
- After a severe incident or significant control failure.
- When laws, contracts, frameworks, organizational responsibilities, or risk tolerance change.
- When RouteAssist undergoes a material change.

Amendments require committee approval and executive approval when they alter executive authority, risk appetite, or High-risk acceptance.

---

## 18. NIST AI RMF Alignment

| Function | Charter contribution |
| --- | --- |
| GOVERN | Establishes authority, accountability, policy expectations, risk tolerance, roles, third-party oversight, and documentation |
| MAP | Requires context, affected-party, impact, scope, and material-change review |
| MEASURE | Requires evidence, evaluation, monitoring, human-factor testing, and independent challenge |
| MANAGE | Establishes prioritization, treatment, approval, acceptance, restriction, suspension, incident, and recovery authority |

Detailed mappings are maintained in [`07-framework-crosswalk.md`](07-framework-crosswalk.md).

---

## 19. Approval

| Approval role | Name or title | Decision | Date |
| --- | --- | --- | --- |
| Executive sponsor | Chief Operating Officer | Pending | — |
| Committee Chair | AI Governance Committee Chair | Pending | — |
| Business owner | Dispatch Director | Pending | — |
| Technology owner | CIO / IT Director | Pending | — |
| Document coordinator | GRC Analyst | Prepared | 2026-09-20 |

This charter becomes effective only after the required approvals are documented.

---

## 20. Document Control

| Field | Value |
| --- | --- |
| Document title | AI Governance Charter |
| Repository path | `docs/08-ai-governance-charter.md` |
| Version | 1.0 |
| Status | Draft portfolio artifact |
| Owner | AI Governance Committee |
| Coordinator | GRC Analyst |
| Approver | Chief Operating Officer |
| Review frequency | At least annually and upon material change |
| Classification | Public fictional portfolio content |

### Version history

| Version | Date | Author | Change summary |
| --- | --- | --- | --- |
| 1.0 | 2026-09-20 | Tommy Marshall | Created the initial RouteAssist governance charter, committee structure, authority, lifecycle gates, risk acceptance rules, and escalation requirements. |

---

## 21. Related Documents

- [Project README](../README.md)
- [Project Overview and Methodology](00-project-overview-and-methodology.md)
- [Organization Profile and AI Use Case](01-organization-profile-and-ai-use-case.md)
- [Stakeholder and Accountability Map](02-stakeholder-and-accountability-map.md)
- [AI System Inventory and Impact Screening](03-ai-system-inventory-and-impact-screening.md)
- [Data Flow and System Context](04-data-flow-and-system-context.md)
- [AI Risk Assessment Methodology](05-ai-risk-assessment-methodology.md)
- [AI Risk Register](06-ai-risk-register.md)
- [AI Governance Framework Crosswalk](07-framework-crosswalk.md)
- [AI Control Matrix](09-ai-control-matrix.md)
- [Human Oversight and Escalation Plan](10-human-oversight-and-escalation-plan.md)
- [AI Evaluation and Testing Plan](11-ai-evaluation-and-testing-plan.md)
- [Monitoring, Metrics, and Reporting Plan](12-monitoring-metrics-and-reporting-plan.md)
- [AI Incident Response Plan](13-ai-incident-response-plan.md)
- [Gap Assessment and POA&M](15-gap-assessment-and-poam.md)

---

## 22. Portfolio Notice

This charter is part of an educational portfolio project based on a fictional organization and fictional AI system. The governance structure, roles, decision rights, and approval records are illustrative.

This document does not establish legal authority, regulatory compliance, certification, independent assurance, or approval for a real AI system.
