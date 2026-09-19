# AI System Inventory and Impact Screening

## PLG RouteAssist

**Organization:** Peachtree Logistics Group (fictional)  
**AI system:** PLG RouteAssist  
**System identifier:** `AI-SYS-001`  
**Use-case identifier:** `UC-001`  
**Document owner:** GRC Analyst  
**Business owner:** Dispatch Director  
**Technical owner:** CIO / IT Director  
**Lifecycle status:** Proposed / predeployment assessment  
**Document status:** Draft portfolio artifact  
**Version:** 1.0  
**Review frequency:** At least annually and upon material change

---

## 1. Document Purpose

This document creates the authoritative AI inventory record for PLG RouteAssist and performs an initial impact screening to determine the level of governance, evaluation, oversight, and approval required before pilot or operational use.

The screening is a triage mechanism. It does not replace the detailed risk assessment, legal or privacy review, security review, technical evaluation, or human-oversight analysis. A lower score in one area does not cancel a severe concern in another area.

---

## 2. Inventory and Screening Principles

PLG applies the following principles:

1. Every AI system and material AI use case must be inventoried before use.
2. The inventory must identify business, technical, data, risk, and vendor ownership.
3. Impact screening must consider users and people affected by the system.
4. The highest credible impact may determine the governance tier even when the average score is lower.
5. Intended human review does not automatically reduce inherent impact.
6. Vendor-hosted systems remain subject to PLG governance.
7. A system cannot approve its own inventory tier, controls, or deployment.
8. Missing information increases uncertainty and may require a more conservative tier.
9. Material change requires rescreening and may require complete reassessment.
10. Inventory approval means the record is accepted for governance purposes; it does not authorize deployment.

---

## 3. AI System Inventory Record

### 3.1 Identification

| Field | Inventory value |
| --- | --- |
| System identifier | `AI-SYS-001` |
| System name | PLG RouteAssist |
| Use-case identifier | `UC-001` |
| System type | AI-assisted operational decision-support system |
| Organization | Peachtree Logistics Group |
| Business unit | Dispatch and Operations |
| Business owner | `ROLE-004` — Dispatch Director |
| Technical owner | `ROLE-005` — CIO / IT Director |
| Data and evaluation owner | `ROLE-006` — Data / AI Lead |
| Governance lead | `ROLE-003` — GRC Analyst |
| Security owner | `ROLE-007` — Information Security Lead |
| Vendor owner | `ROLE-009` — Procurement / Vendor Manager |
| Executive sponsor | `ROLE-001` — Chief Operating Officer |
| Governance authority | `ROLE-002` — AI Governance Committee |
| Current lifecycle stage | Proposed / predeployment assessment |
| Deployment status | Not approved for pilot or production use |
| Inventory status | Registered; impact-screening review required |

### 3.2 Business purpose

RouteAssist is proposed to provide advisory recommendations to authorized dispatch and operations personnel. The system may support:

- Delivery prioritization
- Driver or courier assignment
- Route selection
- Estimated timing
- Operational exception classification
- Schedule adjustments
- Identification of cases requiring supervisory review

The intended business outcome is more consistent and timely operational decision support while preserving human authority and accountability.

### 3.3 Decision role

| Attribute | Inventory value |
| --- | --- |
| Decision role | Advisory |
| Final decision maker | Authorized PLG personnel |
| Human review | Required according to risk and impact level |
| Override capability | Required |
| Escalation capability | Required |
| Autonomous consequential action | Prohibited |
| Risk acceptance by system | Prohibited |

RouteAssist output must not be treated as a final employment, medical, legal, safety, service-access, or risk-acceptance decision.

---

## 4. Capability Inventory

| Capability ID | Capability | Output | Human authority | Initial sensitivity |
| --- | --- | --- | --- | --- |
| `CAP-001` | Delivery prioritization | Recommended priority | Dispatcher or supervisor confirms or rejects | High when time-sensitive or medical delivery is involved |
| `CAP-002` | Assignment recommendation | Recommended driver or courier | Dispatcher verifies eligibility and context | High when patterns affect opportunity or workload |
| `CAP-003` | Route recommendation | Proposed route | Dispatcher or driver may accept, modify, or reject | High when safety or medical timing is affected |
| `CAP-004` | Exception classification | Suggested exception category | Authorized employee validates classification | Moderate to high depending on downstream use |
| `CAP-005` | Schedule-adjustment recommendation | Proposed sequencing, timing, or assignment change | Dispatcher or supervisor approves or rejects | High when multiple deliveries or critical service commitments are affected |
| `CAP-006` | Escalation flag | Alert for human review | Supervisor determines action | Moderate; failure to flag can increase other impacts |

Capabilities may receive different controls and evaluation thresholds. Approval of one capability does not authorize all capabilities.

---

## 5. User and Affected-Party Inventory

### 5.1 Direct users

| Group | Relationship | Access expectation |
| --- | --- | --- |
| Dispatchers | Primary recommendation reviewers | Role-based, named-user access after training |
| Dispatch supervisors | Elevated review and escalation | Role-based access with additional approval authority |
| Operations managers | Trend and operational review | Limited reporting and oversight access |
| Data / AI personnel | Evaluation and monitoring | Controlled technical and analytical access |
| IT and security personnel | Administration and security | Privileged access governed by least privilege and logging |
| GRC and assurance personnel | Risk, evidence, and control review | Read or audit access appropriate to role |

### 5.2 Affected parties

| Group | Potential effect |
| --- | --- |
| PLG-employed drivers | Assignment frequency, workload, routes, travel burden, safety, and performance perception |
| Independent couriers | Access to assignments, workload distribution, route feasibility, and income opportunity |
| Warehouse personnel | Timing, staging, workload, and operational disruption |
| Commercial customers | Delivery timeliness, reliability, communication, and complaint outcomes |
| Healthcare clients | Time-sensitive service, contractual commitments, privacy, and escalation |
| Shipment recipients | Delay, misrouting, failed delivery, and access to service |
| Customer-service personnel | Complaint workload and reliance on system-generated explanations |
| PLG leadership | Business performance, financial, contractual, reputational, and risk outcomes |

People do not need direct access to RouteAssist to be considered affected parties.

---

## 6. Data Inventory Summary

| Data ID | Category | Examples | Sensitivity | Initial necessity decision |
| --- | --- | --- | --- | --- |
| `DATA-001` | Order and shipment data | Order ID, service type, destination, status, and delivery window | Confidential | Necessary for approved use, subject to minimization |
| `DATA-002` | Service-level and priority data | Contracted service level, urgency, and medical-delivery indicator | Confidential; potentially sensitive | Necessary for approved prioritization with heightened controls |
| `DATA-003` | Driver and courier availability | Identity, availability, location, workload, vehicle, and eligibility | Personal and confidential | Limited fields necessary for assignment support |
| `DATA-004` | Route and geolocation data | Origin, destination, distance, restrictions, and travel estimate | Location and confidential | Necessary for routing; access and retention must be limited |
| `DATA-005` | Traffic and environmental data | Traffic, closures, severe weather, and disruption | Operational or public/vendor data | Necessary for current route context |
| `DATA-006` | Operational history | Prior timing, delays, exception categories, and outcomes | Confidential | Use requires quality, representativeness, retention, and feedback-loop review |
| `DATA-007` | Incident and exception data | Failed delivery, safety concern, complaint, and resolution | Confidential; may contain sensitive details | Necessary for limited classification, monitoring, and investigation purposes |
| `DATA-008` | System and human-review records | Recommendation, uncertainty, decision, override, rationale, user, and timestamp | Confidential and audit-sensitive | Required for traceability, monitoring, and investigation |

Detailed sources, transfers, storage, access, retention, and trust boundaries will be documented in [`04-data-flow-and-system-context.md`](04-data-flow-and-system-context.md).

---

## 7. Technology and Dependency Inventory

| Component or dependency | Relationship to RouteAssist | Ownership | Initial concern |
| --- | --- | --- | --- |
| Logistics and freight platform | Provides order, service, and shipment data | PLG and vendor | Data accuracy, access, integration failure, and purpose limitation |
| Dispatch and delivery platform | Provides availability and receives approved decisions | PLG and vendor | Feedback loops, unauthorized automation, and downstream propagation |
| Warehouse Management System | Provides readiness or fulfillment context | PLG | Incomplete or delayed operational data |
| Mapping and traffic service | Provides route and traffic data | Third party | Availability, latency, inaccurate conditions, licensing, and vendor change |
| Identity and access service | Authenticates users and administrators | PLG | Unauthorized access, excessive privilege, and account compromise |
| Logging and monitoring service | Collects events and evidence | PLG | Missing logs, tampering, retention, and alert failure |
| Vendor-hosted AI service or API | Generates or supports recommendations | Third party | Opacity, change notification, security, data use, subcontractors, and exit risk |
| Microsoft 365 | Stores governance or operational documentation | PLG and vendor | Access, sharing, retention, and record integrity |
| Mobile applications and devices | Present routes or assignments to personnel | PLG, vendors, and approved users | Device security, outdated data, and limited interface context |

The final architecture and trust-zone analysis will be maintained in the system-context deliverable.

---

## 8. Deployment and Lifecycle Inventory

| Lifecycle field | Current state |
| --- | --- |
| Proposal | Complete |
| Initial use-case definition | Complete |
| Stakeholder and accountability mapping | Complete |
| Inventory registration | Complete through this document |
| Impact screening | Completed provisionally through this document |
| System and data-flow mapping | Pending |
| Detailed risk assessment | Pending |
| Control design | Pending |
| Evaluation planning | Pending |
| Evaluation execution | Pending |
| Pilot approval | Not granted |
| Production approval | Not granted |
| Ongoing monitoring | Not operational |
| Retirement planning | Preliminary requirement only |

---

## 9. Impact-Screening Method

### 9.1 Screening scale

Each dimension receives a score from 1 to 4.

| Score | Level | General interpretation |
| --- | --- | --- |
| 1 | Low | Limited and readily reversible effect; minimal sensitive data or operational reliance |
| 2 | Moderate | Noticeable effect requiring documented controls and review; harm is generally limited or recoverable |
| 3 | High | Material effect on people, operations, safety, privacy, security, rights, contracts, or trust; strong controls and governance required |
| 4 | Critical | Potential for severe, widespread, difficult-to-reverse, life-safety, essential-service, or otherwise intolerable harm |

### 9.2 Governance tiers

| Tier | Screening condition | Governance expectation |
| --- | --- | --- |
| Tier 1 — Limited | All dimensions score 1 and no override condition applies | Basic inventory, owner approval, acceptable-use controls, and periodic review |
| Tier 2 — Moderate | Highest score is 2 and no override condition applies | Documented risk assessment, controls, evaluation, owner approval, and monitoring |
| Tier 3 — High | Any dimension scores 3, or a Tier 3 override condition applies | Cross-functional review, formal impact and risk assessment, human oversight, testing, monitoring, incident planning, and committee approval |
| Tier 4 — Critical | Any dimension scores 4, or a Tier 4 override condition applies | Executive oversight, strict use limitations, independent challenge, extensive validation, enhanced monitoring, and possible prohibition |

### 9.3 Tier override rule

The final tier is the highest of:

1. The highest individual dimension score
2. Any applicable override condition
3. A higher tier assigned through professional judgment because uncertainty or combined effects are not captured by individual scores

An average score will be calculated for transparency but will not reduce the final tier.

---

## 10. Impact Dimensions

The screening evaluates:

1. Operational criticality
2. Safety and physical harm
3. Medical-delivery or essential-service effect
4. Workforce and economic effect
5. Fairness and harmful differential effect
6. Privacy and sensitive-data effect
7. Cybersecurity and integrity effect
8. Autonomy and human-oversight effect
9. Customer and recipient effect
10. Legal, contractual, and compliance effect
11. Scale and reach
12. Reversibility and detectability
13. Third-party dependency and transparency
14. Reputational and stakeholder-trust effect

---

## 11. Impact-Screening Results

| Dimension | Score | Level | Rationale | Required follow-up |
| --- | ---: | --- | --- | --- |
| Operational criticality | 3 | High | Recommendations may affect dispatch sequencing, assignments, delivery windows, and connected operations. Errors can propagate across multiple deliveries. | Scenario testing, continuity procedures, fallback process, and operational monitoring |
| Safety and physical harm | 3 | High | An unsafe or impractical route may affect drivers, couriers, recipients, cargo, or the public. | Safety constraints, human rejection authority, edge-case testing, and incident escalation |
| Medical-delivery or essential-service effect | 4 | Critical | Improper prioritization or routing of time-sensitive medical deliveries could contribute to severe consequences. | Exclude from initial pilot or apply separately approved heightened governance, testing, and mandatory review |
| Workforce and economic effect | 3 | High | Repeated assignment recommendations may influence workload, opportunity, travel burden, earnings, or performance perception. | Workforce-impact analysis, monitoring, dispute mechanism, HR review, and secondary-use prohibition |
| Fairness and harmful differential effect | 3 | High | Historical or proxy data may produce materially different outcomes across workers, geographies, customer groups, or delivery types. | Slice analysis, outcome monitoring, affected-party review, and treatment thresholds |
| Privacy and sensitive-data effect | 3 | High | The system may process identity, availability, location, customer, delivery, and medical-delivery information. | Data minimization, access control, retention, privacy review, and secondary-use controls |
| Cybersecurity and integrity effect | 3 | High | Manipulated inputs, compromised accounts, insecure integrations, or altered outputs could affect decisions and expose data. | Threat assessment, authentication, authorization, logging, input validation, and security testing |
| Autonomy and human-oversight effect | 3 | High | Time pressure and recommendation presentation may create automation bias or nominal review. | Meaningful human-review design, training, override monitoring, and non-retaliation controls |
| Customer and recipient effect | 3 | High | Incorrect recommendations may cause delay, failed service, inaccurate communication, or complaint burden. | Customer-impact monitoring, complaint process, human-approved communication, and escalation |
| Legal, contractual, and compliance effect | 3 | High | Data use, workforce effects, medical-delivery commitments, vendor obligations, and incident notification may create exposure. | Legal/privacy review, contract review, documented obligations, and notification procedures |
| Scale and reach | 2 | Moderate | Initial use is expected to be geographically and operationally limited, but effects may scale if expanded. | Pilot boundaries, volume limits, expansion triggers, and rescreening |
| Reversibility and detectability | 3 | High | Some errors may be corrected, but delayed detection can make delivery, safety, workforce, or trust impacts difficult to reverse. | Timely logs, alerts, manual fallback, complaint channels, and stop conditions |
| Third-party dependency and transparency | 3 | High | Vendor-hosted AI and external data services may limit visibility into changes, performance, training data, incidents, or subcontractors. | Due diligence, contract requirements, evidence, change notification, and exit planning |
| Reputational and stakeholder-trust effect | 3 | High | Harmful outcomes or weak explanations could damage relationships with workers, customers, healthcare clients, and partners. | Transparency, complaint handling, executive reporting, and incident communications |

### 11.1 Score summary

```text
Total score: 42
Dimensions assessed: 14
Average score: 3.0
Highest individual score: 4 — Critical
```

The average score is informational. The critical medical-delivery dimension controls the final tier.

---

## 12. Override Conditions

### 12.1 Tier 3 override conditions

Tier 3 applies when any of the following is true:

- The system materially influences workforce assignment, opportunity, or workload.
- The system processes sensitive location, workforce, customer, or health-related delivery information.
- A failure may materially disrupt time-sensitive logistics operations.
- Users may rely on recommendations under significant time pressure.
- A vendor-hosted model or material external dependency limits transparency.
- The system requires ongoing performance, drift, or harmful-impact monitoring.
- Recommendations may affect safety, service access, or contractual commitments.

Multiple Tier 3 conditions apply to RouteAssist.

### 12.2 Tier 4 override conditions

Tier 4 applies when any of the following is true:

- The system may directly or indirectly contribute to severe physical harm.
- The system autonomously makes a consequential employment, medical, legal, or service-access decision.
- The system operates in a critical or essential context without effective human intervention.
- Failure may cause severe and difficult-to-reverse harm before detection.
- The proposed use is prohibited by PLG policy or applicable authority.

RouteAssist does not have autonomous authority. However, the proposed use can affect time-sensitive medical deliveries, creating a Tier 4 concern for that capability and use context.

---

## 13. Final Impact Classification

| Field | Decision |
| --- | --- |
| Overall governance tier | **Tier 4 — Critical** |
| Primary tier driver | Potential effect on time-sensitive medical deliveries |
| Secondary drivers | Safety, workforce, fairness, privacy, security, human oversight, vendor dependency, and operational criticality |
| Decision role | Advisory only |
| Production approval | Not granted |
| Pilot approval | Not granted |
| Initial pilot position | Routine, lower-impact delivery scenarios only; medical-delivery use excluded unless separately approved |
| Required governance body | AI Governance Committee with executive oversight |
| Required reassessment | At each governance gate and upon material change |

### 13.1 Classification rationale

RouteAssist receives an overall Tier 4 classification because its proposed scope includes recommendations that may influence time-sensitive medical deliveries. Even though a person is expected to review the recommendation, ineffective, rushed, or overly deferential review may allow a harmful recommendation to influence an operational decision.

The Tier 4 classification does not mean RouteAssist is prohibited in every context. It means PLG must either:

1. Exclude the critical use from the initial scope and govern the remaining capabilities according to their risk, or
2. Apply heightened controls, evaluation, human oversight, monitoring, and executive approval before the critical use is permitted.

---

## 14. Capability-Level Tiering

| Capability | Routine context | High-impact context | Initial decision |
| --- | --- | --- | --- |
| Delivery prioritization | Tier 3 | Tier 4 when medical or severe safety implications exist | Restrict initial pilot to approved nonmedical scenarios |
| Assignment recommendation | Tier 3 | Tier 3 when repeated patterns affect opportunity or workload | Permit only after workforce-impact controls and evaluation |
| Route recommendation | Tier 3 | Tier 4 when severe safety or time-sensitive medical consequences are credible | Require human authority, safety controls, and restricted pilot scope |
| Exception classification | Tier 2 or 3 | Tier 3 when classification drives material downstream action | Require human validation before finalization |
| Schedule-adjustment recommendation | Tier 3 | Tier 4 when critical deliveries are affected | Require supervisor review and defined high-impact escalation |
| Escalation flag | Tier 2 or 3 | Tier 3 when failure to flag can allow severe harm | Evaluate both missed alerts and excessive alerts |

Capability-level tiering prevents a lower-impact capability from automatically inheriting approval for a higher-impact use.

---

## 15. Required Governance Path

Because RouteAssist is classified Tier 4 overall, PLG must complete:

1. Approved organization profile and use-case boundaries.
2. Stakeholder, affected-party, accountability, and RACI mapping.
3. Complete system inventory and impact screening.
4. System context, architecture, data-flow, and trust-boundary documentation.
5. Detailed AI risk assessment and risk-register approval.
6. NIST AI RMF crosswalk.
7. AI governance charter and applicable policies and standards.
8. Risk-based control matrix with owners, evidence, and test procedures.
9. Human-oversight, override, escalation, suspension, and return-to-service plan.
10. Evaluation plan approved before testing.
11. Representative scenario, slice, edge-case, misuse, regression, and human-review testing.
12. Defined acceptance and rejection thresholds.
13. Privacy, security, legal, contractual, workforce, and vendor reviews.
14. Monitoring plan for performance, drift, harmful impact, complaints, overrides, security, and control operation.
15. AI-specific incident-response process and exercise.
16. Documented residual-risk decisions.
17. Independent challenge of selected high-impact evidence and conclusions.
18. AI Governance Committee approval and executive approval where required.

Completion of the documents does not itself establish that the requirements are satisfied. Evidence must support each decision.

---

## 16. Initial Pilot Restrictions

If PLG later authorizes a pilot, the initial scope should:

- Exclude medical-delivery prioritization unless separately evaluated and approved.
- Include only defined routine delivery types.
- Include only trained, named dispatchers and supervisors.
- Limit geography to areas represented in evaluation data.
- Use only approved and minimized data sources.
- Preserve final human decision authority.
- Require supervisor review for defined elevated cases.
- Operate for a fixed period with scheduled review points.
- Use enhanced logging and daily or weekly risk review.
- Include clear fallback procedures.
- Include stop conditions for severe incidents, safety concerns, threshold breaches, control failures, unauthorized use, or unexplained harmful patterns.

---

## 17. Required Control Themes

The final control matrix should address:

| Theme | Minimum control expectation |
| --- | --- |
| Governance | Approved inventory, use-case boundaries, accountable owners, decision gates, and documented risk acceptance |
| Access | Named accounts, least privilege, multifactor authentication, privileged-access controls, and periodic review |
| Data | Approved sources, minimization, quality rules, lineage, retention, and purpose limitation |
| Human oversight | Review levels, authority, training, context, override, rationale, escalation, and non-retaliation |
| Evaluation | Approved metrics, thresholds, scenarios, slices, edge cases, regression, and independent challenge |
| Safety | Unsafe-route rejection, high-impact escalation, fallback procedures, and medical-use restrictions |
| Workforce | Secondary-use prohibition, workload monitoring, dispute mechanism, and HR review |
| Fairness and harmful impact | Relevant slice analysis, threshold review, complaint analysis, and corrective action |
| Security | Threat analysis, secure integrations, input validation, logging, monitoring, incident response, and vendor security |
| Change management | Material-change definition, approval, regression testing, rollback, and revalidation |
| Monitoring | Performance, drift, override, complaint, incident, access, vendor, and control indicators |
| Vendor | Due diligence, data-use terms, change notification, incident notification, evidence, audit rights, and exit planning |
| Incident response | Severity, reporting, containment, investigation, notification, recovery, evidence preservation, and lessons learned |

---

## 18. Required Evaluation Themes

Evaluation must address:

- Recommendation accuracy and operational usefulness
- False-positive and false-negative consequences
- Performance across delivery types and service levels
- Performance across geographic and route conditions
- Performance during incomplete, delayed, or unusual data conditions
- Time-sensitive and safety-related scenarios
- Medical-delivery scenarios before any such use is authorized
- Workload and assignment distribution effects
- Human ability to identify errors and override recommendations
- Reviewer understanding of uncertainty and limitations
- Automation bias and time-pressure scenarios
- Security, manipulation, and misuse cases
- Explanation or rationale usefulness
- Regression following material change
- Logging and evidence completeness
- Safe failure and manual fallback

An aggregate performance score cannot, by itself, justify approval.

---

## 19. Information Gaps

The following information remains pending and may change the classification or required controls:

| Gap ID | Missing or unconfirmed information | Owner | Treatment |
| --- | --- | --- | --- |
| `IG-001` | Final vendor and model architecture | CIO / IT Director | Obtain before technical and vendor review |
| `IG-002` | Model development, training, and validation information | Data / AI Lead | Obtain vendor evidence or document limitation |
| `IG-003` | Final data sources, lineage, retention, and permitted secondary uses | Data / AI Lead and Legal/Privacy Advisor | Complete data-flow and privacy review |
| `IG-004` | Representative evaluation dataset and slice definitions | Data / AI Lead | Define before evaluation approval |
| `IG-005` | Quantitative acceptance thresholds | AI Governance Committee | Approve before testing |
| `IG-006` | Exact medical-delivery scenarios and severity boundaries | Dispatch Director | Define before any medical-use evaluation |
| `IG-007` | Vendor change-notification and incident-notification commitments | Procurement / Vendor Manager | Address in due diligence and contract review |
| `IG-008` | Human-interface design and uncertainty presentation | CIO / IT Director and Data / AI Lead | Evaluate through usability and human-review testing |
| `IG-009` | Manual fallback capacity during outage or suspension | Operations Manager | Validate in continuity exercise |
| `IG-010` | Complaint, dispute, and affected-party notice requirements | Legal/Privacy Advisor and Customer Service Manager | Define before pilot |

Missing information will not be interpreted as evidence that risk is absent.

---

## 20. Inventory Status and Decision

| Decision field | Result |
| --- | --- |
| Inventory record created | Yes |
| Record complete enough for next assessment stage | Yes, with documented information gaps |
| Impact screening completed | Yes, provisionally |
| Overall tier | Tier 4 — Critical |
| Approved to continue detailed assessment | Yes |
| Approved for limited pilot | No |
| Approved for production | No |
| Immediate next step | Complete system context and data-flow analysis, then detailed risk assessment |
| Governance review required | Yes |

The decision to continue assessment does not authorize operational use.

---

## 21. Rescreening Triggers

This inventory and impact screening must be reviewed when:

- A new capability or use case is proposed.
- RouteAssist changes from advisory to automated action.
- Medical-delivery, safety-related, or other high-impact use changes.
- A new user or affected-party group is introduced.
- A new geography, business unit, service, customer type, or delivery category is added.
- A new sensitive data source or downstream system is introduced.
- The model, vendor, algorithm, threshold, interface, or architecture materially changes.
- A third-party dependency or subcontractor changes.
- Evaluation or monitoring reveals a new or more severe impact.
- A severe incident, complaint pattern, override pattern, or security event occurs.
- Human intervention becomes less effective or less timely.
- A legal, contractual, policy, or organizational requirement changes.
- The system is reactivated after extended inactivity.

---

## 22. Inventory Maintenance Requirements

The inventory owner must ensure that:

- The record remains current and uniquely identified.
- The business and technical owners are active and aware of their duties.
- Lifecycle status and approval status are accurate.
- Capabilities, users, affected parties, data, dependencies, and vendors are current.
- Related risks, controls, evaluations, incidents, exceptions, and changes are linked.
- Review dates and decisions are recorded.
- Retired systems include data-disposition, access-removal, contract, evidence-retention, and dependency-removal actions.

The GRC Analyst coordinates inventory governance. Business and technical owners remain accountable for the accuracy of their assigned information.

---

## 23. NIST AI RMF Alignment

This artifact primarily supports:

| NIST AI RMF function | Application |
| --- | --- |
| GOVERN | Establishes ownership, inventory status, governance tier, review requirements, and lifecycle accountability |
| MAP | Documents intended purpose, users, affected parties, data, capabilities, dependencies, and impact context |
| MEASURE | Identifies evaluation themes and information needed to measure performance and impact |
| MANAGE | Assigns governance requirements, pilot restrictions, rescreening triggers, and next actions |

Detailed subcategory mapping will be maintained in [`07-framework-crosswalk.md`](07-framework-crosswalk.md).

---

## 24. Document Control

| Field | Value |
| --- | --- |
| Document title | AI System Inventory and Impact Screening |
| Repository path | `docs/03-ai-system-inventory-and-impact-screening.md` |
| Version | 1.0 |
| Status | Draft portfolio artifact |
| Owner | GRC Analyst |
| Business owner | Dispatch Director |
| Technical owner | CIO / IT Director |
| Approver | AI Governance Committee |
| Review frequency | At least annually and upon material change |
| Classification | Public fictional portfolio content |

### Version history

| Version | Date | Author | Change summary |
| --- | --- | --- | --- |
| 1.0 | 2026-09-19 | Tommy Marshall | Created the RouteAssist inventory record, impact-screening method, provisional Tier 4 classification, governance path, and pilot restrictions. |

---

## 25. Related Documents

- [Project README](../README.md)
- [Project Overview and Methodology](00-project-overview-and-methodology.md)
- [Organization Profile and AI Use Case](01-organization-profile-and-ai-use-case.md)
- [Stakeholder and Accountability Map](02-stakeholder-and-accountability-map.md)
- [Data Flow and System Context](04-data-flow-and-system-context.md)
- [AI Risk Assessment Methodology](05-ai-risk-assessment-methodology.md)
- [AI Risk Register](06-ai-risk-register.md)
- [Framework Crosswalk](07-framework-crosswalk.md)
- [AI Governance Charter](08-ai-governance-charter.md)
- [AI Control Matrix](09-ai-control-matrix.md)
- [Human Oversight and Escalation Plan](10-human-oversight-and-escalation-plan.md)
- [AI Evaluation and Testing Plan](11-ai-evaluation-and-testing-plan.md)
- [Monitoring, Metrics, and Reporting Plan](12-monitoring-metrics-and-reporting-plan.md)

---

## 26. Portfolio Notice

This document is part of an educational portfolio project based on a fictional organization and fictional AI system. The inventory details, impact scores, governance tier, dependencies, and approval decisions are illustrative.

The screening is not a legal determination, regulatory classification, certification, independent assurance conclusion, or guarantee that a real AI system is safe, fair, secure, compliant, reliable, or suitable for production use.
