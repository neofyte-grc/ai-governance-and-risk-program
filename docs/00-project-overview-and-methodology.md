# Project Overview and Methodology

## AI Governance & Risk Assessment

**Organization:** Peachtree Logistics Group (fictional)  
**AI system:** PLG RouteAssist  
**System identifier:** `AI-SYS-001`  
**Document owner:** GRC Analyst  
**Document status:** Draft portfolio artifact  
**Version:** 1.0  
**Primary framework:** NIST AI Risk Management Framework  
**Review frequency:** At major project milestones and when the project scope changes

---

## 1. Document Purpose

This document establishes the governing methodology for the Peachtree Logistics Group AI Governance & Risk Assessment. It defines the project objective, business problem, scope, exclusions, assumptions, constraints, assessment approach, evidence standards, deliverables, success criteria, and change-control expectations.

All later project artifacts should remain consistent with this document. If a later discovery materially changes the system boundary, risk methodology, use case, affected parties, or assessment objectives, this document must be reviewed and updated before dependent artifacts are finalized.

---

## 2. Project Summary

Peachtree Logistics Group (PLG) is a fictional regional logistics organization headquartered in Atlanta, Georgia. PLG provides warehousing, last-mile delivery, medical courier, and freight brokerage services throughout the southeastern United States.

PLG is evaluating **RouteAssist**, an AI-assisted operational decision-support system. RouteAssist is intended to recommend delivery priorities, driver or courier assignments, routes, exception classifications, and potential schedule adjustments. The system uses operational information such as order details, delivery windows, location data, traffic conditions, driver availability, and incident records.

AI-assisted recommendations may improve efficiency and consistency, but they can also create operational, privacy, security, safety, fairness, compliance, workforce, vendor, and reputational risks. These risks are particularly important when recommendations affect time-sensitive medical deliveries, workload distribution, customer commitments, or access to services.

This project designs a practical governance and risk program that allows PLG to evaluate RouteAssist without transferring organizational accountability to the AI system.

---

## 3. Business Problem

PLG wants to gain operational value from AI-assisted routing and dispatch while maintaining human accountability and preventing unmanaged harm.

Without a defined governance program, PLG may be unable to answer essential questions such as:

- Who is accountable for RouteAssist and its outcomes?
- Which uses are approved, restricted, or prohibited?
- What data does the system use, and is that data appropriate?
- Which individuals or groups may be affected by its recommendations?
- What risks must be assessed before deployment?
- What performance and risk thresholds must the system meet?
- When must a person review, reject, override, or escalate a recommendation?
- How will PLG detect performance degradation, drift, misuse, or harmful impact?
- What evidence will demonstrate that governance controls are operating?
- What happens when RouteAssist produces an unsafe, inaccurate, unfair, insecure, or unauthorized result?

The central governance question is:

> How can PLG use AI-generated operational recommendations while preserving human accountability, testing system performance, protecting affected parties, and responding effectively when the system behaves unexpectedly?

---

## 4. Project Goal

The goal of this project is to design a traceable AI governance and risk-management program for RouteAssist using the NIST AI Risk Management Framework.

The program will connect the following activities:

```text
AI use case
    → stakeholders and affected parties
    → system and data context
    → impact and risk assessment
    → governance and control design
    → evaluation and acceptance decisions
    → ongoing monitoring
    → human oversight and escalation
    → incident response and improvement
```

---

## 5. Project Objectives

The project will:

1. Define the intended purpose, permitted uses, prohibited uses, users, affected parties, system boundaries, dependencies, and limitations of RouteAssist.
2. Establish accountable owners, decision rights, governance forums, review responsibilities, escalation paths, and risk-acceptance authority.
3. Create an inventory record and initial impact classification for the AI system.
4. Document relevant data sources, flows, integrations, outputs, trust boundaries, and downstream actions.
5. Develop an AI risk-assessment methodology with defined likelihood, impact, inherent-risk, residual-risk, and treatment criteria.
6. Identify risks across governance, data, performance, fairness, human factors, privacy, security, safety, operations, vendors, change management, monitoring, and incident response.
7. Map project activities to the NIST AI RMF functions of GOVERN, MAP, MEASURE, and MANAGE.
8. Design risk-based controls with defined owners, frequencies, evidence, test procedures, and related risks.
9. Establish meaningful human-review, override, escalation, and recordkeeping requirements.
10. Define an AI evaluation approach with test conditions, metrics, thresholds, slice analysis, acceptance criteria, and revalidation triggers.
11. Create ongoing performance, risk, drift, and control-monitoring requirements.
12. Establish an AI-specific incident-response process.
13. Address third-party AI and vendor risks.
14. Demonstrate how governance controls would operate through fictional sample evidence.
15. Identify control gaps and create a prioritized Plan of Action and Milestones (POA&M).
16. Translate detailed findings into an executive summary and interview-ready portfolio narrative.

---

## 6. Intended Audience

This project is written for:

- PLG executive leadership
- The AI Governance Committee
- The RouteAssist system owner
- Operations, dispatch, and warehouse leadership
- Information technology and information-security personnel
- GRC, privacy, legal, procurement, and vendor-management stakeholders
- Human reviewers who act on RouteAssist recommendations
- Internal assurance or audit personnel
- Recruiters and hiring managers reviewing the portfolio case study

The documents should be understandable to both technical and nontechnical readers.

---

## 7. AI System Overview

| Field | Description |
| --- | --- |
| System name | PLG RouteAssist |
| System identifier | `AI-SYS-001` |
| System type | AI-assisted operational decision-support system |
| Lifecycle status | Proposed / predeployment evaluation |
| Business owner | Dispatch Director |
| Technical owner | CIO / IT Director |
| Executive sponsor | Chief Operating Officer |
| Risk oversight | AI Governance Committee |
| Primary users | Dispatchers, operations supervisors, and authorized managers |
| Primary purpose | Recommend delivery priorities, assignments, routes, exception classifications, and schedule adjustments |
| Decision role | Advisory; authorized personnel retain decision authority |
| Deployment environment | Mixed cloud and operational technology environment |
| Geographic context | Southeastern United States |
| Highest-concern use context | Time-sensitive medical delivery and decisions that materially affect individuals or service recipients |

The complete system description will be maintained in [`01-organization-profile-and-ai-use-case.md`](01-organization-profile-and-ai-use-case.md) and the system inventory record in [`03-ai-system-inventory-and-impact-screening.md`](03-ai-system-inventory-and-impact-screening.md).

---

## 8. Governance Boundary

RouteAssist is a decision-support system. It does not replace human accountability.

Authorized PLG personnel remain responsible for reviewing relevant context and making consequential operational decisions. RouteAssist may not independently:

- Make hiring, termination, disciplinary, performance-rating, or compensation decisions.
- Deny a customer, shipment recipient, driver, courier, or employee access to services or opportunities.
- Change the priority of a time-sensitive medical delivery without documented human review.
- Approve a new use case or expand an existing use beyond its approved purpose.
- Approve a material model, data, vendor, configuration, or integration change.
- Accept residual risk on behalf of PLG.
- Close a material AI incident.
- Resume operation following a severe AI incident or system suspension.

Any proposed change to these boundaries requires documented governance review and approval.

---

## 9. Project Scope

### 9.1 In scope

The assessment includes:

1. RouteAssist business justification and AI use-case intake.
2. Intended purpose, expected benefits, limitations, and prohibited uses.
3. AI system inventory and impact classification.
4. System users, stakeholders, affected parties, and governance roles.
5. Decision authority, risk ownership, review responsibilities, and escalation paths.
6. Input data, output data, data sources, system flows, integrations, and trust boundaries.
7. Operational processes affected by RouteAssist recommendations.
8. AI governance, data, performance, reliability, fairness, privacy, security, safety, workforce, vendor, operational, and reputational risks.
9. Human review, challenge, rejection, override, escalation, and recordkeeping.
10. Governance policies, standards, control objectives, and control activities.
11. Predeployment testing, acceptance criteria, and approval gates.
12. Postdeployment performance, drift, impact, risk, and control monitoring.
13. Material-change review and revalidation.
14. AI incident identification, triage, containment, investigation, recovery, communication, and lessons learned.
15. Third-party AI services, vendor due diligence, contractual expectations, and exit risk.
16. Evidence requirements and sample control records.
17. Gap assessment, remediation priorities, and POA&M tracking.
18. Executive reporting and risk communication.

### 9.2 Systems and interfaces in scope

The project may evaluate the relationship between RouteAssist and the following fictional PLG systems:

- Cloud logistics and freight brokerage platform
- Dispatch and delivery mobile platform
- Warehouse Management System
- Mapping, traffic, and geolocation services
- Driver and courier scheduling records
- Customer order and delivery-window records
- Incident and exception-management records
- Microsoft 365 collaboration environment
- Vendor-hosted AI services and application programming interfaces
- Monitoring, logging, and reporting tools

### 9.3 Data categories in scope

Relevant data categories include:

- Customer and shipment information
- Delivery addresses and geolocation data
- Delivery dates, windows, priorities, and service levels
- Driver and courier identity, status, availability, and assignment information
- Vehicle and route information
- Operational performance and historical delivery data
- Incident, delay, exception, and complaint records
- Medical-delivery indicators and limited healthcare-client delivery details
- System logs, recommendation records, reviewer actions, and override rationales
- Vendor-provided data and external mapping or traffic information

Detailed data identifiers and flows will be documented in [`04-data-flow-and-system-context.md`](04-data-flow-and-system-context.md).

---

## 10. Out of Scope

The following activities are excluded:

- Building, training, fine-tuning, or deploying a production AI model.
- Writing production software or connecting to live PLG systems.
- Processing real employee, courier, customer, patient, shipment, or delivery information.
- Penetration testing, adversarial exploitation, or disruptive testing of a live environment.
- Direct inspection of a real vendor's internal model, source code, infrastructure, or proprietary training data.
- Issuing legal opinions or making formal regulatory determinations.
- Performing an independent audit, certification, attestation, or assurance engagement.
- Certifying that RouteAssist is safe, secure, fair, unbiased, compliant, reliable, or fit for production use.
- Conducting a formal privacy impact assessment under a specific jurisdiction.
- Replacing organizational legal counsel, privacy counsel, security engineering, data science, model-validation, or internal-audit functions.
- Assessing unrelated PLG systems except where they provide data to, receive output from, or materially influence RouteAssist.

An excluded item may still be recorded as a dependency, limitation, or recommended future activity.

---

## 11. Assumptions

This fictional assessment assumes that:

1. PLG leadership supports the assessment and provides reasonable access to fictional stakeholders and documentation.
2. RouteAssist is in a proposed or predeployment stage and is not responding to an active incident at project initiation.
3. PLG intends RouteAssist to advise authorized personnel rather than make autonomous consequential decisions.
4. Relevant system, data, vendor, process, and operational information is available for review.
5. PLG can identify accountable business, technical, data, risk, and control owners.
6. Dispatchers and operations personnel are available to explain real-world workflows and failure consequences.
7. Test data used in the portfolio is synthetic or fictional.
8. System outputs and human decisions can be logged with appropriate access controls and retention requirements.
9. PLG has basic incident-management, change-management, access-control, and vendor-management processes that can be extended for AI-specific risks.
10. A vendor may supply some or all of the AI capability, which limits direct visibility into proprietary components.
11. Final legal, privacy, contractual, security, and production approvals would require review by qualified organizational personnel.
12. Risk scores and evaluation results included in the portfolio are illustrative rather than claims about a real deployed system.

If an assumption becomes invalid, related risks and artifacts must be reviewed.

---

## 12. Constraints

The project operates under the following constraints:

- **No operational disruption:** Assessment activities must not interfere with active delivery, warehouse, dispatch, or medical-courier operations.
- **No live exploitation:** The project will not conduct active exploitation or destructive security testing.
- **Limited resources:** PLG has limited security, data-science, legal, and compliance resources.
- **Budget sensitivity:** Recommendations should be risk-based, prioritized, and feasible for a midsize organization.
- **Vendor opacity:** Proprietary models, training data, internal validation methods, or subcontractor details may not be fully available.
- **Mixed technology environment:** PLG uses cloud, on-premises, mobile, vendor-hosted, and potentially employee-owned technologies.
- **Time-sensitive operations:** Controls must account for urgent dispatch and delivery decisions without removing necessary accountability.
- **Data sensitivity:** The use case may involve location, workforce, customer, and medical-delivery information.
- **Portfolio limitation:** Evidence and test results are fictional and cannot establish real-world control effectiveness.
- **Evolving AI risk:** System behavior, operating conditions, data, vendors, threats, and stakeholder impacts may change after initial approval.

---

## 13. Guiding Principles

The following principles guide all project decisions:

### 13.1 Human accountability

People and organizational leaders remain accountable for decisions and outcomes. Accountability may not be delegated to RouteAssist or its vendor.

### 13.2 Purpose limitation

RouteAssist may be used only for documented and approved purposes. A useful system in one context is not automatically appropriate in another.

### 13.3 Risk proportionality

Governance rigor should increase with the potential severity, scale, reversibility, and likelihood of harm.

### 13.4 Evidence before trust

Claims about performance, safety, fairness, reliability, or control operation require evidence. Vendor statements alone are not treated as sufficient assurance.

### 13.5 Meaningful human oversight

Human review must provide real authority, adequate information, sufficient time, appropriate competence, and the ability to reject or override a recommendation.

### 13.6 Affected-party awareness

The assessment considers people who use RouteAssist as well as people affected by its recommendations.

### 13.7 Traceability

Risks, controls, tests, evidence, metrics, incidents, and remediation actions must be connected through stable identifiers.

### 13.8 Continuous improvement

Approval is not the end of governance. Monitoring, incidents, complaints, overrides, operational changes, and new evidence must inform reassessment.

### 13.9 Clear communication

Governance requirements should be understandable and usable by the people responsible for implementing them.

---

## 14. Framework Methodology

### 14.1 Primary framework

The project uses the **NIST Artificial Intelligence Risk Management Framework (AI RMF 1.0)** as its primary organizing framework.

The AI RMF Core contains four functions:

| Function | Project application |
| --- | --- |
| **GOVERN** | Establish culture, policies, accountability, roles, decision rights, inventory, risk tolerance, documentation, oversight, and lifecycle requirements. |
| **MAP** | Define the business context, intended use, system boundary, stakeholders, affected parties, data, impacts, dependencies, assumptions, and foreseeable misuse. |
| **MEASURE** | Evaluate system performance, reliability, uncertainty, harmful outcomes, impact differences, security, privacy, human interaction, and control effectiveness. |
| **MANAGE** | Prioritize risks, select treatments, make approval decisions, monitor changes, respond to incidents, communicate residual risk, and improve the program. |

GOVERN is treated as a cross-cutting function that informs MAP, MEASURE, and MANAGE activities throughout the lifecycle.

### 14.2 Framework use

The framework will be used to:

- Organize governance activities.
- Identify missing practices.
- Support consistent terminology.
- Create traceability between risks, controls, evaluations, evidence, and decisions.
- Explain the program to technical and business stakeholders.
- Guide improvement priorities.

The framework will not be used to claim certification, legal compliance, or independent assurance.

### 14.3 Supporting references

Selected supporting references may be used when they add practical detail, including:

- NIST AI RMF Playbook
- NIST Cybersecurity Framework 2.0
- NIST Privacy Framework
- NIST Special Publication 800-53 control concepts
- NIST Secure Software Development Framework concepts
- ISO/IEC 27001 information-security management concepts
- ISO/IEC 42001 AI management-system concepts
- Organizational policies, contractual requirements, and risk tolerance

Any supporting mapping will identify the source and purpose. The project will avoid implying equivalence between frameworks where none has been established.

### 14.4 Authoritative framework references

- [NIST AI Risk Management Framework](https://www.nist.gov/itl/ai-risk-management-framework)
- [Artificial Intelligence Risk Management Framework (AI RMF 1.0)](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.100-1.pdf)
- [NIST AI RMF Playbook](https://airc.nist.gov/airmf-resources/playbook/)

---

## 15. Assessment Methodology

The project will use the following phased approach.

### Phase 1 — Context and scoping

Activities:

- Define the organization and business problem.
- Document the proposed AI use case.
- Establish intended and prohibited uses.
- Identify users, affected parties, and stakeholders.
- Assign preliminary ownership and decision rights.
- Create the AI inventory record.
- Conduct initial impact screening.
- Document the system context and data flows.

Primary outputs:

- Project overview and methodology
- Organization profile and AI use case
- Stakeholder and accountability map
- AI system inventory and impact screening
- Data-flow and system-context documentation
- Foundational diagrams

### Phase 2 — Risk analysis and framework alignment

Activities:

- Define the AI risk taxonomy.
- Establish likelihood and impact criteria.
- Identify risk events, causes, consequences, affected parties, and existing controls.
- Calculate inherent risk.
- Identify treatment needs and accountable owners.
- Map activities to the NIST AI RMF.

Primary outputs:

- AI risk-assessment methodology
- AI risk register
- Framework crosswalk

### Phase 3 — Governance and control design

Activities:

- Establish governance forums, authority, approvals, and escalation.
- Define policies and operating standards.
- Design control objectives and activities.
- Assign control owners and performance frequencies.
- Define evidence and test procedures.
- Establish human-review and override requirements.
- Create reusable governance templates.

Primary outputs:

- AI governance charter
- Responsible AI policy
- AI acceptable-use standard
- AI system change and revalidation standard
- AI control matrix
- Human oversight and escalation plan
- Governance templates

### Phase 4 — Evaluation, monitoring, and response

Activities:

- Define evaluation questions, datasets, scenarios, metrics, and thresholds.
- Test expected, edge, failure, misuse, and high-impact conditions.
- Evaluate results across relevant operational slices.
- Define performance, drift, risk, and control monitoring.
- Establish alert and escalation thresholds.
- Define AI incident-response procedures.
- Assess third-party and vendor AI risk.
- Create fictional sample evidence.

Primary outputs:

- AI evaluation and testing plan
- Monitoring, metrics, and reporting plan
- AI incident-response plan
- Third-party and vendor AI risk review
- Sample governance and control evidence

### Phase 5 — Findings, remediation, and communication

Activities:

- Compare current and target governance capabilities.
- Identify and prioritize gaps.
- Create remediation actions, owners, milestones, and target dates.
- Describe residual risk and required decisions.
- Prepare executive and portfolio narratives.
- Document lessons learned and project limitations.

Primary outputs:

- Gap assessment and POA&M
- Executive summary and recommendations
- Lessons learned and portfolio reflection
- Executive briefing outline
- Final repository README

---

## 16. Risk-Assessment Approach

### 16.1 Risk-statement structure

Each risk should be written using a cause-event-impact structure:

> Because **[condition or cause]**, there is a possibility that **[risk event]**, resulting in **[impact to people, operations, compliance, security, finances, or reputation]**.

Example:

> Because historical delivery data may underrepresent unusual medical-delivery conditions, RouteAssist may recommend an inappropriate priority or route during an uncommon event, resulting in delayed delivery, operational disruption, or harm to a service recipient.

### 16.2 Risk dimensions

Each risk record should consider:

- Source or cause
- Risk event
- Potential consequences
- Affected parties
- Affected assets or processes
- Relevant data
- Existing controls
- Likelihood
- Impact
- Inherent risk
- Treatment decision
- Planned controls
- Residual risk
- Risk owner
- Target date
- Related evaluation, evidence, metric, incident, or remediation identifier

### 16.3 Risk taxonomy

The risk taxonomy will include:

- Governance and accountability
- Intended use and foreseeable misuse
- Data quality and data governance
- Performance, reliability, and robustness
- Fairness and harmful impact
- Explainability, transparency, and communication
- Human factors and automation bias
- Privacy and data protection
- Security and system integrity
- Safety and operational continuity
- Workforce and organizational impact
- Third-party and supply-chain risk
- Change management and revalidation
- Monitoring and drift
- Incident response and recovery
- Legal, contractual, and compliance exposure
- Reputation and stakeholder trust

### 16.4 Scoring model

Risks will be rated using a five-point likelihood scale and a five-point impact scale.

```text
Risk score = Likelihood × Impact
```

The detailed definitions, rating bands, treatment rules, and residual-risk method will be established in [`05-ai-risk-assessment-methodology.md`](05-ai-risk-assessment-methodology.md). Scores support prioritization but do not replace professional judgment, affected-party analysis, or mandatory requirements.

---

## 17. AI Evaluation Methodology

The project will include a defined evaluation methodology rather than relying only on qualitative risk statements.

### 17.1 Evaluation objectives

Evaluations will determine whether RouteAssist:

- Performs its intended operational function under expected conditions.
- Remains reliable under unusual, incomplete, delayed, or changing conditions.
- Meets documented acceptance thresholds.
- Produces materially different outcomes across relevant operational groups or conditions.
- Enables meaningful human understanding, challenge, rejection, and override.
- Resists defined misuse and security scenarios.
- Maintains performance following approved changes.
- Generates sufficient logs and evidence for investigation and assurance.

### 17.2 Evaluation dimensions

Planned dimensions include:

- Accuracy and operational usefulness
- False-positive and false-negative consequences
- Reliability and robustness
- Data quality and coverage
- Performance by delivery type
- Performance by geography or route characteristics
- Performance by time window and operating conditions
- Effects on workload and assignment distribution
- Time-sensitive and medical-delivery scenarios
- Human-review effectiveness
- Explanation or rationale usefulness
- Privacy and security behavior
- Misuse and prohibited-use scenarios
- Regression following material change

### 17.3 Test types

The evaluation plan may use:

- Baseline testing
- Scenario-based testing
- Edge-case and stress testing
- Slice-based performance analysis
- Human-in-the-loop simulation
- Override and escalation testing
- Data-quality testing
- Security and misuse-case testing
- Regression testing
- Control-design and control-operation testing

### 17.4 Acceptance decisions

Evaluation results may support one of the following decisions:

- Approve for limited pilot
- Approve with conditions
- Require remediation and retesting
- Restrict specific uses
- Suspend evaluation or use
- Reject the proposed use

No single aggregate metric will be treated as sufficient evidence of fitness for use. The detailed methodology will be documented in [`11-ai-evaluation-and-testing-plan.md`](11-ai-evaluation-and-testing-plan.md).

---

## 18. Human-Oversight Methodology

Human oversight will be assessed as a complete control system.

The design will address:

- Which recommendations require review.
- Which roles may approve, reject, modify, or override a recommendation.
- What information reviewers receive.
- What qualifications and training reviewers need.
- How much time reviewers have.
- How uncertainty and limitations are communicated.
- Which conditions require escalation.
- When the system must be limited, paused, or suspended.
- How reviewer actions and rationales are recorded.
- How overrides, repeated disagreements, and automation bias are monitored.
- Who may authorize return to service after suspension.

The methodology will distinguish meaningful review from nominal approval. A person cannot provide effective oversight if they lack authority, information, competence, time, or a realistic ability to disagree with the system.

---

## 19. Control-Design Methodology

Controls will be designed in response to identified risks and governance requirements.

Each control record should include:

- Control identifier
- Control objective
- Control activity
- Related risk identifiers
- NIST AI RMF mapping
- Control owner
- Responsible performer
- Frequency or trigger
- Preventive, detective, or corrective classification
- Manual, automated, or hybrid classification
- Required evidence
- Test procedure
- Exception and escalation process
- Design status
- Operating-effectiveness status

Controls should be specific enough that another person can understand what must occur, who performs it, when it occurs, and what evidence proves completion.

---

## 20. Evidence and Documentation Standards

### 20.1 Evidence principles

Evidence should be:

- **Relevant:** Directly connected to a control, decision, evaluation, or requirement.
- **Reliable:** Produced by an appropriate source and protected from unauthorized alteration.
- **Complete:** Covers the required period, population, fields, approvals, and exceptions.
- **Timely:** Created close to the activity it supports.
- **Traceable:** Linked to stable identifiers.
- **Reproducible:** Allows a qualified reviewer to understand how a result was reached.
- **Proportionate:** Appropriate to the significance of the risk and decision.

### 20.2 Evidence limitations

All evidence in this repository is fictional and created for educational purposes. It demonstrates what evidence could look like; it does not prove that a real control operated or that a real system met an acceptance threshold.

### 20.3 Documentation requirements

Material decisions should document:

- Decision requested
- Decision maker
- Date
- Information reviewed
- Alternatives considered
- Risk and affected-party considerations
- Conditions or limitations
- Approval, rejection, or escalation outcome
- Residual risk
- Follow-up actions

---

## 21. Traceability Method

The repository will use stable identifiers.

| Record type | Identifier format | Example |
| --- | --- | --- |
| AI system | `AI-SYS-###` | `AI-SYS-001` |
| Role | `ROLE-###` | `ROLE-004` |
| Data category | `DATA-###` | `DATA-006` |
| AI risk | `AIR-###` | `AIR-007` |
| AI control | `AIC-###` | `AIC-012` |
| Evaluation | `EVAL-###` | `EVAL-003` |
| Metric or indicator | `MET-###` | `MET-009` |
| Evidence item | `EVD-###` | `EVD-014` |
| Gap | `GAP-###` | `GAP-005` |
| Remediation action | `POAM-###` | `POAM-005` |
| AI incident | `AI-INC-YYYY-###` | `AI-INC-2026-001` |

High and critical risks should trace through the following chain:

```text
AI use case or process
    → affected stakeholder or asset
    → risk
    → control
    → evaluation or control test
    → evidence
    → monitoring metric or threshold
    → escalation or remediation
```

Traceability gaps should be recorded in the gap assessment and POA&M.

---

## 22. Stakeholder-Engagement Method

The assessment will use fictional stakeholder perspectives to test whether governance requirements are practical.

Engagement topics include:

| Stakeholder group | Primary assessment topics |
| --- | --- |
| Executive leadership | Business value, risk tolerance, funding, accountability, and risk acceptance |
| Dispatch and operations | Workflow, decision urgency, exceptions, failure consequences, overrides, and usability |
| Drivers and couriers | Assignment effects, mobile interaction, workload, communication, and dispute mechanisms |
| IT and security | Architecture, access, logging, integration, monitoring, change control, and incident response |
| Data or AI personnel | Data suitability, model behavior, evaluation, limitations, performance, and changes |
| GRC, legal, and privacy | Policies, obligations, documentation, impacts, exceptions, and assurance |
| Procurement and vendor management | Due diligence, contracts, subcontractors, audit rights, notifications, and exit plans |
| Healthcare clients and customers | Service requirements, transparency, reliability, complaints, and escalation |
| Internal audit or assurance | Evidence quality, control testing, issue tracking, and independent challenge |

The complete responsibility and RACI analysis will be documented in [`02-stakeholder-and-accountability-map.md`](02-stakeholder-and-accountability-map.md).

---

## 23. Deliverables

### 23.1 Core documents

| File | Purpose |
| --- | --- |
| `00-project-overview-and-methodology.md` | Establish the project's governing methodology. |
| `01-organization-profile-and-ai-use-case.md` | Define the organization, use case, intended use, benefits, limitations, and prohibited uses. |
| `02-stakeholder-and-accountability-map.md` | Define stakeholders, affected parties, roles, ownership, decision rights, and RACI assignments. |
| `03-ai-system-inventory-and-impact-screening.md` | Create the system record and determine the initial impact tier and review path. |
| `04-data-flow-and-system-context.md` | Document the system boundary, components, integrations, data, outputs, and trust boundaries. |
| `05-ai-risk-assessment-methodology.md` | Define risk taxonomy, scoring scales, treatment rules, and review cadence. |
| `06-ai-risk-register.md` | Record identified risks, scores, controls, treatments, owners, and target dates. |
| `07-framework-crosswalk.md` | Map governance activities and evidence to the NIST AI RMF. |
| `08-ai-governance-charter.md` | Establish governance authority, forums, approvals, risk acceptance, and reporting. |
| `09-ai-control-matrix.md` | Connect risks to controls, owners, evidence, frequencies, and tests. |
| `10-human-oversight-and-escalation-plan.md` | Define review, override, escalation, suspension, and recordkeeping requirements. |
| `11-ai-evaluation-and-testing-plan.md` | Define evaluation questions, methods, metrics, thresholds, and acceptance decisions. |
| `12-monitoring-metrics-and-reporting-plan.md` | Establish KPIs, KRIs, drift signals, thresholds, dashboards, and reporting cadence. |
| `13-ai-incident-response-plan.md` | Define AI incident severity, triage, containment, investigation, recovery, and improvement. |
| `14-third-party-and-vendor-ai-risk-review.md` | Evaluate vendor governance, data, security, transparency, monitoring, incidents, and exit risks. |
| `15-gap-assessment-and-poam.md` | Compare current and target states and track prioritized remediation. |
| `16-executive-summary-and-recommendations.md` | Communicate the risk posture, major findings, decisions, and roadmap. |
| `17-lessons-learned-and-portfolio-reflection.md` | Record tradeoffs, limitations, learning outcomes, and future improvements. |

### 23.2 Supporting artifacts

The project also includes:

- Responsible AI policy
- AI acceptable-use standard
- AI system change and revalidation standard
- Reusable governance templates
- Fictional sample evidence
- System, data-flow, accountability, and escalation diagrams
- Executive briefing outline
- Repository README

---

## 24. Roles and Responsibilities

| Role | Project responsibility |
| --- | --- |
| Chief Operating Officer | Executive sponsor; approves resources and accepts designated high residual risks. |
| AI Governance Committee | Reviews material use cases, risks, exceptions, evaluation results, incidents, and approval decisions. |
| GRC Analyst | Leads methodology, risk assessment, framework mapping, control design, evidence requirements, and reporting. |
| Dispatch Director | Business and system owner; accountable for the use case and operational outcomes. |
| CIO / IT Director | Technical owner; accountable for architecture, integration, access, logging, change management, and technical operations. |
| Information Security Lead | Assesses security threats, access controls, logging, monitoring, and incident coordination. |
| Privacy or Legal Advisor | Reviews privacy, legal, contractual, notice, and rights considerations. |
| Data or AI Lead | Documents system behavior, data, evaluation methods, limitations, performance, and changes. |
| Dispatch Supervisors | Perform or supervise human review, override, escalation, and operational feedback. |
| Procurement / Vendor Manager | Conducts due diligence and manages contractual, subcontractor, notification, and exit requirements. |
| Internal Audit / Assurance | Provides independent challenge and tests selected governance controls. |

Final role identifiers and RACI assignments will be defined in the stakeholder and accountability map.

---

## 25. Review and Approval Gates

The proposed lifecycle includes the following decision gates:

| Gate | Decision | Minimum evidence |
| --- | --- | --- |
| Gate 1 — Intake | Proceed to assessment or reject the proposal | Completed use-case intake, accountable owner, business need, preliminary data and impact information |
| Gate 2 — Impact and risk | Proceed to control design and evaluation | System inventory, impact screening, system context, data flows, risk assessment |
| Gate 3 — Pilot readiness | Approve limited pilot, approve with conditions, or require remediation | Controls, policies, evaluation plan, test results, human-oversight design, incident plan, vendor review |
| Gate 4 — Operational use | Approve defined production use, restrict use, or reject deployment | Acceptance criteria met, residual risks approved, monitoring active, training complete, evidence available |
| Gate 5 — Material change | Approve change, require revalidation, roll back, or suspend | Change record, impact analysis, regression results, updated risks and documentation |
| Gate 6 — Periodic review | Continue, modify, restrict, suspend, or retire | Monitoring trends, incidents, complaints, overrides, control tests, vendor changes, reassessment |

No gate may be approved solely because the system performed well on one aggregate metric.

---

## 26. Quality-Assurance Criteria

Each project artifact should:

- Use consistent organizational facts and system terminology.
- Use stable identifiers and maintain traceability.
- Distinguish fictional facts, assumptions, limitations, and recommendations.
- Explain why major governance requirements exist.
- Identify accountable and responsible roles.
- Define measurable requirements where practical.
- Include evidence expectations for material controls and decisions.
- Consider users and affected parties.
- Address both normal operations and foreseeable failure conditions.
- Use relative Markdown links to related repository artifacts.
- Avoid unsupported claims of compliance, fairness, security, safety, or effectiveness.
- Be understandable to a nontechnical business stakeholder.
- Include version, owner, status, and review information when functioning as a controlled governance document.

---

## 27. Success Criteria

The project will be considered successful when:

1. The intended use, prohibited uses, system boundary, stakeholders, affected parties, data, and dependencies are documented.
2. Governance roles, decision rights, risk ownership, and escalation paths are assigned.
3. The AI risk methodology is repeatable and consistently applied.
4. Material risks include owners, treatment decisions, controls, target dates, and residual-risk considerations.
5. Controls include owners, frequencies, evidence, tests, and escalation requirements.
6. The evaluation plan includes measurable acceptance criteria and relevant scenario or slice analysis.
7. Human reviewers have authority, information, competence, time, override capability, and documentation requirements.
8. Monitoring includes performance, drift, harmful impact, human behavior, incidents, complaints, overrides, and control operation.
9. The incident-response process includes triage, containment, investigation, notification, recovery, evidence preservation, and lessons learned.
10. Vendor risks and contractual expectations are documented.
11. Fictional sample evidence demonstrates how the program would operate.
12. High and critical risks follow the required traceability chain.
13. Gaps are prioritized in a POA&M with owners and target dates.
14. Executive reporting clearly states decisions, business impact, limitations, and residual risk.
15. Repository links function when all artifacts are uploaded.
16. The project can be explained confidently in an interview without overstating real-world implementation or assurance.

---

## 28. Limitations

This project has the following limitations:

- PLG and RouteAssist are fictional.
- No live model, production environment, vendor, or dataset was assessed.
- Evaluation results and evidence samples are illustrative.
- Risk ratings reflect defined fictional conditions and professional judgment, not measured production outcomes.
- The assessment cannot validate real legal, privacy, security, operational, or contractual compliance.
- The project cannot establish that a real AI system is safe, fair, reliable, secure, or appropriate for deployment.
- Framework mapping demonstrates alignment of activities; it does not constitute certification or independent assurance.
- Real deployment would require qualified cross-functional review and additional technical validation.

These limitations should be repeated where necessary in executive and public-facing materials.

---

## 29. Change Control

This methodology must be reviewed when any of the following occurs:

- The intended use or prohibited-use boundary changes.
- A new user group or affected party is identified.
- A new data source, sensitive data category, integration, or downstream action is introduced.
- The model, vendor, configuration, system architecture, or deployment environment materially changes.
- Risk scoring or acceptance criteria change.
- A severe incident, repeated complaint, unexpected impact, or significant monitoring threshold breach occurs.
- A new legal, contractual, policy, or business requirement materially affects the project.
- Evidence shows that an assumption is invalid.
- Governance ownership or risk-acceptance authority changes.

Changes should document:

- What changed
- Why it changed
- Which artifacts are affected
- Who reviewed and approved the change
- Whether reassessment, retesting, or reapproval is required

---

## 30. Document Control

| Field | Value |
| --- | --- |
| Document title | Project Overview and Methodology |
| Repository path | `docs/00-project-overview-and-methodology.md` |
| Version | 1.0 |
| Status | Draft portfolio artifact |
| Owner | GRC Analyst |
| Approver | AI Governance Committee |
| Review frequency | At project milestones and upon material scope or methodology change |
| Classification | Public fictional portfolio content |

### Version history

| Version | Date | Author | Change summary |
| --- | --- | --- | --- |
| 1.0 | 2026-09-18 | Tommy Marshall | Initial project overview and methodology established. |

---

## 31. Related Documents

- [Project README](../README.md)
- [Organization Profile and AI Use Case](01-organization-profile-and-ai-use-case.md)
- [Stakeholder and Accountability Map](02-stakeholder-and-accountability-map.md)
- [AI System Inventory and Impact Screening](03-ai-system-inventory-and-impact-screening.md)
- [Data Flow and System Context](04-data-flow-and-system-context.md)
- [AI Risk Assessment Methodology](05-ai-risk-assessment-methodology.md)
- [AI Risk Register](06-ai-risk-register.md)
- [Framework Crosswalk](07-framework-crosswalk.md)
- [AI Governance Charter](08-ai-governance-charter.md)
- [AI Control Matrix](09-ai-control-matrix.md)
- [Human Oversight and Escalation Plan](10-human-oversight-and-escalation-plan.md)
- [AI Evaluation and Testing Plan](11-ai-evaluation-and-testing-plan.md)
- [Monitoring, Metrics, and Reporting Plan](12-monitoring-metrics-and-reporting-plan.md)
- [AI Incident Response Plan](13-ai-incident-response-plan.md)
- [Third-Party and Vendor AI Risk Review](14-third-party-and-vendor-ai-risk-review.md)
- [Gap Assessment and POA&M](15-gap-assessment-and-poam.md)
- [Executive Summary and Recommendations](16-executive-summary-and-recommendations.md)
- [Lessons Learned and Portfolio Reflection](17-lessons-learned-and-portfolio-reflection.md)

---

## 32. Portfolio Notice

This document is part of an educational portfolio project based on a fictional organization and fictional AI system. It does not contain real PLG, employee, courier, customer, patient, shipment, or delivery information.

The document does not provide legal advice, regulatory advice, certification, independent assurance, or a guarantee that any AI system is safe, fair, secure, compliant, reliable, or suitable for production use.
