# AI Governance Framework Crosswalk

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
**Primary framework:** NIST AI Risk Management Framework 1.0

---

## 1. Purpose

This crosswalk maps the RouteAssist governance program, identified risks, planned controls, and evidence to recognized AI governance frameworks and principles.

It is intended to:

- Demonstrate traceability between the project artifacts and external guidance.
- Identify where one control supports multiple framework outcomes.
- Reduce duplicate governance work.
- Support control design, evaluation, reporting, and future assurance activities.
- Highlight gaps that require remediation before pilot or production approval.

This document is not a certification, legal opinion, or claim of conformity.

---

## 2. Frameworks Included

| Framework | Role in this project | Application |
| --- | --- | --- |
| NIST AI RMF 1.0 | Primary organizing framework | Structures AI risk activities through GOVERN, MAP, MEASURE, and MANAGE |
| NIST AI RMF Playbook | Implementation guidance | Informs suggested actions and evidence for AI RMF outcomes |
| ISO/IEC 42001:2023 | Management-system reference | Supports governance, policy, objectives, roles, risk processes, operational controls, evaluation, and improvement |
| ISO/IEC 23894:2023 | AI risk-management reference | Supports risk identification, analysis, evaluation, treatment, monitoring, and communication |
| OECD AI Principles | Responsible-AI principles reference | Supports human-centered values, transparency, robustness, accountability, and inclusive outcomes |

Framework descriptions and mappings are paraphrased for portfolio use. Organizations must obtain and interpret authoritative standards applicable to their environment.

---

## 3. Crosswalk Method

The crosswalk uses the following relationship types:

| Relationship | Meaning |
| --- | --- |
| Direct | The PLG activity or control is designed primarily to address the framework outcome |
| Supporting | The activity contributes to the outcome but is not sufficient by itself |
| Planned | The activity has been designed but not implemented or validated |
| Gap | Required capability or evidence is absent, incomplete, or unverified |

Crosswalk entries do not establish compliance. A framework outcome is considered supported only when the related control is implemented, operating, and backed by sufficient evidence.

---

## 4. NIST AI RMF Function-Level Mapping

| Function | RouteAssist application | Primary artifacts | Key risks addressed |
| --- | --- | --- | --- |
| GOVERN | Establish policies, accountability, risk tolerance, inventory, third-party governance, and oversight | Stakeholder map, governance charter, risk methodology, risk register, control matrix | `AIR-006`, `AIR-010`, `AIR-013`, `AIR-020` |
| MAP | Define context, purpose, affected parties, impacts, dependencies, boundaries, and risk assumptions | Organization profile, use case, system inventory, impact screening, data flow and context | `AIR-001` through `AIR-007`, `AIR-010`, `AIR-013`, `AIR-019` |
| MEASURE | Evaluate technical performance, fairness, privacy, security, explainability, human oversight, and uncertainty | Risk register, evaluation plan, metrics plan, evidence records | `AIR-002` through `AIR-005`, `AIR-009`, `AIR-011`, `AIR-012`, `AIR-014`, `AIR-015`, `AIR-019` |
| MANAGE | Prioritize risks, implement treatment, restrict use, respond to incidents, monitor residual risk, and govern changes | Risk register, control matrix, oversight plan, incident plan, POA&M | All registered risks, with priority on `AIR-001`, `AIR-002`, `AIR-009`, and `AIR-017` |

---

## 5. Detailed NIST AI RMF Crosswalk

### 5.1 GOVERN

| AI RMF outcome | RouteAssist implementation | Related artifacts or evidence | Status |
| --- | --- | --- | --- |
| `GOVERN 1.1` — Legal and regulatory requirements are understood and managed | Legal and Privacy Advisor reviews privacy, employment, contractual, and sector obligations | Legal register, privacy review, vendor terms, governance minutes | Planned |
| `GOVERN 1.2` — Trustworthy-AI characteristics are integrated into policies and processes | Governance program addresses validity, safety, security, resilience, accountability, transparency, explainability, privacy, and fairness | Governance charter, control matrix, evaluation plan | Planned |
| `GOVERN 1.3` — Risk processes and documentation are maintained | Stable identifiers connect systems, risks, controls, evidence, metrics, incidents, and remediation | `AI-SYS-001`, `UC-001`, `AIR-*`, future `AIC-*` and `POAM-*` records | Direct / Planned |
| `GOVERN 1.4` — Risk tolerance is established and communicated | Critical and High risks require defined approval; prohibited uses and pilot boundaries are documented | Risk methodology, risk register, governance charter | Planned |
| `GOVERN 1.5` — Ongoing monitoring and review are established | Monthly pilot review, quarterly stabilized review, and trigger-based reassessment are required | Monitoring plan, committee minutes, reassessment records | Planned |
| `GOVERN 1.6` — AI systems are inventoried | RouteAssist is registered as `AI-SYS-001` with purpose, owner, scope, impact tier, and lifecycle status | AI system inventory and impact screening | Direct |
| `GOVERN 1.7` — Decommissioning and safe retirement are addressed | Exit, data return/deletion, access removal, record retention, and fallback requirements will be documented | Vendor terms, decommission checklist, records schedule | Gap |
| `GOVERN 2.1` — Roles and responsibilities are documented | A RACI and decision-rights model assigns accountability across business, technical, security, privacy, HR, vendor, and assurance roles | Stakeholder and accountability map | Direct |
| `GOVERN 2.2` — Personnel receive appropriate training | Dispatchers, supervisors, administrators, incident responders, and control owners receive role-based training | Training plan, completion records, exercises | Planned |
| `GOVERN 2.3` — Executive leadership is accountable | COO sponsors the program; AI Governance Committee reviews risk and approval decisions | Charter, approval records, meeting minutes | Planned |
| `GOVERN 3.1–3.2` — Workforce and culture support responsible risk decisions | Cross-functional participation, escalation, non-retaliation, and effective challenge are required | Charter, oversight plan, training and survey results | Planned |
| `GOVERN 4.1–4.3` — Organizational teams support risk management | Business, IT, AI, security, privacy, HR, procurement, incident, and audit functions have defined responsibilities | RACI, committee roster, control ownership | Direct / Planned |
| `GOVERN 5.1–5.2` — Relevant internal and external perspectives are considered | Workers, couriers, customers, recipients, healthcare clients, and vendors are included in impact and feedback processes | Affected-party register, complaints, interviews, pilot feedback | Planned |
| `GOVERN 6.1` — Third-party risks are governed | Vendor due diligence, contract protections, version notice, incident notice, service levels, and exit provisions are required | Vendor assessment, contract, assurance reports | Planned |
| `GOVERN 6.2` — Third-party issues are monitored and addressed | Vendor performance, material changes, subprocessors, incidents, and evidence gaps trigger review | Vendor dashboard, change notices, issue log | Planned |

### 5.2 MAP

| AI RMF outcome | RouteAssist implementation | Related artifacts or evidence | Status |
| --- | --- | --- | --- |
| `MAP 1.1` — Intended purpose and context are documented | RouteAssist provides advisory routing, prioritization, and assignment recommendations for dispatch operations | Organization profile and AI use case | Direct |
| `MAP 1.2` — Interdisciplinary perspectives inform risk identification | Operations, IT, AI, security, privacy, HR, procurement, customer service, incident, and assurance roles participate | Stakeholder map, workshop records | Planned |
| `MAP 1.3` — Business value and deployment context are understood | Expected benefits, operational constraints, time sensitivity, mixed workforce, and manual processes are documented | Project overview, use case, impact screening | Direct |
| `MAP 1.4` — Business processes and human interactions are mapped | Recommendation review, approval, override, escalation, downstream action, and feedback flows are defined | Data-flow and system-context document | Direct |
| `MAP 1.5` — Organizational risk tolerance is applied to context | Medical delivery, worker impact, privacy, and safety exposures receive heightened treatment | Impact screening, risk methodology, risk register | Planned |
| `MAP 1.6` — System requirements and limitations are documented | Advisory-only behavior, prohibited uses, data boundaries, human review, stop conditions, and fallback are specified | Use case, inventory, oversight plan | Planned |
| `MAP 2.1` — System categorization considers impacts | RouteAssist is classified Tier 4 because plausible medical-delivery harm can be severe | AI system inventory and impact screening | Direct |
| `MAP 2.2` — Knowledge limits and uncertainty are identified | Data, vendor behavior, human performance, rare events, drift, and affected-party impacts carry explicit uncertainty | Risk register, evaluation plan | Direct / Planned |
| `MAP 2.3` — Scientific and technical assumptions are documented | Assumptions about data quality, model performance, route sources, explanations, and monitoring require validation | Assumption log, evaluation results | Gap / Planned |
| `MAP 3.1` — Benefits and costs are examined | Efficiency and consistency benefits are balanced against safety, workforce, privacy, security, and trust impacts | Business case, impact screening, risk register | Planned |
| `MAP 3.2` — Potential costs include non-monetary impacts | Analysis includes injury, delayed medical delivery, unequal opportunity, privacy harm, workload, and trust | Impact screening, risk register | Direct |
| `MAP 3.3` — Targeted application and affected communities are considered | Employed drivers, independent couriers, recipients, customers, and healthcare clients are separately identified | Affected-party register and fairness analysis | Planned |
| `MAP 4.1` — Risks and benefits are mapped across the lifecycle | Risks are tracked from design and procurement through pilot, operation, change, incident, and retirement | Risk register, lifecycle gates, POA&M | Planned |
| `MAP 5.1` — Likelihood and magnitude of impacts are characterized | Risks use documented 1–5 likelihood and impact scales with rationale and uncertainty | Risk methodology and risk register | Direct |
| `MAP 5.2` — Practices support regular impact assessment | Material changes, incidents, complaints, threshold breaches, and scope changes trigger reassessment | Change procedure, monitoring plan, incident plan | Planned |

### 5.3 MEASURE

| AI RMF outcome | RouteAssist implementation | Related artifacts or evidence | Status |
| --- | --- | --- | --- |
| `MEASURE 1.1` — Measurement approaches are selected for identified risks | Evaluation covers route safety, accuracy, data quality, assignment outcomes, human review, privacy, security, and resilience | Evaluation and testing plan | Planned |
| `MEASURE 1.2` — Metrics are appropriate to context and impact | Metrics are defined by service type, geography, worker group, risk tier, and operational condition | Metrics catalog and dashboard | Planned |
| `MEASURE 1.3` — Independent or objective review is considered | GRC coordinates evidence review; Internal Audit may validate selected controls and conclusions | Assurance plan, sampling results | Planned |
| `MEASURE 2.1` — Test sets, methods, and tools are documented | Normal, edge, high-impact, misuse, failure, and human-factor scenarios are specified | Test protocol, dataset record, results | Planned |
| `MEASURE 2.2` — Evaluations are repeatable and documented | Version, configuration, dataset, scenario, threshold, result, reviewer, and date are retained | Evaluation records and evidence repository | Planned |
| `MEASURE 2.3` — Performance and trustworthiness characteristics are evaluated | Accuracy, safety, fairness, privacy, security, explainability, and reliability are evaluated separately and together | Test results, red-team findings, usability study | Planned |
| `MEASURE 2.4` — Production-like conditions and human interaction are tested | Dispatcher review is tested under realistic volume, ambiguity, and time pressure | Human-oversight simulation and pilot evidence | Planned |
| `MEASURE 2.5` — System limitations are identified and communicated | Limitations and unsupported conditions appear in training, procedures, and the interface | Limitations register, interface screenshots | Planned |
| `MEASURE 2.6` — Safety and resilience are evaluated | Route edge cases, outage, degraded inputs, dependency failure, fallback, and recovery are tested | Safety tests, continuity exercise | Planned |
| `MEASURE 2.7` — Security and privacy are evaluated | Access, integration integrity, logging, minimization, retention, and vendor practices are tested | Security assessment, privacy review, log tests | Planned |
| `MEASURE 2.8` — Fairness and harmful outcomes are evaluated | Workload, opportunity, earnings proxy, distance, undesirable routes, and override patterns are compared across relevant groups | Slice analysis, HR/GRC review | Planned |
| `MEASURE 2.9` — Explainability and transparency are evaluated | Reviewers must understand recommendation basis, uncertainty, limits, and available actions | Usability testing, reviewer survey | Planned |
| `MEASURE 2.10` — Privacy risk is measured and documented | Data necessity, access, disclosure, retention, deletion, and secondary-use risks are reviewed | Privacy assessment and evidence | Planned |
| `MEASURE 2.11` — Environmental effects are considered where relevant | Hosting and computational impacts will be recorded if material to procurement or operation | Vendor documentation | Not yet assessed |
| `MEASURE 2.12` — Evaluation results inform decisions | Failed thresholds block or restrict deployment and create remediation actions | Approval gate, exception record, POA&M | Planned |
| `MEASURE 2.13` — Effectiveness of controls is assessed | Design and operating effectiveness tests are required before residual risk is accepted | Control matrix, test records | Planned |
| `MEASURE 3.1–3.3` — Risks are tracked over time | Performance, drift, override, complaint, incident, availability, and control metrics are monitored | Monitoring plan, dashboards, trend reports | Planned |
| `MEASURE 4.1–4.3` — Feedback from relevant parties is gathered | Workers, dispatchers, customers, and other affected parties can report problems and dispute outcomes | Feedback channels, case records, trend analysis | Planned |

### 5.4 MANAGE

| AI RMF outcome | RouteAssist implementation | Related artifacts or evidence | Status |
| --- | --- | --- | --- |
| `MANAGE 1.1` — Risks are prioritized using mapped and measured information | Critical and High risks receive treatment priority; medical use is excluded from the initial pilot | Risk register, treatment priorities | Direct |
| `MANAGE 1.2` — Treatment considers impacts and available resources | Controls combine avoidance, reduction, contractual transfer, monitoring, and acceptance | Risk register, control matrix, POA&M | Planned |
| `MANAGE 1.3` — Responses are approved by accountable roles | Control owners implement treatment; authorized leaders approve exceptions and residual risk | Governance charter, approval records | Planned |
| `MANAGE 2.1` — Treatment plans are documented and monitored | Each risk identifies owner, controls, evidence, milestone, target rating, and trigger | Risk register and POA&M | Direct / Planned |
| `MANAGE 2.2` — Mechanisms maximize benefits and minimize harms | Advisory-only operation, human review, stop conditions, dispute handling, and fallback constrain harm | Control matrix and oversight plan | Planned |
| `MANAGE 2.3` — Response options include restriction or disengagement | PLG may pause a capability, revert to manual dispatch, roll back a change, suspend the vendor service, or prohibit a use | Incident, change, and continuity procedures | Planned |
| `MANAGE 2.4` — Residual risk is documented | Target residual ratings are planning objectives; acceptance requires validated evidence and authorized approval | Risk methodology, register, acceptance record | Direct / Planned |
| `MANAGE 3.1` — Third-party risks are managed throughout the relationship | Due diligence, contract controls, monitoring, change notice, incident notice, and exit requirements apply | Vendor management records | Planned |
| `MANAGE 4.1` — Risk treatment is communicated to relevant parties | Owners receive assigned actions; users receive boundaries, limitations, escalation, and fallback instructions | Training, procedures, governance reporting | Planned |
| `MANAGE 4.2` — Incidents and errors are managed and communicated | AI incident criteria, severity, reporting, containment, evidence preservation, notification, and recovery are defined | AI incident response plan | Planned |

---

## 6. ISO/IEC 42001 Management-System Crosswalk

| ISO/IEC 42001 area | RouteAssist application | Primary evidence | Status |
| --- | --- | --- | --- |
| Clause 4 — Organizational context | PLG context, stakeholders, scope, dependencies, constraints, and affected parties are documented | Project overview, organization profile, stakeholder map | Documented |
| Clause 5 — Leadership | Executive sponsorship, governance authority, policy, and accountability are assigned | Governance charter, RACI, approvals | Planned |
| Clause 6 — Planning | AI risks, opportunities, objectives, treatments, and change triggers are defined | Risk methodology, risk register, POA&M | Planned |
| Clause 7 — Support | Competence, awareness, communication, resources, and controlled documentation are established | Training records, communications, document control | Planned |
| Clause 8 — Operation | Lifecycle gates, data controls, human oversight, vendor controls, testing, monitoring, and incident processes govern operation | Control matrix and operating plans | Planned |
| Clause 9 — Performance evaluation | Metrics, internal review, management review, and evidence assess program performance | Monitoring reports, audit results, committee reviews | Planned |
| Clause 10 — Improvement | Findings, incidents, nonconformities, and lessons learned create corrective actions | POA&M, corrective-action records, lessons learned | Planned |
| Annex A control themes | Policies, roles, resources, impact assessment, lifecycle, data, information for interested parties, use, and third parties are represented | Full project artifact set | Partially mapped |

PLG does not claim ISO/IEC 42001 certification or conformity. This mapping is a readiness and design aid only.

---

## 7. ISO/IEC 23894 Risk-Management Crosswalk

| Risk-management activity | RouteAssist application | Primary evidence |
| --- | --- | --- |
| Communication and consultation | Cross-functional governance and affected-party feedback | Stakeholder map, meeting records, complaint channels |
| Scope, context, and criteria | Use-case boundaries, assumptions, impact tier, likelihood and impact criteria | Project overview, inventory, risk methodology |
| Risk identification | Structured taxonomy, scenarios, data flows, impact screening, and workshops | Data-flow document, risk register |
| Risk analysis | Cause-event-impact statements, likelihood, impact, uncertainty, and interdependencies | Risk register |
| Risk evaluation | Rating bands, tolerance, escalation, acceptance authority, and prioritization | Risk methodology, governance charter |
| Risk treatment | Avoid, reduce, transfer/share, accept, restrict, or discontinue | Risk register, control matrix, POA&M |
| Monitoring and review | Metrics, alerts, periodic reviews, reassessment triggers, and assurance | Monitoring plan and review records |
| Recording and reporting | Linked identifiers, evidence, decisions, exceptions, incidents, and remediation | Repository artifacts and governance reports |

---

## 8. OECD AI Principles Crosswalk

| OECD principle | RouteAssist application | Related risks |
| --- | --- | --- |
| Inclusive growth, sustainable development, and well-being | Evaluate whether efficiency benefits create disproportionate worker, customer, recipient, or community harm | `AIR-001`, `AIR-002`, `AIR-004`, `AIR-019` |
| Human-centered values and fairness | Preserve human authority, prohibit inappropriate employment use, assess assignment outcomes, and provide dispute mechanisms | `AIR-004`, `AIR-005`, `AIR-006`, `AIR-018` |
| Transparency and explainability | Communicate AI involvement, recommendation basis, uncertainty, limitations, and review options | `AIR-005`, `AIR-012`, `AIR-018` |
| Robustness, security, and safety | Validate performance, protect integrations, monitor drift, maintain fallback, and respond to incidents | `AIR-001`, `AIR-002`, `AIR-003`, `AIR-008`, `AIR-009`, `AIR-011`, `AIR-016`, `AIR-017` |
| Accountability | Assign accountable owners, preserve evidence, require approval, and track corrective actions | `AIR-013`, `AIR-014`, `AIR-015`, `AIR-020` |

---

## 9. Risk-to-Framework Traceability

| Risk ID | Primary NIST AI RMF functions | ISO/IEC 42001 areas | OECD principles |
| --- | --- | --- | --- |
| `AIR-001` | MAP, MEASURE, MANAGE | Planning, operation, evaluation | Well-being; robustness, security, and safety |
| `AIR-002` | MAP, MEASURE, MANAGE | Operation, evaluation | Robustness, security, and safety |
| `AIR-003` | MAP, MEASURE, MANAGE | Planning, operation | Robustness, security, and safety |
| `AIR-004` | GOVERN, MAP, MEASURE, MANAGE | Context, planning, operation, evaluation | Human-centered values and fairness |
| `AIR-005` | GOVERN, MAP, MEASURE, MANAGE | Support, operation, evaluation | Human-centered values; transparency |
| `AIR-006` | GOVERN, MAP, MANAGE | Leadership, planning, operation | Human-centered values and fairness; accountability |
| `AIR-007` | GOVERN, MAP, MEASURE, MANAGE | Context, planning, operation | Human-centered values; accountability |
| `AIR-008` | GOVERN, MEASURE, MANAGE | Operation, evaluation | Robustness, security, and safety |
| `AIR-009` | MAP, MEASURE, MANAGE | Operation, evaluation, improvement | Robustness, security, and safety |
| `AIR-010` | GOVERN, MAP, MANAGE | Planning, operation, evaluation | Accountability; robustness, security, and safety |
| `AIR-011` | MAP, MEASURE, MANAGE | Operation, evaluation, improvement | Robustness, security, and safety |
| `AIR-012` | MAP, MEASURE, MANAGE | Operation, evaluation | Transparency and explainability |
| `AIR-013` | GOVERN, MAP, MANAGE | Leadership, planning, operation | Accountability |
| `AIR-014` | GOVERN, MEASURE, MANAGE | Support, operation, evaluation | Accountability |
| `AIR-015` | GOVERN, MEASURE, MANAGE | Evaluation, improvement | Accountability; robustness, security, and safety |
| `AIR-016` | MAP, MEASURE, MANAGE | Operation, evaluation | Robustness, security, and safety |
| `AIR-017` | GOVERN, MEASURE, MANAGE | Operation, improvement | Accountability; robustness, security, and safety |
| `AIR-018` | GOVERN, MAP, MEASURE, MANAGE | Context, support, evaluation, improvement | Human-centered values; transparency; accountability |
| `AIR-019` | MAP, MEASURE, MANAGE | Planning, operation, evaluation | Inclusive outcomes; fairness |
| `AIR-020` | GOVERN, MANAGE | Leadership, planning, evaluation | Accountability |

---

## 10. Priority Framework Gaps

| Gap ID | Gap | Framework relevance | Required action | Target milestone |
| --- | --- | --- | --- | --- |
| `FWG-001` | Governance charter and formal approval authority are not yet approved | GOVERN; ISO Clause 5 | Approve charter, membership, quorum, decision rights, and escalation authority | Before pilot decision |
| `FWG-002` | Legal, privacy, and contractual obligations register is incomplete | GOVERN 1.1; ISO Clauses 4 and 6 | Complete obligation analysis and assign owners | Before vendor connection |
| `FWG-003` | Vendor and model documentation is unavailable | GOVERN 6; MAP 2; MANAGE 3 | Complete due diligence and contract evidence requirements | Before contract execution |
| `FWG-004` | Evaluation datasets, thresholds, and baselines are not approved | MEASURE 1–2 | Approve evaluation protocol and acceptance thresholds | Before pilot |
| `FWG-005` | Human-oversight effectiveness has not been demonstrated | MEASURE 2; MANAGE 2 | Conduct usability and time-pressure simulations | Before pilot |
| `FWG-006` | Monitoring, feedback, and complaint mechanisms are not operational | MEASURE 3–4 | Implement dashboards, alerts, intake, ownership, and trend review | Before pilot |
| `FWG-007` | Incident response and continuity procedures have not been exercised | MANAGE 2 and 4; ISO Clauses 8–10 | Conduct tabletop and manual-fallback exercises | Before pilot |
| `FWG-008` | Decommissioning and exit requirements are incomplete | GOVERN 1.7; ISO Clauses 8 and 10 | Define data return, deletion, access removal, retention, and service exit | Before production approval |

All gaps will be transferred to the project POA&M with accountable owners, due dates, dependencies, evidence requirements, and status.

---

## 11. Crosswalk Maintenance

The GRC Analyst will review this crosswalk:

- When a framework or authoritative interpretation changes.
- When the RouteAssist use case, impact tier, architecture, data, vendor, or affected parties change.
- When a control, risk, evaluation, incident, or POA&M item materially changes.
- Before pilot and production approval.
- At least annually after stabilization.

Updates must preserve traceability and must not convert a planned mapping into an implemented or effective status without evidence.

---

## 12. Authoritative References

- [NIST AI Risk Management Framework 1.0](https://doi.org/10.6028/NIST.AI.100-1)
- [NIST AI RMF Playbook](https://airc.nist.gov/airmf-resources/playbook/)
- [ISO/IEC 42001:2023 — Artificial intelligence management system](https://www.iso.org/standard/81230.html)
- [ISO/IEC 23894:2023 — Guidance on risk management](https://www.iso.org/standard/77304.html)
- [OECD AI Principles](https://oecd.ai/en/ai-principles)

---

## 13. Document Control

| Field | Value |
| --- | --- |
| Document title | AI Governance Framework Crosswalk |
| Repository path | `docs/07-framework-crosswalk.md` |
| Version | 1.0 |
| Status | Draft portfolio artifact |
| Owner | GRC Analyst |
| Approver | AI Governance Committee |
| Review frequency | At least annually and upon material change |
| Classification | Public fictional portfolio content |

### Version history

| Version | Date | Author | Change summary |
| --- | --- | --- | --- |
| 1.0 | 2026-09-20 | Tommy Marshall | Created the initial RouteAssist crosswalk across NIST AI RMF, ISO/IEC 42001, ISO/IEC 23894, and OECD AI Principles. |

---

## 14. Related Documents

- [Project README](../README.md)
- [Project Overview and Methodology](00-project-overview-and-methodology.md)
- [Organization Profile and AI Use Case](01-organization-profile-and-ai-use-case.md)
- [Stakeholder and Accountability Map](02-stakeholder-and-accountability-map.md)
- [AI System Inventory and Impact Screening](03-ai-system-inventory-and-impact-screening.md)
- [Data Flow and System Context](04-data-flow-and-system-context.md)
- [AI Risk Assessment Methodology](05-ai-risk-assessment-methodology.md)
- [AI Risk Register](06-ai-risk-register.md)
- [AI Governance Charter](08-ai-governance-charter.md)
- [AI Control Matrix](09-ai-control-matrix.md)
- [Human Oversight and Escalation Plan](10-human-oversight-and-escalation-plan.md)
- [AI Evaluation and Testing Plan](11-ai-evaluation-and-testing-plan.md)
- [Monitoring, Metrics, and Reporting Plan](12-monitoring-metrics-and-reporting-plan.md)
- [AI Incident Response Plan](13-ai-incident-response-plan.md)
- [Gap Assessment and POA&M](15-gap-assessment-and-poam.md)

---

## 15. Portfolio Notice

This crosswalk is part of an educational portfolio project based on a fictional organization and fictional AI system. Framework descriptions are summarized and mappings are illustrative.

This document does not reproduce the full text of any standard and does not establish compliance, conformity, certification, legal sufficiency, or independent assurance.
